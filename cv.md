# CV

## Kobylan Gaziz

### Contact information

- email: kobylan.kaz@gmail.com
- github: [tab here to open my git](https://github.com/kobylan)

### Goal

I have an idea, but not enough skill to do it.

### Skills

- Golang
- HTML/CSS
- Javascript

### Code example

```go
    package main

    import (
    	"io/ioutil"
    	"log"
    	"net/http"
    	"strings"
    )

    func handler(w http.ResponseWriter, r *http.Request) {
    	resp, err := http.Get("https://groupietrackers.herokuapp.com/" + r.URL.Path[1:])
    	if err != nil {
    		panic(err)
    	}
    	defer resp.Body.Close()
    	data, err := ioutil.ReadAll(resp.Body)
    	str := strings.ReplaceAll(string(data), "https://groupietrackers.herokuapp.com/", "http://localhost:8080/")
    	data = []byte(str)
    	if err != nil {
    		panic(err)
    	}
    	w.Write(data)
    }

    func main() {
    	http.HandleFunc("/", handler)
    	log.Fatal(http.ListenAndServe(":8080", nil))
    }
```

### Experience

Creater macmeharder.com

### Education

I. **SSAU 2017-2019**
II. **TAU 2019-present**
III.**Alem school 2019-present**

### English

- B1 - Intermediate
