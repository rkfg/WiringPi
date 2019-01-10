project('wiringPi', 'c')

src = [
'wiringPi/ads1115.c',
'wiringPi/bmp180.c',
'wiringPi/drcNet.c',
'wiringPi/drcSerial.c',
'wiringPi/ds18b20.c',
'wiringPi/htu21d.c',
'wiringPi/max31855.c',
'wiringPi/max5322.c',
'wiringPi/mcp23008.c',
'wiringPi/mcp23016.c',
'wiringPi/mcp23017.c',
'wiringPi/mcp23s08.c',
'wiringPi/mcp23s17.c',
'wiringPi/mcp3002.c',
'wiringPi/mcp3004.c',
'wiringPi/mcp3422.c',
'wiringPi/mcp4802.c',
'wiringPi/pcf8574.c',
'wiringPi/pcf8591.c',
'wiringPi/piHiPri.c',
'wiringPi/piThread.c',
'wiringPi/pseudoPins.c',
'wiringPi/rht03.c',
'wiringPi/sn3218.c',
'wiringPi/softPwm.c',
'wiringPi/softServo.c',
'wiringPi/softTone.c',
'wiringPi/sr595.c',
'wiringPi/wiringPi.c',
'wiringPi/wiringPiI2C.c',
'wiringPi/wiringPiSPI.c',
'wiringPi/wiringSerial.c',
'wiringPi/wiringShift.c',
'wiringPi/wpiExtensions.c',
]

cc = meson.get_compiler('c')
m_dep = cc.find_library('m', required : false)
crypt_dep = cc.find_library('crypt', required : true)
rt_dep = cc.find_library('rt', required : true)

deps = [
  dependency('threads'),
  m_dep,
  crypt_dep,
  rt_dep,
]
inc = include_directories('include')
lib = shared_library('wiringPi', src,
  dependencies : deps,
  version : '2.46',
  include_directories : inc
)

wiringPi_dep = declare_dependency(include_directories : inc, link_with : lib)
