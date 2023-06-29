from https://github.com/silveirago/DIY-Midi-Controller-full

changé la lib [ResponsiveAnalogRead](libraries/ResponsiveAnalogRead) avec la version à jour  
changé [2023.04.14_en_DIY_midi_controller_full.ino](2023.04.14_en_DIY_midi_controller_full/2023.04.14_en_DIY_midi_controller_full.ino)
```
268 byte PCC = 3;  // Program Change
269 byte PBB = 4;  // Pitch Bend
```
parce que PB et PC déja use dans shiftPWM

changé [CShiftPWM.cpp](libraries/ShiftPWM/CShiftPWM.cpp)
```
 39 CShiftPWM::~CShiftPWM() {
 40         if(m_PWMValues){
 41                 free( m_PWMValues );
 42         }
 43 }   
 ```
