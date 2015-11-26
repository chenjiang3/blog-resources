控制assets的播放，你可以使用AVPlayer对象。在播放的过程中，你可以使用AVPlayerItem对象来管理asset的呈现，AVPlayerItemTrack来管理track。要显示视频，需要使用AVPlayerLayer。

#播放Assets
一个播放器就是控制asset播放的对象，比如开始和结束，seek到指定的时间。可以使用AVPlayer来播放单个asset，用AVQueuePlayer来播放多个连续的asset。
一个player向你提供播放的信息，如果需要，你通过player的状态同步显示到界面上。你也可以直接把player的输出显示笑傲指定的动画层（AVPlayerLayer或者AVSynchronizedLayer），想知道更多关于layer的信息，请查看[Core Animation Programming Guide](https://developer.apple.com/library/prerelease/ios/documentation/Cocoa/Conceptual/CoreAnimation_guide/Introduction/Introduction.html#//apple_ref/doc/uid/TP40004514)

```
多个layer的情况：你可以创建多个AVPlayerLayer对象，但是只有最近创建的layer才会显示视频画面。
```
虽然是播放asset，但是不能直接把asset传给AVPlayer对象，你应该提供AVPlayerItem对象给AVPlayer。一个player item管理着和它相关的asset。一个player item























