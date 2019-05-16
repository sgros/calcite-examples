# What's in here?
In this repository you'll find some examples wich show how to use Apache Calcite to perform certain tasks. Currently, there are two working examples:

### SQLParser

This example will take SQL expression as the first argument in the command line, parse it using Apache Calcit's parser, turn it intothe SQLNode structure and dump SQL created from SQL node into stdout.

The main (and only) file SQLParse.java can be found in directory `src/main/java/hr/fer/zemris/calcite/sqlparser/`

### Sql2Rel

This example is built on the previous one and is a bit more complicated. It will also take SQL statement from the command line and then it'll turn it into the RelNode data structure.

The main (and only) file Sql2Rel.java can be found in directory `src/main/java/hr/fer/zemris/calcite/sql2rel/`.

# How to compile and run

I'm using command line to compile and run these examples, so I'll use that.

## Compilation

First, I expect that you have maven in your PATH. To compile all the examples, run the following command:

mvn compile

that should be it.

## Configuration

You need to have PostgreSQL up and running in order to try Sql2Rel example. For trying SQLParser there are no prerequisites.

## Run

To run the code use the script `run` in the repository's root directory. For example, to try SQLParse, do the following:

/run hr.fer.zemris.calcite.sqlparser.SQLParse "SELECT * FROM tables"

