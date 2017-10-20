# Nils 0.1.0 Released: Reached Production State!
I worked long on a Framework that bundels today and Future Features as i am into Load Optimization of distributed Loading since some years.


# What is Nils?
Nils is the short form of Nikolaos (Santa Claus) it is composed from the greek words Nike and Laos 
- > Nike = Winner
- > Laos = Public
- = Winner of the Public!
It offers DOM Diffing, Streams, Workflows for WebDevelopment


# Guides
- TODO MVC
- PWA
- CHAT GUIDE
- ATM GUIDE

# Feature List
- Full Reactiv Programing flow using DIREKTSPEED Nils wich is a Extended version of Most Streams.
- Streaming WebComponents with live bindings.
- Works out of the box with any Template language and partial paradigm
- Works with any HTML, Data Producer.
- Compatible with all Framworks and Coding Styles:
  - A+ Promises, Streams, Values, Functions, Symbols
  - fast adoption of libs like transducers or other 2020 Standarts for JavaScript
  - Ultra Fast Loading in Steal with Development Mode
  - Better Stack Traces.
  - Better debuging 
  - Better Testing
  - up to n X Faster then normal CanJS n == Number of elements
  - Allows workign with Data Streams and BigData Data Sience Scenarios
- To much more to write now because i am a single person :)
## About the Author
I Optimized near any protocol did experiments with stuff like 
- SuperChannels that are able to Transfer Some Terabyte per sec.
- All Frontend Frameworks and rendering Methods Around
- All Module Loaders for the Frontend
- All bundling Algos Around
- All Loading Algos Around
- Write and understand syntax in 20 + Languages really well Senior Dev Level.

Why do i list all that? I want to make sure that you understand that i really know what i write here.
I could not find any framework for the frontend that uses the Now Day Methods.
- WebComponents
- Streams
- es7+
- Creating bundels of all that tech
 - you will now say babel -> CJS sure sure but today Browsers support es6 nativ and need modules in that syntax to work as webcomponents
 
 Any way Nils is a Collection (Framework of Frameworks) that complets the new nativ Browser features and allows extrem fast adoption of future workflows
 in 2030 they will be common practice.
 
 ## Projects depending on nils 
 - CanJS X (canjsx) a Compatibility Layer for old CanJS Based Projects to migrate to Nils.
 
 # canjsx
This is a CanJS Version X for Stream It aims to be the defacto Framework of Frameworks based on direktspeed-nils

# Small First example
This shows how canjsX Improves existing CanJS can-define/map Objects
- We can Update the viewModel Reactive
- can-connect is not needed any more
- works with Any data source
```javascript
const Nils = require('../../')
const defineMap = require('can-define/map/map')
const Component = require('can-component')
const view = require('index.stache')

const app = new Nils()

const viewModel = defineMap.extend({sealed: false},{})


// Init ViewModel
// could be also a defineMap->Stream
app.stream.of({
  inputX: '',
  inputY: ''
})
// Observe DOM Elements
// return { update, assign }
.combineArray((observed)=>observed,[
  app.fromInput(document.querySelector('input.x'))
  .map((val)=>{
  return { inputX: val }
  }),
  app.fromInput(document.querySelector('input.y'))
  .map((val)=>{
    return { inputY: val }
  })
])
// Returns the ViewModelUpdating State aka can-x-connect :)
// This can also be a complet Can Component
// its only for demo
.loop(function applyVM(lastSetVal, setVal){
  let seed = lastSetVal.viewModel.updateDeep(setVal)
  return return { seed, value: seed };
},Component.extend({
  tag: 'kasse-login',
  ViewModel,
  view
}))
// Acticvate the Stream All gets executed as sideEffect
.map((comp)=>comp.render())
.drain()
```
