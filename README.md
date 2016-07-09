# AOJ checker

```
$ go get github.com/sotetsuk/aojchecker
```

# Example

```go
func main() {
        // interesting example
        id := "ALDS1_5_B"
        userList := []string{"sotetsuk", "nishimuuuuuu", "ryof", "chiiia12", "kikunantoka", "a_Higu", "smochi", "sat0yu", "cauchym", "sassan", "akito0107", "non1207"}

        doc, _ := aojchecker.GetDoc(id)
        Records := aojchecker.ParseRecords(doc)
        for _, userName := range userList {
                if Records.HasUser(userName) {
                        fmt.Println(fmt.Sprintf("solved: %v", userName))
                } else {
                        fmt.Println(fmt.Sprintf("not yet: %v", userName))
                }
        }
}
```
