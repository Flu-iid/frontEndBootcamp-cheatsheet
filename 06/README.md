# toDo solution
## changing according to input
```js
function App() {
  const [list, setList] = useState([]);
  const [show, setShow] = useState("");

  return (
    <div>
      <form onSubmit={(e) => e.preventDefault()}>
      <input
        type="text"
        placeholder="enterValue"
        onChange={e=>setShow(e.target.value)}
      />
      <button type="submit" onClick={()=>{setShow("")}}>add</button>
    </form>
    <p>{show}</p>
    </div>
  );
}
```
## adding to list and removing from list
```js
function App() {
  const [list, setList] = useState([]);
  const [show, setShow] = useState("");

  const addToList = () => {
    if (show) {
      const help = [...list, show];
      setList(help);
      setShow("");
    }
  };
  const removeFromList = (index) => {
    const help = [...list]
    help.splice(index,1)
    setList(help)
  }
  console.log(list)
  return (
    <div>
      <form onSubmit={(e) => e.preventDefault()}>
        <input
          className="border-solid border-2 border-red-800"
          type="text"
          placeholder="enterValue"
          onChange={(e) => setShow(e.target.value)}
          value={show}
          autoFocus
        />
        <button type="submit" onClick={addToList}>
          add
        </button>
      </form>
      <div>
        {list.map((item, index) => (
          <div key={index}>
            <p>{item}</p>
            <button onClick={removeFromList}>X</button>
          </div>
        ))}
      </div>
    </div>
  );
}
```


































# `react-toastify`




# `sweetalert2`






## bootstrap install
bootstrap 12 grid
> `npm install react-bootstrap bootstrap`

> sweatalert2








