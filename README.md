-- Script para Roblox - Hop Los Brothers

-- Criar ScreenGui
local ScreenGui = Instance.new("ScreenGui")
ScreenGui.Name = "HopLosBrothers"
ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

-- Criar Frame principal
local Frame = Instance.new("Frame")
Frame.Size = UDim2.new(0, 300, 0, 200)
Frame.Position = UDim2.new(0.5, -150, 0.5, -100)
Frame.BackgroundColor3 = Color3.new(0, 0, 0) -- Preto
Frame.Parent = ScreenGui
Frame.Draggable = true -- Permite mover o frame

-- Título
local Title = Instance.new("TextLabel")
Title.Size = UDim2.new(1, 0, 0, 30)
Title.Position = UDim2.new(0, 0, 0, 0)
Title.Text = "Hop Los Brothers"
Title.TextColor3 = Color3.new(1, 1, 1) -- Branco
Title.BackgroundTransparency = 1
Title.Parent = Frame

-- Texto TikTok
local TikTokText = Instance.new("TextLabel")
TikTokText.Size = UDim2.new(1, 0, 0, 20)
TikTokText.Position = UDim2.new(0, 0, 0, 30)
TikTokText.Text = "TikTok: LosBrothers.ofc"
TikTokText.TextColor3 = Color3.new(1, 1, 1) -- Branco
TikTokText.BackgroundTransparency = 1
TikTokText.Parent = Frame

-- Botão Server Hop
local ServerHopButton = Instance.new("TextButton")
ServerHopButton.Size = UDim2.new(0, 100, 0, 30)
ServerHopButton.Position = UDim2.new(0.5, -50, 0, 70)
ServerHopButton.Text = "Server Hop"
ServerHopButton.TextColor3 = Color3.new(0, 0, 0) -- Preto
ServerHopButton.BackgroundColor3 = Color3.new(1, 1, 1) -- Branco
ServerHopButton.Parent = Frame
ServerHopButton.MouseButton1Click:Connect(function()
    print("Server Hop clicado.")
end)

-- Botão Fechar
local CloseButton = Instance.new("TextButton")
CloseButton.Size = UDim2.new(0, 50, 0, 20)
CloseButton.Position = UDim2.new(1, -50, 0, 0)
CloseButton.Text = "Fechar"
CloseButton.TextColor3 = Color3.new(0, 0, 0) -- Preto
CloseButton.BackgroundColor3 = Color3.new(1, 1, 1) -- Branco
CloseButton.Parent = Frame
CloseButton.MouseButton1Click:Connect(function()
    ScreenGui:Destroy()
end)

-- Botão Minimizar
local MinimizeButton = Instance.new("TextButton")
MinimizeButton.Size = UDim2.new(0, 50, 0, 20)
MinimizeButton.Position = UDim2.new(1, -100, 0, 0)
MinimizeButton.Text = "Minimizar"
MinimizeButton.TextColor3 = Color3.new(0, 0, 0) -- Preto
MinimizeButton.BackgroundColor3 = Color3.new(1, 1, 1) -- Branco
MinimizeButton.Parent = Frame
MinimizeButton.MouseButton1Click:Connect(function()
    Frame.Visible = false
end)

-- Botão Tela Cheia
local FullscreenButton = Instance.new("TextButton")
FullscreenButton.Size = UDim2.new(0, 50, 0, 20)
FullscreenButton.Position = UDim2.new(0, 0, 0, 0)
FullscreenButton.Text = "Tela Cheia"
FullscreenButton.TextColor3 = Color3.new(0, 0, 0) -- Preto
FullscreenButton.BackgroundColor3 = Color3.new(1, 1, 1) -- Branco
FullscreenButton.Parent = Frame
FullscreenButton.MouseButton1Click:Connect(function()
    if Frame.Size == UDim2.new(0, 300, 0, 200) then
        Frame.Size = UDim2.new(1, 0, 1, 0)
    else
        Frame.Size = UDim2.new(0, 300, 0, 200)
    end
end)
