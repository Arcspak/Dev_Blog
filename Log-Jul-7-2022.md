## Update preview of Data Toolkit and subsequent development plan

Hello anyone, this is Arcspark.

After putting our resources on the shelf in the [Unity Asset Store](https://assetstore.unity.com/publishers/69610), we received some feedback,
some related to the functions of the [🗃️ Data Toolkit](https://assetstore.unity.com/packages/slug/224909), and most related to documentation.
After receiving these feedbacks, we immediately began to make adjustments. 
Now the [new document](https://github.com/Arcspak/Tutorials/blob/main/Data_Toolkit/Data_Toolkit_Quick_Tutorial.pdf) has been completed,
with more API descriptions and sample code, and covers all important functions as much as possible.
For some review reasons of Unity Asset Store, we cannot update the PDF document files in the published package in real time.
We therefore recommend that you check out our [online documentation page](https://github.com/Arcspak/Tutorials) for timely update.

## Preview of new features of Data Toolkit
Some users reported that they could not create a standard SQLite database file at runtime.
Instead, they could only create a new table in the original file to realize the function, which caused some logical confusion.
Now we have implemented a new method, which allows users to create new database files in persistent data path and automatically deal with platform related path problems.

Another big change is about CSV Util in Data Toolkit.
The first row of CSV file generally represents the table header declaration, identifying the data name and data type of each column. The remaining lines are data.
The data of header row is used to describe the type of data and provide the key name information of the whole column.

This is a common practice that conforms to the characteristics of data-driven development, and a lot of large game development companies, such as Blizzard and EA, also use this way to complete a configuration or description file in their projects.

However, header row is not a part of standard syntax rule in CSV format. Using pure CSV without header row to manage game data is also needed.
Therefore, we have updated the functions of CSVTable to support pure CSV.

Now the two formats of CSV can both be parsed and serialized correctly. CSVTable will distinguish, parse and serialize them automatically.
The operations on them can be completed with a unified interface.
The two forms of csvtables are all indicated differently in the field about ColumnHeader, so users don't need to pay much attention to the differences.
Complete the operation naturally and intuitively, which is the scheme we have always advocated and practiced.

The above changes have been developed and tested(in the new version 1.1) and will be available soon.

## Development plan
While updating the data toolkit, we also have new development plans to help developers develop games more smoothly and quickly.
We found that most developers spend a lot of time on resource management, including writing a lot of code on the processes of loading/unloading asset in both AssetBundle and Resources path, dealing with platform differences, and establishing resource pools.

Time to use tools to organize project structure and assets. This tool needs to provide a simple interface while realizing all the above functions. We're now work on it.

Although there is no specific timetable, this package on asset and data management will probably be completed in a few weeks, and will enter the testing and later submission review stage.

We will still have the first week discount on this new asset. If you need this tool, please follow our news.

## EOF
These are all the contents worth sharing at present. Any feedback you can give me on this would be highly appreciated, please let us know if you have any comments.
See you next time!
