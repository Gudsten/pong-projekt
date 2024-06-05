<table>
  <thead>
    <tr>
      <th>#pong projekt</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>import turtle</td>
    </tr>
    <tr>
      <td>import time</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>#sets up the screen</td>
    </tr>
    <tr>
      <td>win = turtle.Screen()</td>
    </tr>
    <tr>
      <td>win.title("Pong Game")</td>
    </tr>
    <tr>
      <td>win.bgcolor("black")</td>
    </tr>
    <tr>
      <td>win.setup(width=800, height=600)</td>
    </tr>
    <tr>
      <td>win.tracer(0)</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>#Initial scores</td>
    </tr>
    <tr>
      <td>score_a = 0</td>
    </tr>
    <tr>
      <td>score_b = 0</td>
    </tr>
    <tr>
      <td>win_condition = 25</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>#Powerup activation flags</td>
    </tr>
    <tr>
      <td>big_platform_activated_a = False</td>
    </tr>
    <tr>
      <td>big_platform_activated_b = False</td>
    </tr>
    <tr>
      <td>fast_platform_activated_a = False</td>
    </tr>
    <tr>
      <td>fast_platform_activated_b = False</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>#Paddle a</td>
    </tr>
    <tr>
      <td>paddle_a = turtle.Turtle()</td>
    </tr>
    <tr>
      <td>paddle_a.speed(0)</td>
    </tr>
    <tr>
      <td>paddle_a.shape("square")</td>
    </tr>
    <tr>
      <td>paddle_a.color("white")</td>
    </tr>
    <tr>
      <td>paddle_a.shapesize(stretch_wid=6, stretch_len=1)</td>
    </tr>
    <tr>
      <td>paddle_a.penup()</td>
    </tr>
    <tr>
      <td>paddle_a.goto(-350, 0)</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>#Paddle b</td>
    </tr>
    <tr>
      <td>paddle_b = turtle.Turtle()</td>
    </tr>
    <tr>
      <td>paddle_b.speed(0)</td>
    </tr>
    <tr>
      <td>paddle_b.shape("square")</td>
    </tr>
    <tr>
      <td>paddle_b.color("white")</td>
    </tr>
    <tr>
      <td>paddle_b.shapesize(stretch_wid=6, stretch_len=1)</td>
    </tr>
    <tr>
      <td>paddle_b.penup()</td>
    </tr>
    <tr>
      <td>paddle_b.goto(350, 0)</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>#Ball</td>
    </tr>
    <tr>
      <td>ball = turtle.Turtle()</td>
    </tr>
    <tr>
      <td>ball.speed(20)</td>
    </tr>
    <tr>
      <td>ball.shape("square")</td>
    </tr>
    <tr>
      <td>ball.color("white")</td>
    </tr>
    <tr>
      <td>ball.penup()</td>
    </tr>
    <tr>
      <td>ball.goto(0, 0)</td>
    </tr>
    <tr>
      <td>ball.dx = 0.2</td>
    </tr>
    <tr>
      <td>ball.dy = 0.2</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>#Score display</td>
    </tr>
    <tr>
      <td>pen = turtle.Turtle()</td>
    </tr>
    <tr>
      <td>pen.speed(0)</td>
    </tr>
    <tr>
      <td>pen.color("white")</td>
    </tr>
    <tr>
      <td>pen.penup()</td>
    </tr>
    <tr>
      <td>pen.hideturtle()</td>
    </tr>
    <tr>
      <td>pen.goto(0, 260)</td>
    </tr>
    <tr>
      <td>pen.write("Spelare 1: [0] Spelare 2: (0)", align="center", font=("Courier", 24))</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>#Function to move paddle a</td>
    </tr>
    <tr>
      <td>def paddle_a_up():</td>
    </tr>
    <tr>
      <td>y = paddle_a.ycor()</td>
    </tr>
    <tr>
      <td>y += 20</td>
    </tr>
    <tr>
      <td>paddle_a.sety(y)</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>def paddle_a_down():</td>
    </tr>
    <tr>
      <td>y = paddle_a.ycor()</td>
    </tr>
    <tr>
      <td>y -= 20</td>
    </tr>
    <tr>
      <td>paddle_a.sety(y)</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>#Function to move paddle b</td>
    </tr>
    <tr>
      <td>def paddle_b_up():</td>
    </tr>
    <tr>
      <td>y = paddle_b.ycor()</td>
    </tr>
    <tr>
      <td>y += 20</td>
    </tr>
    <tr>
      <td>paddle_b.sety(y)</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>def paddle_b_down():</td>
    </tr>
    <tr>
      <td>y = paddle_b.ycor()</td>
    </tr>
    <tr>
      <td>y -= 20</td>
    </tr>
    <tr>
      <td>paddle_b.sety(y)</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>#Keybord bindings</td>
    </tr>
    <tr>
      <td>win.listen()</td>
    </tr>
    <tr>
      <td>win.onkeypress(paddle_a_up, "w")</td>
    </tr>
    <tr>
      <td>win.onkeypress(paddle_a_down, "s")</td>
    </tr>
    <tr>
      <td>win.onkeypress(paddle_b_up, "Up")</td>
    </tr>
    <tr>
      <td>win.onkeypress(paddle_b_down, "Down")</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>#Power up text display</td>
    </tr>
    <tr>
      <td>powerup_pen = turtle.Turtle()</td>
    </tr>
    <tr>
      <td>powerup_pen.speed(0)</td>
    </tr>
    <tr>
      <td>powerup_pen.color("yellow")</td>
    </tr>
    <tr>
      <td>powerup_pen.penup()</td>
    </tr>
    <tr>
      <td>powerup_pen.hideturtle()</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>def display_powerup_text(player, powerup):</td>
    </tr>
    <tr>
      <td>powerup_pen.clear()</td>
    </tr>
    <tr>
      <td>powerup_pen.goto(0, 0)</td>
    </tr>
    <tr>
      <td>if player == 1:</td>
    </tr>
    <tr>
      <td>powerup_pen.write(f"Spelare 1 fick {powerup}!!", align="center", font=("Courier", 24))</td>
    </tr>
    <tr>
      <td>else:</td>
    </tr>
    <tr>
      <td>powerup_pen.write(f"Spelare 2 fick {powerup}!", align="center", font=("Courier", 24))</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>win.ontimer(lambda: start_corner_timer(player, powerup), 2000)</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>def start_corner_timer(player, powerup):</td>
    </tr>
    <tr>
      <td>powerup_pen.clear()</td>
    </tr>
    <tr>
      <td>move_powerup_text(player, powerup, 10)</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>def move_powerup_text(player, powerup, time_left):</td>
    </tr>
    <tr>
      <td>powerup_pen.clear()</td>
    </tr>
    <tr>
      <td>if player == 1:</td>
    </tr>
    <tr>
      <td>powerup_pen.goto(-350, 250)</td>
    </tr>
    <tr>
      <td>else:</td>
    </tr>
    <tr>
      <td>powerup_pen.goto(350, 250)</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>if time_left > 0:</td>
    </tr>
    <tr>
      <td>powerup_pen.write(f"{powerup}: {time_left}s", align="center", font=("Courier", 18))</td>
    </tr>
    <tr>
      <td>win.ontimer(lambda: move_powerup_text(player, powerup, time_left - 1), 1000)</td>
    </tr>
    <tr>
      <td>else:</td>
    </tr>
    <tr>
      <td>powerup_pen.clear()</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>#Functions to activate powerups</td>
    </tr>
    <tr>
      <td>def bigPlatform():</td>
    </tr>
    <tr>
      <td>global big_platform_activated_a, big_platform_activated_b</td>
    </tr>
    <tr>
      <td>if score_a >= 5 and not big_platform_activated_a:</td>
    </tr>
    <tr>
      <td>paddle_a.shapesize(stretch_wid=12, stretch_len=1)</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>display_powerup_text(1, "Big Platform")</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>big_platform_activated_a = True</td>
    </tr>
    <tr>
      <td>if score_b >= 5 and not big_platform_activated_b:</td>
    </tr>
    <tr>
      <td>paddle_b.shapesize(stretch_wid=12, stretch_len=1)</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>display_powerup_text(2, "Big Platform")</td>
    </tr>
    <tr>
      <td>big_platform_activated_b = True</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>def fastPlatform():</td>
    </tr>
    <tr>
      <td>global fast_platform_activated_a, fast_platform_activated_b</td>
    </tr>
    <tr>
      <td>if score_a >= 10 and not fast_platform_activated_a:</td>
    </tr>
    <tr>
      <td>win.onkeypress(lambda: paddle_a.sety(paddle_a.ycor() + 40), "w")</td>
    </tr>
    <tr>
      <td>win.onkeypress(lambda: paddle_a.sety(paddle_a.ycor() - 40), "s")</td>
    </tr>
    <tr>
      <td>display_powerup_text(1, "Fast Platform")</td>
    </tr>
    <tr>
      <td>fast_platform_activated_a = True</td>
    </tr>
    <tr>
      <td>if score_b >= 10 and not fast_platform_activated_b:</td>
    </tr>
    <tr>
      <td>win.onkeypress(lambda: paddle_b.sety(paddle_b.ycor() + 40), "Up")</td>
    </tr>
    <tr>
      <td>win.onkeypress(lambda: paddle_b.sety(paddle_b.ycor() - 40), "Down")</td>
    </tr>
    <tr>
      <td>display_powerup_text(2, "Fast Platform")</td>
    </tr>
    <tr>
      <td>fast_platform_activated_b = True</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td># Obstacles</td>
    </tr>
    <tr>
      <td>obstacle_left = turtle.Turtle()</td>
    </tr>
    <tr>
      <td>obstacle_left.speed(0)</td>
    </tr>
    <tr>
      <td>obstacle_left.shape("square")</td>
    </tr>
    <tr>
      <td>obstacle_left.color("red")</td>
    </tr>
    <tr>
      <td>obstacle_left.shapesize(stretch_wid=5, stretch_len=2)</td>
    </tr>
    <tr>
      <td>obstacle_left.penup()</td>
    </tr>
    <tr>
      <td>obstacle_left.goto(-175, 0)</td>
    </tr>
    <tr>
      <td>obstacle_left.hideturtle()</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>obstacle_right = turtle.Turtle()</td>
    </tr>
    <tr>
      <td>obstacle_right.speed(0)</td>
    </tr>
    <tr>
      <td>obstacle_right.shape("square")</td>
    </tr>
    <tr>
      <td>obstacle_right.color("red")</td>
    </tr>
    <tr>
      <td>obstacle_right.shapesize(stretch_wid=5, stretch_len=2)</td>
    </tr>
    <tr>
      <td>obstacle_right.penup()</td>
    </tr>
    <tr>
      <td>obstacle_right.goto(175, 0)</td>
    </tr>
    <tr>
      <td>obstacle_right.hideturtle()</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td># Show obstacles</td>
    </tr>
    <tr>
      <td>def show_obstacles():</td>
    </tr>
    <tr>
      <td>obstacle_left.showturtle()</td>
    </tr>
    <tr>
      <td>obstacle_right.showturtle()</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td># Hide obstacles</td>
    </tr>
    <tr>
      <td>def hide_obstacles():</td>
    </tr>
    <tr>
      <td>obstacle_left.hideturtle()</td>
    </tr>
    <tr>
      <td>obstacle_right.hideturtle()</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>#main game loop</td>
    </tr>
    <tr>
      <td>start_time = time.time()</td>
    </tr>
    <tr>
      <td>while True:</td>
    </tr>
    <tr>
      <td>win.update()</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>current_time = time.time()</td>
    </tr>
    <tr>
      <td>elapsed_time = current_time - start_time</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td># Toggle obstacles every 15 seconds</td>
    </tr>
    <tr>
      <td>if int(elapsed_time // 15) % 2 == 0:</td>
    </tr>
    <tr>
      <td>show_obstacles()</td>
    </tr>
    <tr>
      <td>else:</td>
    </tr>
    <tr>
      <td>hide_obstacles()</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>#Move the ball</td>
    </tr>
    <tr>
      <td>ball.setx(ball.xcor() + ball.dx)</td>
    </tr>
    <tr>
      <td>ball.sety(ball.ycor() + ball.dy)</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>#Border collision</td>
    </tr>
    <tr>
      <td>if ball.ycor() > 290:</td>
    </tr>
    <tr>
      <td>ball.sety(290)</td>
    </tr>
    <tr>
      <td>ball.dy *= -1</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>if ball.ycor() < -290:</td>
    </tr>
    <tr>
      <td>ball.sety(-290)</td>
    </tr>
    <tr>
      <td>ball.dy *= -1</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>#Score update and ball reset</td>
    </tr>
    <tr>
      <td>if ball.xcor() > 390:</td>
    </tr>
    <tr>
      <td>ball.goto(0, 0)</td>
    </tr>
    <tr>
      <td>ball.dx *= -1</td>
    </tr>
    <tr>
      <td>score_a += 1</td>
    </tr>
    <tr>
      <td>pen.clear()</td>
    </tr>
    <tr>
      <td>pen.write("Spelare 1: [{}] Spelare 2: ({})".format(score_a, score_b), align="center", font=("Courier", 24))</td>
    </tr>
    <tr>
      <td>fastPlatform()</td>
    </tr>
    <tr>
      <td>bigPlatform()</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>if ball.xcor() < -390:</td>
    </tr>
    <tr>
      <td>ball.goto(0, 0)</td>
    </tr>
    <tr>
      <td>ball.dx *= -1</td>
    </tr>
    <tr>
      <td>score_b += 1</td>
    </tr>
    <tr>
      <td>pen.clear()</td>
    </tr>
    <tr>
      <td>pen.write("Spelare 1: [{}] Spelare 2: ({})".format(score_a, score_b), align="center", font=("Courier", 24))</td>
    </tr>
    <tr>
      <td>fastPlatform()</td>
    </tr>
    <tr>
      <td>bigPlatform()</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>#Paddle and ball collisions</td>
    </tr>
    <tr>
      <td>if (ball.dx > 0 and ball.xcor() > 340 and paddle_b.ycor() - 50 < ball.ycor() < paddle_b.ycor() + 50):</td>
    </tr>
    <tr>
      <td>ball.setx(340)</td>
    </tr>
    <tr>
      <td>ball.dx *= -1</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>if (ball.dx < 0 and ball.xcor() < -340 and paddle_a.ycor() - 50 < ball.ycor() < paddle_a.ycor() + 50):</td>
    </tr>
    <tr>
      <td>ball.setx(-340)</td>
    </tr>
    <tr>
      <td>ball.dx *= -1</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td># Obstacle and ball collision</td>
    </tr>
    <tr>
      <td>if obstacle_left.isvisible() and (-195 < ball.xcor() < -155 and obstacle_left.ycor() - 50 < ball.ycor() < obstacle_left.ycor() + 50):</td>
    </tr>
    <tr>
      <td>if abs(ball.xcor() + 175) > abs(ball.ycor()):</td>
    </tr>
    <tr>
      <td>ball.dx *= -1</td>
    </tr>
    <tr>
      <td>else:</td>
    </tr>
    <tr>
      <td>ball.dy *= -1</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>if obstacle_right.isvisible() and (155 < ball.xcor() < 195 and obstacle_right.ycor() - 50 < ball.ycor() < obstacle_right.ycor() + 50):</td>
    </tr>
    <tr>
      <td>if abs(ball.xcor() - 175) > abs(ball.ycor()):</td>
    </tr>
    <tr>
      <td>ball.dx *= -1</td>
    </tr>
    <tr>
      <td>else:</td>
    </tr>
    <tr>
      <td>ball.dy *= -1</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>#check for win condition</td>
    </tr>
    <tr>
      <td>if score_a >= 25:</td>
    </tr>
    <tr>
      <td>pen.penup()</td>
    </tr>
    <tr>
      <td>pen.goto(0, 0)</td>
    </tr>
    <tr>
      <td>pen.write("Spelare 1 vinner!!!", move=True, align="center", font=("Comic Sans", 30, "bold"))</td>
    </tr>
    <tr>
      <td>break</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>if score_b >= 25:</td>
    </tr>
    <tr>
      <td>pen.penup()</td>
    </tr>
    <tr>
      <td>pen.goto(0, 0)</td>
    </tr>
    <tr>
      <td>pen.write("Spelare 2 vinner!!!", move=True, align="center", font=("Comic Sans", 30, "bold"))</td>
    </tr>
    <tr>
      <td>break</td>
    </tr>
    <tr>
      <td>&nbsp;</td>
    </tr>
  </tbody>
</table>
