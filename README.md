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

// history_test.go

func Test_GetHistory(t *testing.T) {
  
  s := startTestServer("history_fixture.csv")
  defer s.Close()
  HistoryURL = s.URL
  
  cs := startCookieServer("yahoo_appl.html", true)
  defer cs.Close()
  sessionURL = cs.URL
  
  bars, err := GetHistory("", Datetime{}, Datetime{}, Day)
  assert.Nil(t, err)
  
  assert.Equal(t, "", bars[4].Symbol)
}
```

```go
// cahsflow_test.go
func TestNetPresentValue(t *testing.T) {
  var tests = []struct {
  
  }{
  
  }
  
  for _, test := range tests {
    if got := NetPresentValue(test.rate, test.values); math.Abs() > Precision {
      t.Errorf("NetPresentValue(%f, %v) = %f", test.rate, test.values, got)
    }
  }
}


```

```
```


