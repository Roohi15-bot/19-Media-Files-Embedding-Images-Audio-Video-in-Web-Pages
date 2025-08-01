Media elements—images, audio, and video—make websites engaging and interactive. 

# 1. Embedding Images with img

           <img src="profile.jpg" alt="Zakeer's Profile Picture" />

Attribute          	Purpose
> src	Path to the image file

> alt	Text shown if image fails to load (also for screen readers)

> width / height	Controls image size

> loading="lazy"	Delays image loading until needed (optimization)

 Best Practices:
> Always provide alt text for accessibility

> Use loading="lazy" for better performance

> Avoid stretching by setting max-width: 100%

    img {
       max-width: 100%;
       height: auto;
       display: block;
    }

# 2. Embedding Audio with audio

      <audio controls>
            <source src="podcast.mp3" type="audio/mpeg" />
            Your browser does not support the audio element.
     </audio>
     
Attribute	Description
> controls	Adds play/pause UI

> autoplay	Starts automatically ( not recommended)

> loop	Repeats audio

> muted	Starts muted

 Supported Audio Formats:
> .mp3

> .ogg

> .wav

# 3. Embedding Video with video

        <video controls width="400">
             <source src="intro.mp4" type="video/mp4" />
             Your browser does not support the video tag.
       </video>
       
Attribute	Description
> controls	Adds video player UI

> autoplay	Plays on page load (must be muted)

> loop	Repeats video

> muted	Starts muted

> poster	Placeholder image before play

Supported Video Formats:

> .mp4 (most widely supported)

> .webm

> .ogg

# 4. Media File Paths (Relative vs Absolute)

       <!-- Relative path -->
       <img src="assets/logo.png" />

      <!-- Absolute path -->
      <img src="https://example.com/assets/logo.png" />
      
 Use relative paths for local files, absolute for CDN/external content.

 # 5. Responsive Media Tips
 
     Images:
           img {
            max-width: 100%;
            height: auto;
       }
       
 Prevents overflow on small screens

     Video Container:
          .video-wrapper {
           position: relative;
           padding-bottom: 56.25%; /* 16:9 aspect ratio */
           height: 0;
          overflow: hidden;
      }

       .video-wrapper iframe,
       .video-wrapper video {
             position: absolute;
             top: 0;
             left: 0;
             width: 100%;
             height: 100%;
          }
          
 Makes embedded videos mobile-friendly and maintains aspect ratio

# Real-World Examples

#  Hero Banner with Image

      <section class="hero">
           <img src="images/banner.jpg" alt="Hero background image" />
           <h1>Build Beautiful UIs</h1>
      </section>

# Background Music (Muted + Loop)

          <audio autoplay loop muted>
              <source src="bg-music.mp3" type="audio/mp3" />
          </audio>
          
 Useful for games or portfolio projects (but use responsibly).

#  Product Demo Video

           <video controls poster="preview.jpg" width="600">
           <source src="demo.mp4" type="video/mp4" />
     </video>
     
 Used in marketing, SaaS product walkthroughs, testimonials.

 # Summary
Element	Purpose	Key Attributes
> img	Display images	src, alt, loading, width, height

> audio	Play sound	controls, autoplay, loop, muted

> video	Play video	controls, poster, autoplay, muted

> source	Media fallback	Used inside audio and video.




