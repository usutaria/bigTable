From Google Support : For increment method of readModifyWrite method in Google Bigtable.

1.	Store the long value:
•	Allocate a ByteBuffer with the size of a long (8 bytes).
•	Put the long value in the buffer.
•	Get the byte array from the buffer.
•	Create a ByteString from the byte array.
•	Set the ByteString as the value for the mutation.
2.	Retrieve the long value:
•	Call the readRow method with the row key to get the row object.
•	Get the first cell with the column family and column qualifier.
•	Get the ByteString value from the cell.
•	Wrap the ByteString in a ByteBuffer.
•	Get the long value from the ByteBuffer.
•	Print the long value.
Key Points and Best Practices
•	Efficiency: Storing longs as their byte representations ensures optimal storage space utilization in Bigtable.
•	Increment/Decrement: Use the increment method for efficient atomic updates on long values stored in Bigtable.
•	Data Types: Always match the data type when storing and retrieving to avoid errors (e.g., don't try to retrieve a 64-bit long as a string).
•	Error Handling: Implement proper error handling (e.g., catching IOExceptions, BigtableException etc.) to make your code robust.

Resources:
https://github.com/bijukunjummen/cloud-bigtable-sample
https://github.com/pinterest/ktlint
