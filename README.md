# MINDS-APP
Mental Health  
def Start(color,what):
    background = Rect(0,0,400,400,fill=color,visible=what)
    Label('Welcome to the Mood tracking APP!', 200, 36, size=16, font ='montserrat',visible=what)
    Label('This app is made to help you recogize your emotions!', 200, 59, size=12, font ='montserrat',visible=what)
    Label('MENTAL HEALTH MATTERS!! ', 200, 100, size=12, font ='montserrat',visible=what)
Start('yellow',True)


#Angry
Angry1 =Circle(75,300,40,fill = 'coral'),
Angry2 = Circle(72,290,40,fill='orangeRed')
Angry3 = Label('ANGRY',72,290,size=13, bold = True)

#Sad
Sad1 =Circle(194,300,40,fill = 'paleTurquoise')
Sad2 =   Circle(191,290,40,fill='deepSkyBlue')
Sad3 = Label('SAD',191,290,size=13, bold = True)

#Anxious
Nerv1 = Circle(310,300,40,fill = 'paleGreen')
Nerv2 =  Circle(307,290,40,fill='lime')
Nerv3 = Label('ANXIOUS',307,290,size=13, bold = True)

#
reset = Group (Rect(25,13,77,33,fill='darkSlateBlue',visible=False),
        Polygon(36, 30, 53, 18 ,53,40,fill='orange',visible=False),
             Line(50,30,88,30,lineWidth=9,fill='orange',visible= False)
            )

     
def DisSet():
        Angry1.visible = True
        Angry2.visible = True
        Angry3.visible = True
        Sad1.visible = True
        Sad2.visible = True
        Sad3.visible = True
        Nerv1.visible = True
        Nerv2.visible = True
        Nerv3.visible = True


def NotHappy(color,what):
    back=Rect(0,0,400,400,fill=color,visible=what)
    Label('Sadness', 200, 36, size=20, font ='montserrat',visible=what)
    Label('Good Coping', 110, 110, size= 17, font ='montserrat',visible=what)
    Label(' Skills ', 110, 134, size= 17, font ='montserrat',visible=what)
    Label('Bad Coping', 297, 110, size= 17, font ='montserrat',visible=what)
    Label(' Skills ', 297, 134, size= 17, font ='montserrat',visible=what)
    
def Mad(color,what):
    back=Rect(0,0,400,400,fill=color,visible=what)
    Label('Anger', 200, 36, size=20, font ='montserrat',visible=what)
    Label('Good Coping', 110, 110, size= 17, font ='montserrat',visible=what)
    Label(' Skills ', 110, 134, size= 17, font ='montserrat',visible=what)
    Label('Bad Coping', 297, 110, size= 17, font ='montserrat',visible=what)
    Label(' Skills ', 297, 134, size= 17, font ='montserrat',visible=what)

def Nerv (color,what):
    back=Rect(0,0,400,400,fill=color,visible=what)
    Label('Anxiety', 200, 36, size=20, font ='montserrat',visible=what)
    Label('Good Coping', 110, 110, size= 17, font ='montserrat',visible=what)
    Label(' Skills ', 110, 134, size= 17, font ='montserrat',visible=what)
    Label('Bad Coping', 297, 110, size= 17, font ='montserrat',visible=what)
    Label(' Skills ', 297, 134, size= 17, font ='montserrat',visible=what)
    
def onMousePress (mouseX,mouseY):
    if Sad2.contains(mouseX,mouseY):
        NotHappy('powderBlue',True)
        #ReSet(True)
        for rset in reset.children:
            rset.visible = True
    elif reset.contains(mouseX,mouseY):
        Start('yellow',True)
        
    if Angry2.contains(mouseX,mouseY):
        Mad('orangeRed',True)
        #ReSet(True)
        for rset in reset.children:
            rset.visible = True
    elif reset.contains(mouseX,mouseY):
        Start('yellow',True)
        
    if Nerv2.contains(mouseX,mouseY):
        Nerv('lime',True)
        #ReSet(True)
        for rset in reset.children:
            rset.visible = True
    elif reset.contains(mouseX,mouseY):
        Start('yellow',True) 
        
        


