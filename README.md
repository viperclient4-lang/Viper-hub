local RedzLib = loadstring(game:HttpGet("https://raw.githubusercontent.com/REDZHUB/RedzLibV5/main/Source.lua"))()

-- Criando a Janela
local Window = RedzLib:MakeWindow({
  Name = "🐍 Viper Client | Trial",
  Subtitle = "por guizin",
  SaveConfig = true
})

-- SISTEMA DE KEY (TELA INICIAL)
Window:AddTab("Chave de Acesso")

Window:AddSection("Verificação")

Window:AddTextBox({
  Name = "Digite a Key:",
  Default = "",
  PlaceholderText = "Sua key aqui...",
  Callback = function(Value)
     if Value == "beta_teste" then
        RedzLib:SetClipboard("Link do seu Discord aqui") -- Opcional
        RedzLib:Notify({
            Title = "Viper Client",
            Content = "Acesso Liberado! Use o menu lateral.",
            Duration = 5
        })
     else
        RedzLib:Notify({
            Title = "Erro",
            Content = "Key incorreta! Tente novamente.",
            Duration = 5
        })
     end
  end
})

Window:AddButton({
  Name = "Obter Key (Copiar Link)",
  Callback = function()
     setclipboard("discord.gg/seulink")
  end
})

-- ABA DE MOVIMENTAÇÃO
Window:AddTab("Movimentação")

Window:AddSection("Atributos")

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
Window:AddTab("Créditos")

Window:AddSection("Desenvolvedor")
Window:AddLabel("Feito por: guizin")

Window:AddSection("Status")
Window:AddLabel("Versão Grátis")
Window:AddLabel("Válido até: 21/02/26")
