# Unit test para reducer que actualiza un estado

## Código

```js
it('should add the winner to the state', () => {
    const action = {
      type: fetchBattleWins.fulfilled,
      payload: { winner: 'monster-1', tie: false },
    };
    const state = monstersReducerExtended(undefined, action);

    expect(state.winner).toEqual(
      expect.objectContaining({
        winner: 'monster-1',
        tie: false,
      }),
    );
  })
```

## Pasos



