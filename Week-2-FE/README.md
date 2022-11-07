# Week 2 Bootcamp FE
## React JS lanjutan PropTypes

PropTypes adalah salah satu fitur yang ada di React.js yang digunakan untuk memvalidasi tipe data props yang dikirimkan dari komponen induk ke komponen anak. Jika tipe data yang dikirimkan tidak sesuai dengan yang diharapkan, maka akan muncul pesan error di console. Cara penggunaannya cukup mudah, cukup import PropTypes dari package react lalu tambahkan properti propTypes pada komponen yang akan di validasi.

```javascript
import React from 'react';
import PropTypes from 'prop-types';

const MyComponent = (props) => {
  return (
    <div>
      <h1>{props.title}</h1>
      <p>{props.description}</p>
    </div>
  );
};

MyComponent.propTypes = {
  title: PropTypes.string,
  description: PropTypes.string,
};

export default MyComponent;
```

- proptypes untuk tipe data string

  ```javascript
  MyComponent.propTypes = {
    title: PropTypes.string,
  };
  ```

- proptypes untuk tipe data number

  ```javascript
  MyComponent.propTypes = {
    title: PropTypes.number,
  };
  ```
- proptypes array of object

  ```javascript
  MyComponent.propTypes = {
    title: PropTypes.arrayOf(
      PropTypes.shape({
        id: PropTypes.number,
        name: PropTypes.string,
      })
    ),
  };
  ```
  ## React Router
  React Router adalah sebuah library yang digunakan untuk membuat routing, Routing adalah proses untuk mengatur alur navigasi di aplikasi. React Router 6 merupakan versi terbaru dari React Router yang dirilis pada tanggal 18 Juni 2021. Pada versi terbaru ini, 
  React Router 6 menghilangkan fitur yang sudah tidak digunakan lagi seperti Switch, Redirect, dan Link. 
  Pada React Router 6, fitur tersebut digantikan dengan fitur baru yaitu Routes, Outlet, dan Link. Pada React Router 6,
  fitur Routes digunakan untuk mengatur alur navigasi, Outlet digunakan untuk menampilkan komponen sesuai dengan alur navigasi yang ditentukan,
  dan Link digunakan untuk membuat link navigasi. Berikut adalah contoh penggunaan Routes, Outlet, dan Link pada React Router 6.
  
  ### Instalasi

  Untuk menginstall React Router v6, jalankan perintah berikut pada terminal:

```bash
npm install react-router-dom -S
```

### Penggunaan react router

Untuk menggunakan React Router v6, kita perlu mengimport beberapa komponen dari
library tersebut. Komponen-komponen tersebut antara lain:

1. `BrowserRouter` - Komponen ini digunakan untuk membuat routing pada aplikasi
   React.
2. `Routes` - Komponen ini digunakan untuk membuat routing pada aplikasi React.
3. `Route` - Komponen ini digunakan untuk membuat routing pada aplikasi React.
4. `Link` - Komponen ini digunakan untuk membuat link pada aplikasi React.
5. `Outlet` - Komponen ini digunakan untuk membuat routing pada aplikasi React.
6. `useNavigate` - Komponen ini digunakan untuk membuat routing pada aplikasi
   React.
7. `useParams` - Komponen ini digunakan untuk membuat routing pada aplikasi
   React.
8. `useLocation` - Komponen ini digunakan untuk membuat routing pada aplikasi
   React.
9. `useMatch` - Komponen ini digunakan untuk membuat routing pada aplikasi
   React.

Dan masih banyak lagi komponen-komponen lainnya yang dapat digunakan untuk
membuat routing pada aplikasi React. Untuk lebih jelasnya, silahkan baca
dokumentasi React Router v6 di
[sini](https://reactrouter.com/docs/en/v6/getting-started/overview).

Berikut ini adalah contoh penggunaan React Router v6 pada aplikasi React:

```jsx
import "bootstrap/dist/css/bootstrap.min.css";
import { LinkContainer } from "react-router-bootstrap";
import Container from "react-bootstrap/Container";
import Nav from "react-bootstrap/Nav";
import Navbar from "react-bootstrap/Navbar";
import { Routes, Route} from "react-router-dom";
import Home from "./pages/Home";
import About from "./pages/About";
import Portofolio from "./pages/Portofolio";
import Blog from "./pages/Blog";
import "./App.css"

function App() {
  return (
    <>
      <Navbar expand="lg">
        <Container fixed="top">
          <Navbar.Brand href="#home">TgrRys</Navbar.Brand>
          <Navbar.Toggle aria-controls="basic-navbar-nav" />
          <Navbar.Collapse id="basic-navbar-nav">
            <Nav className="ms-auto">
              <LinkContainer to="/">
                <Nav.Link>Home</Nav.Link>
              </LinkContainer>
              <LinkContainer to="/about">
                <Nav.Link>About</Nav.Link>
              </LinkContainer>
              <LinkContainer to="/portofolio">
                <Nav.Link>Portofolio</Nav.Link>
              </LinkContainer>
              <LinkContainer to="/blog">
                <Nav.Link>Blog</Nav.Link>
              </LinkContainer>
            </Nav>
          </Navbar.Collapse>
        </Container>
      </Navbar>

      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
        <Route path="/portofolio" element={<Portofolio />} />
        <Route path="/blog" element={<Blog />} />
      </Routes>
    </>
  );
}

export default App;

```

## State Management React Redux

State management adalah proses untuk mengatur data yang digunakan di aplikasi web. 
State management biasanya digunakan untuk mengatur data yang digunakan di banyak komponen. 
State management juga digunakan untuk mengatur data yang digunakan di komponen yang berada di lapisan yang berbeda. 
State management yang paling populer saat ini adalah Redux. Redux adalah state management yang digunakan untuk mengatur data yang digunakan di aplikasi web.
Redux memiliki 3 komponen utama yaitu Store, Action, dan Reducer. Store digunakan untuk menyimpan data, Action digunakan untuk mengirimkan data ke Store, dan Reducer digunakan untuk mengubah data yang ada di Store.
Redux memiliki beberapa kelebihan antara lain:

1. Redux memudahkan kita untuk mengelola state pada aplikasi React.
2. Redux memudahkan kita untuk mengelola state pada aplikasi React yang
   kompleks.
3. Redux memudahkan kita untuk mengelola state pada aplikasi React yang berskala
   besar.
4. Redux memudahkan kita untuk mengelola state pada aplikasi React yang berskala
   besar dan kompleks.
5. Redux memudahkan kita untuk mengelola state pada aplikasi React yang berskala
   besar dan kompleks dengan banyak pengguna.
   
Berikut adalah contoh dan langkah-langkah penggunaan Redux dan react-redux pada React.js.

### Instalasi

Untuk menginstall Redux, jalankan perintah berikut pada terminal:

```bash
npm install redux react-redux -S
```

### Penggunaan react redux

Untuk menggunakan Redux, kita perlu mengimport beberapa komponen dari library
tersebut. Komponen-komponen tersebut antara lain:

1. `Provider` - Komponen ini digunakan untuk membuat store pada aplikasi React.
2. `useSelector` - Komponen ini digunakan untuk mengambil state dari store pada
   aplikasi React.
3. `useDispatch` - Komponen ini digunakan untuk mengirimkan action ke store pada
   aplikasi React.
4. `createStore` - Komponen ini digunakan untuk membuat store pada aplikasi
   React.
5. `combineReducers` - Komponen ini digunakan untuk menggabungkan beberapa
   reducer pada aplikasi React.
6. `createAction` - Komponen ini digunakan untuk membuat action pada aplikasi
   React.
7. `createReducer` - Komponen ini digunakan untuk membuat reducer pada aplikasi
   React.
8. `createAsyncThunk` - Komponen ini digunakan untuk membuat action pada
   aplikasi React.
- Membuat Store

  ```javascript
  import { createStore } from 'redux';

  const store = createStore(() => {});
  ```

- Membuat Reducer

  ```javascript
  import { createStore } from 'redux';

  const initialState = {
    counter: 0,
  };

  const reducer = (state = initialState, action) => {
    return state;
  };

  const store = createStore(reducer);
  ```

- Membuat Action

  ```javascript
  import { createStore } from 'redux';

  const initialState = {
    counter: 0,
  };

  const reducer = (state = initialState, action) => {
    return state;
  };

  const store = createStore(reducer);

  const increment = () => {
    return {
      type: 'INCREMENT',
    };
  };

  const decrement = () => {
    return {
      type: 'DECREMENT',
    };
  };

  store.dispatch(increment());
  store.dispatch(decrement());
  ```

- Membuat Reducer

  ```javascript
  import { createStore } from 'redux';

  const initialState = {
    counter: 0,
  };

  const reducer = (state = initialState, action) => {
    switch (action.type) {
      case 'INCREMENT':
        return {
          ...state,
          counter: state.counter + 1,
        };
      case 'DECREMENT':
        return {
          ...state,
          counter: state.counter - 1,
        };
      default:
        return state;
    }
  };

  const store = createStore(reducer);

  const increment = () => {
    return {
      type: 'INCREMENT',
    };
  };

  const decrement = () => {
    return {
      type: 'DECREMENT',
    };
  };

  store.dispatch(increment());
  store.dispatch(decrement());
  ```

- Membuat React Component

  ```javascript
  import React from 'react';
  import { createStore } from 'redux';

  const initialState = {
    counter: 0,
  };

  const reducer = (state = initialState, action) => {
    switch (action.type) {
      case 'INCREMENT':
        return {
          ...state,
          counter: state.counter + 1,
        };
      case 'DECREMENT':
        return {
          ...state,
          counter: state.counter - 1,
        };
      default:
        return state;
    }
  };

  const store = createStore(reducer);

  const increment = () => {
    return {
      type: 'INCREMENT',
    };
  };

  const decrement = () => {
    return {
      type: 'DECREMENT',
    };
  };

  store.dispatch(increment());
  store.dispatch(decrement());

  const App = () => {
    return (
      <div>
        <h1>Counter</h1>
        <h2>0</h2>
        <button>Increment</button>
        <button>Decrement</button>
      </div>
    );
  };

  export default App;
  ```

- Menggunakan React Redux

  ```javascript
  import React from 'react';
  import { createStore } from 'redux';
  import { Provider, useSelector, useDispatch } from 'react-redux';

  const initialState = {
    counter: 0,
  };

  const reducer = (state = initialState, action) => {
    switch (action.type) {
      case 'INCREMENT':
        return {
          ...state,
          counter: state.counter + 1,
        };
      case 'DECREMENT':
        return {
          ...state,
          counter: state.counter - 1,
        };
      default:
        return state;
    }
  };

  const store = createStore(reducer);

  const increment = () => {
    return {
      type: 'INCREMENT',
    };
  };

  const decrement = () => {
    return {
      type: 'DECREMENT',
    };
  };

  store.dispatch(increment());
  store.dispatch(decrement());

  const App = () => {
    return (
      <Provider store={store}>
        <div>
          <h1>Counter</h1>
          <Counter />
          <Counter />
        </div>
      </Provider>
    );
  };

  const Counter = () => {
    const counter = useSelector((state) => state.counter);
    const dispatch = useDispatch();

    return (
      <div>
        <h2>{counter}</h2>
        <button onClick={() => dispatch(increment())}>Increment</button>
        <button onClick={() => dispatch(decrement())}>Decrement</button>
      </div>
    );
  };

  export default App;
  ```

### Redux Thunk

Redux Thunk adalah middleware yang digunakan untuk mengelola action pada Redux.
Redux Thunk memiliki beberapa kelebihan antara lain:

1. Redux Thunk memudahkan kita untuk mengelola action pada Redux.
2. Redux Thunk memudahkan kita untuk mengelola action pada Redux yang kompleks.
3. Redux Thunk memudahkan kita untuk mengelola action pada Redux yang berskala
   besar.

### Instalasi

Untuk menginstall Redux Thunk, jalankan perintah berikut pada terminal:

```bash
npm install redux-thunk -S
```

### Cara Penggunaan

Untuk menggunakan Redux Thunk, kita perlu mengimport beberapa komponen dari
library tersebut. Komponen-komponen tersebut antara lain:

1. `applyMiddleware` - Komponen ini digunakan untuk mengaktifkan middleware pada
   Redux.
2. `thunk` - Komponen ini digunakan untuk mengaktifkan middleware pada Redux.
3. `createAsyncThunk` - Komponen ini digunakan untuk membuat action pada
   aplikasi React.

Berikut ini adalah contoh penggunaan Redux Thunk pada aplikasi React:

```jsx
import React from "react";
import {
  Provider,
  useSelector,
  useDispatch,
  createStore,
  combineReducers,
  createAction,
  createReducer,
  applyMiddleware,
  thunk,
  createAsyncThunk,
} from "react-redux";

const initialState = {
  count: 0,
};

const thunkIncrement = createAsyncThunk("THUNK_INCREMENT", (payload) => {
  return new Promise((resolve) => {
    setTimeout(() => {
      resolve(payload);
    }, 1000);
  });
});

const thunkDecrement = createAsyncThunk("THUNK_DECREMENT", (payload) => {
  return new Promise((resolve) => {
    setTimeout(() => {
      resolve(payload);
    }, 1000);
  });
});

const counterReducer = createReducer(initialState, {
  [thunkIncrement.fulfilled]: (state, action) => {
    return {
      ...state,
      count: state.count + action.payload,
    };
  },
  [thunkDecrement.fulfilled]: (state, action) => {
    return {
      ...state,
      count: state.count - action.payload,
    };
  },
});

const store = createStore(
  combineReducers({ counter: counterReducer }),
  applyMiddleware(thunk)
);

const Counter = () => {
  const count = useSelector((state) => state.counter.count);
  const dispatch = useDispatch();

  return (
    <div>
      <h1>Counter</h1>
      <p>{count}</p>
      <button onClick={() => dispatch(thunkIncrement(1))}>+</button>
      <button onClick={() => dispatch(thunkDecrement(1))}>-</button>
    </div>
  );
};

const App = () => {
  return (
    <Provider store={store}>
      <Counter />
    </Provider>
  );
};

export default App;
```




  
