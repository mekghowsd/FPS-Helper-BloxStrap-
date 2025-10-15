# FPS Helper for Bloxstrap

These settings are a curated collection of Roblox fast flags (FFlags) that aim to improve network latency, reduce visual overhead, and squeeze out a little more FPS when you launch Roblox through [Bloxstrap](https://github.com/pizzaboxer/bloxstrap). The defaults supplied by Roblox are a good fit for most players, so treat every change here as an experiment that **you should test and tweak for your own hardware and network**.

## How to import the presets

1. Launch Bloxstrap and open **Fast Flags**.
2. Choose **Edit JSON**.
3. Copy the JSON block for the preset you want and paste it into the editor. You can mix and match values, but keep an eye out for conflicting keys.
4. Save and restart Roblox from Bloxstrap to apply the changes.

If you ever need to undo these tweaks, you can clear the JSON or click **Reset Fast Flags** inside Bloxstrap.

> [!CAUTION]
> Roblox can and does change the behaviour of FFlags at any time. If the client behaves oddly after applying a preset, revert the change or remove only the suspect flag to diagnose the issue. Tweaking network-related flags can impact stability on poor connections, while removing textures may break experiences that rely on specific materials.

## Presets

### Lower latency / ping

```json
{
  "DFIntConnectionMTUSize": 900,
  "FIntRakNetResendBufferArrayLength": 128,
  "FFlagOptimizeNetwork": true,
  "FFlagOptimizeNetworkRouting": true,
  "FFlagOptimizeNetworkTransport": true,
  "FFlagOptimizeServerTickRate": true,
  "DFIntServerPhysicsUpdateRate": 60,
  "DFIntServerTickRate": 60,
  "DFIntRakNetResendRttMultiple": 1,
  "DFIntRaknetBandwidthPingSendEveryXSeconds": 1,
  "DFIntOptimizePingThreshold": 50,
  "DFIntPlayerNetworkUpdateQueueSize": 20,
  "DFIntPlayerNetworkUpdateRate": 60,
  "DFIntNetworkPrediction": 120,
  "DFIntNetworkLatencyTolerance": 1,
  "DFIntMinimalNetworkPrediction": 0.1
}
```

### Disable textures (higher FPS, low visual quality)

```json
{
  "FStringPartTexturePackTable2022": "{\"foil\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[238,238,238,255]},\"asphalt\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[227,227,228,234]},\"basalt\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[160,160,158,238]},\"brick\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[229,214,205,227]},\"cobblestone\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[218,219,219,243]},\"concrete\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[225,225,224,255]},\"crackedlava\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[76,79,81,156]},\"diamondplate\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[210,210,210,255]},\"fabric\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[221,221,221,255]},\"glacier\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[225,229,229,243]},\"glass\":{\"ids\":[\"rbxassetid://9873284556\",\"rbxassetid://9438453972\"],\"color\":[254,254,254,7]},\"granite\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[210,206,200,255]},\"grass\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[196,196,189,241]},\"ground\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[165,165,160,240]},\"ice\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[235,239,241,248]},\"leafygrass\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[182,178,175,234]},\"limestone\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[250,248,243,250]},\"marble\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[181,183,193,249]},\"metal\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[226,226,226,255]},\"mud\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[193,192,193,252]},\"pavement\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[218,218,219,236]},\"pebble\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[204,203,201,234]},\"plastic\":{\"ids\":[\"\",\"rbxassetid://0\"],\"color\":[255,255,255,255]},\"rock\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[211,211,210,248]},\"corrodedmetal\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[206,177,163,180]},\"salt\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[249,249,249,255]},\"sand\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[218,216,210,240]},\"sandstone\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[241,234,230,246]},\"slate\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[235,234,235,254]},\"snow\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[239,240,240,255]},\"wood\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[217,209,208,255]},\"woodplanks\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[207,208,206,254]}}",
  "FStringPartTexturePackTablePre2022": "{\"foil\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[255,255,255,255]},\"brick\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[204,201,200,232]},\"cobblestone\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[212,200,187,250]},\"concrete\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[208,208,208,255]},\"diamondplate\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[170,170,170,255]},\"fabric\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[105,104,102,244]},\"glass\":{\"ids\":[\"rbxassetid://7547304948\",\"rbxassetid://7546645118\"],\"color\":[254,254,254,7]},\"granite\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[113,113,113,255]},\"grass\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[165,165,159,255]},\"ice\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[255,255,255,255]},\"marble\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[199,199,199,255]},\"metal\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[199,199,199,255]},\"pebble\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[208,208,208,255]},\"corrodedmetal\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[159,119,95,200]},\"sand\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[220,220,220,255]},\"slate\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[193,193,193,255]},\"wood\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[227,227,227,255]},\"woodplanks\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[212,209,203,255]},\"asphalt\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[123,123,123,234]},\"basalt\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[154,154,153,238]},\"crackedlava\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[74,78,80,156]},\"glacier\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[226,229,229,243]},\"ground\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[114,114,112,240]},\"leafygrass\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[121,117,113,234]},\"limestone\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[235,234,230,250]},\"mud\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[130,130,130,252]},\"pavement\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[142,142,144,236]},\"rock\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[154,154,154,248]},\"salt\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[220,220,221,255]},\"sandstone\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[174,171,169,246]},\"snow\":{\"ids\":[\"rbxassetid://0\",\"rbxassetid://0\"],\"color\":[218,218,218,255]}}",
  "FFlagMSRefactor5": false,
  "FFlagDebugSkyGray": true
}
```

### Higher FPS (general performance tweaks)

```json
{
  "DFIntDebugFRMQualityLevelOverride": 1,
  "DFFlagTextureQualityOverrideEnabled": true,
  "DFIntTextureQualityOverride": 3,
  "DFIntConnectionMTUSize": 900,
  "FFlagDebugDisableTelemetryEphemeralCounter": true,
  "FFlagDebugDisableTelemetryEphemeralStat": true,
  "FFlagDebugDisableTelemetryEventIngest": true,
  "FFlagDebugDisableTelemetryPoint": true,
  "FFlagDebugDisableTelemetryV2Counter": true,
  "FFlagDebugDisableTelemetryV2Event": true,
  "FFlagDebugDisableTelemetryV2Stat": true,
  "FFlagDebugSkyGray": true,
  "FFlagDebugDisplayFPS": true,
  "FIntFRMMinGrassDistance": 0,
  "FIntFRMMaxGrassDistance": 0,
  "FIntRenderGrassDetailStrands": 0,
  "FIntRenderGrassHeightScaler": 0,
  "DFIntMaxFrameBufferSize": 4,
  "DebugGraphicsDisableVulkan": true,
  "DebugGraphicsDisableVulkan11": true,
  "DebugGraphicsDisableOpenGL": true,
  "DebugGraphicPreferD3D11": true,
  "FIntRobloxGuiBlurIntensity": 0,
  "FIntFullscreenTitleBarTriggerDelayMillis": 18000000,
  "FFlagFastGPULightCulling3": true,
  "FFlagNewLightAttenuation": true,
  "FFlagDisablePostFx": true,
  "DFIntClientLightingTechnologyChangedTelemetryHundredthsPercent": 0,
  "DFIntClientLightingEnvmapPlacementTelemetryHundredthsPercent": 100,
  "FIntMockClientLightingTechnologyIxpExperimentMode": 0,
  "FIntMockClientLightingTechnologyIxpExperimentQualityLevel": 7
}
```

## Tips

- Apply one preset at a time so it is easier to understand how each tweak impacts your experience.
- Consider saving each preset as a separate JSON file so you can quickly import and revert from a known baseline.
- Some experiences may enforce their own lighting or post-processing effects. If a preset does not change anything, it may be overridden by the game.

Happy experimenting!
