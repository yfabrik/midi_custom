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


changé [2023.04.14_en_DIY_midi_controller_full.ino](2023.04.14_en_DIY_midi_controller_full/2023.04.14_en_DIY_midi_controller_full.ino)
```
531 byte POT_MIDI_CH = 1;  //* MIDI channel to be used
532 byte BUTTON_MIDI_CH = 1;
533 byte ENCODER_MIDI_CH = 1;

535 byte NOTE = 31;      //* Lowest NOTE to be used - if not using custom NOTE NUMBER
```

commented [2023.04.14_en_DIY_midi_controller_full.ino](2023.04.14_en_DIY_midi_controller_full/2023.04.14_en_DIY_midi_controller_full.ino)
```
394 //#ifdef USING_CUSTOM_CC_N

    // What type of message do you want to send?
    // Control Change - Pitch Bend

    // CC: Control change
    // PBB: Pitch Bend

    //* Put here the type of message you want to send, in the same order you declared the button pins
    // "CC" for Control Change | "PBB" for Pitch Bend
    byte MESSAGE_TYPE_POT[N_POTS] = { CC, PBB };

    byte POT_CC_N[N_POTS] = { 1, 2 };  // Add the CC NUMBER or MACKIE of each pot you want

    //#endif
```
because MESSAGE_TYPE_POT needed in 1 debug  
POT_CC_N used in mackie too 