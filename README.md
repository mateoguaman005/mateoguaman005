import machine
import time

rojo = machine.Pin(13, machine.Pin.OUT)
amarillo = machine.Pin(12, machine.Pin.OUT)
verde = machine.Pin(14, machine.Pin.OUT)

def semaforo_rojo():
    rojo.on()
    amarillo.off()
    verde.off()


def semaforo_amarillo():
    rojo.off()
    amarillo.on()
    verde.off()

def semaforo_verde():
    rojo.off()
    amarillo.off()
    verde.on()

while True:
    semaforo_rojo()
    time.sleep(5)
    semaforo_amarillo()
    time.sleep(2)
    semaforo_verde()
    time.sleep(5)
--->
