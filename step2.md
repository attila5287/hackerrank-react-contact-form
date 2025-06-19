```JS
import { useState } from 'react'
import reactLogo from './assets/react.svg'
import './App.css'

function App() {
  const [name , setName] = useState('')
  const [email, setEmail] = useState('')
  const [message, setMessage] = useState('')
  const [submitted, setSubmitted] = useState(null);
  const [error, setError] = useState(null);
  const handleSubmit = () => {
    const formData = {
      name: name,
      email: email,
      message: message
    }
    if (name === '' || email === '' || message === '') {
      setError('Please fill in all fields')
      setSubmitted(null)
      return
    }
    setName('')
    setEmail('')
    setMessage('')
    setSubmitted(formData)
    setError(null)
    console.log(formData)
  }

  return (
    <>
      <h1>
        <img
          className="logo-spin"
          src={reactLogo}
          alt="logo"
          style={{ width: "40px", height: "40px", marginRight: "10px" }}
        />
        <a
          href="https://github.com/attila5287/hackerrank-react-contact-form"
          target="_blank"
        >
          Contact Form
        </a>
      </h1>
      <div
        className="card"
        style={{
          border: "1px white solid",
          padding: "10px",
          margin: "10px",
          borderRadius: "5px",
        }}
      >
        <input
          type="text"
          placeholder="Name"
          value={name}
          onChange={(e) => setName(e.target.value)}
        />
        <br />
        <input
          type="email"
          placeholder="Email"
          value={email}
          onChange={(e) => setEmail(e.target.value)}
        />
        <br />
        <textarea
          placeholder="Message"
          value={message}
          onChange={(e) => setMessage(e.target.value)}
        />
        <br />
        <button onClick={handleSubmit}>Submit</button>
      </div>
      {submitted && (
        <div
          className="card"
          style={{
            border: "1px turquoise solid",
            padding: "0px",
            margin: "0px",
            borderRadius: "25px",
          }}
        >
          <h2 style={{ color: "turquoise" }}>Form Submitted</h2>
          <p>Name: {submitted.name}</p>
          <p>Email: {submitted.email}</p>
          <p>Message: {submitted.message}</p>
        </div>
      )}
      {error && (
        <div
          className="card"
          style={{
            border: "1px red solid",
            padding: "0px",
            margin: "0px",
            borderRadius: "25px",
          }}
        >
          <h2 style={{ color: "red" }}>Error</h2>
          <p>{error}</p>
        </div>
      )}
    </>
  );
}

export default App

```