# Dual-Mode Stopwatch

A **Dual-Mode Stopwatch** implemented on an **ATmega32 AVR microcontroller**. The stopwatch supports **count-up (normal)** and **count-down (timer)** modes with pause, resume, reset, and manual time adjustment functionalities.

---

## Features

- **Dual Mode Operation**: Count up or down. Toggle modes with a button.
- **Time Adjustment**: While paused, adjust hours, minutes, and seconds.
- **Pause & Resume**: Controlled via external interrupts (INT1 and INT2).
- **Reset Functionality**: External interrupt (INT0) resets time to `00:00:00` and switches to count-up mode.
- **Timer-Based Operation**: 16-bit Timer1 in CTC mode generates a 1-second interrupt for time updates.
- **Visual Indicators**: LEDs indicate the current mode; buzzer activates on countdown completion.

---

## Components Used

- **ATmega32 Microcontroller**  
- **6-digit 7-Segment Display**  
- **Push Buttons** (Mode toggle, Start/Pause, Resume, Reset, Time adjustment)  
- **LED Indicators** (Mode display)  
- **Buzzer** (Countdown alarm)  
- **16-bit Timer1** (CTC Mode, 1s Interrupt)  
- **External Interrupts** (INT0, INT1, INT2)  

---

## How It Works

1. **Startup**: Stopwatch starts in **count-up mode**.  
2. **Pause & Resume**: INT1 stops the stopwatch; INT2 resumes it.  
3. **Reset**: INT0 sets time to `00:00:00` and switches to count-up mode.  
4. **Time Adjustment**: Modify hours, minutes, seconds while paused.  
5. **Mode Toggle**: Switch between count-up and count-down modes.  
6. **Countdown Alarm**: Buzzer triggers when timer reaches `00:00:00`.

---

## Future Improvements

- Integrate **RTC Module** for real-time tracking  
- Use **EEPROM** to retain stopwatch state after reset/power-off  
- Upgrade to **OLED or LCD display** for better readability  

---

## Author

👤 **Adham Muhammed** 
