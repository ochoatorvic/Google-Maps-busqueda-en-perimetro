<html>
	<head>
		<style type="text/css">
			#mapa{
				height: 400px;
				width: 600px;
				margin: 20px auto;
			}
		</style>
		<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/1.7.2/jquery.min.js"></script>
		<script type="text/javascript" src="http://maps.google.com/maps/api/js?sensor=false"></script>
		<script type="text/javascript" src="jquery-gmap3-4.1/gmap3.js"></script>
		<script type="text/javascript">
			var MiOrigen = {lat:19.073718233532563, lng:-98.21571350097656};
			var DistanciaMax = 1000;
			var MapZoom = 15;
			var MarkersList = [
								{lat:19.060414267254345, lng:-98.23193550109863, data:'A'},
								{lat:19.057006982229623, lng:-98.22772979736328, data:'B'},
								{lat:19.055222185947514, lng:-98.23760032653809, data:'C'},
								{lat:19.052707213137126, lng:-98.21828842163086, data:'D'},
								{lat:19.0662551644169, lng:-98.24060440063477, data:'E'},
								{lat:19.06771535655511, lng:-98.23253631591797, data:'F'},
								{lat:19.077774108392486, lng:-98.2466983795166, data:'G'},
								{lat:19.08077539186489, lng:-98.23270797729492, data:'H'},
								{lat:19.06649853066647, lng:-98.23296546936035, data:'I'},
								{lat:19.058386129839022,lng:-98.23236465454102, data:'J'},
								{lat:19.06309137066209, lng:-98.23502540588379, data:'K'}
							];
			var MarkersSearch;

			function obtenerUbicacion(posicion){
				var latitud = posicion.coords.latitude;
				var longitud = posicion.coords.longitude;
				MiOrigen = {lat:latitud, lng:longitud};
				buscarEnPerimetro();//MiOrigen,MarkersList,DistanciaMax
			}

			function errorUbicacion(errorgeo){
				alert("Servicio no disponible");
			}

			function buscarEnPerimetro(){
				jQuery("#mapa").gmap3(
					{
						action:'init', 
						center:MiOrigen, 
						zoom:MapZoom, 
						mapTypeId:google.maps.MapTypeId.ROADMAP
					},
					{
						action:'addMarker',
						icon: new google.maps.MarkerImage('http://maps.gstatic.com/mapfiles/icon_green.png'),
						latLng:MiOrigen
					},
					{
						action: 'addCircle',
						circle:{
							options:{
								center: MiOrigen,
								radius : DistanciaMax,
								fillColor : "#1E74FF",
								strokeColor : "#1E74FF"
							}
						},
						map:{
							center:true,
							zoom:MapZoom
						}
					},
					{	action:'getDistance',
						options:{
							origins:[MiOrigen],
							destinations:MarkersList,
							travelMode: google.maps.TravelMode.DRIVING
						},
						callback: function(results){
							var html = '';
							if (results){
								for (var i = 0; i < results.rows.length; i++){
									var elements = results.rows[i].elements;
									for(var j=0; j<elements.length; j++){
										switch(elements[j].status){
											case google.maps.DistanceMatrixStatus.OK:
												if(elements[j].distance.value <= DistanciaMax){
													jQuery("#mapa").gmap3(
														{
															action:'addMarker',
															latLng:MarkersList[j],
															data: "Te encuentras a " +elements[j].distance.text + " de distancia, aproximadamente a " + elements[j].duration.text,
															events:{
																mouseover: function(marker, event, data){
																	var map = $(this).gmap3('get'),
																	infowindow = $(this).gmap3({action:'get', name:'infowindow'});
																	if (infowindow){
																		infowindow.open(map, marker);
																		infowindow.setContent(data);
																	} else {
																		$(this).gmap3({action:'addinfowindow', anchor:marker, options:{content: data}});
																	}
																},
																mouseout: function(){
																	var infowindow = $(this).gmap3({action:'get', name:'infowindow'});
																	if (infowindow){
																		infowindow.close();
																	}
																}
															}
														}
													);
												}
												break;
										}
									}
								}
							} else {
								alert("error");
							}
						}
					}
				);
			}
			
			jQuery(document).ready(
				function(){
					navigator.geolocation.getCurrentPosition(obtenerUbicacion, errorUbicacion);
				}
			);	
			
		</script>
	</head>
	<body>
		<div id="mapa"></div>
	</body>
</html>