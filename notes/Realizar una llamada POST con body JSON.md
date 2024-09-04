# Realizar una llamada POST con body JSON

## Código

```js
import { API_URL } from '../../constants/env';
import { Battle, Players } from '../../models/interfaces/battle.interface';

const battle = async (players: Players): Promise<Battle> =>
  await fetch(`${API_URL}/battle`, {
    method: 'POST',
    headers: {
      'Content-Type': 'application/json',
    },
    body: JSON.stringify(players),
  }).then(response => response.json());

export const MonsterServiceExtended = {
  battle,
};
```

## Pasos

1. Definir interfaces, tanto de parametro como de respuesta
2. Crear funcion asincrono que retorne una promesa, atencion a donde van los types
3. Hacer fetch y en el segundo parametro pasar la config de arriba.
4. Resolver la promesa y retornar el json de la resuesta
