```javascript

===> working with react-router-dom
//
//
===> package installed, => npm install react-router-dom
===> put this file below in the 'app.js'

    import React from 'react';
    import Posts from './components/Posts/Posts';
    import Form from './components/Form/Form';
    import EditPost from './components/EditPost/EditPost';
    import Register from './components/Register/Register';
    import Signin from './components/Signin/Signin';
    import Navbar from './components/Navbar/Navbar';
    import { BrowserRouter, Routes, Route } from 'react-router-dom';

    const App = () => {
        return (
            <div>
                <BrowserRouter>
                    <Navbar />
                    <Routes>
                        <Route exact path='/' element={<Posts />} />
                        <Route exact path='/posts/createpost' element={<Form />} />
                        <Route exact path='/posts/editpost/:id' element={<EditPost />} />
                        <Route exact path='/register' element={<Register />} />
                        <Route exact path='/signin' element={<Signin />} />
                    </Routes>
                </BrowserRouter>
            </div>
        );
    };

    export default App;
