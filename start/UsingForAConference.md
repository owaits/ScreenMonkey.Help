# Using Screen Monkey for a Conference

In this example, we will assume we are using Screen Monkey to help us with a conference. The conference will contain the following elements:

1.  Lead in music  
      
    The Lead in music is played using an MP3 file named LeadIn.MP3.
    
2.  Image with Conference Logo  
      
    While the Lead in music is playing an image with the conference logo is presented via multiple projection systems. The conference logo is an image named ConferenceOpener.PNG.
    
3.  Master of Ceremonies and Keynote Speaker  
      
    A live video feed will present all stage activity on the projection systems. The computer is equipped with a video capture device named Video WebCam.
    
4.  Supplemental Images and Lower Thirds  
      
    During the keynote speech, Lower Thirds will be used to identify the presenters. During the keynote, the presenter will advise the audience that books and other materials are available in a specific area. These images will be superimposed on top of the live video. There are three images involved.
    

*   Emcee.PNG  
      
    Provides a lower third to identify the Master of Ceremonies.
    
*   Keynote.PNG  
      
    Provides a lower third to identify the Keynote speaker.
    
*   BookImage.PNG  
      
    Provides an image of the book the Keynote speaker has written.
    

6.  Lead out music  
      
    The Lead out music is played using an MP3 file named LeadOut.MP3.
    

As you can see, we need to be able to easily present different types of media. For our example conference, we have two different audio files in MP3 format, a live video feed and a few different images that will be presented and even superimposed over the video.

## Preparing Screen Monkey before the conference

Long before the conference begins, you will want to prepare Screen Monkey.

First, we add these files to Screen Monkey.

To add a media file to Screen Monkey, you click once on any of the blank squares.

(These blank squares are called "slots")

![](..\images\ClickEmptySquare.png)

After you click a slot, the Create Clip dialog opens.

![](..\images\CreateClip.png)

Since the first thing we are likely to do is play the lead in music, we click the Audio icon followed by OK.

The Open dialog should display allowing us to browse to where the music content is located.

For this example, I placed all the content inside the same folder. I selected the LeadIn.MP3 file and clicked Open.

![](..\images\OpenAudio.png)

The main Screen Monkey window (called the Dashboard) should now look like this:

![](..\images\FirstClipAdded.png)

The process of adding clips is repeated as shown above until the Screen Monkey dashboard looks similar to this:

![](..\images\ConferenceLoaded.png)

At this point we are now ready to USE Screen Monkey during our conference.

## Presenting the media during the conference

Let's walk through the process of presenting the show at our conference. As the conference begins, we need to play our Lead In music as well as present the conference image. So we click the LeadIn clip once and the Lead In music should begin playing. Then we click the Conference image once and it should begin presenting on the projectors connected to the computer.

![](..\images\ConferenceStart.png)

Notice how the clip outlines turn yellow. For the audio clip, a small yellow triangle appears in the upper right corner to let you know audio is playing. Also note the letter A in the upper left corner of the clip. This indicates the clip is playing on the Audio layer. Notice the clip to the immediate right. This is the conference image and the bright yellow border indicates it's the active layer. If you look at the left side of the Dashboard, the L1 square is highlighted to let you know Layer 1 is presenting the image.

When the Master of Ceremonies (EmCee) approaches the stage it's time to stop playing the LeadIn music and start presenting the live video feed. Notice the little row of squares on the left side of the Main Dashboard. Each of these represents a layer. Click the Audio layer to select it, then click the Clear Audio clip.

![](..\images\ClickAudioLayer.png)

Click the L1 layer to select it, then click the video camera icon to start the feed and the live video will begin presenting on the projectors.  We selected L1 because that is the layer that will be "behind" all the others.

![](..\images\startcamera.png)

At this point the EmCee is on stage and about to begin talking to the audience and introduce the keynote speaker. When the address begins, you will want to display the [lower third](javascript:void(0);) that will present the EmCee's name.

To display the lower third, click the L2 layer to select it, then click the EmCee clip to present it. Because you first selected L2, the Emcee clip is presented on Layer 2. This means Layer 1 is still presenting the live video feed and Layer 2 is presenting in front of the Live video feed. So your audience sees both at the same time.

As you can hopefully see, it's really easy to present the content. Once you are finished playing any given clip, click the layer on the left side to choose it, then click the "Clear Layer" clip on the left side of Screen Monkey. That will totally clear the layer and immediately stop playing the selected clip.

Using Screen Monkey, there was no need for locating the audio files, opening and playing them using a media player. No need to use something like a mechanical A/B switch to change from presenting live video to images or images to live video.

Instead, the show was polished and seamless!

![](..\images\Noteimage.png)

This topic presented one possible use of Screen Monkey. The intent was to provide an overview of how such a situation might unfold. As you may imagine, simplicity was the goal here. There are more efficient ways of working with Screen Monkey. For example, pre-assigning clips so that they appear on specific layers.