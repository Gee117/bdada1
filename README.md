**Description:-**

I have created a MapReduce solution using Python's multiprocessing module to process a dataset of smartphones and identify the number of phones that meet specific pricing-related criteria. While the conditions being checked are technical features (such as internal memory, 4G support, and screen resolution), the ultimate goal is to filter out phones that likely fit within a higher price bracket based on these attributes.

The key conditions we are filtering for in the dataset include:

 1.**Internal Memory:** The phone must have more than 40 GB, which generally correlates with higher-priced models.

 2. **4G Support:** Phones that support 4G are often newer and more expensive.

 3. **Pixel Height:** A higher screen resolution (above 500 pixels in height) suggests better display quality, typically associated with 
  premium phones.

 4. **Pixel Width:** A screen width greater than 1000 pixels usually indicates a larger and higher-definition display, adding to the price.

 5. **RAM:** Phones with more than 200 MB of RAM are more capable of handling modern applications, another factor that contributes to higher pricing.

**How Map-Reduce works:-**

The **mapping phase** is handled by the function map_func. 

Input: Each record (row) from the dataset, which represents a smartphone's details (e.g., internal memory, 4G support, pixel height/width, RAM, etc.).

Processing: The map_func checks each record to see if the smartphone meets all the specified conditions for pricing (e.g., more than 40 GB memory, 4G support, etc.).

Output: For each record that meets all the criteria, the function returns 1, indicating that this phone is valid. If it does not meet the conditions, it returns 0.

The **Reduce phase** is handled by the reduce_func.

Input: The results of the map_func applied to each record (i.e., a list of 1s and 0s, where 1 means a valid phone and 0 means it didn’t meet the conditions).

Processing: The reduce_func sums up the list of results (1s and 0s) to get the total count of valid phones that meet the criteria.
