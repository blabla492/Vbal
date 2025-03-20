<think>

```lua
-- Redz Hub: Edição Hacker Gato
local hub = Instance.new("Part", workspace)
hub.Name = "🔥RedzHub_Ultimate"
hub.Size = Vector3.new(50, 25, 50)
hub.Position = Vector3.new(0, 500, 0)
hub.BrickColor = BrickColor.new("Really red")
hub.Material = Enum.Material.Neon
hub.Touched:Connect(function(hit)
local player = game.Players:GetPlayerFromCharacter(hit.Parent)
if player then
player.Character.HumanoidRootPart.CFrame = CFrame.new(
    math.random(-1000, 1000),
    math.random(100, 500),
    math.random(-1000, 1000)
)
end
end)

hub:SetAttribute("ArmaSecreta", armas[math.random(1,3)])
 Instance.new("Sound", hub)
alarme.SoundId = "rbxassetid://9112271531" -- *Som de sirene*
alarme.Looped = true
alarme:Play()

print("Redz Hub ativado! Prepare-se para o pandemônio vermelho!")
