# costycnc-invert-dir-step-foamcut-grbl-1.1-pwm

copied from https://github.com/gnea/grbl

put folder grbl folder  in My documents/Arduino/libraries  (Folder libraries appear after open Arduino program )

I have a cnc shield 4.0 with pin and dir inversed ... so in cpu_map.h inverse pins

    at line 39
     #define X_STEP_BIT      5  // Uno Digital Pin 2
     #define Y_STEP_BIT      6  // Uno Digital Pin 3
     #define Z_STEP_BIT      7  // Uno Digital Pin 4
  
    at line 47
    #define X_DIRECTION_BIT   2  // Uno Digital Pin 5
    #define Y_DIRECTION_BIT   3  // Uno Digital Pin 6
    #define Z_DIRECTION_BIT   4  // Uno Digital Pin 7
  
in defaults.h at line 32  

     #define DEFAULT_X_STEPS_PER_MM 100.0
     #define DEFAULT_Y_STEPS_PER_MM 100.0
     #define DEFAULT_Z_STEPS_PER_MM 250.0
     #define DEFAULT_X_MAX_RATE 1000.0 // mm/min
     #define DEFAULT_Y_MAX_RATE 1000.0 // mm/min
     #define DEFAULT_Z_MAX_RATE 500.0 // mm/min
     #define DEFAULT_X_ACCELERATION (100.0*60*60) // 10*60*60 mm/min^2 = 10 mm/sec^2
     #define DEFAULT_Y_ACCELERATION (100.0*60*60) // 10*60*60 mm/min^2 = 10 mm/sec^2
     
  and line 44
  
       #define DEFAULT_SPINDLE_RPM_MAX 255.0 // rpm
  
