## away-we-go
![alt text](images/gopher.png "Gopher")

### prep :: idioms :: mental models
- don't need abstraction layers to decouple
- go provides thinnest possible layer between the concrete (hardware) and decoupled world
- prime focus the hardware is the platform
- go is based on a real machine
- you will know how the code will run on a machine
- every decision you make in go comes at a cost
- cost vs benefit is key in designing & architecting go software
- you can write programs that require minimal amount of resources to run
- champion efficiency, quality, and simplicity

### Productivity vs Performance
- instead of sacrificing performance to be productive, go allows for both
- it's not about being faster, but "fast enough"
- working with Go is intended to be fast
- it should take at most a few seconds to build a large executable on a single computer
- go enables us to take advantage of the hardware
- fosters an excellent balance between power and expressiveness, just like C
- do want you want to do by just programming in a straightforward manner
- it's all about the REAL machine, not VIRTUAL which makes for more accurate predictions
- Go has it all really, it's just about figuring out HOW to tap into it all

_"The hardware folks will not put more cores into their hardware if the software isn’t going to use them, so, it is this balancing act of each other staring at each other, and we are hoping that Go is going to break through on the software side.” - Rick Hudson (2015)_

### Correctness vs Performance
- stop trying to optimize for performance (e.g. Node/JS)
- focus on optimizing for correctness
- once correct, then benchmark
- simple, straightforward code is the way
- Go is built on these foundations
- make decisions with correctness optimizations as first priority

_"Go blows away Node in pretty much every way IMO. You get all the niceties of blocking code without actually blocking, you get (relatively) tiny binaries that you can deploy anywhere with ease and no fuss, instead of 250mb of node_modules that everyone comes up with hacks to work around." - TJ Holowaychuk (2017)_

### Code Reviews
- integrity must be the #1 priority 
- become serious about writing reliable code
- reads, writes, and memory allocations should all be accurate, consistent, and efficieant
- data should never be corrupted
- error-handling must never be an exception, but always an integral part your code
- reduce bugs by writing less code and having less tests
- once the code has integrity it also must be highly readable

### Kit Projects
- single Kit projects should first be established
- then create multiple projects for different sets of programs to be deployed together
- a standard library, used by a company or org
- packages that belong to the Kit project should have highest levels of portability
- should be usable across multiple Application projects
- provide a very specific but foundational domain of functionality
- should not be allowed to have a vendor folder
- 3rd party packages should build against the latest version of those dependences

**Sample Kit:**
```
github.com/some-repo/kit
├── CONTRIBUTORS
├── LICENSE
├── README.md
├── cfg/
├── examples/
├── log/
├── pool/
├── tcp/
├── timezone/
├── udp/
└── web/
```

### future explorations, notes, repos, projects
- daemons
- expressive concurrency primitives 
- error-handling
- stlib
- 3rd party packages
- scalable serverless apps
- webhook managers
- embedding binary data
- headers
- redirects
- elasticsearch
- encoding utils
- stripe api
- analytics
- binary updates
- runes
- collate
- encoding
- number
- secure
- transform
- unicode
- message/catalog
- message/pipeline
- search
- width


_"...performance means nothing if your application is frail, difficult to debug, refactor and develop." - TJ Holowaychuk (2014)_

