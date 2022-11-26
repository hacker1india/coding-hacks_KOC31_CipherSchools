# coding-hacks_KOC31_CipherSchools
# I AM A LEARNER

def calcAngle(h, m):

    if (h < 0 or m < 0 or h > 24 or m > 60):
        print('Wrong input')

    if (h == 24):
        h = 0
    if (m == 60):
        m = 0
        h += 1;
        if (h > 24):
            h = h - 24;

    hour_angle = 0.5 * (h * 60 + m)
    minute_angle = 6 * m

    angle = abs(hour_angle - minute_angle)


    angle = min(360 - angle, angle)

    return angle

h = 5
m = 30
print('Angle ', calcAngle(h, m))

h = 12
m = 00
print('Angle ', calcAngle(h, m))

h = 7
m = 30
print('Angle ', calcAngle(h, m))


