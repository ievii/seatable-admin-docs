# System limitations

## General limitations

| Category                   | Limitation Type                         | Threshold                                     | Additional notes                                             |
| :------------------------- | :--------------------------------------- | :-------------------------------------------- | :----------------------------------------------------------- |
| Base                      | Rows                                    | 100,000                                        | The base becomes read-only when exceeding 100,000 rows.            |
|                            | Rows 2                            | 150,000                                        | The base will not be loaded to the memory if exceeding 150,000 rows. |
|                            | Archived rows                        | no limit                                    |     |
|                            | Tables                        | 200                                           |                                                              |
| | Base external links | 100 | |
| | View external links | 100 | |
| | External apps | 100 | |
| | Forms | 100 | |
| Table                     | Columns                           | 500                                           |                                                              |
| External links viewing     | Viewing rate of a base's external link  | 300/min maximum                               |                                                              |
| Import / export operations | Size of a base being exported as a .dtable file  | 100MB                                        | This limit can be set by yourself for the Developer / Enterprise Edition. Set "DTABLE_EXPORT_MAX_SIZE" in dtable_web_settings.py. A base's attachments can be viewed and deleted in batch in the base's Attachments Management. |
|                            | Import of a xlsx/csv file                        | 50,000 records maximum                         |                                                              |
| | Export of a table | 10,000 records or 1,000,000 cells | |
| | Export of a view in table | 1,000,000 cells | |
| Big data Import / export operations | Import from xlsx to big data storage | 500,000 records | Can be modified it in the configuration file of dtable_web_settings.py. |
|  | Update from xlsx to big data storage | 500,000 records | Can be modified it in the configuration file of dtable_web_settings.py. |
|  | Export big data view to Excel | 250,000 records | Can be modified it in the configuration file of dtable_web_settings.py. |
| Groups | Group members | 500 | |
|  | Group bases | 500 | |
| Common dataset (CDS) | Syncs of CDS | Sync up to the first 50,000 records | |
| Scripts                    |                                          |                                               |                                                              |
| Notification rules         |                                          |                                               |                                                              |
| Automation rules | Records meet specific conditions after modification | For batch modification, check the first 50 records. A rule can be triggered up to 10 times per minute. | |
|  | Add record | For batch addition, check the first 50 records. A rule can be triggered up to 10 times per minute. | |
|  | Run periodically on records meet conditions | Lock a maximum of 200 rows and send a maximum of 50 emails in one trigger | |



## API limitations

| Category                   | Limitation Type                         | Threshold                                     | Additional notes                                             |
| :------------------------- | :--------------------------------------- | :-------------------------------------------- | :----------------------------------------------------------- |
| API calls                | Max. number of rows appending in a single call    | 1,000                                          |                                                                |
|                            | Max. number of rows modification in a single call | 1,000                                          |                                                              |
|                            | Max. numbers of rows deletion in a single call     | 10,000                                         |                                                              |
|                            | Max. numbers of rows listed in a single call       | 10,000                                          | Use the `start` and `limit` params to list further rows.                                                             |
| API calling rate          | API calling for a single base              | 300/min for the cloud edition. 5000/day.                     | This limit can be set by yourself for the Developer Edition. You should use batch APIs to reduce API calls.  |
|                            | API calling for getting rows of a table | 100/min for a single table,  600/hour maximum | We strongly suggest that you use  SQL if the API calling is frequent or add some cache in your code. |
| | SQL calling for a single base | 5000/day |  |

