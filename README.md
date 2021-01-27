# clock-angle-calculator
Calculate angle between hour and minute hands



#!/usr/bin/env python3

def calculate(time='12:30'): #165

    time_minute = int(time.partition(':')[2])
    time_hour = int(time.partition(':')[0])

    hour = ((time_hour*30) + (time_minute/2))
    if hour >= 360:
        hour -= 360
    minute = time_minute * 6

    if hour > minute:
        #calculate diff between hour and minute.
        angle = hour-minute
    elif hour < minute:
        angle = minute-hour
    else: #hour = minute
        angle = 0


    print(hour, minute)
    return print(angle)



calculate('3:42')
