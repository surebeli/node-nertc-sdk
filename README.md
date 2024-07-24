# NERTC Electron SDK API 概览

### 说明

[NERtcEngine](NERtcEngine.html) 包含了 Electron NeRTC 接口。
[NERtcChannel](NERtcChannel.html) 包含了 Electron NeRTC Channel 接口。


### 房间管理

|方法|功能描述|起始版本|
|---|---|---|
[initialize](NERtcEngine.html#initialize__anchor)|初始化 NERTC SDK 服务|V3.9.0
[release](NERtcEngine.html#release__anchor)|销毁 IRtcEngine 对象|V3.9.0
[getVersion](NERtcEngine.html#getVersion__anchor)|查询 SDK 版本号|V3.9.0
[setChannelProfile](NERtcEngine.html#setChannelProfile__anchor)|设置房间场景|V3.9.0
[setClientRole](NERtcEngine.html#setClientRole__anchor)|设置用户角色|V3.9.0
[joinChannel](NERtcEngine.html#joinChannel__anchor)|加入房间|V3.9.0
[leaveChannel](NERtcEngine.html#leaveChannel__anchor)|离开房间|V3.9.0
[getConnectionState](NERtcEngine.html#getConnectionState__anchor)|获取网络连接状态|V3.9.0
[createChannel](NERtcEngine.html#createChannel__anchor)|创建一个 NERtcChannel 对象|V5.5.21
[joinChannelWithOptions](NERtcEngine.html#joinChannelWithOptions__anchor)|加入房间附带可选信息|V5.5.21
[switchChannel](NERtcEngine.html#switchChannel__anchor)|快速切换音视频房间|V4.4.8
[switchChannelWithOptions](NERtcEngine.html#switchChannelWithOptions__anchor)|快速切换音视频房间，可带自定义信息|V4.4.8
[switchChannelWithOptionsEx](NERtcEngine.html#switchChannelWithOptionsEx__anchor)|快速切换音视频房间扩展接口|V5.4.0

### 房间事件

|事件|功能描述|起始版本|
|---|---|---|
[onClientRoleChanged](NERtcEngine.html#event:onClientRoleChanged__anchor)|用户角色已切换回调|V3.9.0
[onJoinChannel](NERtcEngine.html#event:onJoinChannel__anchor)|加入房间回调|V3.9.0
[onRejoinChannel](NERtcEngine.html#event:onRejoinChannel__anchor)|重新加入房间回调|V3.9.0
[onLeaveChannel](NERtcEngine.html#event:onLeaveChannel__anchor)|离开房间回调|V3.9.0
[onUserJoined](NERtcEngine.html#event:onUserJoined__anchor)|远端用户加入当前房间回调|V3.9.0
[onUserLeft](NERtcEngine.html#event:onUserLeft__anchor)|远端用户离开当前房间回调|V3.9.0
[onDisconnect](NERtcEngine.html#event:onDisconnect__anchor)|服务器连接断开回调|V3.9.0
[onReconnectingStart](NERtcEngine.html#event:onReconnectingStart__anchor)|开始重连回调|V3.9.0
[onConnectionStateChange](NERtcEngine.html#event:onConnectionStateChange__anchor)|网络连接状态已改变回调|V3.9.0
[onReleasedHwResources](NERtcEngine.html#event:onReleasedHwResources__anchor)|通话结束设备资源释放回调|V3.9.0
[onRecvSEIMsg](NERtcEngine.html#event:onRecvSEIMsg__anchor)|监听 SEI 数据回调|V4.1.110
[onUserJoinedWithExtraInfo](NERtcEngine.html#event:onUserJoinedWithExtraInfo__anchor)|远端用户加入当前频道回调扩展接口|V5.4.0
[onUserLeftWithExtraInfo](NERtcEngine.html#event:onUserLeftWithExtraInfo__anchor)|远端用户离开当前频道回调扩展接口|V5.4.0


### 音频管理

|方法|功能描述|起始版本|
|---|---|---|
[setAudioProfile](NERtcEngine.html#setAudioProfile__anchor)|设置音频编码配置|V3.9.0
[adjustRecordingSignalVolume](NERtcEngine.html#adjustRecordingSignalVolume__anchor)|调节录音音量|V3.9.0
[adjustPlaybackSignalVolume](NERtcEngine.html#adjustPlaybackSignalVolume__anchor)|设置音频编码配置|V3.9.0
[enableLocalAudio](NERtcEngine.html#enableLocalAudio__anchor)|开关本地音频采集|V3.9.0
[muteLocalAudioStream](NERtcEngine.html#muteLocalAudioStream__anchor)|开关本地音频发送|V3.9.0
[subscribeRemoteAudioStream](NERtcEngine.html#subscribeRemoteAudioStream__anchor)|订阅／取消订阅指定音频流|V3.9.0
[subscribeRemoteSubStreamAudio](NERtcEngine.html#subscribeRemoteSubStreamAudio__anchor)|订阅／取消订阅指定音频辅流|V5.4.0
[setRemoteHighPriorityAudioStream](NERtcEngine.html#setRemoteHighPriorityAudioStream__anchor)|设置远端用户音频流高优先级|V4.1.110
[setAudioEffectPreset](NERtcEngine.html#setAudioEffectPreset__anchor)|设置 SDK 预设的人声的变声音效|V4.1.110
[setVoiceBeautifierPreset](NERtcEngine.html#setVoiceBeautifierPreset__anchor)|设置 SDK 预设的美声效果。调用该方法可以为本地发流用户设置 SDK 预设的人声美声效果|V4.1.110
[setLocalVoicePitch](NERtcEngine.html#setLocalVoicePitch__anchor)|设置本地语音音调。该方法改变本地说话人声音的音调|V4.1.110
[setLocalVoiceEqualization](NERtcEngine.html#setLocalVoiceEqualization__anchor)|设置本地语音音效均衡，即自定义设置本地人声均衡波段的中心频率|V4.1.110
[enableLocalSubStreamAudio](NERtcEngine.html#enableLocalSubStreamAudio__anchor)|开关本地音频辅流|V5.5.21
[muteLocalSubStreamAudio](NERtcEngine.html#muteLocalSubStreamAudio__anchor)|开关本地音频辅流发送|V5.5.21
[subscribeRemoteSubStreamAudio](NERtcEngine.html#subscribeRemoteSubStreamAudio__anchor)|订阅／取消订阅指定音频辅流|V5.5.21
[subscribeAllRemoteAudioStream](NERtcEngine.html#subscribeAllRemoteAudioStream__anchor)|订阅／取消订阅所有远端用户的音频主流|V5.5.21
[setAudioSubscribeOnlyBy](NERtcEngine.html#setAudioSubscribeOnlyBy__anchor)|设置自己的音频只能被房间内指定的人订阅|V5.5.21
[setSubscribeAudioAllowlist](NERtcEngine.html#setSubscribeAudioAllowlist__anchor)|指定只订阅的音频流|V5.5.21
[setSubscribeAudioBlocklist](NERtcEngine.html#setSubscribeAudioBlocklist__anchor)|指定不订阅的音频流|V5.5.21
[setStreamAlignmentProperty](NERtcEngine.html#setStreamAlignmentProperty__anchor)|开启精准对齐，对齐本地系统与服务端的时间|V5.5.21
[getNtpTimeOffset](NERtcEngine.html#getNtpTimeOffset__anchor)|获取本地系统时间与服务端时间差值|V5.5.21
[startAudioRecording](NERtcEngine.html#startAudioRecording__anchor)|开始客户端录音|V4.4.8
[startAudioRecordingWithConfig](NERtcEngine.html#startAudioRecordingWithConfig__anchor)|开始客户端录音扩展接口|V5.4.0
[stopAudioRecording](NERtcEngine.html#stopAudioRecording__anchor)|停止客户端录音|V5.4.0
[setLocalVoiceReverbParam](NERtcEngine.html#setLocalVoiceReverbParam__anchor)|设置本地语音混响效果|V5.4.0
[enableMediaPub](NERtcEngine.html#enableMediaPub__anchor)|开启或关闭本地媒体流（主流）的发送|V5.4.0


### 视频管理

|方法|功能描述|起始版本|
|---|---|---|
[enableLocalVideo](NERtcEngine.html#enableLocalVideo__anchor)|开关本地视频|V3.9.0
[setVideoConfig](NERtcEngine.html#setVideoConfig__anchor)|设置视频发送配置|V3.9.0
[setupLocalVideoCanvas](NERtcEngine.html#setupLocalVideoCanvas__anchor)|设置本地用户视图|V3.9.0
[setupRemoteVideoCanvas](NERtcEngine.html#setupRemoteVideoCanvas__anchor)|设置远端用户视图|V3.9.0
[setRenderMode](NERtcEngine.html#setRenderMode__anchor)|设置本地/远端视图显示模式|V3.9.0
[startVideoPreview](NERtcEngine.html#startVideoPreview__anchor)|开启视频预览|V3.9.0
[stopVideoPreview](NERtcEngine.html#stopVideoPreview__anchor)|停止视频预览|V3.9.0
[muteLocalVideoStream](NERtcEngine.html#muteLocalVideoStream__anchor)|开关本地视频发送|V3.9.0
[subscribeRemoteVideoStream](NERtcEngine.html#subscribeRemoteVideoStream__anchor)|订阅 / 取消订阅指定远端用户的视频流|V3.9.0
[setLocalVideoMirrorMode](NERtcEngine.html#setLocalVideoMirrorMode__anchor)|设置本地视频镜像模式|V3.9.0
[setParameters](NERtcEngine.html#setParameters__anchor)|复杂参数设置|V3.9.0
[getParameters](NERtcEngine.html#getParameters__anchor)|获取内部参数|V5.5.21
[sendSEIMsg](NERtcEngine.html#sendSEIMsg__anchor)| 发送媒体补充增强信息（SEI）|V4.1.110
[sendSEIMsgWithType](NERtcEngine.html#sendSEIMsgWithType__anchor)| 发送媒体补充增强信息（SEI）可选主辅流|V4.1.110
[captureImageByUid](NERtcEngine.html#captureImageByUid__anchor)| 在指定用户的画布上截图|V4.1.112
[enableLocalVideoWithType](NERtcEngine.html#enableLocalVideoWithType__anchor)|开关本地主辅流视频|V5.5.21
[setCameraCaptureConfig](NERtcEngine.html#setCameraCaptureConfig__anchor)|设置本地摄像头的视频主流采集配置|V5.5.21
[setCameraCaptureConfigWithType](NERtcEngine.html#setCameraCaptureConfigWithType__anchor)|设置本地摄像头的视频主流或辅流采集配置|V5.5.21
[setVideoConfigWithType](NERtcEngine.html#setVideoConfigWithType__anchor)|设置主辅流视频发送配置|V5.5.21
[enableDualStreamMode](NERtcEngine.html#enableDualStreamMode__anchor)|设置视频双流发送|V3.9.0
[setLocalVideoMirrorModeWithType](NERtcEngine.html#setLocalVideoMirrorModeWithType__anchor)|设置主辅流本地视频镜像模式|V5.5.21
[startVideoPreviewWithType](NERtcEngine.html#startVideoPreviewWithType__anchor)|开启主辅流视频预览|V5.5.21
[stopVideoPreviewWithType](NERtcEngine.html#stopVideoPreviewWithType__anchor)|停止主辅流视频预览|V5.5.21
[muteLocalVideoStreamWithType](NERtcEngine.html#muteLocalVideoStreamWithType__anchor)|开关本地主辅流视频发送|V5.5.21
[startChannelMediaRelay](NERtcEngine.html#startChannelMediaRelay__anchor)|开始跨房间媒体流转发|V5.5.21
[updateChannelMediaRelay](NERtcEngine.html#updateChannelMediaRelay__anchor)|更新媒体流转发的目标房间|V5.5.21
[stopChannelMediaRelay](NERtcEngine.html#stopChannelMediaRelay__anchor)|停止跨房间媒体流转发|V5.5.21
[setLocalPublishFallbackOption](NERtcEngine.html#setLocalPublishFallbackOption__anchor)|设置弱网条件下发布的音视频流回退选项|V5.5.21
[setRemoteSubscribeFallbackOption](NERtcEngine.html#setRemoteSubscribeFallbackOption__anchor)|设置弱网条件下订阅的音视频流回退选项|V5.5.21
[enableSuperResolution](NERtcEngine.html#enableSuperResolution__anchor)|启用或停止 AI 超分|V4.4.0
[enableEncryption](NERtcEngine.html#enableEncryption__anchor)|开启或关闭媒体流加密|V4.4.0
[enableVirtualBackground](NERtcEngine.html#enableVirtualBackground__anchor)|启用/禁用虚拟背景|V5.4.0
[isFeatureSupported](NERtcEngine.html#isFeatureSupported__anchor)|获取当前设备是否支持虚拟背景功能|V5.4.0
[setLocalMediaPriority](NERtcEngine.html#setLocalMediaPriority__anchor)|设置本地用户的媒体流优先级|V4.4.8
[enableLocalData](NERtcEngine.html#enableLocalData__anchor)|开启/关闭本地数据通道|V5.4.0
[subscribeRemoteData](NERtcEngine.html#subscribeRemoteData__anchor)|取消或恢复订阅指定远端用户数据通道流|V5.4.0
[sendData](NERtcEngine.html#sendData__anchor)|通过数据通道发送数据|V5.4.0
[setLocalVideoWatermarkConfigs](NERtcEngine.html#setLocalVideoWatermarkConfigs__anchor)|设置视频水印，水印在本地预览及发送过程中均生效|V5.5.20


### 本地媒体事件

|事件|功能描述|起始版本|
|---|---|---|
[onFirstVideoDataReceived](NERtcEngine.html#event:onFirstVideoDataReceived__anchor)|已显示首帧远端视频回调|V3.9.0
[onFirstAudioDataReceived](NERtcEngine.html#event:onFirstAudioDataReceived__anchor)|已接收到远端音频首帧回调|V3.9.0
[onFirstAudioFrameDecoded](NERtcEngine.html#event:onFirstAudioFrameDecoded__anchor)|已解码远端音频首帧的回调|V3.9.0
[onFirstVideoFrameDecoded](NERtcEngine.html#event:onFirstVideoFrameDecoded__anchor)|已接收到远端视频并完成解码回调|V3.9.0
[onFirstVideoDataReceivedWithType](NERtcEngine.html#event:onFirstVideoDataReceivedWithType__anchor)|已显示首帧远端视频回调扩展接口|V3.9.0
[onFirstVideoFrameDecodedWithType](NERtcEngine.html#event:onFirstVideoFrameDecodedWithType__anchor)|已显示首帧远端视频回调扩展接口|V3.9.0


### 远端媒体事件

|事件|功能描述|起始版本|
|---|---|---|
[onUserAudioStart](NERtcEngine.html#event:onUserAudioStart__anchor)|远端用户开启音频回调|V3.9.0
[onUserAudioStop](NERtcEngine.html#event:onUserAudioStop__anchor)|远端用户停用音频回调|V3.9.0
[onUserVideoStart](NERtcEngine.html#event:onUserVideoStart__anchor)|远端用户开启视频回调|V3.9.0
[onUserVideoStop](NERtcEngine.html#event:onUserVideoStop__anchor)|远端用户停用视频回调|V3.9.0
[onUserVideoProfileUpdate](NERtcEngine.html#event:onUserVideoProfileUpdate__anchor)|远端用户视频配置更新回调|V3.9.0
[onUserAudioMute](NERtcEngine.html#event:onUserAudioMute__anchor)|远端用户是否静音回调|V3.9.0
[onUserVideoMute](NERtcEngine.html#event:onUserVideoMute__anchor)|远端用户是否禁视频流回调|V3.9.0
[onUserVideoMuteWithType](NERtcEngine.html#event:onUserVideoMuteWithType__anchor)|远端用户是否禁视频流回调扩展接口|V5.4.0
[onUserSubStreamAudioStart](NERtcEngine.html#event:onUserSubStreamAudioStart__anchor)|远端用户开启音频辅流回调|V5.4.0
[onUserSubStreamAudioStop](NERtcEngine.html#event:onUserSubStreamAudioStop__anchor)|远端用户停用音频辅流回调|V5.4.0
[onUserSubStreamAudioMute](NERtcEngine.html#event:onUserSubStreamAudioMute__anchor)|远端用户是否静音的回调|V5.4.0


### 数据统计事件

|事件|功能描述|起始版本|
|---|---|---|
[onRemoteAudioStats](NERtcEngine.html#event:onRemoteAudioStats__anchor)|通话中远端音频流的统计信息回调|V3.9.0
[onRtcStats](NERtcEngine.html#event:onRtcStats__anchor)|当前通话统计回调|V3.9.0
[onNetworkQuality](NERtcEngine.html#event:onNetworkQuality__anchor)|通话中每个用户的网络上下行质量报告回调|V3.9.0
[onLocalAudioStats](NERtcEngine.html#event:onLocalAudioStats__anchor)|本地音频流统计信息回调|V3.9.0
[onLocalVideoStats](NERtcEngine.html#event:onLocalVideoStats__anchor)|本地视频流统计信息回调|V3.9.0
[onRemoteVideoStats](NERtcEngine.html#event:onRemoteVideoStats__anchor)|通话中远端视频流的统计信息回调|V3.9.0

### 屏幕共享

|方法|功能描述|起始版本|
|---|---|---|
[startScreenCaptureByDisplayId](NERtcEngine.html#startScreenCaptureByDisplayId__anchor)|通过屏幕 ID 共享屏幕，该方法仅适用于 macOS|V3.9.0
[startScreenCaptureByWindowId](NERtcEngine.html#startScreenCaptureByWindowId__anchor)|通过窗口 ID 共享窗口|V3.9.0
[updateScreenCaptureRegion](NERtcEngine.html#updateScreenCaptureRegion__anchor)|更新屏幕共享区域|V3.9.0
[stopScreenCapture](NERtcEngine.html#stopScreenCapture__anchor)|停止屏幕共享|V3.9.0
[startScreenCaptureByScreenRect](NERtcEngine.html#startScreenCaptureByScreenRect__anchor)|通过指定区域共享屏幕|V3.9.0
[pauseScreenCapture](NERtcEngine.html#pauseScreenCapture__anchor)|暂停屏幕共享|V3.9.0
[resumeScreenCapture](NERtcEngine.html#resumeScreenCapture__anchor)|恢复屏幕共享|V3.9.0
[setupLocalSubStreamVideoCanvas](NERtcEngine.html#setupLocalSubStreamVideoCanvas__anchor)|设置本端的辅流视频画布|V3.9.0
[setupRemoteSubStreamVideoCanvas](NERtcEngine.html#setupRemoteSubStreamVideoCanvas__anchor)|设置远端的辅流视频回放画布|V3.9.0
[subscribeRemoteVideoSubStream](NERtcEngine.html#subscribeRemoteVideoSubStream__anchor)|订阅或取消订阅远端的屏幕共享辅流视频，订阅之后才能接收远端的辅流视频数据|V3.9.0
[setSubStreamRenderMode](NERtcEngine.html#setSubStreamRenderMode__anchor)|设置屏幕共享辅流视频渲染缩放模式|V3.9.0
[enumerateScreenCaptureSourceInfo](NERtcEngine.html#enumerateScreenCaptureSourceInfo__anchor)|枚举屏幕分享源信息|V4.1.110
[setScreenCaptureMouseCursor](NERtcEngine.html#setScreenCaptureMouseCursor__anchor)|在共享屏幕或窗口时，更新是否显示鼠标|V5.4.0
[setExcludeWindowList](NERtcEngine.html#setExcludeWindowList__anchor)|设置屏幕捕捉时需屏蔽的窗口列表, 该方法在捕捉过程中可动态调用|V4.4.8
[updateScreenCaptureParameters](NERtcEngine.html#updateScreenCaptureParameters__anchor)|更新屏幕共享参数|V4.4.8

### 屏幕共享事件

|事件|功能描述|起始版本|
|---|---|---|
[onScreenCaptureStatus](NERtcEngine.html#event:onScreenCaptureStatus__anchor)|屏幕共享暂停/恢复/开始/结束等回调|V5.5.21
[onUserSubStreamVideoStart](NERtcEngine.html#event:onUserSubStreamVideoStart__anchor)|远端用户开启屏幕共享辅流通道的回调|V3.9.0
[onUserSubStreamVideoStop](NERtcEngine.html#event:onUserSubStreamVideoStop__anchor)|远端用户停止屏幕共享辅流通道的回调|V3.9.0

### 音乐文件播放及混音

|方法|功能描述|起始版本|
|---|---|---|
[startAudioMixing](NERtcEngine.html#startAudioMixing__anchor)|开始播放音乐文件|V3.9.0
[stopAudioMixing](NERtcEngine.html#stopAudioMixing__anchor)|停止播放音乐文件|V3.9.0
[pauseAudioMixing](NERtcEngine.html#pauseAudioMixing__anchor)|暂停播放音乐文件|V3.9.0
[resumeAudioMixing](NERtcEngine.html#resumeAudioMixing__anchor)|恢复播放音乐文件|V3.9.0
[setAudioMixingPlaybackVolume](NERtcEngine.html#setAudioMixingPlaybackVolume__anchor)|设置音乐文件播放音量|V3.9.0
[setAudioMixingSendVolume](NERtcEngine.html#setAudioMixingSendVolume__anchor)|设置音乐文件的发送音量|V3.9.0
[getAudioMixingPlaybackVolume](NERtcEngine.html#getAudioMixingPlaybackVolume__anchor)|获取音乐文件的播放音量|V3.9.0
[getAudioMixingSendVolume](NERtcEngine.html#getAudioMixingSendVolume__anchor)|获取音乐文件的发送音量|V3.9.0
[getAudioMixingDuration](NERtcEngine.html#getAudioMixingDuration__anchor)|获取音乐文件的总长度|V3.9.0
[getAudioMixingCurrentPosition](NERtcEngine.html#getAudioMixingCurrentPosition__anchor)|获取音乐文件的播放进度|V3.9.0
[setAudioMixingPosition](NERtcEngine.html#setAudioMixingPosition__anchor)|设置音乐文件的播放进度|V3.9.0
[setAudioMixingPitch](NERtcEngine.html#setAudioMixingPitch__anchor)|设置当前伴音文件的音调|V5.5.21
[getAudioMixingPitch](NERtcEngine.html#getAudioMixingPitch__anchor)|获取当前伴音文件的音调|V5.5.21

### 音乐文件播放及混音事件

|事件|描述|起始版本|
|---|---|---|
[onAudioMixingStateChanged](NERtcEngine.html#event:onAudioMixingStateChanged__anchor)|本地用户的音乐文件播放状态改变回调|V3.9.0
[onAudioMixingTimestampUpdate](NERtcEngine.html#event:onAudioMixingTimestampUpdate__anchor)|本地用户的音乐文件播放进度回调|V3.9.0

### 音效文件播放管理

|方法|功能描述|起始版本|
|---|---|---|
[getEffectPlaybackVolume](NERtcEngine.html#getEffectPlaybackVolume__anchor)|获取音效文件播放音量|V3.9.0
[setEffectPlaybackVolume](NERtcEngine.html#setEffectPlaybackVolume__anchor)|设置音效文件播放音量|V3.9.0
[playEffect](NERtcEngine.html#playEffect__anchor)|播放指定音效文件|V3.9.0
[stopEffect](NERtcEngine.html#stopEffect__anchor)|停止播放指定音效文件|V3.9.0
[stopAllEffects](NERtcEngine.html#stopAllEffects__anchor)|停止播放所有音效文件|V3.9.0
[pauseEffect](NERtcEngine.html#pauseEffect__anchor)|暂停音效文件播放|V3.9.0
[pauseAllEffects](NERtcEngine.html#pauseAllEffects__anchor)|暂停所有音效文件播放|V3.9.0
[resumeEffect](NERtcEngine.html#resumeEffect__anchor)|恢复播放指定音效文件|V3.9.0
[resumeAllEffects](NERtcEngine.html#resumeAllEffects__anchor)|恢复播放所有音效文件|V3.9.0
[setEffectSendVolume](NERtcEngine.html#setEffectSendVolume__anchor)|调节音效文件发送音量|V3.9.0
[getEffectSendVolume](NERtcEngine.html#getEffectSendVolume__anchor)|获取音效文件发送音量|V3.9.0
[setEffectPitch](NERtcEngine.html#setEffectPitch__anchor)|设置指定音效文件的音调|V5.4.0
[getEffectPitch](NERtcEngine.html#getEffectPitch__anchor)|获取指定音效文件的音调|V5.4.0
[setEffectPosition](NERtcEngine.html#setEffectPosition__anchor)|设置指定音效文件的播放位置|V5.4.0
[getEffectCurrentPosition](NERtcEngine.html#getEffectCurrentPosition__anchor)|获取指定音效文件的播放进度|V5.4.0
[getEffectDuration](NERtcEngine.html#getEffectDuration__anchor)|获取指定音效文件的时长|V5.4.0


### 音效文件播放管理事件

|事件|描述|起始版本|
|---|---|---|
[onAudioEffectFinished](NERtcEngine.html#event:onAudioEffectFinished__anchor)|本地音效文件播放已结束回调|V3.9.0
[onAudioEffectTimestampUpdate](NERtcEngine.html#event:onAudioEffectTimestampUpdate__anchor)|本地用户的指定音效文件播放进度回调|V4.6.29


### 本地声卡采集

|方法|功能描述|起始版本|
|---|---|---|
[enableLoopbackRecording](NERtcEngine.html#enableLoopbackRecording__anchor)|开启声卡采集|V4.1.110
[adjustLoopbackRecordingSignalVolume](NERtcEngine.html#adjustLoopbackRecordingSignalVolume__anchor)|调节声卡采集信号音量|V4.1.110
[adjustUserPlaybackSignalVolume](NERtcEngine.html#adjustUserPlaybackSignalVolume__anchor)|调节本地播放的指定远端用户的指定流类型的信号音量|V4.1.110
[adjustChannelPlaybackSignalVolume](NERtcEngine.html#adjustChannelPlaybackSignalVolume__anchor)|调节本地播放的指定房间的所有远端用户的信号音量|V5.4.0
[checkNECastAudioDriver](NERtcEngine.html#checkNECastAudioDriver__anchor)|检测虚拟声卡是否安装（仅适用于 Mac 系统）|V5.4.0


### 音量提示

|方法|功能描述|起始版本|
|---|---|---|
[enableAudioVolumeIndication](NERtcEngine.html#enableAudioVolumeIndication__anchor)|启用说话者音量提示|V3.9.0
[enableAudioVolumeIndicationEx](NERtcEngine.html#enableAudioVolumeIndicationEx__anchor)|启用说话者音量提示|V5.5.21

### 音量提示事件

|事件|描述|起始版本|
|---|---|---|
[onRemoteAudioVolumeIndication](NERtcEngine.html#event:onRemoteAudioVolumeIndication__anchor)|提示频道内谁正在说话及说话者音量的回调|V3.9.0
[onLocalAudioVolumeIndication](NERtcEngine.html#event:onLocalAudioVolumeIndication__anchor)|提示频道内本地用户瞬时音量的回调|V3.9.0
[onLocalAudioVolumeIndicationEx](NERtcEngine.html#event:onLocalAudioVolumeIndicationEx__anchor)|提示频道内本地用户瞬时音量的回调扩展接口|V3.9.0

### 耳返

|方法|功能描述|起始版本|
|---|---|---|
[enableEarback](NERtcEngine.html#enableEarback__anchor)|开启耳返功能|V3.9.0
[setEarbackVolume](NERtcEngine.html#setEarbackVolume__anchor)|设置耳返音量|V3.9.0

### 旁路推流（互动直播）

|方法|功能描述|起始版本|
|---|---|---|
[addLiveStreamTask](NERtcEngine.html#addLiveStreamTask__anchor)|添加房间推流任务|V3.9.0
[updateLiveStreamTask](NERtcEngine.html#updateLiveStreamTask__anchor)|更新修改房间推流任务|V3.9.0
[removeLiveStreamTask](NERtcEngine.html#removeLiveStreamTask__anchor)|删除房间推流任务|V3.9.0

### 旁路推流（互动直播）事件

|事件|描述|起始版本|
|---|---|---|
[onAddLiveStreamTask](NERtcEngine.html#event:onAddLiveStreamTask__anchor)|通知添加直播任务结果|V3.9.0
[onUpdateLiveStreamTask](NERtcEngine.html#event:onUpdateLiveStreamTask__anchor)|通知更新直播任务结果|V3.9.0
[onRemoveLiveStreamTask](NERtcEngine.html#event:onRemoveLiveStreamTask__anchor)|通知删除直播任务结果|V3.9.0
[onLiveStreamState](NERtcEngine.html#event:onLiveStreamState__anchor)|通知直播推流状态|V3.9.0

### 音频设备管理

|方法|功能描述|起始版本|
|---|---|---|
[setRecordDevice](NERtcEngine.html#setRecordDevice__anchor)|设置音频采集设备|V3.9.0
[getRecordDevice](NERtcEngine.html#getRecordDevice__anchor)|获取当前音频采集设备|V3.9.0
[enumeratePlayoutDevices](NERtcEngine.html#enumeratePlayoutDevices__anchor)|枚举音频播放设备|V3.9.0
[enumerateRecordDevices](NERtcEngine.html#enumerateRecordDevices__anchor)|获取系统中所有的音频采集设备列表|V5.5.21
[setPlayoutDevice](NERtcEngine.html#setPlayoutDevice__anchor)|设备音频播放设备|V3.9.0
[getPlayoutDevice](NERtcEngine.html#getPlayoutDevice__anchor)|获取当前音频播放设备|V3.9.0
[setRecordDeviceVolume](NERtcEngine.html#setRecordDeviceVolume__anchor)|设置当前音频采集设备音量|V3.9.0
[getRecordDeviceVolume](NERtcEngine.html#getRecordDeviceVolume__anchor)|获取当前音频采集设备音量|V3.9.0
[setPlayoutDeviceVolume](NERtcEngine.html#setPlayoutDeviceVolume__anchor)|设置当前音频播放设备音量|V3.9.0
[getPlayoutDeviceVolume](NERtcEngine.html#getPlayoutDeviceVolume__anchor)|获取当前音频播放设别音量|V3.9.0
[setPlayoutDeviceMute](NERtcEngine.html#setPlayoutDeviceMute__anchor)|设置当前播放设备静音状态|V3.9.0
[getPlayoutDeviceMute](NERtcEngine.html#getPlayoutDeviceMute__anchor)|获取当前播放设备静音状态|V3.9.0
[setRecordDeviceMute](NERtcEngine.html#setRecordDeviceMute__anchor)|设置当前采集设备静音状态|V3.9.0
[getRecordDeviceMute](NERtcEngine.html#getRecordDeviceMute__anchor)|获取当前采集设备静音状态|V3.9.0
[startRecordDeviceTest](NERtcEngine.html#startRecordDeviceTest__anchor)|开始测试音频采集设备|V3.9.0
[stopRecordDeviceTest](NERtcEngine.html#stopRecordDeviceTest__anchor)|停止测试音频采集设备|V3.9.0
[startPlayoutDeviceTest](NERtcEngine.html#startPlayoutDeviceTest__anchor)|开始测试音频播放设备|V3.9.0
[stopPlayoutDeviceTest](NERtcEngine.html#stopPlayoutDeviceTest__anchor)|停止测试音频播放设备|V3.9.0
[startAudioDeviceLoopbackTest](NERtcEngine.html#startAudioDeviceLoopbackTest__anchor)|开始音频采集播放设备回路测试|V3.9.0
[stopAudioDeviceLoopbackTest](NERtcEngine.html#stopAudioDeviceLoopbackTest__anchor)|停止音频采集播放设备回路测试|V3.9.0

|事件|描述|起始版本|
|---|---|---|
[onAudioHowling](NERtcEngine.html#event:onAudioHowling__anchor)|检测到啸叫回调|V3.9.0

### 视频设备管理

|方法|功能描述|起始版本|
|---|---|---|
[setVideoDevice](NERtcEngine.html#setVideoDevice__anchor)|设置视频采集设备|V3.9.0
[getVideoDevice](NERtcEngine.html#getVideoDevice__anchor)|获取当前视频采集设备|V3.9.0
[enumerateVideoCaptureDevices](NERtcEngine.html#enumerateVideoCaptureDevices__anchor)|获取系统中所有的视频采集设备列表|V5.5.21
[setVideoDeviceWithType](NERtcEngine.html#setVideoDeviceWithType__anchor)|指定视频采集设备，可选主辅流|V5.5.21
[getVideoDeviceWithType](NERtcEngine.html#getVideoDeviceWithType__anchor)|获取当前使用的视频采集设备信息|V5.5.21


### 设备管理事件

|方法|功能描述|起始版本|
|---|---|---|
[onAudioDeviceStateChanged](NERtcEngine.html#event:onAudioDeviceStateChanged__anchor)|音频设备状态更改回调|V3.9.0
[onAudioDefaultDeviceChanged](NERtcEngine.html#event:onAudioDefaultDeviceChanged__anchor)|音频默认设备更改回调|V3.9.0
[onVideoDeviceStateChanged](NERtcEngine.html#event:onVideoDeviceStateChanged__anchor)|视频设备状态更改回调|V3.9.0

### 故障排查

|方法|功能描述|起始版本|
|---|---|---|
[startAudioDump](NERtcEngine.html#startAudioDump__anchor)|开始记录音频 dump 音频 dump 可用于分析音频问题|V3.9.0
[stopAudioDump](NERtcEngine.html#stopAudioDump__anchor)|结束记录音频 dump|V3.9.0
[getErrorDescription](NERtcEngine.html#getErrorDescription__anchor)|获取错误描述|V3.9.0
[uploadSdkInfo](NERtcEngine.html#uploadSdkInfo__anchor)|上传SDK日志信息|V3.9.0
[startAudioDumpWithType](NERtcEngine.html#startAudioDumpWithType__anchor)|开始记录指定通道音频 dump 音频 dump 可用于分析音频问题|V5.5.21

### 网络探测

|方法|功能描述|起始版本|
|---|---|---|
[startLastmileProbeTest](NERtcEngine.html#startLastmileProbeTest__anchor)|开始通话前网络质量探测|V4.5.0
[stopLastmileProbeTest](NERtcEngine.html#stopLastmileProbeTest__anchor)|停止通话前网络质量探测|V4.5.0
[setCloudProxy](NERtcEngine.html#setCloudProxy__anchor)|开启并设置云代理服务|V5.4.0

### 美颜

|方法|功能描述|起始版本|
|---|---|---|
[startBeauty](NERtcEngine.html#startBeauty__anchor)|开启美颜功能模块|V5.4.0
[stopBeauty](NERtcEngine.html#stopBeauty__anchor)|结束美颜功能模块|V4.5.0
[enableBeauty](NERtcEngine.html#enableBeauty__anchor)|暂停或恢复美颜效果|V5.4.0
[getBeautyEffect](NERtcEngine.html#getBeautyEffect__anchor)|获取指定美颜类型的强度设置|V5.4.0
[setBeautyEffect](NERtcEngine.html#setBeautyEffect__anchor)|设置美颜效果|V5.4.0
[addBeautyFilter](NERtcEngine.html#addBeautyFilter__anchor)|添加滤镜效果|V5.4.0
[removeBeautyFilter](NERtcEngine.html#removeBeautyFilter__anchor)|取消滤镜效果|V5.4.0
[setBeautyFilterLevel](NERtcEngine.html#setBeautyFilterLevel__anchor)|设置滤镜强度|V5.4.0
[addBeautySticker](NERtcEngine.html#addBeautySticker__anchor)|添加贴纸效果|V5.4.0
[removeBeautySticker](NERtcEngine.html#removeBeautySticker__anchor)|取消贴纸效果|V5.4.0
[addBeautyMakeup](NERtcEngine.html#addBeautyMakeup__anchor)|添加美妆效果|V5.4.0
[removeBeautyMakeup](NERtcEngine.html#removeBeautyMakeup__anchor)|取消美妆效果|V5.4.0

### 空间音效

|方法|功能描述|起始版本|
|---|---|---|
[setRangeAudioMode](NERtcEngine.html#setRangeAudioMode__anchor)|设置玩家本人在房间中的范围语音模式，该设置不影响其他人|V5.4.0
[setRangeAudioTeamID](NERtcEngine.html#setRangeAudioTeamID__anchor)|设置范围语音的小队 ID|V5.4.0
[setAudioRecvRange](NERtcEngine.html#setAudioRecvRange__anchor)|设置空间音效的距离衰减属性和语音范围|V5.4.0
[updateSelfPosition](NERtcEngine.html#updateSelfPosition__anchor)|更新本地用户的空间位置|V5.4.0
[enableSpatializerRoomEffects](NERtcEngine.html#enableSpatializerRoomEffects__anchor)|开启或关闭空间音效的房间混响效果|V5.4.0
[setSpatializerRoomProperty](NERtcEngine.html#setSpatializerRoomProperty__anchor)|设置空间音效的房间混响属性|V5.4.0
[setSpatializerRenderMode](NERtcEngine.html#setSpatializerRenderMode__anchor)|设置空间音效的渲染模式|V5.4.0
[initSpatializer](NERtcEngine.html#initSpatializer__anchor)|初始化引擎 3D 音效算法|V5.4.0
[enableSpatializer](NERtcEngine.html#enableSpatializer__anchor)|开启或关闭空间音效|V5.4.0

### 权限秘钥

|方法|功能描述|起始版本|
|---|---|---|
[updatePermissionKey](NERtcEngine.html#updatePermissionKey__anchor)|更新权限密钥|V5.4.0

### QS事件

|事件|功能描述|起始版本|
|---|---|---|
[onRequestSendKeyFrame](NERtcEngine.html#event:onRequestSendKeyFrame__anchor)|I 帧请求事件回调|V5.4.0
[onBitrateUpdated](NERtcEngine.html#event:onBitrateUpdated__anchor)|视频码率信息回调|V5.4.0
[onVideoCodecUpdated](NERtcEngine.html#event:onVideoCodecUpdated__anchor)|视频编码器信息回调|V5.4.0



### 其他事件

|事件|功能描述|起始版本|
|---|---|---|
[onError](NERtcEngine.html#event:onError__anchor)|发生错误回调|V3.9.0
[onWarning](NERtcEngine.html#event:onWarning__anchor)|发生警告回调|V3.9.0
[onApiCallExecuted](NERtcEngine.html#event:onApiCallExecuted__anchor)|API 调用结束回调|V5.4.0
[onRemoteVideoReceiveSizeChanged](NERtcEngine.html#event:onRemoteVideoReceiveSizeChanged__anchor)|接收的远端视频分辨率变化回调|V5.4.1
[onLocalVideoRenderSizeChanged](NERtcEngine.html#event:onLocalVideoRenderSizeChanged__anchor)|本地视频预览的分辨率变化回调|V5.4.1
[onFirstVideoFrameRender](NERtcEngine.html#event:onFirstVideoFrameRender__anchor)|已接收到远端视频首帧并完成渲染的回调|V3.9.0
[onRecvSEIMsg](NERtcEngine.html#event:onRecvSEIMsg__anchor)|监听 SEI 数据回调|V4.1.110
[onAudioRecording](NERtcEngine.html#event:onAudioRecording__anchor)|音频录制状态回调|V3.9.0
[onMediaRelayStateChanged](NERtcEngine.html#event:onMediaRelayStateChanged__anchor)|跨房间媒体流转发状态发生改变回调|V3.9.0
[onMediaRelayEvent](NERtcEngine.html#event:onMediaRelayEvent__anchor)|媒体流相关转发事件回调|V3.9.0
[onLocalPublishFallbackToAudioOnly](NERtcEngine.html#event:onLocalPublishFallbackToAudioOnly__anchor)|本地发布流已回退为音频流、或已恢复为音视频流回调|V3.9.0
[onRemoteSubscribeFallbackToAudioOnly](NERtcEngine.html#event:onRemoteSubscribeFallbackToAudioOnly__anchor)|订阅的远端流已回退为音频流、或已恢复为音视频流回调|V3.9.0
[onLastmileQuality](NERtcEngine.html#event:onLastmileQuality__anchor)|通话前网络上下行 last mile 质量状态回调|V4.5.0
[onLastmileProbeResult](NERtcEngine.html#event:onLastmileProbeResult__anchor)|通话前网络上下行 Last mile 质量探测报告回调|V4.5.0
[onMediaRightChange](NERtcEngine.html#event:onMediaRightChange__anchor)|服务端禁言音视频权限变化回调|V5.4.0
[onCheckNECastAudioDriverResult](NERtcEngine.html#event:onCheckNECastAudioDriverResult__anchor)|收到检测安装声卡的内容回调|V5.4.0
[onVirtualBackgroundSourceEnabled](NERtcEngine.html#event:onVirtualBackgroundSourceEnabled__anchor)|通知虚拟背景功能是否成功启用的回调|V5.4.0
[onLocalVideoWatermarkState](NERtcEngine.html#event:onLocalVideoWatermarkState__anchor)|本地视频水印生效结果回调|V5.4.0
[onPermissionKeyWillExpire](NERtcEngine.html#event:onPermissionKeyWillExpire__anchor)|权限密钥即将过期事件回调|V5.4.0
[onUpdatePermissionKey](NERtcEngine.html#event:onUpdatePermissionKey__anchor)|更新权限密钥事件回调|V5.4.0
[onUserDataReceiveMessage](NERtcEngine.html#event:onUserDataReceiveMessage__anchor)|远端用户通过数据通道发送数据的回调|V5.4.0
[onUserDataStart](NERtcEngine.html#event:onUserDataStart__anchor)|远端用户开启数据通道的回调|V5.4.0
[onUserDataStop](NERtcEngine.html#event:onUserDataStop__anchor)|远端用户停用数据通道的回调|V5.4.0
[onUserDataStateChanged](NERtcEngine.html#event:onUserDataStateChanged__anchor)|远端用户数据通道状态变更回调|V5.4.0
[onUserDataBufferedAmountChanged](NERtcEngine.html#event:onUserDataBufferedAmountChanged__anchor)|远端用户数据通道 buffer 变更回调|V5.4.0





























