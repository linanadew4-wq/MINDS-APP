# MINDS-APP
Mental Health  
def Start():
    homeScreen.visible = True
    moodButtons.visible = True
    reset.visible =False
    sadSkillLable.value=""
    angrySkillLable.value=""
    nervSkillLable.value=""
homeScreen = Group(
    Rect(0,0,400,400,fill='yellow'),
    Label('Welcome to the Mood tracking APP!', 200, 36, size=16, font ='montserrat'),
    Label('MENTAL HEALTH MATTERS!! ', 200, 100, size=12, font ='montserrat')
)

moodButtons = Group(
    #Angry
    Circle(75,300,40,fill = 'coral'),
    Circle(72,290,40,fill='orangeRed'),
    Label('ANGRY',72,290,size=13, bold = True),
    
    #Sad
    Circle(194,300,40,fill = 'paleTurquoise'),
    Circle(191,290,40,fill='deepSkyBlue'),
    Label('SAD',191,290,size=13, bold = True),
    
    #Anxious
    Circle(310,300,40,fill = 'paleGreen'),
    Circle(307,290,40,fill='lime'),
    Label('ANXIOUS',307,290,size=13, bold = True)
                   )
reset = Group(
    Rect(25,13,77,33,fill='darkSlateBlue'),
    Polygon(36, 30, 53, 18 ,53,40,fill='orange'),
    Line(50,30,88,30,lineWidth=9,fill='orange')
             )
reset.visible = False

sadScreen = Group(
    Rect(0,0,400,400,fill='powderBlue'),
    Label('Sadness', 200, 36, size=20, font ='montserrat'),
    Label('Advice', 110, 110, size= 17, font ='montserrat'),
    Label(' To help you! ', 110, 134, size= 17, font ='montserrat'),
    Label('Click the Screen', 297, 110, size= 17, font ='montserrat'),
    Label(' To go to the next advice!', 297, 134, size= 13, font ='montserrat')
                 )
sadScreen.visible=False

angryScreen = Group(
    Rect(0,0,400,400,fill='orangeRed'),
    Label('Anger', 200, 36, size=20, font ='montserrat'),
    Label('Advice', 110, 110, size= 17, font ='montserrat'),
    Label(' To help you! ', 110, 134, size= 17, font ='montserrat'),
    Label('Click the Screen', 297, 110, size= 17, font ='montserrat'),
    Label(' To go to the next advice!', 297, 134, size= 13, font ='montserrat')
                    )
angryScreen.visible=False

nervScreen=Group (
    Rect(0,0,400,400,fill='lime'),
    Label('Anxiety', 200, 36, size=20, font ='montserrat'),
    Label('Advice', 110, 110, size= 17, font ='montserrat'),
    Label(' To help you! ', 110, 134, size= 17, font ='montserrat'),
    Label('Click the Screen', 297, 110, size= 17, font ='montserrat'),
    Label(' To go to the next advice!', 297, 134, size= 13, font ='montserrat')
                )
nervScreen.visible = False

def hideAllScreens():
    homeScreen.visible = False
    angryScreen.visible =False
    sadScreen.visible=False
    nervScreen.visible = False
    moodButtons.visible=False
    
def onMousePress(x,y):
    # reset
    if reset.contains(x,y):
        hideAllScreens()
        Start()
        
    #sad button
    
    if moodButtons.children[3].contains(x,y):
        hideAllScreens()
        reset.visible =True
        sadScreen.visible = True
        reset.toFront()
    #angry
    elif moodButtons.children[1].contains(x,y):
        hideAllScreens()
        reset.visible =True
        angryScreen.visible = True
        reset.toFront()
    #nerv
    elif moodButtons.children[7].contains(x,y):
        hideAllScreens()
        reset.visible =True
        nervScreen.visible = True
        reset.toFront()
