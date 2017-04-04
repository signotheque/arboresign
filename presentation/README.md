# Arboresign presentation

April 2017

- Made with [reveal-md](https://github.com/webpro/reveal-md) + [DeckTape](https://github.com/astefanutti/decktape)


## Writing stage

- The content is written in markdown in the file 'slides.md'. Some HTML is required for the two column layout and image resizing.

During the presentation redaction, the presentation is served by *reveal-md*. The result can be reloaded live with the watcher option `-w`. 
  
      reveal-md slides.md -w

The presentation is available at: http://localhost:1948/slides.md#/ 

      
## Compilation stage

To be served without reveal-md, the presentation has to be compiled as a static website. It is written in the ` _static` directory

      reveal-md slides.md --static

It can be served via a simple http-server:       http://127.0.0.1:8080/_static   

## PDF export

The presentation is exported in PDF thru [DeckTape](https://github.com/astefanutti/decktape) in the file `slides.pdf`.
 
      phantomjs decktape-1.0.0/decktape.js http://localhost:1948/slides.md#/ slides.pdf
  


