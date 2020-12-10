function newLine()
    local mon = peripheral.wrap("left")
    x, y = mon.getCursorPos()
    mon.setCursorPos(1, y + 1)
end

function displayTries(tries)
    local mon = peripheral.wrap("left")
    mon.setCursorPos(1, 2)
    mon.clearLine()
    mon.write("You have " .. 10 - tries .. " tries left")
    newLine()
end

term.clear()
local mon = peripheral.wrap("left")
mon.clear()
mon.setCursorPos(1, 1)
mon.write("Guess a number (1 - 100)")
newLine()
mon.setBackgroundColor(8192) 
mon.setTextColor(16384)
numb = math.random(1, 100)
tries = 0;
while (tries < 10) do
    displayTries(tries)
    guess = io.read()
    guess = tonumber(guess)
    mon.write(guess)
    newLine()
    if (guess == numb) then
        win = true;
        mon.write("Congratulations, you guessed the number!")
		newLine()
        mon.setCursorPos(1, 5)
        mon.clearLine()
        break
    else
        mon.write("Nah b, guess again")		
        newLine()
        if (guess > numb) then
            mon.clearLine()	
            mon.write("Your guess was too high")
            newLine()
        else
            mon.clearLine()
            mon.write("Your guess was too low")
            newLine()
        end
        tries = tries + 1
    end
end
if (tries == 10) then
    mon.write("You're out of guesses!")
    newLine()
end

function newLine ()
    local x, y = monitor.getCursorPos()
    mon.setCursorPos(1, y)
end
