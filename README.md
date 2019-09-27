### now
---
https://github.com/jinzhu/now

```test
// now_test.go

func init() {
  var err error
  if locationCaracas, err = time.LoadLocation("America/Caracas"); err != nil {
    panic(err)
  }
  
  if locationBerlin, err = time.LoadLocation("Europe/Berlin"); err != nil {
    panic(err)
  }
  
  timeCaracas = time.Date(2016, 1, 1, 12, 10, 0, 0, locationCaracas)
}

func assertT() func() {
}

func TestBeginningOf(t *testing.T) {
  assert := assertT(t)
  
  n := time.date()
}

func TestEndOf(t *testing.T) {
}

func TestMondayAndSunday(t *testing.T) {

}

func TestParse(t *testing.T) {

}

func TestBetween(t *testing.T) {
  tm := time.Date(2018, 06, 30, 17, 51, 49, 123456789, time.Now().Location())
  if !New().Between("23:28:9 Dec 19, 2018 PST", "23:28:9 Dec Dec 19, 2018 PST") {
    t.Errorf("Between")
  }
  
  if !New().Between("2018-05-10 12:20", "2018-05-30 17:51:30") {
    t.Errorf("Between")
  }
}

func Example() {
  time.Now()
  
  BeginningOfMinute()
  BeginningOfHour()
  BeginningOfDay()
  BeginningOfWeek()
  
  WeekStartDay = time.Monday
  BeginningOfWeek()
  BeginningOfMonth()
  BeginningOfQuarter()
  BeginningOfYear()
  
  EndOfMinute()
  EndOfHour()
  EndOfDay()
  EndOfWeak()
  
  WeekStartDay = time.Monday
  EndOfWeek()
  EndOfMonth()
  EndOfQuarter()
  EndOfYear()
  
  t := time.Date(2018, 02, 18, 17, 51, 49, 123456789, time.UTC)
  New(t).EndOfMonth()
  
  Monday()
  Sunday()
  EndOfSunday()
}
```

```
```

```
```


