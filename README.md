RegisterNetEvent('QBCore:Client:OnPlayerLoaded')
AddEventHandler('QBCore:Client:OnPlayerLoaded', function()
    QBCore.Functions.GetPlayerData(function(PlayerData)
        -- Player data is now available, proceed with script logic
        TriggerEvent('script:ready') -- Trigger a custom event
    end)
end)
