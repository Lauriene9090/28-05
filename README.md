# 28-05

import { useState, useRef } from "react"

export default function App(){
  let variable = 0
  const [state, setState] = useState(0)
  const ref = useRef(0)

  const showValue = () => {
    alert(`
      valor Variavel: ${variable}
      valor do State: ${state}
      valor do Ref: ${ref.current}
      `)
  }

  return(
    <div>
      <p>Valor variavel: {variable}</p>
      <p>Valor do State: {state}</p>
      <p>Valor do Ref: {ref.current}</p>
      <button onClick={() => variable++}>Aumentar Variavel</button>
      <button onClick={() => ref.current++}>Aumentar Ref</button>
      <button onClick={() => setState(state => state + 1)}>Aumentar State</button>
      <button onClick={showValue}>Exibir Valores</button>
  
    </div>
  )
}
