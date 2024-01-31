# Exporting Data from MongoDB to a CSV File

Although it is possible to just work with MongoDB on some analytical platforms, a lot of data scientists use an analysis platform that cannot work with MongoDB directly. A common practice in data science is to export all or part of the data into a CSV file that almost any analytical tool can import. 

You can export the result of MongoDB queries using the mongoexport command in the terminal shell. This command uses the following arguments:

The mongoexport file is located in /big-data-3/mongodb/bin/. The format of the command is as follows: 

```bash
./bin/mongoexport --db  <dbname> --collection <collectionName> --out  <OutfileName>
```

Your assignment is to export user data from the sample db to any output file. 

| Argument | Description |
|---|---|
| --collection <name> | The collection to use. |
| --db <name>   | The database to use. |
| --fields <field 1>,<field 2>,<...> | The fields to include in the query result. |
| --query <query> | The query to perform. |
| --out <name> | The name of the output file. |
| --type=<type> | Format of export, either csv or json. |

In this exercise, we ask you to export your tweet  data from MongoDB to a CSV file. In Part 2, we will be performing analytics on the tweet texts, so export this field from MongoDB into a CSV file.