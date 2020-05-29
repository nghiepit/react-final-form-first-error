# react-final-form-first-error

[![NPM version](https://img.shields.io/npm/v/react-final-form-first-error.svg)](https://www.npmjs.com/package/react-final-form-first-error)
[![NPM yearly download](https://img.shields.io/npm/dy/react-final-form-first-error.svg)](https://www.npmjs.com/package/react-final-form-first-error)

> A plugin get the first error for 🏁 React Final Form

## Installation

```bash
yarn add react-final-form-first-error
```

## Usage

```jsx
import {Form, Field} from 'react-final-form';
import {FormError, useFirstError} from 'react-final-form-first-error';

const LoginForm = (props) => {
  return (
    <Form
      onSubmit={...}
      validate={...}
      render={(props) => (
        <form onSubmit={props.handleSubmit}>
          <FormError {...props} /> // <--------- 😎

          <Field name="username">
            {({input}) => (
              <input
                {...input}
                type="text"
                placeholder="Enter username"
                autoComplete="off"
              />
            )}
          </Field>

          <Field name="password">
            {({input}) => (
              <input
                {...input}
                type="password"
                placeholder="Enter password"
                autoComplete="off"
              />
            )}
          </Field>

          <button type="submit">Login</button>
        </form>
      )}
    />
  );
};
```

## License

MIT © [Nghiep](https://nghiepit.dev)