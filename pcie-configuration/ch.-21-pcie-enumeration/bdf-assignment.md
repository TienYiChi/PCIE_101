# BDF Assignment

## Initiate Requests before BDF assignment

* Before assignment, a function only "knows" its function number, and nothing else.

## Initiate Completions before BDF assignment

* Bus#, Device# should be set to 0. The original requester must ignore this completer ID value.

## Memorize ID

* Each time a function receives a <mark style="color:red;">**Type0 Config Write Request**</mark>**,** it saves the BDF as its ID in a function-specific manner.
