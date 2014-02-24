mjpopup2013
===========

Appel du plugin 
___________________________________
			
<!-- APPEL DE LA BIBLIOTHEQUE -->
<script type="text/javascript" src="http://code.jquery.com/jquery-1.8.3.min.js"></script>

<!-- APPEL DE MJPOPUP -->
<script type="text/javascript" src="js/jquery.cookie.js"></script>
<script type="text/javascript" src="js/mjpopup.min.1.0.0.js"></script>

<!-- UTILISATION DU PLUGIN -->
<script type="text/javascript">
//...utilisation de mjpopup
</script>

Un appel simple avec son exemple
___________________________________
			
jQuery(document).ready(function() {
	jQuery(this).mjpopup();
});

Toutes les fonctionnalitées
___________________________________
	
jQuery(document).ready(function() {
	jQuery(this).mjpopup({
		//active debug
		'debug' : false,
		//click or no
		'onClick': {
			'active' : false,
			'class' : 'showPopup'
		},
		//cookie
		'cookie' : {
			'active' : false,
			'name' : 'mjpopup',
			'time' : 1
	  	},
		//create overlay
		'overlay': {
			'class': 'popup_overlay',
			'closeOnClick': true,
			'css': {
				'background' : 'url(img/overlay1.png)',
				'backgroundRepeat' : 'repeat',
				'zIndex' : 999,
				'width' : '100%',
				'position' : 'absolute',
				'top' :0,
				'height' : jQuery(document).height()
			}
		},
		//create div popup
		'popup': {
			'class': 'popup_div_view',
			'width': 940,
			'height': 538,
			'css': {
				'borderWidth': 8,
				'borderColor': '#D0D0D0',
				'borderStyle': 'solid',
				'borderRadius': '6px 0px 6px 6px',
				'float' : 'left',
				'height' : '500px',
				'position' : 'relative',
				'zIndex' : 999999
			},
			'htmlpopup' : '<img src="img/mjpopup.jpg" />'
		},
		//close button
		'close': {
			'text' : 'fermer',//string and One word
			'class' : 'close',
			'EscClose': true,
			'css': {
				'color' : 'black',
				'display' : 'block',
				'float' : 'right',
				'padding' : '4px 9px', //px or em
				'backgroundColor' : '#D0D0D0',
				'fontSize' : '12px', //px
				'borderRadius' : '2px 2px 0 0',
				'textTransform' : 'uppercase',
				'fontWeight' : 'bold',
				'cursor' : 'pointer',
				'zIndex' : 999999
			}
		},
		//effect appearance/disappearance for background
		'effect': {
			'bgIn': 'fade',
			'bgTime' : 800,
			'bgOut' : 'fade',
			'popupIn' : 'slide',
			'popupTime' : 1000,
			'popupOut' : 'slide'
		}
	});
});

Le mode debug
___________________________________
jQuery(document).ready(function() {
	jQuery(this).mjpopup({
		//active debug
		'debug' : true,
		//click or no
		'onClick': {
			'active' : true,
			'class' : 'showPopup'
		},
		//create div popup
		'popup': 
		{
			'width': 'fezfz', <= voici l'erreur
			'height': 365,
			'htmlpopup' : '<img src="img/mjpopup1.jpg" />',
			'css':
			{
				'height' : '365px',
				'width': '940px'
			}
		}
	})
	
	
Je vous invite à consulter le site exemple : http://popup.mj-plugin.com