import pygame

from pygame import MOUSEBUTTONDOWN

pygame.init()

screen_width = 800
screen_height = 600

screen = pygame.display.set_mode((screen_width, screen_height))
pygame.display.set_caption("Pygame Basics")
font= pygame.font.Font(None, 30)
text= font.render("PLAY", True, 'black')
exitext= font.render("EXIT", True, "Black")
background_color = (0, 128, 255)
button= pygame.Rect(150,150,150,50)
exitbutton= pygame.Rect(500,150,150,50)

def bouncingball():
    circx, circy = 200, 100
    speedx, speedy = 0.6893, 0.6893
    running= True
    while running:
        for event in pygame.event.get():
            if event.type == pygame.QUIT:
                running = False
        screen.fill(background_color)
        circx += speedx
        circy += speedy
        if circx + 29 > screen_width or circx - 29 < 0:
            speedx = -speedx
        if circy + 29 > screen_height or circy - 29 < 0:
            speedy = -speedy

        pygame.draw.circle(screen, "White", (circx, circy), 29)
        pygame.display.flip()
    return

running = True
while running:
   for event in pygame.event.get():
       if event.type == pygame.QUIT:
           running = False
       if event.type == MOUSEBUTTONDOWN:
           if exitbutton.collidepoint(event.pos):
               running = False
       if event.type == MOUSEBUTTONDOWN:
           if button.collidepoint(event.pos):
               bouncingball()

   screen.fill(background_color)
   pygame.draw.rect(screen,(255,150,255),button,border_radius=10)
   screen.blit(text, (button.x+50,button.y+15))
   pygame.draw.rect(screen, (110,255,255),exitbutton, border_radius=10)
   screen.blit(exitext,(exitbutton.x+50, exitbutton.y+15))
   pygame.display.flip()
