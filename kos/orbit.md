### Comprobado: :x:

```
// Secuencia de lanzamiento
lock throttle to 1.
wait 1.
stage.

// Esperando para comenzar el giro
wait until vessel:verticalspeed = 98.0.
sas on.
set sasmode to prograde.

// Continúa acelerando hasta alcanzar una altura estable
wait until alt:apoapsis = 70000.
lock throttle to 0.6.

// Corrigiendo a una órbita segura
wait until alt:apoapsis = 80000.
lock throttle to 0.0.
stage.

// Creación de la maniobra
set orbitnode to node(timespan(0,0,0,0,apoapsis:eta),0,0,1900).
add orbitnode.
print "Apogeo final: " + orbitnode:orbit:apoapsis.
print "Perigeo final: " + orbitnode:orbit:periapsis.

// Realiza la maniobra final.
lock steering to maneuver.
wait until maneuvernode:eta = 0
lock throttle to 1.0.
wait until alt:periapsis > 70000.
lock throttle to 0.6.
wait until alt:periapsis > 80000.
lock throttle to 0.0.
print "Órbita completada.".
