# React helper decorators
This library introduces a set of ES7/TypeScript decorators that offer you a new way to set up React lifecycle hooks.

Here is how it looks like:

	import {Life} from 'react-helper-decorators';
	class MyComponent extends React.Component {
		@Life.didUpdate
		@Life.didMount
		invalidate() {
			//code to execute on componentDidUpdate and componentDidMount
		}
	}

	class DerivedComponent extends MyComponent {
		@Life.didUpdate
		afterUpdate() {
			//code to execute on componentDidUpdate
		}
	}

The decorators add functions to the relevant lifecycle methods in a way that doesn't interfere with previous hooks.

Also, when using an IDE with TypeScript tooling, the `Life` namespace reminds you of the available lifecycle hooks and their signatures.