# Hi

-- Importation de HttpService
local HttpService = game:GetService("HttpService")

-- Création de l'interface utilisateur
local D00bleExecGui = Instance.new("ScreenGui")
local MainFrame = Instance.new("Frame")
local WelcomeFrame = Instance.new("Frame")
local WelcomeText = Instance.new("TextLabel")
local HomeButton = Instance.new("TextButton")
local DocumentButton = Instance.new("TextButton")
local SearchButton = Instance.new("TextButton")
local SettingsButton = Instance.new("TextButton")
local CloseButton = Instance.new("TextButton")
local SearchPageFrame = Instance.new("Frame")
local ScriptsHubText = Instance.new("TextLabel")
local ScriptFrame = Instance.new("Frame")
local TextBoxContainer1 = Instance.new("Frame")
local TextBoxContainer2 = Instance.new("Frame")
local TextBoxContainer3 = Instance.new("Frame")
local ScriptTextBox1 = Instance.new("TextBox")
local ScriptTextBox2 = Instance.new("TextBox")
local ScriptTextBox3 = Instance.new("TextBox")
local ExecuteButton = Instance.new("TextButton")
local BottomText = Instance.new("TextLabel")
local SpeedPageFrame = Instance.new("Frame")
local SpeedTextBox = Instance.new("TextBox")
local SetSpeedButton = Instance.new("TextButton")
local Tab1Button = Instance.new("TextButton")
local Tab2Button = Instance.new("TextButton")
local Tab3Button = Instance.new("TextButton")

-- Propriétés de l'interface utilisateur
D00bleExecGui.Name = "D00bleExecGui"
D00bleExecGui.Parent = game.CoreGui
D00bleExecGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

-- MainFrame
MainFrame.Name = "MainFrame"
MainFrame.Parent = D00bleExecGui
MainFrame.BackgroundColor3 = Color3.new(0.2, 0.2, 0.2) -- Gris foncé
MainFrame.BorderColor3 = Color3.new(1, 0, 0) -- Rouge
MainFrame.BorderSizePixel = 5
MainFrame.Position = UDim2.new(0.15, 0, 0.15, 0)
MainFrame.Size = UDim2.new(0.7, 0, 0.7, 0)
MainFrame.Active = true
MainFrame.Draggable = true -- Rend le GUI déplaçable

-- Page d'accueil (WelcomeFrame)
WelcomeFrame.Name = "WelcomeFrame"
WelcomeFrame.Parent = MainFrame
WelcomeFrame.Size = UDim2.new(1, 0, 1, 0)
WelcomeFrame.BackgroundColor3 = Color3.new(0.2, 0.2, 0.2) -- Gris foncé

WelcomeText.Name = "WelcomeText"
WelcomeText.Parent = WelcomeFrame
WelcomeText.BackgroundTransparency = 1
WelcomeText.Size = UDim2.new(1, 0, 0.8, 0)
WelcomeText.Position = UDim2.new(0, 0, 0.1, 0)
WelcomeText.Font = Enum.Font.Gotham
WelcomeText.Text = "WELCOME: Thank you for using our D00ble executor"
WelcomeText.TextColor3 = Color3.new(1, 1, 1)
WelcomeText.TextSize = 18
WelcomeText.TextWrapped = true

-- Boutons de navigation
HomeButton.Name = "HomeButton"
HomeButton.Parent = MainFrame
HomeButton.BackgroundColor3 = Color3.new(0, 0, 0) -- Noir
HomeButton.BorderColor3 = Color3.new(1, 0, 0) -- Rouge
HomeButton.BorderSizePixel = 5
HomeButton.Position = UDim2.new(0, 0, 0, 0)
HomeButton.Size = UDim2.new(0.1, 0, 0.1, 0)
HomeButton.Font = Enum.Font.Gotham
HomeButton.Text = "🏠"
HomeButton.TextColor3 = Color3.new(1, 1, 1)
HomeButton.TextSize = 24

DocumentButton.Name = "DocumentButton"
DocumentButton.Parent = MainFrame
DocumentButton.BackgroundColor3 = Color3.new(0, 0, 0) -- Noir
DocumentButton.BorderColor3 = Color3.new(1, 0, 0) -- Rouge
DocumentButton.BorderSizePixel = 5
DocumentButton.Position = UDim2.new(0, 0, 0.1, 0)
DocumentButton.Size = UDim2.new(0.1, 0, 0.1, 0)
DocumentButton.Font = Enum.Font.Gotham
DocumentButton.Text = "📜"
DocumentButton.TextColor3 = Color3.new(1, 1, 1)
DocumentButton.TextSize = 24

SearchButton.Name = "SearchButton"
SearchButton.Parent = MainFrame
SearchButton.BackgroundColor3 = Color3.new(0, 0, 0) -- Noir
SearchButton.BorderColor3 = Color3.new(1, 0, 0) -- Rouge
SearchButton.BorderSizePixel = 5
SearchButton.Position = UDim2.new(0, 0, 0.2, 0)
SearchButton.Size = UDim2.new(0.1, 0, 0.1, 0)
SearchButton.Font = Enum.Font.Gotham
SearchButton.Text = "🔎"
SearchButton.TextColor3 = Color3.new(1, 1, 1)
SearchButton.TextSize = 24

SettingsButton.Name = "SettingsButton"
SettingsButton.Parent = MainFrame
SettingsButton.BackgroundColor3 = Color3.new(0, 0, 0) -- Noir
SettingsButton.BorderColor3 = Color3.new(1, 0, 0) -- Rouge
SettingsButton.BorderSizePixel = 5
SettingsButton.Position = UDim2.new(0, 0, 0.3, 0)
SettingsButton.Size = UDim2.new(0.1, 0, 0.1, 0)
SettingsButton.Font = Enum.Font.Gotham
SettingsButton.Text = "⚙"
SettingsButton.TextColor3 = Color3.new(1, 1, 1)
SettingsButton.TextSize = 24

CloseButton.Name = "CloseButton"
CloseButton.Parent = MainFrame
CloseButton.BackgroundColor3 = Color3.new(0, 0, 0)
CloseButton.BorderColor3 = Color3.new(1, 0, 0)
CloseButton.BorderSizePixel = 5
CloseButton.Position = UDim2.new(0.9, 0, 0, 0)
CloseButton.Size = UDim2.new(0.1, 0, 0.1, 0)
CloseButton.Font = Enum.Font.Gotham
CloseButton.Text = "✖"
CloseButton.TextColor3 = Color3.new(1, 1, 1)
CloseButton.TextSize = 24

-- Page Scripts Hub
SearchPageFrame.Name = "SearchPageFrame"
SearchPageFrame.Parent = MainFrame
SearchPageFrame.Size = UDim2.new(1, 0, 1, 0)
SearchPageFrame.BackgroundTransparency = 1
SearchPageFrame.Visible = false

ScriptsHubText.Name = "ScriptsHubText"
ScriptsHubText.Parent = SearchPageFrame
ScriptsHubText.BackgroundTransparency = 1
ScriptsHubText.Size = UDim2.new(1, 0, 0.1, 0)
ScriptsHubText.Font = Enum.Font.Gotham
ScriptsHubText.Text = "Scripts Hub"
ScriptsHubText.TextColor3 = Color3.new(1, 1, 1)
ScriptsHubText.TextSize = 18
ScriptsHubText.TextWrapped = true

-- Fonction pour créer un bouton de script
local function createScriptButton(name, position, script)
    local button = Instance.new("TextButton")
    button.Name = name
    button.Parent = SearchPageFrame
    button.BackgroundColor3 = Color3.new(0, 0, 0) -- Noir
    button.BorderColor3 = Color3.new(1, 0, 0) -- Rouge
    button.BorderSizePixel = 5
    button.Size = UDim2.new(0.8, 0, 0.1, 0)
    button.Position = position
    button.Font = Enum.Font.Gotham
    button.Text = name
    button.TextColor3 = Color3.new(1, 1, 1)
    button.TextSize = 14
    
    button.MouseButton1Click:Connect(function()
        ScriptTextBox.Text = script
        showScriptPage()
    end)
    
    return button
end

-- Création des boutons de script
createScriptButton("Ghost Hub", UDim2.new(0.1, 0, 0.3, 0), [[
    loadstring(game:HttpGet('https://raw.githubusercontent.com/GhostPlayer352/Test4/main/GhostHub'))()
]])
createScriptButton("Fly v3", UDim2.new(0.1, 0, 0.45, 0), [[
    loadstring(game:HttpGet("https://raw.githubusercontent.com/XNEOFF/FlyGuiV3/main/FlyGuiV3.txt"))()
]])
createScriptButton("IY", UDim2.new(0.1, 0, 0.6, 0), [[
    loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))()
]])
createScriptButton("Remote Spy", UDim2.new(0.1, 0, 0.75, 0), [[
    loadstring(game:HttpGet("https://pastebin.com/raw/BDhSQqUU", true))()
]])

-- Page d'exécution du script (ScriptFrame)
ScriptFrame.Name = "ScriptFrame"
ScriptFrame.Parent = MainFrame
ScriptFrame.Size = UDim2.new(1, 0, 1, 0)
ScriptFrame.BackgroundTransparency = 1
ScriptFrame.Visible = false

-- Création des `TextBox` et `TextBoxContainer` pour les onglets Tab1, Tab2, Tab3
TextBoxContainer1.Name = "TextBoxContainer1"
TextBoxContainer1.Parent = ScriptFrame
TextBoxContainer1.BackgroundColor3 = Color3.new(0.5, 0.5, 0.5) -- Gris
TextBoxContainer1.BorderColor3 = Color3.new(1, 0, 0) -- Rouge
TextBoxContainer1.BorderSizePixel = 5
TextBoxContainer1.Position = UDim2.new(0.1, 0, 0.2, 0)
TextBoxContainer1.Size = UDim2.new(0.8, 0, 0.5, 0)

ScriptTextBox1.Name = "ScriptTextBox1"
ScriptTextBox1.Parent = TextBoxContainer1
ScriptTextBox1.BackgroundColor3 = Color3.new(1, 1, 1)
ScriptTextBox1.BackgroundTransparency = 0.5
ScriptTextBox1.Position = UDim2.new(0, 5, 0, 5)
ScriptTextBox1.Size = UDim2.new(1, -10, 1, -10)
ScriptTextBox1.Font = Enum.Font.Code
ScriptTextBox1.MultiLine = true
ScriptTextBox1.PlaceholderText = "--Enter your script here--"
ScriptTextBox1.TextColor3 = Color3.new(0, 0, 0)
ScriptTextBox1.TextSize = 14
ScriptTextBox1.TextWrapped = true
ScriptTextBox1.TextXAlignment = Enum.TextXAlignment.Left

TextBoxContainer2.Name = "TextBoxContainer2"
TextBoxContainer2.Parent = ScriptFrame
TextBoxContainer2.BackgroundColor3 = Color3.new(0.5, 0.5, 0.5) -- Gris
TextBoxContainer2.BorderColor3 = Color3.new(1, 0, 0) -- Rouge
TextBoxContainer2.BorderSizePixel = 5
TextBoxContainer2.Position = UDim2.new(0.1, 0, 0.2, 0)
TextBoxContainer2.Size = UDim2.new(0.8, 0, 0.5, 0)

ScriptTextBox2.Name = "ScriptTextBox2"
ScriptTextBox2.Parent = TextBoxContainer2
ScriptTextBox2.BackgroundColor3 = Color3.new(1, 1, 1)
ScriptTextBox2.BackgroundTransparency = 0.5
ScriptTextBox2.Position = UDim2.new(0, 5, 0, 5)
ScriptTextBox2.Size = UDim2.new(1, -10, 1, -10)
ScriptTextBox2.Font = Enum.Font.Code
ScriptTextBox2.MultiLine = true
ScriptTextBox2.PlaceholderText = "--Enter your script here--"
ScriptTextBox2.TextColor3 = Color3.new(0, 0, 0)
ScriptTextBox2.TextSize = 14
ScriptTextBox2.TextWrapped = true
ScriptTextBox2.TextXAlignment = Enum.TextXAlignment.Left

TextBoxContainer3.Name = "TextBoxContainer3"
TextBoxContainer3.Parent = ScriptFrame
TextBoxContainer3.BackgroundColor3 = Color3.new(0.5, 0.5, 0.5) -- Gris
TextBoxContainer3.BorderColor3 = Color3.new(1, 0, 0) -- Rouge
TextBoxContainer3.BorderSizePixel = 5
TextBoxContainer3.Position = UDim2.new(0.1, 0, 0.2, 0)
TextBoxContainer3.Size = UDim2.new(0.8, 0, 0.5, 0)

ScriptTextBox3.Name = "ScriptTextBox3"
ScriptTextBox3.Parent = TextBoxContainer3
ScriptTextBox3.BackgroundColor3 = Color3.new(1, 1, 1)
ScriptTextBox3.BackgroundTransparency = 0.5
ScriptTextBox3.Position = UDim2.new(0, 5, 0, 5)
ScriptTextBox3.Size = UDim2.new(1, -10, 1, -10)
ScriptTextBox3.Font = Enum.Font.Code
ScriptTextBox3.MultiLine = true
ScriptTextBox3.PlaceholderText = "--Enter your script here--"
ScriptTextBox3.TextColor3 = Color3.new(0, 0, 0)
ScriptTextBox3.TextSize = 14
ScriptTextBox3.TextWrapped = true
ScriptTextBox3.TextXAlignment = Enum.TextXAlignment.Left

-- Cache les TextBoxContainer pour commencer
TextBoxContainer2.Visible = false
TextBoxContainer3.Visible = false

-- Boutons Tab 1, Tab 2, Tab 3
Tab1Button.Name = "Tab1Button"
Tab1Button.Parent = ScriptFrame
Tab1Button.BackgroundColor3 = Color3.new(0, 0, 0) -- Noir
Tab1Button.BorderColor3 = Color3.new(1, 0, 0) -- Rouge
Tab1Button.BorderSizePixel = 5
Tab1Button.Size = UDim2.new(0.15, 0, 0.05, 0)
Tab1Button.Position = UDim2.new(0.1, 0, 0.1, 0)
Tab1Button.Font = Enum.Font.Gotham
Tab1Button.Text = "Tab 1"
Tab1Button.TextColor3 = Color3.new(1, 1, 1)
Tab1Button.TextSize = 14

Tab2Button.Name = "Tab2Button"
Tab2Button.Parent = ScriptFrame
Tab2Button.BackgroundColor3 = Color3.new(0, 0, 0) -- Noir
Tab2Button.BorderColor3 = Color3.new(1, 0, 0) -- Rouge
Tab2Button.BorderSizePixel = 5
Tab2Button.Size = UDim2.new(0.15, 0, 0.05, 0)
Tab2Button.Position = UDim2.new(0.425, 0, 0.1, 0)
Tab2Button.Font = Enum.Font.Gotham
Tab2Button.Text = "Tab 2"
Tab2Button.TextColor3 = Color3.new(1, 1, 1)
Tab2Button.TextSize = 14

Tab3Button.Name = "Tab3Button"
Tab3Button.Parent = ScriptFrame
Tab3Button.BackgroundColor3 = Color3.new(0, 0, 0) -- Noir
Tab3Button.BorderColor3 = Color3.new(1, 0, 0) -- Rouge
Tab3Button.BorderSizePixel = 5
Tab3Button.Size = UDim2.new(0.15, 0, 0.05, 0)
Tab3Button.Position = UDim2.new(0.75, 0, 0.1, 0)
Tab3Button.Font = Enum.Font.Gotham
Tab3Button.Text = "Tab 3"
Tab3Button.TextColor3 = Color3.new(1, 1, 1)
Tab3Button.TextSize = 14

-- Gestionnaires d'événements pour les boutons Tab 1, Tab 2, Tab 3
Tab1Button.MouseButton1Click:Connect(function()
    TextBoxContainer1.Visible = true
    TextBoxContainer2.Visible = false
    TextBoxContainer3.Visible = false
end)

Tab2Button.MouseButton1Click:Connect(function()
    TextBoxContainer1.Visible = false
    TextBoxContainer2.Visible = true
    TextBoxContainer3.Visible = false
end)

Tab3Button.MouseButton1Click:Connect(function()
    TextBoxContainer1.Visible = false
    TextBoxContainer2.Visible = false
    TextBoxContainer3.Visible = true
end)

ExecuteButton.Name = "ExecuteButton"
ExecuteButton.Parent = ScriptFrame
ExecuteButton.BackgroundColor3 = Color3.new(0, 0, 0)
ExecuteButton.BorderColor3 = Color3.new(1, 0, 0)
ExecuteButton.BorderSizePixel = 5
ExecuteButton.Position = UDim2.new(0.1, 0, 0.8, 0)
ExecuteButton.Size = UDim2.new(0.2, 0, 0.1, 0)
ExecuteButton.Font = Enum.Font.Gotham
ExecuteButton.Text = "Exe"
ExecuteButton.TextColor3 = Color3.new(1, 1, 1)
ExecuteButton.TextSize = 14

-- Gestionnaire d'événements pour l'exécution du script
ExecuteButton.MouseButton1Click:Connect(function()
    local scriptToExecute = ""
    if TextBoxContainer1.Visible then
        scriptToExecute = ScriptTextBox1.Text
    elseif TextBoxContainer2.Visible then
        scriptToExecute = ScriptTextBox2.Text
    elseif TextBoxContainer3.Visible then
        scriptToExecute = ScriptTextBox3.Text
    end
    
    if scriptToExecute ~= "" then
        local success, errorMessage = pcall(function()
            loadstring(scriptToExecute)()
        end)
        if not success then
            warn("Erreur d'exécution du script: " .. errorMessage)
        end
    end
end)

BottomText.Name = "BottomText"
BottomText.Parent = ScriptFrame
BottomText.BackgroundTransparency = 1
BottomText.Position = UDim2.new(0.7, 0, 0.9, 0)
BottomText.Size = UDim2.new(0.3, 0, 0.1, 0)
BottomText.Font = Enum.Font.Gotham
BottomText.Text = "By D00bleHaxx"
BottomText.TextColor3 = Color3.new(1, 1, 1)
BottomText.TextSize = 14
BottomText.TextWrapped = true
BottomText.TextXAlignment = Enum.TextXAlignment.Right
BottomText.TextYAlignment = Enum.TextYAlignment.Bottom

-- Page de réglage de vitesse (SpeedPageFrame)
SpeedPageFrame.Name = "SpeedPageFrame"
SpeedPageFrame.Parent = MainFrame
SpeedPageFrame.Size = UDim2.new(1, 0, 1, 0)
SpeedPageFrame.BackgroundTransparency = 1
SpeedPageFrame.Visible = false

SpeedTextBox.Name = "SpeedTextBox"
SpeedTextBox.Parent = SpeedPageFrame
SpeedTextBox.BackgroundColor3 = Color3.new(1, 1, 1)
SpeedTextBox.Position = UDim2.new(0.1, 0, 0.2, 0)
SpeedTextBox.Size = UDim2.new(0.8, 0, 0.1, 0)
SpeedTextBox.Font = Enum.Font.Gotham
SpeedTextBox.PlaceholderText = "Enter speed"
SpeedTextBox.TextColor3 = Color3.new(0, 0, 0)
SpeedTextBox.TextSize = 14

SetSpeedButton.Name = "SetSpeedButton"
SetSpeedButton.Parent = SpeedPageFrame
SetSpeedButton.BackgroundColor3 = Color3.new(0, 0, 0)
SetSpeedButton.BorderColor3 = Color3.new(1, 0, 0)
SetSpeedButton.BorderSizePixel = 5
SetSpeedButton.Position = UDim2.new(0.1, 0, 0.4, 0)
SetSpeedButton.Size = UDim2.new(0.2, 0, 0.1, 0)
SetSpeedButton.Font = Enum.Font.Gotham
SetSpeedButton.Text = "Set Speed"
SetSpeedButton.TextColor3 = Color3.new(1, 1, 1)
SetSpeedButton.TextSize = 14

-- Gestionnaire d'événement pour le bouton Set Speed
SetSpeedButton.MouseButton1Click:Connect(function()
    local speed = tonumber(SpeedTextBox.Text)
    if speed then
        local player = game.Players.LocalPlayer
        local character = player.Character
        if character then
            local humanoid = character:FindFirstChildOfClass("Humanoid")
            if humanoid then
                humanoid.WalkSpeed = speed
                print("Vitesse réglée à", speed)
            else
                warn("Le joueur n'a pas de personnage ou d'humanoïde")
            end
        end
    else
        warn("Veuillez entrer une valeur numérique valide")
    end
end)

-- Fonction pour gérer la visibilité du GUI
local function toggleGui()
    MainFrame.Visible = not MainFrame.Visible
    if MainFrame.Visible then
        CloseButton.Text = "✖"
    else
        CloseButton.Text = "＋"
    end
end

-- Gestionnaire d'événements pour le bouton CloseButton
CloseButton.MouseButton1Click:Connect(toggleGui)

-- Fonctions de navigation entre les pages
local function showWelcomePage()
    WelcomeFrame.Visible = true
    ScriptFrame.Visible = false
    SearchPageFrame.Visible = false
    SpeedPageFrame.Visible = false
end

local function showScriptPage()
    WelcomeFrame.Visible = false
    ScriptFrame.Visible = true
    SearchPageFrame.Visible = false
    SpeedPageFrame.Visible = false
end

local function showSearchPage()
    WelcomeFrame.Visible = false
    ScriptFrame.Visible = false
    SearchPageFrame.Visible = true
    SpeedPageFrame.Visible = false
end

local function showSpeedPage()
    WelcomeFrame.Visible = false
    ScriptFrame.Visible = false
    SearchPageFrame.Visible = false
    SpeedPageFrame.Visible = true
end

-- Gestionnaires d'événements pour les boutons de navigation
HomeButton.MouseButton1Click:Connect(showWelcomePage)
DocumentButton.MouseButton1Click:Connect(showScriptPage)
SearchButton.MouseButton1Click:Connect(showSearchPage)
SettingsButton.MouseButton1Click:Connect(showSpeedPage)

-- Gestionnaire d'événements pour l'exécution du script
ExecuteButton.MouseButton1Click:Connect(function()
    local scriptToExecute = ""
    if TextBoxContainer1.Visible then
        scriptToExecute = ScriptTextBox1.Text
    elseif TextBoxContainer2.Visible then
        scriptToExecute = ScriptTextBox2.Text
    elseif TextBoxContainer3.Visible then
        scriptToExecute = ScriptTextBox3.Text
    end
    
    if scriptToExecute ~= "" then
        local success, errorMessage = pcall(function()
            loadstring(scriptToExecute)()
        end)
        if not success then
            warn("Erreur d'exécution du script: " .. errorMessage)
        end
    end
end)

-- Initialement, affiche la page d'accueil
showWelcomePage()