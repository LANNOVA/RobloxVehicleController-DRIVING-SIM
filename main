local seat = script.Parent.Seat
 
local checkpart = script.Parent.CheckPart
local stoppart = script.Parent.RedPart
local gopart = script.Parent.GreenPart
 
gopart.Position = Vector3.new(-183.9, -13.4, 38)
stoppart.Position = Vector3.new(-183.9, -13.4, 38)
 
seat.Throttle = 1
 
script.Parent.Body.Touched:Connect(function(hitturn)
    if hitturn.Name == "Turn" then
        seat.Steer = 1.50
        wait(1.5)
        seat.Steer = 0
    end
end)
 
script.Parent.Body.Touched:Connect(function(hitstop)
    if hitstop.Name == "RedPart" then
        seat.Throttle = 0
        stoppart.Position = checkpart.Position
        gopart.Position = Vector3.new(-183.9, -13.4, 38)
    end
end)
 
script.Parent.Body.Touched:Connect(function(hitpass)
    if hitpass.Name == "GreenPart" then
        seat.Throttle = 1
        gopart.Position = checkpart.Position
        stoppart.Position = Vector3.new(-183.9, -13.4, 38)
    end
end)
