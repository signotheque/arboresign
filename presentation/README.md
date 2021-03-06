# Arboresign presentation

April 2017

- Made with [reveal-md](https://github.com/webpro/reveal-md) + [DeckTape](https://github.com/astefanutti/decktape)


## Writing stage

- The content is written in markdown in the file 'slides.md'. Some HTML is required for the two column layout and image resizing.

During the presentation redaction, the presentation is served by *reveal-md*. The result can be reloaded live with the watcher option `-w`. 
  
      npm run dev

or 

      reveal-md slides.md -w

The presentation is available at: http://localhost:1948/slides.md#/ 

      
## Compilation stage

To be served without reveal-md, the presentation has to be compiled as a static website. It is written in the current directory

      npm run build

or 

      reveal-md slides.md --static

It can be served via a simple http-server:       http://127.0.0.1:8080

## PDF export

Requirements: the presentation must be compiled as static and served via http://127.0.0.1:8080

The presentation is exported in PDF thru [DeckTape](https://github.com/astefanutti/decktape) in the file `slides.pdf`.

      npm config set arboresign:decktape_root <absolute_path_to_decktape_install>
      npm run export

or 

      phantomjs decktape-1.0.0/decktape.js http://127.0.0.1:8080 slides.pdf
  


