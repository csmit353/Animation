# Animation
input.onButtonPressed(Button.A, function () {
    basic.clearScreen()
    for (let index = 0; index <= 4; index++) {
        led.plot(index, Math.randomRange(0, 5))
    }
})
input.onButtonPressed(Button.B, function () {
    if (led.point(0, 0)) {
        basic.showIcon(IconNames.Yes)
    } else {
        basic.showIcon(IconNames.No)
    }
})
led.plot(1, 0)
led.plot(3, 0)
led.plot(2, 1)
led.plot(1, 3)
led.plot(2, 3)
led.plot(3, 3)
basic.forever(function () {
    led.toggle(0, 2)
    led.toggle(4, 2)
    basic.pause(250)
    led.toggle(0, 3)
    led.toggle(4, 3)
})
