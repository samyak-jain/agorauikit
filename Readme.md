# Agora UI KIT

## How to Use

1. Import Library

2. Create a videocall object

```
AgoraVideoCall videoCall = new AgoraVideoCall(getApplicationContext(), appid, token, channel);
```

3. Get the predefined intent

```
Intent intent = videocall.start();
```

4. Start the activity

```
startActivity(intent);
```

## Customization Options

For customizing the call screen a few methods are provided  

First create the config object

```
UIConfig config = new UIConfig();
```

Call the methods that you want to use

```
config.hideSwitchCamera();
config.hideVideoMute();
```

You can also chain the methods

```
config.hideAudioMute().showCheckButton();
```

We also provide a check button which you can use to start your custom intent. For example:  

Say you want the check button to start your custom activity called TestActivity

```
config.showCheckButton();
Intent intent = new Intent(getBaseContext(), TestActivity.class);
videocall.setIntent(intent);
```

You can then call the start method 

```
startActivity(videocall.start())
```
