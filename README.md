Integrantes: Joaquin Gandola y Mateo Igon


calcularDemora(origen: Direccion, destino: Direccion, paradas: [Parada]){

var int tiempoDemoraTotal = calcularDemora(origen, paradas.get(0).getDireccion());

var int size =paradas.size();

for(int i = 0; i< size-2; i++){

   var Direccion parada1 = paradas.get(i).getDireccion();

   var Direccion parada2 = paradas.get(i+1).getDireccion();
    
   var int tiempoAParada = calcularDemora(parada1 , parada2);
    
   tiempoDemoraTotal +=tiempoAParada;
   
   }

var int tiempoDemoraADestino = calcularDemora(paradas.get(size-1).getDireccion(), destino);

tiempoDemoraTotal +=tiempoDemoraADestino ;

return tiempoDemoraTotal;

}
