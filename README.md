## Flash with Openocd

### Openocd config file in root
```
source [find interface/stlink.cfg]

source [find target/stm32h7x.cfg]

adapter speed 2000
init
reset halt
```

### Compile
```
make clean
```

### Flash
```
openocd -f openocd.cfg -c "program build/lab-1.elf verify reset exit"
```
