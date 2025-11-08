# Balls and their admirers

Dette C-program er lavet i forbindelse med kursus: **62712 – Basic C-programming (Uge 09)**  
Programmet bruger **raylib** til at animere bolde (i programmet 100), hvor hver bold følger en tilfældig bold, der i programmet bliver kaldt en leder.


> [!WARNING]
> ## **OBS**
> Som det kan ses i videoen længere nede, har inkluderingen af **raylib** en rød streg under sig, 
> hvilket kunne tyde på at det ikke er hentet og ikke kan bruges. Men som det også kan ses i video, kører programmet korrekt, når ***raylib*** er linket.
> ### Hvor skal raylib mappen placeres?:
> I dette screenshot, kan det ses hvor raylib- mappen skal placeres:
>
>  <img width="300" height="281" alt="image" src="https://github.com/user-attachments/assets/3d5884d2-9841-473b-ba3e-5979a096b890" />


## Beskrivelse af en bold:
En bold har datastrukturen ***struct*** har følgende attributter/medlemmer:
- Position *x* & *y*
- Velocity *x* & *y*
- Radius
- Farve
- Pointer (til den bold den følger)


## Filer
- `main.c` – **Samlet kørsel og logik**, inkl.:
  - initiering af bolde (position, farve, radius, hastighed)
  - kobling af en tilfældig leder for hver bold der initialiseres.
  - opdatering af både bevægelsen og tegningen af boldene
- `compile_flags.txt`
- `.vscode/tasks.json`
  - så det kan køre programmet med F5-tasten


## Funktioner

- `init_ball_random(Ball *p)`
  - Tildeler bolden en tilfældig position, farve, radius, hastighed og leder

- `init_balls_random()`
  - Initialiserer alle *(100)* bolde  med `init_ball_random(Ball *p)`

- `update_vel_for_following(Ball *p)`
  - Opdaterer boldens hastighed, så den bevæger sig mod sin leder

- `update_pos(Ball *p)`
  - Opdaterer position, hvis bolden rammer kanterne

- `draw_ball(Ball *p)`
  - Tegner bolden i vinduet

- `update_elements()`
  - Opdaterer og tegner alle bolde pr. frame

## Eksempel kørsel
Hvis programmet kører rigtigt, vil der poppe et nyt vindue op med de animerede bolde som vist her i videoen:

https://github.com/user-attachments/assets/33846f8e-25a4-48ec-9c83-b8f899557ecd




