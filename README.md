react-es6
=========

This project is a POC with the following constraints :

* Use React
* Use ES6

The end goal is to do an isomorphic app with React, so this project is a sandbox to play with React and ES6 and will lay the foundations for my next project :

* Do an isomorphic app
* Same router on frontend and backend with multiple routes
* Unit tests

###No constraints on :

* Application features (simple app, must only use data from a remote server)
	* The remote server will be an instance of [topheman-apis-proxy](https://github.com/topheman/topheman-apis-proxy) (there will be work on this side to provide offline mock data for unit tests)
* Module bundler / Task runner / Transpiler

###Steps :

Here are the following steps I intend to follow (may change) - should be tagged when stable to keep track of evolution :

- [x] Setup transpiler to use ES6 (babel via webpack were selected)
- [x] Setup simpliest React component (make sure jsx and ES6 transpiling works)
- [x] Add sass / bootstrap support via webpack (to have the same kinds of constraints as a regular app)
- [ ] Add simple Gulpfile to : 
	- [ ] copy assets from `src`to `build`
	- [ ] run the `webpack` build
- [ ] Add React.Router
- [ ] Make the App using React components and routes (keep in mind isomorphism for later)
- [ ] ...

###Basic features :

May change

* Home page :
	* feature : search for users
	* <searchUsers> component
		* form field
		* manages AJAX requests
		* feeds the <basicList> of users retrieved 
	* <basicList> component
		* takes users from <searchUsers> as input, loops through
		* lists users and displays them in <basicUser> component
	* <basicUser> component
		* displays some infos
		* shows a link to the full profile (via router)
* /user/:username :
	* feature : 
		* shows full profile of user
		* shows repositories of user (pagination ?)