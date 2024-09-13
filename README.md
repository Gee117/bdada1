**Description:-**
I have created a MapReduce solution using Python's multiprocessing module to process a dataset of smartphones and identify the number of phones that meet specific pricing-related criteria. While the conditions being checked are technical features (such as internal memory, 4G support, and screen resolution), the ultimate goal is to filter out phones that likely fit within a higher price bracket based on these attributes. \n

The key conditions we are filtering for in the dataset include: \n
1.**Internal Memory:** The phone must have more than 40 GB, which generally correlates with higher-priced models.
2. **4G Support:** Phones that support 4G are often newer and more expensive.
3. **Pixel Height:** A higher screen resolution (above 500 pixels in height) suggests better display quality, typically associated with premium phones.
4. **Pixel Width:** A screen width greater than 1000 pixels usually indicates a larger and higher-definition display, adding to the price.
5. **RAM:** Phones with more than 200 MB of RAM are more capable of handling modern applications, another factor that contributes to higher pricing.
