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

## Customization Options (Experimental)

1. Modifiying elements in predefined view

You can use methods like ```removeCallButton()``` and ```setAudioButtonIcon()``` to change the look of the resulting Activity

2. Add Custom View in predefined Activity

You can add your own view elements in the activity - 

First create a view group:
```ViewGroup mLinearLayout = (ViewGroup) findViewById(R.id.linear_layout);```

Get the view from the layout inflator:
```View view = videocall.getView(mLinearLayout)```

Add desired customizations to the view

Add the view to the layout

```videocall.addView(view);```

3. Create custom layout using callbacks

Add an event listener
```videocall.setViewListener(new AgoraVideoCall.ViewListener() {
	@Override
	public void onUserJoined(SurfaceView surfaceview, int uid) {
	}
	@Override
	public void onUserLeft(int uid) {
	}
   }
```

You can add custom logic to these methods
