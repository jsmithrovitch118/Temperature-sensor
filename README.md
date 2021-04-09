
import bme280
import time

try:
    while True:
        temperature,pressure,humidity = bme280.readBME280All()
        temperature = (temperature * 9/5) + 32
        print("temp= %.2f" %temperature)
        time.sleep(.3)
        
        
except KeyboardInterrupt:
    SystemExit()
