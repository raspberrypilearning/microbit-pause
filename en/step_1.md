You can use a `pause`{:class='microbitbasic'} block to make your program wait for a set time.

- You can find the `pause`{:class='microbitbasic'} block in the `Basic`{:class='microbitbasic'} menu in your Toolbox.

In the Sound meter project, you used a `pause`{:class='microbitbasic'} block at the end of both button events so the sensitivity level displayed on the LEDs for longer.

```microbit
let level = 0
let maximum = 0
input.onButtonPressed(Button.A, function () {
    level += -1
    maximum += -50
    if (level < 1) {
        level = 5
        maximum = 250
    }
    basic.showNumber(level)
    basic.pause(500)
})
```