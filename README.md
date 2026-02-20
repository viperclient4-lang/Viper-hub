local RedzLib = loadstring(game:HttpGet("https://raw.githubusercontent.com/REDZHUB/RedzLibV5/main/Source.lua"))()

-- Criando a Janela (Sem Key agora)
local Window = RedzLib:MakeWindow({
  Name = "🐍 Viper Client | Free",
  Subtitle = "por guizin",
  SaveConfig = true
})

-- ABA PRINCIPAL
Window:AddTab("Principal")

Window:AddSection("Atributos do Jogador")

Window:AddSlider({
  Name = "Velocidade (Speed)",
  Min = 16,
  Max = 250,
  Default = 16,
  Callback = function(Value)
     if game.Players.LocalPlayer.Character and game.Players.LocalPlayer.Character:FindFirstChild("Humanoid") then
        game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = Value
     end
  end
})

Window:AddSlider({
  Name = "Pulo (Jump)",
  Min = 50,
  Max = 250,
  Default = 50,
  Callback = function(Value)
     if game.Players.LocalPlayer.Character and game.Players.LocalPlayer.Character:FindFirstChild("Humanoid") then
        game.Players.LocalPlayer.Character.Humanoid.UseJumpPower = true
        game.Players.LocalPlayer.Character.Humanoid.JumpPower = Value
     end
  end
})

-- ABA DE CRÉDITOS
Window:AddTab("Informações")

Window:AddSection("Desenvolvedor")
Window:AddLabel("Criado por: guizin")

Window:AddSection("Versão")
Window:AddLabel("Viper v1.0 - Sem Key")
  Name = "Pulo (Jump)",
  Min = 50,
  Max = 250,
  Default = 50,
  Callback = function(Value)
     if game.Players.LocalPlayer.Character and game.Players.LocalPlayer.Character:FindFirstChild("Humanoid") then
        game.Players.LocalPlayer.Character.Humanoid.UseJumpPower = true
        game.Players.LocalPlayer.Character.Humanoid.JumpPower = Value
     end
  end
})

-- ABA DE CRÉDITOS
Window:AddTab("Créditos")

Window:AddSection("Desenvolvedor")
Window:AddLabel("Feito por: guizin")

Window:AddSection("Status")
Window:AddLabel("Versão Grátis")
Window:AddLabel("Válido até: 21/02/26")
