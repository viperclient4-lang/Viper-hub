local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()

local Window = Rayfield:CreateWindow({
   Name = "🐍 Viper Client | Original",
   LoadingTitle = "Carregando Viper...",
   LoadingSubtitle = "por guizin",
   ConfigurationSaving = {
      Enabled = false
   },
   KeySystem = false -- Removido para teste
})

local MainTab = Window:CreateTab("Principal", 4483362458)

MainTab:CreateSection("Atributos")

MainTab:CreateSlider({
   Name = "Velocidade (Speed)",
   Range = {16, 300},
   Increment = 1,
   Suffix = "Studs",
   CurrentValue = 16,
   Flag = "Slider1",
   Callback = function(Value)
      if game.Players.LocalPlayer.Character and game.Players.LocalPlayer.Character:FindFirstChild("Humanoid") then
         game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = Value
      end
   end,
})

MainTab:CreateSlider({
   Name = "Pulo (Jump Power)",
   Range = {50, 300},
   Increment = 1,
   Suffix = "Power",
   CurrentValue = 50,
   Flag = "Slider2",
   Callback = function(Value)
      if game.Players.LocalPlayer.Character and game.Players.LocalPlayer.Character:FindFirstChild("Humanoid") then
         game.Players.LocalPlayer.Character.Humanoid.UseJumpPower = true
         game.Players.LocalPlayer.Character.Humanoid.JumpPower = Value
      end
   end,
})

Rayfield:Notify({
   Title = "Viper Client",
   Content = "Script executado com sucesso!",
   Duration = 5,
   Image = 4483362458,
})
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
