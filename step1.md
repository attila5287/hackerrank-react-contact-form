```JS
import { useState } from 'react'
import reactLogo from './assets/react.svg'
import './App.css'

function App() {
  const [name , setName] = useState('')
  const [email, setEmail] = useState('')
  const [message, setMessage] = useState('')
  const [submitted, setSubmitted] = useState(null);
  const handleSubmit = () => {
    const formData = {
      name: name,
      email: email,
      message: message
    }
    setName('')
    setEmail('')
    setMessage('')
    setSubmitted(formData)
    console.log(formData)
  }

  return (
    <>
      <div className="card" style={{border: '1px white solid', padding: '10px', margin: '10px', borderRadius: '5px'}}>
        <input type="text" placeholder="Name" value={name} onChange={(e) => setName(e.target.value)} />
        <br />
        <input type="email" placeholder="Email" value={email} onChange={(e) => setEmail(e.target.value)} />
        <br />
        <textarea placeholder="Message" value={message} onChange={(e) => setMessage(e.target.value)} />
        <br />
        <button onClick={handleSubmit}>Submit</button>
      </div>
      {submitted && (
      <div className="card" style={{border: '1px turquoise solid', padding: '0px', margin: '0px', borderRadius: '25px'}}>
          <h2 style={{color: 'turquoise'}}>Form Submitted</h2>
          <p>Name: {submitted.name}</p>
          <p>Email: {submitted.email}</p>
          <p>Message: {submitted.message}</p>
        </div>
      )}
    </>
  )
}

export default App
```