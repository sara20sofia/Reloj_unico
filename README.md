Reloj_unico

vertical_position = 0
vertical_position1 = 0
vertical_position2 = 0

def setup():
    size(800, 500)
    
def draw ():
    
    global vertical_position
    global vertical_position1
    global vertical_position2
    
    background (map(second(), 0, 59, 250, 0))
    noStroke()
    fill (map(second(), 0, 59, 0, 250))
    
    if vertical_position > height:
        vertical_position = 0
    else:
        vertical_position = map(second(), 0, 59, 0, height)
        
    if vertical_position1 > height:
        vertical_position1 = 0
    else:
        vertical_position1 = map(minute(), 0, 59, 0, height)
        
        
    if vertical_position2 > height:
        vertical_position2 = 0
    else:
        vertical_position2 = map(hour(), 0, 23, 0, height)
        
    ellipse (150, vertical_position, 125, 125)
    ellipse (400, vertical_position1, 125, 125)
    ellipse (650, vertical_position2, 125, 125)
