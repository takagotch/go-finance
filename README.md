### go-finance
---
https://github.com/FlashBoys/go-finance

https://github.com/alpeb/go-finance

```go
// pairs_test.go
func Test_GetCurrencyPairQuote(t *testing.T) {
   
  s := startTestServer("pair_fixture.csv")
  defer s.Close()
  QuoteURL = s.URL
  
  p, err := GetCurrencyPairQuote(USDEUR)
  assert.Nil(t, err)
  
  assert.Equal(t, USDEUR, p.Symbol)
}
```

```go
//




```

```
```


