# Crear y consumir un contexto con estado interno

## Código

```jsx
import { createcontext, usestate } from "react";

const numbercontext = createcontext(null)

function secondcontext({ children }) {
  const [number, setnumber] = usestate(0)

  return (
    <numbercontext.provider value={[number, setnumber]}>
      {children}
    </numbercontext.provider>
  )
}

export default secondcontext;
export { numbercontext };
```

## Pasos

1. Importar los hooks createContext y useState
2. Crear el contexto con el valor por defecto
3. Crear un componente que tenga estado y reciba {children}
4. En el render del componente tiene que usarse el provider del context creado
5. En dicho provider proveer el estado y el set del estado
6. Renderizar children
7. Exportar el context y el provider
