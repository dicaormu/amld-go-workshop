# Introduction to Go

Applied machine learning workflows should maintain a high level of integrity in production and be able to fit into the modern infrastructure that is being utilized across industry and research. As it turns out, much of this modern infrastructure is being driven by the open source Go programming language, especially as related to distributed systems, and an increasing number of individuals and companies (Dell/EMC, The New York Times, and more) are writing their mission critical ML systems in Go.

## Notes

- Although slightly verbose in certain scenarios, Go is extremely readable and forces you to wrestle with trade offs related to application integrity.
- Go's built in tooling and IDE integrations are a huge benefit to development (`gofmt`, `golint`, etc.). 
- ML is more than possible in Go, it is being used in production at major companies.

## Links

[Installing Go and getting started](https://golang.org/doc/install)  
[The Go tour](https://tour.golang.org/welcome/1)  
[Go's stdlib docs](https://golang.org/pkg/)  
[Machine Learning with Go book](https://www.packtpub.com/big-data-and-business-intelligence/machine-learning-go)  
[Go tooling for ML and data science](https://github.com/gopherdata/resources/tree/master/tooling)

## Code Review

[Parse a clean CSV with python](example1/example1.py)  
[Parse a clean CSV with Go](example2/example2.go)  
[Force Integrity breakdown with python CSV parsing](example3/example3.py)  
[Maintain integrity in Go CSV parsing](example4/example4.go)  

## Exercises
install jupyter for go
Build the docker image for jupyter with go in introduction_to_go/gophernotes
```
$ cd introduction_to_go/gophernotes

$ docker build . -t gophernotes/gophernotes
```

Run the built image

```
$ docker run -it -p 8888:8888 -v /PATH/TO/LOCAL/PROJECT/amld-go-workshop:/go/src/amld-go-workshop  gophernotes/gophernotes

```

## introduction_to_go

Notebook
in data there is a csv file: 5kings_battles_v1.csv. It contains all the information about the Battles of the War of Five Kings 

you can find the dataset and the python notebook in 

https://github.com/chrisalbon/war_of_the_five_kings_dataset

### Exercise 1

Implement another way of handling the CSV parsing error we encountered above.  That is, handle the missing value in a way other than throwing an error.

[Template](exercises/template1/template1.go) |
[Answer](exercises/exercise1/exercise1.go)

### Exercise 2

Instead of getting the maximum integer in the integer columns, calculate the sum of integers in the integer column based on [example_clean.csv](data/example_clean.csv) another way of handling the CSV parsing error we encountered above.  

[Template](exercises/template2/template2.go) |
[Answer](exercises/exercise2/exercise2.go)

