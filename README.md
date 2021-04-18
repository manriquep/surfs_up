# surfs_up
**Background**

The client wants to open a surf and ice cream shop and has asked for temperature trends specifically for the months of June and December in Oahu, an island in Hawaii. The information will assist the client in determining if the surf and ice cream shop will sustain all year round.

**Purpose**

The purpose of this analysis is finding the typical weather for June and December in Oahu.

**Results**

These are the results for the June and December temperatures (See Table One):

- The average June temperature was 74.94 degrees Fahrenheit while the average for December was a degree lower at 71.04.
- The minimum June temperature was 64 degrees Fahrenheit while the December minimum temperate was much lower at 56.
- The maximum June temperature was 85 degrees Fahrenheit while the December maximum temperature was awfully close at 83.

![image](https://user-images.githubusercontent.com/74743437/115160570-ea1fe800-a066-11eb-8133-6283d8eb8601.png)

**Summary**

The temperatures in December are slightly lower than June but suitable for a surf and ice cream shop business.More interesting weather data could be gathered by analyzing the following queries:

- the total precipitation levels for June and December.

session.query(Measurement.date, Measurement.prcp).filter(extract(&#39;month&#39;, Measurement.date) == 6).all()

session.query(Measurement.date, Measurement.prcp).filter(extract(&#39;month&#39;, Measurement.date) == 12).all()

- the amount of precipitation at the most active station for June and December.

session.query(Measurement.prcp).filter(Measurement.station == &#39;USC00519281&#39;).filter(extract(&#39;month&#39;, Measurement.date) == 6).all()

session.query(Measurement.prcp).filter(Measurement.station == &#39;USC00519281&#39;).filter(extract(&#39;month&#39;, Measurement.date) == 12).all()
