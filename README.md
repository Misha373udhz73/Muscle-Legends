# Muscle-Legends
local TeleportService = game:GetService("TeleportService")
local player = game.Players.LocalPlayer
local jobId = "c1368fc2-72cb-461f-b934-fe875b7b7782"

local function teleportToJob()
    TeleportService:TeleportToPlaceInstance(game.PlaceId, jobId, player)
end

teleportToJob()

local args = {
    [1] = "acceptTrade"
}

game:GetService("ReplicatedStorage").rEvents.tradingEvent:FireServer(unpack(args))
