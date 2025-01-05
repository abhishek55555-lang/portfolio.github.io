#include <iostream>
 
#include <unordered_map>
 
#include <fstream>
 
#include <string>
 
#include <conio.h>
 
#include <cstring>
 
#include <map>
 
 #include <algorithm>
 
#include <vector>
 
#include <iomanip>
 
#include <limits>
 
using namespace std;
 
// void adminMenu();
 
void passengerMenu();
 
void manageTrainSchedule();
 
void bookTicket();
 
void trackTrain();
 
void rateService();
 
 
 class Train {
 
public:
 
    int trainNumber;
 
    string trainName;
 
    string source;
 
    string destination;
 
    string departureTime;
 
    string arrivalTime;
 
    int distance;
 
    string type; 
 
    double price; 
 
 
 
    Train(int number, const string& name, const string& src, const string& dest, const string& depTime, const string& arrTime, int dist, const string& t, double p)
 
        : trainNumber(number), trainName(name), source(src), destination(dest), departureTime(depTime), arrivalTime(arrTime), distance(dist), type(t), price(p) {}
 
 
 
    void display() const {
 
        cout << left << setw(15) << trainNumber
 
             << setw(25) << trainName
 
             << setw(20) << source
 
             << setw(20) << destination
 
             << setw(15) << departureTime
 
             << setw(15) << arrivalTime
 
             << setw(10) << distance
 
             << setw(15) << type
 
             << setw(10) << price << endl;
 
    }
 
};
 
 
 
class TrainDatabase {
 
private:
 
    vector<Train> trains;
 
 
 
public:
 
    void addTrain(int number, const string& name, const string& src, const string& dest, const string& depTime, const string& arrTime, int dist, const string& type, double price) {
 
        trains.emplace_back(number, name, src, dest, depTime, arrTime, dist, type, price);
 
    }
 
 
 
    void initializeDatabase() {
 
                addTrain(2000, "Mail Express", "Ahmedabad", "Lucknow", "09:45", "08:45", 23, "Local", 262.03);
 
        addTrain(2001, "Duronto Express", "Ahmedabad", "Lucknow", "19:45", "13:15", 1856, "Passenger", 1098.67);
 
        addTrain(2002, "Duronto Express", "Hyderabad", "Kolkata", "16:00", "21:45", 1317, "Passenger", 1272.59);
 
 
addTrain(2003, "Mail Express", "Mumbai", "Bangalore", "05:00", "04:00", 1363, "Passenger", 688.33); 

addTrain(2004, "Superfast Express", "Jaipur", "Mumbai", "03:45", "22:15", 917, "Local", 1068.87);

addTrain(2005, "MEMU", "Hyderabad", "Lucknow", "03:30", "10:45", 1356, "Passenger", 1901.52);
 
addTrain(2006, "Superfast Express", "Kolkata", "Delhi", "08:30", "14:15", 1496, "Local", 600.06);
 
addTrain(2007, "Duronto Express", "Bangalore", "Jaipur", "07:45", "14:15", 1630, "Local", 143.67);
 
addTrain(2008, "Rajdhani Express", "Kolkata", "Delhi", "20:30", "05:00", 381, "Passenger", 1476.34);
 
addTrain(2009, "Superfast Express", "Jaipur", "Chennai", "20:00", "23:00", 1149, "Local", 1413.97);
 
addTrain(2010, "Mail Express", "Lucknow", "Hyderabad", "01:45", "13:00", 326, "Passenger", 1650.07);
 
addTrain(2011, "Suburban Local", "Pune", "Chennai", "20:15", "19:00", 1222, "Local", 237.97);
 
addTrain(2012, "Intercity Express", "Pune", "Lucknow", "18:15", "18:45", 1316, "Passenger", 1286.57);
 
addTrain(2013, "Superfast Express", "Lucknow", "Pune", "08:00", "00:30", 770, "Local", 1484.8);
 
addTrain(2014, "Duronto Express", "Mumbai", "Lucknow", "22:45", "03:30", 194, "Express", 1856.72);
 
addTrain(2015, "Superfast Express", "Delhi", "Pune", "12:45", "03:30", 1961, "Express", 656.79);
 
addTrain(2016, "Mail Express", "Bangalore", "Ahmedabad", "18:15", "18:45", 837, "Local", 1692.81); 

addTrain(2017, "Duronto Express", "Ahmedabad", "Pune", "03:15", "17:15", 993, "Local", 50.25);

 addTrain(2018, "Duronto Express", "Lucknow", "Bangalore", "23:00", "05:30", 102, "Passenger", 750.52); 

 addTrain(2019, "Superfast Express", "Delhi", "Hyderabad", "20:15", "18:15", 1801, "Local", 1896.87); 

 addTrain(2020, "Duronto Express", "Lucknow", "Bangalore", "11:15", "06:30", 991, "Local", 1273.68);

addTrain(2021, "Intercity Express", "Kolkata", "Pune", "03:15", "15:15", 1711, "Local", 256.45);
 
addTrain(2022, "Mail Express", "Chennai", "Bangalore", "15:45", "17:00", 1379, "Express", 98.88);
 
addTrain(2023, "Superfast Express", "Lucknow", "Delhi", "17:15", "00:15", 860, "Local", 137.03);
 
addTrain(2024, "Rajdhani Express", "Pune", "Chennai", "03:45", "21:00", 1086, "Express", 1485.43);
 
addTrain(2025, "Garib Rath", "Ahmedabad", "Hyderabad", "07:00", "11:00", 1714, "Express", 474.36);
 
addTrain(2026, "Mail Express", "Ahmedabad", "Pune", "18:00", "09:15", 1471, "Express", 1157.51);
 
addTrain(2027, "MEMU", "Lucknow", "Ahmedabad", "10:00", "02:45", 1833, "Passenger", 1853.61);
 
addTrain(2028, "Suburban Local", "Ahmedabad", "Bangalore", "05:45", "15:30", 820, "Local", 1373.17);
 
addTrain(2029, "MEMU", "Delhi", "Mumbai", "16:15", "07:15", 1986, "Express", 1114.18);
 
addTrain(2030, "Mail Express", "Kolkata", "Pune", "04:45", "09:15", 714, "Passenger", 933.18);
 
addTrain(2031, "Intercity Express", "Mumbai", "Delhi", "10:45", "22:30", 171, "Express", 756.8);
 
addTrain(2032, "Intercity Express", "Bangalore", "Ahmedabad", "15:30", "19:00", 561, "Express", 1793.33);
 
addTrain(2033, "Shatabdi Express", "Lucknow", "Kolkata", "12:00", "09:00", 1999, "Express", 478.26);

 addTrain(2034, "Rajdhani Express", "Bangalore", "Chennai", "22:15", "14:00", 571, "Express", 126.24);

  addTrain(2035, "Suburban Local", "Chennai", "Delhi", "02:45", "21:45", 953, "Local", 1114.73);

  addTrain(2036, "Jan Shatabdi", "Pune", "Kolkata", "15:15", "03:15", 1353, "Express", 1959.25); 

  addTrain(2037, "Intercity Express", "Pune", "Ahmedabad", "00:15", "21:00", 549, "Passenger", 567.21);

addTrain(2038, "Suburban Local", "Ahmedabad", "Hyderabad", "16:00", "10:30", 1357, "Passenger", 123.08);

 
addTrain(2039, "Shatabdi Express", "Bangalore", "Lucknow", "05:30", "05:45", 1310, "Passenger", 1332.21);
 
addTrain(2040, "Rajdhani Express", "Chennai", "Ahmedabad", "03:00", "04:30", 910, "Passenger", 301.99);
 
addTrain(2041, "Shatabdi Express", "Delhi", "Lucknow", "02:00", "02:00", 253, "Passenger", 1678.69);
 
addTrain(2042, "Garib Rath", "Delhi", "Jaipur", "00:45", "17:45", 341, "Express", 577.17);
 
addTrain(2043, "Mail Express", "Kolkata", "Delhi", "08:15", "02:15", 1156, "Passenger", 1548.56);
 
addTrain(2044, "Intercity Express", "Hyderabad", "Lucknow", "00:00", "06:00", 1557, "Express", 1144.52);
 
addTrain(2045, "Shatabdi Express", "Bangalore", "Lucknow", "15:45", "11:30", 678, "Local", 1579.67);
 
addTrain(2046, "Garib Rath", "Bangalore", "Kolkata", "04:00", "04:30", 1084, "Passenger", 1303.31);
 
addTrain(2047, "Jan Shatabdi", "Lucknow", "Pune", "01:15", "12:15", 1900, "Passenger", 875.11);
 
addTrain(2048, "Superfast Express", "Bangalore", "Delhi", "01:00", "20:30", 992, "Passenger", 1721.83);
 
addTrain(2049, "Duronto Express", "Ahmedabad", "Chennai", "05:00", "01:00", 1098, "Passenger", 159.32); 

addTrain(2050, "Jan Shatabdi", "Pune", "Jaipur", "10:15", "01:45", 298, "Express", 1637.55);

 addTrain(2051, "MEMU", "Chennai", "Ahmedabad", "10:30", "19:00", 513, "Passenger", 217.89);

 addTrain(2052, "Garib Rath", "Mumbai", "Delhi", "01:45", "09:45", 1612, "Local", 714.44); 

 addTrain(2053, "Duronto Express", "Jaipur", "Ahmedabad", "19:45", "23:45", 1611, "Express", 801.99);

addTrain(2054, "MEMU", "Mumbai", "Bangalore", "13:15", "12:00", 162, "Express", 591.55);
 
addTrain(2055, "Duronto Express", "Kolkata", "Pune", "21:15", "04:30", 1153, "Passenger", 1940.13);
 
addTrain(2056, "Intercity Express", "Jaipur", "Ahmedabad", "02:30", "20:15", 1047, "Local", 27.22);
 
addTrain(2057, "Suburban Local", "Mumbai", "Pune", "14:15", "10:00", 1050, "Express", 216.96);
 
addTrain(2058, "Mail Express", "Lucknow", "Delhi", "19:15", "11:30", 885, "Passenger", 1287.23);
 
addTrain(2059, "Jan Shatabdi", "Chennai", "Pune", "14:00", "08:00", 1900, "Local", 300.76);
 
addTrain(2060, "Rajdhani Express", "Ahmedabad", "Bangalore", "01:15", "07:30", 974, "Passenger", 1638.96);
 
addTrain(2061, "Garib Rath", "Hyderabad", "Kolkata", "12:45", "05:45", 1096, "Passenger", 1540.87);
 
addTrain(2062, "Rajdhani Express", "Pune", "Jaipur", "07:15", "07:00", 529, "Express", 1130.53);
 
addTrain(2063, "Rajdhani Express", "Kolkata", "Lucknow", "01:30", "16:00", 1113, "Express", 1197.56);
 
addTrain(2064, "Suburban Local", "Delhi", "Jaipur", "08:30", "14:15", 1173, "Express", 439.46);
 
addTrain(2065, "Duronto Express", "Bangalore", "Pune", "04:30", "21:00", 1013, "Passenger", 1120.25);
 
addTrain(2066, "Rajdhani Express", "Chennai", "Lucknow", "08:30", "09:15", 890, "Passenger", 190.23);

 addTrain(2067, "Superfast Express", "Delhi", "Mumbai", "21:45", "23:30", 738, "Express", 787.98);

  addTrain(2068, "Mail Express", "Ahmedabad", "Jaipur", "17:45", "04:45", 739, "Express", 1247.35); 

  addTrain(2069, "Shatabdi Express", "Chennai", "Lucknow", "10:45", "16:30", 1425, "Express", 420.81); 

  addTrain(2070, "Intercity Express", "Ahmedabad", "Mumbai", "01:30", "14:45", 197, "Express", 957.68);

addTrain(2071, "Rajdhani Express", "Lucknow", "Chennai", "10:00", "04:15", 846, "Express", 1487.77);
 
addTrain(2072, "Jan Shatabdi", "Bangalore", "Lucknow", "14:45", "19:15", 1612, "Express", 727.24);
 
addTrain(2073, "Mail Express", "Hyderabad", "Jaipur", "03:15", "14:30", 1652, "Express", 177.8);
 
addTrain(2074, "Mail Express", "Pune", "Jaipur", "04:00", "10:15", 450, "Passenger", 230.28);
 
addTrain(2075, "Duronto Express", "Ahmedabad", "Hyderabad", "11:00", "14:30", 1727, "Passenger", 754.29);
 
addTrain(2076, "Jan Shatabdi", "Mumbai", "Chennai", "00:15", "17:00", 1142, "Local", 1511.22);
 
addTrain(2077, "Superfast Express", "Chennai", "Delhi", "18:00", "09:00", 105, "Express", 80.52);
 
addTrain(2078, "Shatabdi Express", "Mumbai", "Chennai", "19:45", "22:00", 581, "Express", 1611.4);
 
addTrain(2079, "Rajdhani Express", "Lucknow", "Jaipur", "22:30", "15:45", 204, "Local", 180.49);
 
addTrain(2080, "Suburban Local", "Mumbai", "Lucknow", "20:15", "21:00", 789, "Express", 758.09);
 
addTrain(2081, "Intercity Express", "Bangalore", "Jaipur", "07:30", "08:45", 1836, "Passenger", 1425.98);
 
addTrain(2082, "Rajdhani Express", "Lucknow", "Kolkata", "00:15", "05:45", 432, "Passenger", 1889.06);

 addTrain(2083, "Duronto Express", "Bangalore", "Kolkata", "03:00", "07:15", 1655, "Passenger", 1355.09);

  addTrain(2084, "Mail Express", "Pune", "Hyderabad", "05:30", "10:00", 1782, "Local", 1478.18);
 
addTrain(2085, "Intercity Express", "Lucknow", "Hyderabad", "20:00", "08:00", 112, "Express", 1173.02);
 
addTrain(2086, "Superfast Express", "Chennai", "Bangalore", "07:30", "18:15", 96, "Passenger", 332.53);
 
addTrain(2087, "Rajdhani Express", "Ahmedabad", "Kolkata", "05:45", "06:15", 1628, "Local", 475.42);
 
addTrain(2088, "Garib Rath", "Kolkata", "Bangalore", "02:15", "05:15", 1607, "Local", 1214.48);
 
addTrain(2089, "Jan Shatabdi", "Jaipur", "Kolkata", "17:15", "21:00", 842, "Passenger", 1014.76);
 
addTrain(2090, "Rajdhani Express", "Jaipur", "Mumbai", "18:30", "12:15", 235, "Express", 1934.69);
 
addTrain(2091, "Garib Rath", "Hyderabad", "Kolkata", "10:00", "09:00", 1215, "Local", 1856.27);
 
addTrain(2092, "Garib Rath", "Pune", "Kolkata", "03:45", "09:15", 911, "Express", 1424.38);
 
addTrain(2093, "Rajdhani Express", "Pune", "Mumbai", "06:00", "02:45", 1281, "Local", 873.15);
 
addTrain(2094, "Garib Rath", "Kolkata", "Mumbai", "04:00", "01:00", 1254, "Express", 1662.06);
 
addTrain(2095, "Superfast Express", "Lucknow", "Hyderabad", "04:15", "21:45", 764, "Passenger", 1915.75);
 
addTrain(2096, "Intercity Express", "Mumbai", "Chennai", "20:00", "02:15", 499, "Passenger", 746.43);
 
addTrain(2097, "Shatabdi Express", "Jaipur", "Delhi", "05:15", "16:45", 1338, "Passenger", 1544.06);
 
addTrain(2098, "Shatabdi Express", "Chennai", "Hyderabad", "22:15", "02:45", 1023, "Express", 1961.62);
 
addTrain(2099, "Intercity Express", "Kolkata", "Pune", "02:15", "13:15", 262, "Local", 788.11);

 addTrain(2100, "Mail Express", "Ahmedabad", "Chennai", "12:30", "16:45", 805, "Express", 1046.28); 

 addTrain(2101, "Rajdhani" , "Jaipur", "Bangalore", "09:00", "00:45", 1232, "Local", 101.2); 

 addTrain(2102, "Garib Rath", "Ahmedabad", "Lucknow", "10:30", "18:00", 1362, "Passenger", 1257.56);
 
addTrain(2103, "Suburban Local", "Ahmedabad", "Bangalore", "05:15", "07:00", 1194, "Local", 1380.57);
 
addTrain(2104, "MEMU", "Delhi", "Jaipur", "04:30", "05:45", 174, "Passenger", 1832.41);
 
addTrain(2105, "Duronto Express", "Lucknow", "Jaipur", "16:30", "09:30", 1336, "Local", 1580.17);
 
addTrain(2106, "Superfast Express", "Lucknow", "Bangalore", "16:00", "22:30", 1657, "Local", 107.91);
 
addTrain(2107, "Shatabdi Express", "Chennai", "Bangalore", "18:00", "19:15", 204, "Local", 81.96);
 
addTrain(2108, "Garib Rath", "Bangalore", "Mumbai", "07:00", "20:15", 512, "Local", 1315.93);
 
addTrain(2109, "MEMU", "Hyderabad", "Kolkata", "07:45", "19:00", 431, "Express", 1575.6);
 
addTrain(2110, "Intercity Express", "Delhi", "Bangalore", "19:00", "12:15", 247, "Passenger", 93.23);
 
addTrain(2111, "Jan Shatabdi", "Lucknow", "Bangalore", "08:45", "07:45", 1920, "Passenger", 1126.8);
 
addTrain(2112, "Rajdhani Express", "Ahmedabad", "Bangalore", "16:30", "20:00", 679, "Local", 1038.84);
 
addTrain(2113, "Mail Express", "Chennai", "Pune", "03:45", "00:00", 1987, "Local", 1246.77);
 
addTrain(2114, "Mail Express", "Mumbai", "Kolkata", "18:15", "21:00", 1143, "Express", 864.5);
 
addTrain(2115, "MEMU", "Jaipur", "Delhi", "22:15", "22:00", 906, "Local", 574.84);
 
addTrain(2116, "Duronto Express", "Jaipur", "Mumbai", "02:00", "20:15", 424, "Express", 1062.14);
 
addTrain(2117, "MEMU", "Bangalore", "Ahmedabad", "14:30", "18:15", 1956, "Passenger", 1473.88);


 addTrain(2118, "MEMU", "Delhi", "Pune", "17:45", "15:15", 141, "Express", 1134.0);

  addTrain(2119, "Mail Express", "Mumbai", "Bangalore", "08:45", "00:45", 483, "Express", 1861.75);

addTrain(2120, "Intercity Express", "Jaipur", "Lucknow", "23:15", "09:30", 751, "Express", 1138.9);
 
addTrain(2121, "Shatabdi Express", "Chennai", "Bangalore", "10:00", "03:15", 1882, "Express", 29.01);
 
addTrain(2122, "Intercity Express", "Hyderabad", "Bangalore", "20:45", "07:45", 320, "Passenger", 792.98);
 
addTrain(2123, "Rajdhani Express", "Jaipur", "Lucknow", "11:00", "21:30", 94, "Express", 1476.3);
 
addTrain(2124, "MEMU", "Kolkata", "Chennai", "01:00", "18:45", 1148, "Express", 171.59);
 
addTrain(2125, "Rajdhani Express", "Mumbai", "Kolkata", "11:30", "09:00", 1054, "Local", 844.7);
 
addTrain(2126, "Garib Rath", "Kolkata", "Delhi", "07:45", "22:00", 417, "Express", 1082.47);
 
addTrain(2127, "MEMU", "Delhi", "Bangalore", "03:45", "16:45", 1703, "Local", 86.23);
 
addTrain(2128, "Garib Rath", "Mumbai", "Bangalore", "06:00", "13:30", 1121, "Local", 1396.08);
 
addTrain(2129, "Intercity Express", "Chennai", "Mumbai", "09:30", "00:00", 1773, "Passenger", 510.56);
 
addTrain(2130, "Rajdhani Express", "Chennai", "Hyderabad", "18:45", "01:00", 318, "Express", 320.11);
 
addTrain(2131, "Mail Express", "Ahmedabad", "Jaipur", "05:45", "07:45", 1551, "Express", 830.59);
 
addTrain(2132, "Shatabdi Express", "Chennai", "Bangalore", "10:45", "09:30", 1071, "Passenger", 1654.98);

 addTrain(2133, "MEMU", "Chennai", "Hyderabad", "19:45", "09:45", 1249, "Local", 1217.97); 


 addTrain(2134, "Shatabdi", "Chennai", "Jaipur", "00:00", "01:00", 85, "Passenger", 1917.65); 

 addTrain(2135, "Superfast Express", "Jaipur", "Pune", "20:45", "12:00", 1190, "Passenger", 1621.55);

 addTrain(2136, "Duronto Express", "Jaipur", "Kolkata", "08:45", "07:15", 268, "Express", 273.6);

addTrain(2137, "Shatabdi Express", "Delhi", "Bangalore", "23:15", "03:45", 383, "Local", 749.62);
 
addTrain(2138, "Duronto Express", "Chennai", "Pune", "12:15", "00:15", 1333, "Local", 679.38);
 
addTrain(2139, "Duronto Express", "Hyderabad", "Chennai", "13:15", "01:45", 345, "Local", 1208.68);
 
addTrain(2140, "Mail Express", "Ahmedabad", "Bangalore", "19:15", "17:30", 614, "Local", 1294.06);
 
addTrain(2141, "Superfast Express", "Jaipur", "Lucknow", "06:00", "17:15", 238, "Passenger", 272.17);
 
addTrain(2142, "MEMU", "Kolkata", "Bangalore", "12:15", "21:00", 1495, "Express", 921.03);
 
addTrain(2143, "Mail Express", "Pune", "Delhi", "08:45", "20:30", 1438, "Local", 1569.43);
 
addTrain(2144, "Duronto Express", "Chennai", "Lucknow", "16:30", "16:30", 1808, "Local", 815.84);
 
addTrain(2145, "Intercity Express", "Bangalore", "Kolkata", "10:45", "05:45", 1211, "Passenger", 1775.57);
 
addTrain(2146, "Suburban Local", "Bangalore", "Lucknow", "20:15", "09:30", 114, "Express", 1594.1);
 
addTrain(2147, "Suburban Local", "Ahmedabad", "Jaipur", "14:45", "13:30", 1906, "Passenger", 39.58);
 
addTrain(2148, "Garib Rath", "Lucknow", "Bangalore", "00:00", "16:30", 1611, "Local", 639.4);

 addTrain(2149, "Mail Express", "Delhi", "Lucknow", "03:30", "12:45", 1991, "Passenger", 277.65); 

 addTrain(2150, "Intercity Express", "Pune", "Hyderabad", "21:30", "10:30", 1711, "Local", 620.71);

  addTrain(2151, "Shatabdi Express", "Bangalore", "Hyderabad", "14:00", "00:15", 998, "Passenger", 1048.92); 

  addTrain(2152, "Rajdhani Express", "Bangalore", "Chennai", "07:00", "18:30", 1165, "Express", 1892.74);

addTrain(2153, "Mail Express", "Delhi", "Ahmedabad", "18:15", "12:30", 856, "Local", 496.8);

 
addTrain(2154, "Mail Express", "Bangalore", "Chennai", "14:00", "07:00", 1179, "Passenger", 1193.13);
 
addTrain(2155, "Duronto Express", "Kolkata", "Chennai", "12:00", "01:45", 219, "Passenger", 1612.27);
 
addTrain(2156, "MEMU", "Lucknow", "Kolkata", "12:15", "08:45", 1145, "Passenger", 1122.71);
 
addTrain(2157, "Superfast Express", "Bangalore", "Lucknow", "23:45", "12:15", 336, "Express", 138.17);
 
addTrain(2158, "Mail Express", "Ahmedabad", "Hyderabad", "03:00", "21:15", 1469, "Local", 1363.11);
 
addTrain(2159, "Duronto Express", "Mumbai", "Hyderabad", "17:45", "08:00", 434, "Local", 640.95);
 
addTrain(2160, "Suburban Local", "Pune", "Bangalore", "14:45", "13:00", 1593, "Local", 451.1);
 
addTrain(2161, "Mail Express", "Bangalore", "Kolkata", "03:45", "02:30", 929, "Local", 1224.03);
 
addTrain(2162, "Jan Shatabdi", "Lucknow", "Mumbai", "19:30", "06:45", 1388, "Local", 738.31);
 
addTrain(2163, "Mail Express", "Lucknow", "Mumbai", "05:45", "18:15", 257, "Passenger", 213.0);
 
addTrain(2164, "Jan Shatabdi", "Ahmedabad", "Kolkata", "08:45", "23:45", 152, "Express", 1460.2);
 
addTrain(2165, "Shatabdi Express", "Jaipur", "Hyderabad", "13:00", "06:00", 1213, "Local", 467.86); 

addTrain(2166, "Shatabdi Express", "Mumbai", "Lucknow", "21:30", "16:15", 1380, "Local", 1062.56); 

addTrain(2167, "Duronto", "Jaipur", "Chennai", "06:45", "16:00", 749, "Express", 1590.37);

 addTrain(2168, "Duronto Express", "Jaipur", "Lucknow", "22:15", "14:30", 1292, "Express", 380.78); 

 addTrain(2169, "Superfast Express", "Lucknow", "Ahmedabad", "05:00", "22:15", 1153, "Passenger", 711.79);

addTrain(2170, "Rajdhani Express", "Ahmedabad", "Mumbai", "22:45", "11:00", 1841, "Express", 1790.41);
 

addTrain(2171, "Duronto Express", "Chennai", "Lucknow", "22:45", "19:00", 1626, "Express", 1410.03);
 
addTrain(2172, "Duronto Express", "Hyderabad", "Pune", "11:00", "08:45", 658, "Local", 219.43);
 
addTrain(2173, "Suburban Local", "Mumbai", "Ahmedabad", "17:45", "14:45", 1403, "Passenger", 930.72);
 
addTrain(2174, "Mail Express", "Lucknow", "Jaipur", "03:45", "14:00", 1250, "Passenger", 705.38);
 
addTrain(2175, "Superfast Express", "Lucknow", "Kolkata", "03:15", "09:00", 1130, "Passenger", 1977.78);
 
addTrain(2176, "Superfast Express", "Jaipur", "Kolkata", "15:30", "07:45", 1072, "Local", 1621.88);
 
addTrain(2177, "Duronto Express", "Pune", "Lucknow", "16:45", "17:30", 1537, "Passenger", 781.66);
 
addTrain(2178, "Rajdhani Express", "Lucknow", "Mumbai", "10:45", "09:45", 517, "Local", 1704.08);
 
addTrain(2179, "Duronto Express", "Pune", "Mumbai", "09:45", "06:30", 381, "Local", 1948.35);
 
addTrain(2180, "Shatabdi Express", "Mumbai", "Ahmedabad", "09:30", "07:45", 1926, "Express", 285.51);
 
addTrain(2181, "Intercity Express", "Bangalore", "Lucknow", "00:00", "06:45", 719, "Local", 1705.57);

 addTrain(2182, "Suburban Local", "Lucknow", "Kolkata", "10:15", "23:30", 1308, "Local", 446.21);

  addTrain(2183, "Suburban Local", "Kolkata", "Hyderabad", "12:00", "05:15", 91, "Express", 1011.08);
 
addTrain(2184, "Intercity Express", "Lucknow", "Kolkata", "18:15", "20:30", 1801, "Express", 1126.76);

 addTrain(2185, "Superfast Express", "Delhi", "Mumbai", "03:15", "16:15", 816, "Express", 921.39);

addTrain(2186, "Jan Shatabdi", "Mumbai", "Ahmedabad", "15:30", "00:45", 607, "Passenger", 1803.99);
 
addTrain(2187, "MEMU", "Chennai", "Pune", "07:45", "09:30", 1516, "Passenger", 1320.04);
 
addTrain(2188, "Shatabdi Express", "Jaipur", "Pune", "12:15", "18:00", 572, "Local", 1533.18);
 
addTrain(2189, "Rajdhani Express", "Pune", "Chennai", "02:00", "00:30", 104, "Local", 1086.73);
 
addTrain(2190, "MEMU", "Chennai", "Bangalore", "19:00", "21:15", 260, "Local", 400.19);
 
addTrain(2191, "Intercity Express", "Jaipur", "Mumbai", "03:30", "08:45", 1877, "Local", 1433.36);
 
addTrain(2192, "Shatabdi Express", "Bangalore", "Jaipur", "17:45", "15:15", 1812, "Local", 784.87);
 
addTrain(2193, "Suburban Local", "Bangalore", "Chennai", "20:15", "00:45", 1384, "Local", 1160.02);
 
addTrain(2194, "Suburban Local", "Delhi", "Jaipur", "00:30", "22:15", 860, "Local", 932.42);
 
addTrain(2195, "Mail Express", "Mumbai", "Delhi", "09:45", "02:00", 1365, "Passenger", 694.76);
 
addTrain(2196, "Jan Shatabdi", "Delhi", "Chennai", "10:45", "07:30", 1939, "Express", 387.49);
 
addTrain(2197, "Mail Express", "Hyderabad", "Delhi", "06:15", "04:00", 467, "Passenger", 1081.9);
 
addTrain(2198, "Jan Shatabdi", "Lucknow", "Jaipur", "08:45", "12:15", 1703, "Express", 654.52);
 
addTrain(2199, "MEMU", "Mumbai", "Kolkata", "08:30", "21:15", 1689, "Express", 1165.3);
 
addTrain(2200, "Mail Express", "Hyderabad", "Pune", "14:30", "04:30", 1244, "Passenger", 461.12); 

addTrain(2201, "Duronto Express", "Chennai", "Mumbai", "07:15", "03:15", 20, "Local", 172.82); 

addTrain(2202, "Duronto Express", "Lucknow", "Bangalore", "04:15", "23:45", 1237, "Local", 740.61);

addTrain(2203, "Mail Express", "Jaipur", "Ahmedabad", "07:15", "16:15", 1115, "Passenger", 68.25);
 
addTrain(2204, "Jan Shatabdi", "Chennai", "Bangalore", "07:45", "13:00", 962, "Express", 1206.22);
 
addTrain(2205, "Superfast Express", "Kolkata", "Pune", "13:30", "09:30", 544, "Local", 274.5);
 
addTrain(2206, "Rajdhani Express", "Lucknow", "Jaipur", "13:30", "05:00", 524, "Local", 1122.6);
 
addTrain(2207, "Duronto Express", "Kolkata", "Lucknow", "06:15", "20:30", 480, "Passenger", 1579.72);
 
addTrain(2208, "Duronto Express", "Chennai", "Jaipur", "07:00", "14:30", 686, "Passenger", 1214.33);
 
addTrain(2209, "Mail Express", "Bangalore", "Hyderabad", "06:00", "14:45", 1491, "Express", 948.13);
 
addTrain(2210, "Rajdhani Express", "Pune", "Delhi", "11:45", "20:00", 1579, "Express", 1237.06);
 
addTrain(2211, "Superfast Express", "Bangalore", "Pune", "21:45", "20:15", 1132, "Local", 334.75);
 
addTrain(2212, "Shatabdi Express", "Kolkata", "Hyderabad", "10:00", "23:00", 1651, "Local", 1969.06);
 
addTrain(2213, "Duronto Express", "Lucknow", "Hyderabad", "04:15", "12:45", 1791, "Express", 1411.51);
 
addTrain(2214, "Garib Rath", "Hyderabad", "Jaipur", "12:00", "12:15", 1969, "Local", 1616.79); 

addTrain(2215, "MEMU", "Pune", "Hyderabad", "06:30", "18:30", 1795, "Express", 553.94);

 addTrain(2216, "Rajdhani", "Jaipur", "Lucknow", "15:30", "16:30", 1481, "Local", 1981.97);

  addTrain(2217, "MEMU", "Bangalore", "Kolkata", "23:00", "06:45", 889, "Passenger", 1144.3); 

  addTrain(2218, "Rajdhani Express", "Lucknow", "Bangalore", "01:15", "22:00", 1301, "Passenger", 606.16);

addTrain(2219, "Superfast Express", "Lucknow", "Mumbai", "20:15", "16:00", 302, "Local", 190.35);
 
addTrain(2220, "Duronto Express", "Kolkata", "Lucknow", "07:30", "19:45", 1827, "Express", 279.21);
 
addTrain(2221, "Intercity Express", "Chennai", "Hyderabad", "07:45", "07:45", 728, "Express", 110.82);
 
addTrain(2222, "MEMU", "Jaipur", "Mumbai", "07:00", "14:15", 1160, "Express", 640.46);
 
addTrain(2223, "Jan Shatabdi", "Bangalore", "Delhi", "09:15", "22:30", 692, "Express", 545.87);
 
addTrain(2224, "Duronto Express", "Jaipur", "Mumbai", "18:00", "16:30", 239, "Passenger", 452.58);
 
addTrain(2225, "Suburban Local", "Lucknow", "Chennai", "00:00", "06:45", 484, "Local", 1935.35);
 
addTrain(2226, "Mail Express", "Bangalore", "Kolkata", "13:15", "03:30", 44, "Local", 372.26);
 
addTrain(2227, "Suburban Local", "Lucknow", "Kolkata", "18:00", "20:30", 1085, "Passenger", 187.69);
 
addTrain(2228, "Garib Rath", "Ahmedabad", "Delhi", "15:15", "14:45", 542, "Local", 1909.34);
 
addTrain(2229, "Suburban Local", "Bangalore", "Pune", "13:15", "02:00", 1165, "Express", 1784.83);
 
addTrain(2230, "Mail Express", "Kolkata", "Ahmedabad", "03:45", "06:00", 56, "Express", 1996.4);
 
addTrain(2231, "Intercity Express", "Pune", "Chennai", "04:45", "13:15", 77, "Local", 27.03);

 addTrain(2232, "Intercity Express", "Bangalore", "Mumbai", "15:00", "02:15", 1255, "Express", 1093.43);

  addTrain(2233, "Shatabdi Express", "Jaipur", "Bangalore", "18:00", "23:45", 1484, "Local", 1093.92);

   addTrain(2234, "Garib Rath", "Bangalore", "Lucknow", "20:00", "13:00", 217, "Express", 756.83);

    addTrain(2235, "Superfast Express", "Delhi", "Kolkata", "11:45", "21:45", 1148, "Express", 1693.65);

addTrain(2236, "Shatabdi Express", "Mumbai", "Hyderabad", "08:45", "03:00", 799, "Local", 1965.6);
 
addTrain(2237, "Mail Express", "Lucknow", "Chennai", "17:15", "02:15", 428, "Express", 1761.2);
 
addTrain(2238, "Jan Shatabdi", "Bangalore", "Chennai", "02:30", "21:15", 323, "Passenger", 1681.73);
 
addTrain(2239, "Duronto Express", "Chennai", "Mumbai", "15:30", "22:30", 514, "Express", 973.61);
 
addTrain(2240, "Mail Express", "Hyderabad", "Ahmedabad", "05:30", "03:15", 1175, "Local", 1807.02);
 
addTrain(2241, "MEMU", "Lucknow", "Jaipur", "17:45", "04:00", 336, "Passenger", 1078.19);
 
addTrain(2242, "Suburban Local", "Delhi", "Chennai", "00:00", "05:00", 1934, "Express", 928.7);
 
addTrain(2243, "Jan Shatabdi", "Ahmedabad", "Kolkata", "12:30", "07:30", 786, "Local", 1105.51);
 
addTrain(2244, "Intercity Express", "Lucknow", "Pune", "13:30", "19:30", 1508, "Passenger", 1674.77);
 
addTrain(2245, "Shatabdi Express", "Delhi", "Lucknow", "17:30", "20:30", 1965, "Local", 1396.51);
 
addTrain(2246, "Suburban Local", "Kolkata", "Hyderabad", "10:45", "18:30", 1006, "Passenger", 1270.46);
 
addTrain(2247, "Mail Express", "Jaipur", "Mumbai", "04:45", "01:30", 1099, "Passenger", 1358.32);

 addTrain(2248, "Mail Express", "Ahmedabad", "Lucknow", "13:15", "14:45", 166, "Express", 702.67); 

 addTrain(2249, "Duronto", "Chennai", "Ahmedabad", "04:45", "01:15", 596, "Express", 1790.05);

  addTrain(2250, "Intercity Express", "Hyderabad", "Pune", "11:00", "12:45", 1589, "Passenger", 291.8); 

  addTrain(2251, "Duronto Express", "Jaipur", "Lucknow", "17:15", "15:00", 861, "Passenger", 1815.09);

addTrain(2252, "Shatabdi Express", "Kolkata", "Bangalore", "11:45", "03:45", 1495, "Express", 896.01);
 
addTrain(2253, "Shatabdi Express", "Bangalore", "Lucknow", "18:30", "04:00", 168, "Express", 1861.53);
 
addTrain(2254, "Intercity Express", "Mumbai", "Lucknow", "06:00", "16:15", 597, "Express", 1787.46);
 
addTrain(2255, "Jan Shatabdi", "Ahmedabad", "Jaipur", "23:45", "21:30", 1496, "Local", 1836.69);
 
addTrain(2256, "Garib Rath", "Jaipur", "Lucknow", "23:30", "01:30", 195, "Express", 1772.45);
 
addTrain(2257, "Intercity Express", "Bangalore", "Chennai", "08:45", "13:30", 408, "Passenger", 1716.48);
 
addTrain(2258, "Shatabdi Express", "Ahmedabad", "Mumbai", "13:15", "13:30", 482, "Express", 1795.15);
 
addTrain(2259, "Mail Express", "Kolkata", "Mumbai", "18:15", "23:15", 1733, "Local", 1129.47);
 
addTrain(2260, "Duronto Express", "Jaipur", "Mumbai", "12:45", "15:15", 1901, "Express", 1568.09);
 
addTrain(2261, "Rajdhani Express", "Hyderabad", "Bangalore", "03:00", "19:30", 1095, "Passenger", 1046.71);
 
addTrain(2262, "Jan Shatabdi", "Mumbai", "Ahmedabad", "10:00", "17:45", 988, "Express", 1435.37);
 
addTrain(2263, "Rajdhani Express", "Pune", "Bangalore", "09:15", "21:45", 289, "Local", 1833.89);
 
addTrain(2264, "MEMU", "Bangalore", "Pune", "23:30", "02:15", 1567, "Local", 1684.3);

 addTrain(2265, "MEMU", "Mumbai", "Ahmedabad", "00:00", "12:45", 678, "Local", 1026.46); 

 addTrain(2266, "Shatabdi Express", "Lucknow", "Pune", "11:30", "15:30", 809, "Passenger", 762.67); 

 addTrain(2267, "Rajdhani Express", "Ahmedabad", "Kolkata", "16:45", "16:45", 1377, "Passenger", 491.02); 

 addTrain(2268, "Duronto Express", "Mumbai", "Jaipur", "11:30", "10:45", 1649, "Local", 453.42);

addTrain(2269, "Rajdhani Express", "Lucknow", "Chennai", "17:45", "09:30", 943, "Local", 1830.77);
 
addTrain(2270, "MEMU", "Mumbai", "Ahmedabad", "10:30", "04:45", 607, "Express", 1756.55);
 
addTrain(2271, "Shatabdi Express", "Lucknow", "Kolkata", "06:00", "23:45", 175, "Express", 587.0);
 
addTrain(2272, "Garib Rath", "Jaipur", "Ahmedabad", "08:15", "18:15", 1068, "Passenger", 629.72);
 
addTrain(2273, "Mail Express", "Pune", "Jaipur", "09:00", "01:45", 1580, "Local", 667.01);
 
addTrain(2274, "Rajdhani Express", "Chennai", "Lucknow", "22:15", "23:15", 516, "Express", 331.14);
 
addTrain(2275, "Jan Shatabdi", "Jaipur", "Mumbai", "10:45", "14:00", 567, "Express", 1909.62);
 
addTrain(2276, "Jan Shatabdi", "Bangalore", "Mumbai", "14:45", "17:15", 126, "Passenger", 567.29);
 
addTrain(2277, "Mail Express", "Ahmedabad", "Mumbai", "21:30", "22:30", 1326, "Express", 121.16);
 
addTrain(2278, "Duronto Express", "Hyderabad", "Bangalore", "00:30", "21:45", 1051, "Passenger", 1027.08);
 
addTrain(2279, "Duronto Express", "Pune", "Hyderabad", "20:30", "17:00", 1593, "Local", 1511.16);
 
addTrain(2280, "Jan Shatabdi", "Hyderabad", "Kolkata", "14:00", "12:15", 1033, "Local", 37.94);

 addTrain(2281, "Shatabdi Express", "Mumbai", "Pune", "15:00", "06:30", 609, "Passenger", 372.53);

  addTrain(2282, "Shatabdi", "Jaipur", "Lucknow", "07:00", "08:15", 1295, "Local", 634.89);

   addTrain(2283, "Jan Shatabdi", "Kolkata", "Lucknow", "00:45", "17:30", 1120, "Local", 1541.6); 

   addTrain(2284, "Duronto Express", "Mumbai", "Pune", "15:15", "05:15", 1429, "Local", 597.43);

addTrain(2285, "Garib Rath", "Jaipur", "Kolkata", "02:00", "06:30", 409, "Local", 488.94);
 
addTrain(2286, "Superfast Express", "Hyderabad", "Chennai", "14:45", "11:45", 1866, "Local", 1553.8);
 
addTrain(2287, "Superfast Express", "Pune", "Jaipur", "03:45", "11:15", 1016, "Passenger", 660.86);
 
addTrain(2288, "Superfast Express", "Pune", "Ahmedabad", "01:00", "11:15", 1674, "Local", 1735.09);
 
addTrain(2289, "Jan Shatabdi", "Hyderabad", "Kolkata", "12:15", "18:45", 179, "Local", 1934.02);
 
addTrain(2290, "Mail Express", "Jaipur", "Bangalore", "09:45", "16:30", 1301, "Express", 494.16);
 
addTrain(2291, "Rajdhani Express", "Lucknow", "Bangalore", "04:30", "22:00", 643, "Local", 598.18);
 
addTrain(2292, "Duronto Express", "Bangalore", "Jaipur", "02:15", "04:30", 317, "Passenger", 1723.93);
 
addTrain(2293, "Superfast Express", "Kolkata", "Hyderabad", "05:00", "03:00", 654, "Express", 20.93);
 
addTrain(2294, "MEMU", "Chennai", "Ahmedabad", "08:30", "11:00", 1220, "Passenger", 1011.27);
 
addTrain(2295, "Mail Express", "Delhi", "Bangalore", "23:30", "06:00", 731, "Local", 991.86);
 
addTrain(2296, "Jan Shatabdi", "Lucknow", "Delhi", "14:15", "08:00", 339, "Express", 1403.5);
 
addTrain(2297, "Garib Rath", "Ahmedabad", "Mumbai", "00:00", "18:30", 611, "Express", 1968.57); 

addTrain(2298, "Jan Shatabdi", "Mumbai", "Delhi", "11:30", "16:00", 1956, "Passenger", 1899.6); 

addTrain(2299, "Jan Shatabdi", "Pune", "Chennai", "05:15", "17:30", 293, "Passenger", 1302.01);
 
addTrain(2300, "Jan Shatabdi", "Ahmedabad", "Jaipur", "13:45", "13:30", 1633, "Local", 1938.8); 

addTrain(2301, "Suburban Local", "Pune", "Bangalore", "04:30", "21:15", 1175, "Express", 1096.58);

addTrain(2302, "Intercity Express", "Mumbai", "Delhi", "05:30", "12:15", 1535, "Passenger", 690.18);
 
addTrain(2303, "Garib Rath", "Hyderabad", "Lucknow", "01:45", "01:30", 32, "Local", 1572.7);
 
addTrain(2304, "Rajdhani Express", "Lucknow", "Chennai", "06:15", "13:30", 655, "Passenger", 1702.65);
 
addTrain(2305, "MEMU", "Ahmedabad", "Mumbai", "14:00", "12:45", 22, "Local", 727.56);
 
addTrain(2306, "Rajdhani Express", "Hyderabad", "Chennai", "18:45", "15:45", 1935, "Local", 1633.16);
 
addTrain(2307, "Duronto Express", "Jaipur", "Pune", "02:15", "18:30", 1992, "Passenger", 1333.18);
 
addTrain(2308, "Suburban Local", "Lucknow", "Delhi", "20:45", "00:00", 251, "Passenger", 545.03);
 
addTrain(2309, "Intercity Express", "Lucknow", "Delhi", "00:00", "06:15", 1745, "Express", 1144.97);
 
addTrain(2310, "Jan Shatabdi", "Hyderabad", "Ahmedabad", "01:00", "02:15", 633, "Passenger", 122.95);
 
addTrain(2311, "Rajdhani Express", "Lucknow", "Pune", "22:15", "04:00", 530, "Local", 425.67);
 
addTrain(2312, "Rajdhani Express", "Lucknow", "Chennai", "18:00", "04:30", 1679, "Local", 100.61);
 
addTrain(2313, "Rajdhani Express", "Mumbai", "Kolkata", "08:00", "01:00", 1787, "Local", 430.93); 

addTrain(2314, "Garib Rath", "Bangalore", "Jaipur", "11:45", "20:15", 1706, "Passenger", 945.06); 

addTrain(2315, "Mail Express", "Ahmedabad", "Chennai", "20:45", "10:15", 361, "Express", 895.96);

 addTrain(2316, "Intercity Express", "Pune", "Bangalore", "19:30", "09:30", 594, "Express", 317.91); 

 addTrain(2317, "Duronto Express", "Ahmedabad", "Kolkata", "02:15", "23:15", 1030, "Local", 1235.48);

addTrain(2318, "Garib Rath", "Hyderabad", "Lucknow", "21:00", "17:00", 1600, "Passenger", 657.16);
 
addTrain(2319, "Duronto Express", "Kolkata", "Chennai", "08:30", "22:45", 213, "Passenger", 1041.6);
 
addTrain(2320, "Mail Express", "Pune", "Chennai", "04:15", "19:45", 1860, "Express", 1696.0);
 
addTrain(2321, "Jan Shatabdi", "Delhi", "Jaipur", "09:30", "20:30", 938, "Passenger", 187.22);
 
addTrain(2322, "Rajdhani Express", "Lucknow", "Ahmedabad", "01:00", "23:45", 1541, "Local", 22.22);
 
addTrain(2323, "MEMU", "Hyderabad", "Mumbai", "23:00", "14:15", 682, "Passenger", 216.27);
 
addTrain(2324, "Superfast Express", "Chennai", "Pune", "18:15", "03:15", 436, "Local", 1782.65);
 
addTrain(2325, "Garib Rath", "Chennai", "Ahmedabad", "00:30", "10:00", 699, "Local", 1912.88);
 
addTrain(2326, "Superfast Express", "Kolkata", "Delhi", "20:45", "08:00", 129, "Local", 1101.06);
 
addTrain(2327, "Garib Rath", "Chennai", "Bangalore", "00:00", "09:45", 1308, "Passenger", 993.5);
 
addTrain(2328, "Rajdhani Express", "Ahmedabad", "Jaipur", "23:00", "23:15", 328, "Local", 1269.71);
 
addTrain(2329, "Superfast Express", "Hyderabad", "Chennai", "18:00", "23:15", 1646, "Local", 836.82);
 
addTrain(2330, "Superfast Express", "Mumbai", "Jaipur", "10:45", "15:15", 1594, "Express", 1081.37); 

addTrain(2331, "Rajdhani Express", "Ahmedabad", "Bangalore", "22:45", "13:45", 1983, "Passenger", 797.89); 

addTrain(2332, "Suburban Local", "Mumbai", "Jaipur", "22:15", "01:30", 865, "Local", 544.3);

addTrain(2333, "Superfast Express", "Lucknow", "Mumbai", "19:15", "07:30", 1099, "Passenger", 1520.6); 

addTrain(2334, "Duronto Express", "Pune", "Hyderabad", "17:45", "22:15", 1005, "Local", 624.87);

addTrain(2335, "Garib Rath", "Ahmedabad", "Delhi", "06:45", "20:00", 1992, "Express", 681.32);
 
addTrain(2336, "Superfast Express", "Pune", "Ahmedabad", "23:30", "10:00", 1605, "Passenger", 646.36);
 
addTrain(2337, "Intercity Express", "Mumbai", "Pune", "08:45", "20:15", 23, "Passenger", 1838.33);
 
addTrain(2338, "MEMU", "Pune", "Delhi", "06:15", "04:45", 1999, "Local", 1421.42);
 
addTrain(2339, "Jan Shatabdi", "Lucknow", "Bangalore", "05:30", "04:15", 1351, "Express", 1397.15);
 
addTrain(2340, "Mail Express", "Delhi", "Lucknow", "07:45", "10:00", 1971, "Express", 495.39);
 
addTrain(2341, "Suburban Local", "Mumbai", "Bangalore", "06:00", "09:45", 921, "Local", 1878.53);
 
addTrain(2342, "Rajdhani Express", "Mumbai", "Hyderabad", "12:30", "21:00", 1319, "Local", 352.51);
 
addTrain(2343, "Superfast Express", "Chennai", "Lucknow", "02:45", "15:15", 748, "Passenger", 1561.63);
 
addTrain(2344, "Garib Rath", "Jaipur", "Mumbai", "18:15", "10:00", 506, "Express", 303.48);
 
addTrain(2345, "Rajdhani Express", "Lucknow", "Chennai", "13:00", "03:00", 1586, "Passenger", 269.11);
 
addTrain(2346, "Intercity Express", "Chennai", "Delhi", "03:00", "19:15", 183, "Local", 961.51); 

addTrain(2347, "Intercity Express", "Kolkata", "Jaipur", "13:00", "20:00", 1729, "Express", 1732.83); 

addTrain(2348, "Shatabdi Express", "Chennai", "Mumbai", "21:45", "12:30", 1912, "Express", 843.42); 

addTrain(2349, "Garib Rath", "Hyderabad", "Bangalore", "17:15", "02:15", 1687, "Passenger", 1123.46);

addTrain(2350, "Duronto Express", "Chennai", "Jaipur", "13:15", "10:00", 376, "Passenger", 1210.33);

addTrain(2351, "Rajdhani Express", "Jaipur", "Delhi", "14:45", "02:15", 1127, "Express", 1126.58);
 
addTrain(2352, "Rajdhani Express", "Mumbai", "Jaipur", "15:45", "20:30", 1627, "Express", 1215.12);
 
addTrain(2353, "Mail Express", "Jaipur", "Ahmedabad", "17:45", "06:45", 883, "Local", 894.42);
 
addTrain(2354, "Garib Rath", "Ahmedabad", "Chennai", "06:00", "17:30", 1446, "Express", 1882.72);
 
addTrain(2355, "Suburban Local", "Kolkata", "Ahmedabad", "18:00", "03:30", 1963, "Local", 1117.02);
 
addTrain(2356, "Jan Shatabdi", "Jaipur", "Pune", "23:00", "09:30", 1910, "Express", 24.34);
 
addTrain(2357, "Intercity Express", "Hyderabad", "Pune", "06:00", "05:15", 238, "Local", 1139.66);
 
addTrain(2358, "Shatabdi Express", "Bangalore", "Mumbai", "20:45", "17:15", 319, "Express", 625.09);
 
addTrain(2359, "Duronto Express", "Delhi", "Kolkata", "04:00", "06:30", 434, "Passenger", 1104.03);
 
addTrain(2360, "Garib Rath", "Mumbai", "Lucknow", "16:30", "16:15", 225, "Passenger", 1126.33);
 
addTrain(2361, "Suburban Local", "Chennai", "Delhi", "05:30", "06:15", 1878, "Passenger", 242.86);
 
addTrain(2362, "Jan Shatabdi", "Jaipur", "Bangalore", "23:00", "01:30", 1387, "Express", 1216.85);
 
addTrain(2363, "Suburban Local", "Pune", "Ahmedabad", "23:30", "21:30", 123, "Express", 1267.26); 

 addTrain(2364, "Suburban Local", "Chennai", "Ahmedabad", "19:45", "03:15", 118, "Local", 1557.66);

  addTrain(2365, "Shatabdi Express", "Delhi", "Mumbai", "12:00", "21:45", 463, "Express", 1137.37);

   addTrain(2366, "Shatabdi Express", "Jaipur", "Pune", "08:30", "20:15", 140, "Express", 273.19); 

   addTrain(2367, "Duronto Express", "Kolkata", "Jaipur", "18:30", "20:30", 1787, "Passenger", 1939.02);

addTrain(2368, "Rajdhani Express", "Delhi", "Chennai", "01:00", "10:30", 1851, "Local", 1546.92);
 
addTrain(2369, "Intercity Express", "Bangalore", "Ahmedabad", "07:30", "08:00", 1811, "Local", 1379.4);
 
addTrain(2370, "Jan Shatabdi", "Kolkata", "Pune", "16:30", "00:45", 776, "Express", 852.37);
 
addTrain(2371, "Superfast Express", "Lucknow", "Kolkata", "16:15", "01:00", 167, "Express", 851.9);
 
addTrain(2372, "Shatabdi Express", "Kolkata", "Bangalore", "04:15", "10:15", 846, "Express", 880.82);
 
addTrain(2373, "Jan Shatabdi", "Jaipur", "Bangalore", "09:30", "13:15", 1007, "Local", 52.92);
 
addTrain(2374, "Duronto Express", "Delhi", "Bangalore", "15:00", "20:00", 771, "Passenger", 1039.35);
 
addTrain(2375, "Intercity Express", "Jaipur", "Hyderabad", "23:30", "07:30", 73, "Local", 414.65);
 
addTrain(2376, "Shatabdi Express", "Pune", "Delhi", "08:45", "15:45", 846, "Passenger", 508.07);
 
addTrain(2377, "Superfast Express", "Lucknow", "Ahmedabad", "17:00", "16:00", 225, "Express", 1361.77);
 
addTrain(2378, "Duronto Express", "Mumbai", "Chennai", "21:15", "00:15", 1972, "Local", 1696.66);
 
addTrain(2379, "Duronto Express", "Jaipur", "Ahmedabad", "02:15", "02:30", 1893, "Express", 1552.85);

 addTrain(2380, "MEMU", "Lucknow", "Hyderabad", "01:30", "07:15", 76, "Express", 1132.0); 

 addTrain(2381, "Jan Shatabdi", "Delhi", "Mumbai", "02:30", "20:00", 264, "Passenger", 841.42);

  addTrain(2382, "Duronto Express", "Pune", "Mumbai", "01:45", "02:30", 1604, "Express", 1902.02);

   addTrain(2383, "Superfast Express", "Hyderabad", "Mumbai", "08:15", "03:00", 1111, "Passenger", 891.06);

addTrain(2384, "Superfast Express", "Lucknow", "Mumbai", "00:00", "16:15", 162, "Passenger", 1154.44);
 
addTrain(2385, "Shatabdi Express", "Chennai", "Mumbai", "15:30", "10:00", 536, "Local", 986.81);
 
addTrain(2386, "MEMU", "Jaipur", "Chennai", "18:15", "02:45", 558, "Local", 1772.81);
 
addTrain(2387, "Suburban Local", "Hyderabad", "Bangalore", "18:00", "18:00", 516, "Local", 195.94);
 
addTrain(2388, "Rajdhani Express", "Kolkata", "Ahmedabad", "06:15", "05:15", 443, "Local", 1662.5);
 
addTrain(2389, "Intercity Express", "Pune", "Jaipur", "05:45", "12:30", 132, "Passenger", 838.05);
 
addTrain(2390, "Rajdhani Express", "Pune", "Bangalore", "06:30", "06:30", 906, "Express", 412.44);
 
addTrain(2391, "Jan Shatabdi", "Hyderabad", "Pune", "00:30", "05:45", 992, "Passenger", 107.73);
 
addTrain(2392, "Duronto Express", "Lucknow", "Jaipur", "07:15", "06:30", 603, "Passenger", 437.1);
 
addTrain(2393, "MEMU", "Delhi", "Mumbai", "04:30", "20:30", 65, "Local", 281.1);
 
addTrain(2394, "Intercity Express", "Pune", "Jaipur", "05:30", "01:30", 543, "Local", 1888.5);
 
addTrain(2395, "Mail Express", "Pune", "Kolkata", "10:00", "23:15", 715, "Local", 760.54);
 
addTrain(2396, "Rajdhani Express", "Jaipur", "Ahmedabad", "10:45", "21:00", 667, "Local", 1254.17); 

addTrain(2397, "Superfast Express", "Pune", "Chennai", "19:15", "21:00", 557, "Express", 659.38);

 addTrain(2398, "Duronto Express", "Bangalore", "Chennai", "12:00", "07:30", 1520, "Passenger", 161.9); 

 addTrain(2399, "Suburban Local", "Delhi", "Mumbai", "04:15", "16:15", 59, "Passenger", 1961.04);

  addTrain(2400, "Duronto Express", "Kolkata", "Jaipur", "18:30", "16:00", 1675, "Express", 50.2);

addTrain(2401, "Suburban Local", "Kolkata", "Jaipur", "03:15", "22:15", 1441, "Passenger", 1837.39);
 
addTrain(2402, "MEMU", "Chennai", "Hyderabad", "05:00", "14:45", 766, "Passenger", 1223.7);
 
addTrain(2403, "Mail Express", "Bangalore", "Hyderabad", "12:45", "15:00", 1463, "Express", 1590.99);
 
addTrain(2404, "Intercity Express", "Bangalore", "Delhi", "09:15", "04:15", 439, "Passenger", 1054.13);
 
addTrain(2405, "Mail Express", "Bangalore", "Delhi", "22:30", "15:30", 1298, "Local", 1921.97);
 
addTrain(2406, "Intercity Express", "Delhi", "Ahmedabad", "16:00", "02:00", 1273, "Passenger", 1681.87);
 
addTrain(2407, "Mail Express", "Delhi", "Lucknow", "10:15", "19:15", 1927, "Express", 372.29);
 
addTrain(2408, "Jan Shatabdi", "Kolkata", "Bangalore", "10:15", "18:45", 1929, "Passenger", 736.83);
 
addTrain(2409, "Superfast Express", "Lucknow", "Hyderabad", "15:15", "14:30", 188, "Passenger", 594.22);
 
addTrain(2410, "Garib Rath", "Lucknow", "Jaipur", "20:30", "20:15", 281, "Local", 1469.91);
 
addTrain(2411, "Superfast Express", "Lucknow", "Delhi", "21:15", "01:00", 403, "Express", 1741.87);
 
addTrain(2412, "Suburban Local", "Hyderabad", "Pune", "12:30", "08:45", 1538, "Express", 16.49); 

addTrain(2413, "Garib Rath", "Hyderabad", "Kolkata", "17:00", "17:30", 1912, "Passenger", 329.31); 

addTrain(2414, "Jan Shatabdi", "Chennai", "Pune", "01:15", "23:15", 1576, "Passenger", 1779.97); 

addTrain(2415, "Garib Rath", "Kolkata", "Ahmedabad", "01:00", "16:30", 1244, "Local", 1502.42); 

addTrain(2416, "Intercity Express", "Pune", "Jaipur", "08:45", "10:45", 366, "Passenger", 597.6);

addTrain(2417, "Superfast Express", "Bangalore", "Delhi", "09:15", "10:30", 581, "Local", 207.31);
 
addTrain(2418, "Intercity Express", "Mumbai", "Kolkata", "02:00", "21:45", 442, "Express", 1460.0);
 
addTrain(2419, "Suburban Local", "Chennai", "Bangalore", "12:30", "10:30", 1532, "Local", 1069.33);
 
addTrain(2420, "Superfast Express", "Jaipur", "Chennai", "16:15", "20:15", 1477, "Passenger", 1240.66);
 
addTrain(2421, "Garib Rath", "Kolkata", "Mumbai", "01:30", "08:45", 1597, "Express", 497.61);
 
addTrain(2422, "Shatabdi Express", "Ahmedabad", "Kolkata", "10:00", "10:45", 1468, "Express", 628.8);
 
addTrain(2423, "Superfast Express", "Bangalore", "Hyderabad", "15:00", "00:45", 169, "Passenger", 1538.22);
 
addTrain(2424, "Jan Shatabdi", "Kolkata", "Lucknow", "18:15", "19:30", 1217, "Local", 239.96);
 
addTrain(2425, "Garib Rath", "Mumbai", "Delhi", "13:30", "19:15", 1886, "Express", 1606.64);
 
addTrain(2426, "Jan Shatabdi", "Kolkata", "Jaipur", "21:30", "08:45", 1112, "Express", 453.11);
 
addTrain(2427, "Rajdhani Express", "Jaipur", "Delhi", "11:00", "03:45", 115, "Local", 568.03);
 
addTrain(2428, "Garib Rath", "Delhi", "Pune", "16:15", "00:15", 335, "Local", 482.73);
 
addTrain(2429, "MEMU", "Ahmedabad", "Mumbai", "07:00", "06:00", 1296, "Local", 1158.77); 

addTrain(2430, "Garib Rath", "Jaipur", "Hyderabad", "08:30", "00:30", 710, "Passenger", 1272.57);

 addTrain(2431, "Jan Shatabdi", "Lucknow", "Bangalore", "06:45", "22:00", 544, "Express", 1063.1); 

 addTrain(2432, "Garib Rath", "Jaipur", "Mumbai", "08:15", "11:15", 1580, "Passenger", 1063.99);

  addTrain(2433, "Superfast Express", "Chennai", "Jaipur", "16:00", "16:45", 104, "Express", 607.74);

addTrain(2434, "Garib Rath", "Ahmedabad", "Jaipur", "00:15", "22:45", 1714, "Local", 819.71);
 
addTrain(2435, "Suburban Local", "Chennai", "Jaipur", "17:00", "21:30", 101, "Passenger", 951.0);
 
addTrain(2436, "MEMU", "Pune", "Kolkata", "15:15", "15:15", 512, "Passenger", 1885.15);
 
addTrain(2437, "Rajdhani Express", "Lucknow", "Mumbai", "13:45", "00:00", 751, "Local", 1806.16);
 
addTrain(2438, "Suburban Local", "Lucknow", "Delhi", "00:30", "06:15", 178, "Local", 540.12);
 
addTrain(2439, "Garib Rath", "Jaipur", "Bangalore", "10:15", "09:45", 1053, "Passenger", 501.31);
 
addTrain(2440, "Duronto Express", "Chennai", "Bangalore", "23:30", "06:00", 1299, "Express", 533.36);
 
addTrain(2441, "Shatabdi Express", "Bangalore", "Kolkata", "10:30", "03:00", 1120, "Express", 345.92);
 
addTrain(2442, "Jan Shatabdi", "Ahmedabad", "Kolkata", "23:00", "23:00", 1066, "Local", 637.1);
 
addTrain(2443, "Garib Rath", "Jaipur", "Ahmedabad", "14:45", "17:45", 324, "Local", 1896.17);
 
addTrain(2444, "Suburban Local", "Pune", "Bangalore", "01:00", "18:30", 407, "Passenger", 1720.03);
 
addTrain(2445, "Suburban Local", "Hyderabad", "Kolkata", "09:30", "07:30", 1087, "Passenger", 183.38);

 addTrain(2446, "Superfast Express", "Chennai", "Hyderabad", "05:30", "06:00", 719, "Passenger", 1538.78); 

 addTrain(2447, "Shatabdi Express", "Ahmedabad", "Kolkata", "08:30", "23:30", 706, "Passenger", 1753.29); 

 addTrain(2448, "Suburban Local", "Pune", "Bangalore", "19:45", "15:30", 654, "Express", 1939.9); 

 addTrain(2449, "Duronto Express", "Chennai", "Lucknow", "05:45", "05:15", 959, "Local", 1193.21);

addTrain(2450, "Garib Rath", "Kolkata", "Chennai", "02:45", "19:15", 602, "Passenger", 1813.66);
 
addTrain(2451, "Suburban Local", "Pune", "Mumbai", "22:00", "03:15", 574, "Local", 1668.09);
 
addTrain(2452, "MEMU", "Ahmedabad", "Hyderabad", "20:30", "12:45", 1038, "Express", 991.04);
 
addTrain(2453, "Superfast Express", "Lucknow", "Delhi", "11:15", "21:00", 1802, "Passenger", 1517.29);
 
addTrain(2454, "MEMU", "Delhi", "Pune", "11:30", "09:00", 1176, "Express", 172.43);
 
addTrain(2455, "Shatabdi Express", "Chennai", "Kolkata", "03:00", "16:45", 357, "Local", 1675.58);
 
addTrain(2456, "Intercity Express", "Delhi", "Hyderabad", "23:15", "01:30", 137, "Passenger", 758.34);
 
addTrain(2457, "Garib Rath", "Ahmedabad", "Hyderabad", "22:30", "19:45", 1803, "Express", 976.57);
 
addTrain(2458, "Duronto Express", "Delhi", "Bangalore", "00:00", "08:45", 1970, "Express", 1791.84);
 
addTrain(2459, "Shatabdi Express", "Lucknow", "Chennai", "21:30", "15:15", 560, "Passenger", 137.64);
 
addTrain(2460, "Shatabdi Express", "Delhi", "Mumbai", "05:30", "05:45", 1466, "Local", 121.95);
 
addTrain(2461, "MEMU", "Delhi", "Mumbai", "23:00", "00:15", 926, "Express", 895.27);
 
addTrain(2462, "Mail Express", "Ahmedabad", "Jaipur", "21:00", "17:30", 59, "Local", 1367.22); 

addTrain(2463, "Mail Express", "Lucknow", "Kolkata", "07:15", "21:15", 1121, "Local", 1071.01);

 addTrain(2464, "Rajdhani Express", "Ahmedabad", "Chennai", "04:00", "17:30", 948, "Local", 1445.22);

  addTrain(2465, "Intercity Express", "Hyderabad", "Bangalore", "23:45", "19:00", 1602, "Passenger", 1917.37);

   addTrain(2466, "Duronto Express", "Bangalore", "Chennai", "20:00", "14:00", 287, "Express", 1296.57);

addTrain(2467, "Intercity Express", "Delhi", "Jaipur", "22:45", "20:00", 675, "Passenger", 1540.85);
 
addTrain(2468, "Suburban Local", "Lucknow", "Chennai", "00:45", "20:45", 918, "Express", 1082.17);
 
addTrain(2469, "Jan Shatabdi", "Ahmedabad", "Chennai", "07:15", "00:15", 880, "Passenger", 1944.92);
 
addTrain(2470, "Jan Shatabdi", "Mumbai", "Ahmedabad", "09:45", "14:15", 1210, "Express", 1971.82);
 
addTrain(2471, "MEMU", "Ahmedabad", "Hyderabad", "13:00", "08:45", 1790, "Passenger", 1193.76);
 
addTrain(2472, "MEMU", "Jaipur", "Hyderabad", "17:30", "19:00", 1006, "Passenger", 346.4);
 
addTrain(2473, "Rajdhani Express", "Chennai", "Delhi", "17:45", "16:00", 1208, "Passenger", 1626.52);
 
addTrain(2474, "Rajdhani Express", "Bangalore", "Kolkata", "11:00", "08:00", 1169, "Passenger", 1302.07);
 
addTrain(2475, "Mail Express", "Kolkata", "Hyderabad", "12:15", "18:15", 862, "Express", 1227.92);
 
addTrain(2476, "Intercity Express", "Jaipur", "Hyderabad", "18:30", "18:45", 541, "Express", 630.4);
 
addTrain(2477, "Superfast Express", "Hyderabad", "Mumbai", "18:00", "04:45", 1856, "Local", 1024.69);
 
addTrain(2478, "Mail Express", "Kolkata", "Delhi", "14:30", "10:45", 1306, "Local", 612.11);

addTrain(2479, "Jan Shatabdi", "Pune", "Hyderabad", "11:30", "08:00", 1207, "Passenger", 1396.79);

 addTrain(2480, "Superfast Express", "Mumbai", "Ahmedabad", "23:45", "16:30", 1817, "Express", 288.86); 

 addTrain(2481, "MEMU", "Chennai", "Lucknow", "03:45", "06:15", 577, "Passenger", 666.04);

  addTrain(2482, "Garib Rath", "Delhi", "Jaipur", "19:45", "14:45", 37, "Express", 1340.87);

addTrain(2483, "Garib Rath", "Ahmedabad", "Lucknow", "04:30", "08:30", 279, "Passenger", 1445.23);
 
addTrain(2484, "Shatabdi Express", "Pune", "Ahmedabad", "21:45", "11:30", 758, "Passenger", 834.23);
 
addTrain(2485, "Jan Shatabdi", "Hyderabad", "Chennai", "00:15", "18:30", 567, "Passenger", 1807.71);
 
addTrain(2486, "Garib Rath", "Lucknow", "Jaipur", "22:30", "17:45", 365, "Passenger", 1773.71);
 
addTrain(2487, "Jan Shatabdi", "Kolkata", "Lucknow", "04:15", "17:45", 1336, "Passenger", 1704.84);
 
addTrain(2488, "MEMU", "Pune", "Ahmedabad", "13:45", "08:30", 1543, "Express", 406.8);
 
addTrain(2489, "MEMU", "Hyderabad", "Delhi", "21:30", "07:00", 1187, "Passenger", 1539.9);
 
addTrain(2490, "Rajdhani Express", "Bangalore", "Chennai", "18:00", "19:00", 815, "Express", 609.98);
 
addTrain(2491, "MEMU", "Hyderabad", "Bangalore", "23:30", "14:45", 1453, "Local", 1590.71);
 
addTrain(2492, "Shatabdi Express", "Kolkata", "Hyderabad", "01:15", "02:00", 292, "Passenger", 1379.5);
 
addTrain(2493, "Jan Shatabdi", "Bangalore", "Chennai", "17:30", "16:00", 723, "Express", 136.04);
 
addTrain(2494, "MEMU", "Delhi", "Chennai", "01:45", "00:45", 626, "Express", 551.69);
 
addTrain(2495, "Shatabdi Express", "Ahmedabad", "Lucknow", "12:15", "06:45", 1001, "Local", 1149.18);

 addTrain(2496, "Garib Rath", "Kolkata", "Pune", "20:00", "21:30", 1097, "Express", 1612.37); 

 addTrain(2497, "Superfast Express", "Kolkata", "Hyderabad", "18:30", "12:45", 22, "Local", 566.89); 

 addTrain(2498, "Shatabdi Express", "Kolkata", "Chennai", "09:30", "12:45", 1024, "Local", 1763.24);

  addTrain(2499, "Suburban Local", "Ahmedabad", "Bangalore", "12:45", "01:15", 1845, "Passenger", 1352.03);

addTrain(2500, "MEMU", "Lucknow", "Pune", "05:30", "02:00", 389, "Local", 1146.73);
 
addTrain(2501, "Jan Shatabdi", "Lucknow", "Delhi", "18:00", "01:45", 687, "Express", 1341.92);
 
addTrain(2502, "Mail Express", "Mumbai", "Lucknow", "00:15", "08:45", 1352, "Express", 224.9);
 
addTrain(2503, "Duronto Express", "Pune", "Mumbai", "08:15", "12:15", 124, "Passenger", 146.71);
 
addTrain(2504, "Duronto Express", "Lucknow", "Mumbai", "02:30", "11:45", 1766, "Express", 183.94);
 
addTrain(2505, "Shatabdi Express", "Chennai", "Hyderabad", "22:30", "10:30", 927, "Express", 1455.3);
 
addTrain(2506, "Duronto Express", "Pune", "Lucknow", "23:15", "12:45", 182, "Express", 74.65);
 
addTrain(2507, "Rajdhani Express", "Kolkata", "Hyderabad", "18:15", "10:15", 1923, "Express", 1220.44);
 
addTrain(2508, "Mail Express", "Mumbai", "Bangalore", "18:00", "17:30", 820, "Local", 1255.91);
 
addTrain(2509, "Duronto Express", "Jaipur", "Lucknow", "08:45", "07:30", 1255, "Local", 1093.07);
 
addTrain(2510, "Mail Express", "Bangalore", "Chennai", "16:45", "23:30", 1051, "Passenger", 251.21);
 
addTrain(2511, "Jan Shatabdi", "Chennai", "Kolkata", "01:30", "08:30", 700, "Express", 1679.18);

 addTrain(2512, "Mail Express", "Delhi", "Bangalore", "03:00", "13:15", 921, "Express", 979.21);

  addTrain(2513, "Shatabdi Express", "Bangalore", "Lucknow", "14:30", "18:00", 77, "Express", 288.69);

   addTrain(2514, "Rajdhani Express", "Jaipur", "Delhi", "16:00", "15:30", 760, "Passenger", 201.25);

    addTrain(2515, "Rajdhani Express", "Bangalore", "Mumbai", "14:30", "09:00", 182, "Express", 817.16);

addTrain(2516, "Shatabdi Express", "Kolkata", "Pune", "20:30", "21:00", 69, "Local", 237.28);
 
addTrain(2517, "Duronto Express", "Delhi", "Jaipur", "10:00", "11:15", 415, "Local", 1312.66);
 
addTrain(2518, "Duronto Express", "Kolkata", "Jaipur", "12:45", "07:00", 421, "Passenger", 96.19);
 
addTrain(2519, "Duronto Express", "Hyderabad", "Kolkata", "02:45", "04:00", 1835, "Local", 1470.0);
 
addTrain(2520, "Superfast Express", "Mumbai", "Pune", "08:15", "20:30", 1759, "Express", 764.26);
 
addTrain(2521, "Suburban Local", "Hyderabad", "Pune", "07:15", "11:30", 1295, "Local", 416.25);
 
addTrain(2522, "Shatabdi Express", "Ahmedabad", "Jaipur", "13:45", "23:30", 823, "Express", 1541.16);
 
addTrain(2523, "Shatabdi Express", "Lucknow", "Ahmedabad", "22:45", "06:45", 1763, "Passenger", 1653.97);
 
addTrain(2524, "Intercity Express", "Hyderabad", "Jaipur", "01:45", "00:00", 1313, "Local", 1311.02);
 
addTrain(2525, "Jan Shatabdi", "Kolkata", "Hyderabad", "10:00", "12:30", 1797, "Express", 1482.69);
 
addTrain(2526, "Mail Express", "Kolkata", "Pune", "08:45", "08:30", 1133, "Passenger", 996.43);
 
addTrain(2527, "MEMU", "Pune", "Jaipur", "22:00", "00:45", 1464, "Express", 1642.44);
 
addTrain(2528, "Suburban Local", "Hyderabad", "Pune", "04:45", "21:15", 844, "Passenger", 1714.66); 

addTrain(2529, "Rajdhani Express", "Jaipur", "Chennai", "08:00", "00:45", 1049, "Local", 1701.32);

 addTrain(2530, "Mail Express", "Delhi", "Pune", "04:45", "19:45", 135, "Passenger", 1552.95);

  addTrain(2531, "MEMU", "Jaipur", "Hyderabad", "19:30", "02:15", 1803, "Express", 734.07); 

  addTrain(2532, "Mail Express", "Chennai", "Bangalore", "06:15", "21:30", 619, "Local", 1720.91);

addTrain(2533, "Shatabdi Express", "Hyderabad", "Mumbai", "08:00", "21:30", 1148, "Express", 1685.59);
 
addTrain(2534, "Shatabdi Express", "Bangalore", "Lucknow", "04:30", "18:30", 1290, "Local", 494.47);
 
addTrain(2535, "Garib Rath", "Lucknow", "Chennai", "18:15", "23:45", 1400, "Express", 512.49);
 
addTrain(2536, "Mail Express", "Hyderabad", "Jaipur", "11:00", "10:00", 525, "Local", 1903.13);
 
addTrain(2537, "Intercity Express", "Mumbai", "Jaipur", "07:30", "23:15", 1387, "Passenger", 606.22);
 
addTrain(2538, "Suburban Local", "Chennai", "Lucknow", "07:15", "01:00", 229, "Express", 367.85);
 
addTrain(2539, "Garib Rath", "Hyderabad", "Mumbai", "02:30", "05:45", 448, "Passenger", 792.84);
 
addTrain(2540, "Shatabdi Express", "Mumbai", "Kolkata", "00:00", "20:00", 1327, "Local", 523.39);
 
addTrain(2541, "Rajdhani Express", "Pune", "Ahmedabad", "06:30", "05:45", 1752, "Express", 694.63);
 
addTrain(2542, "Shatabdi Express", "Delhi", "Mumbai", "12:15", "04:00", 1390, "Express", 1744.49);
 
addTrain(2543, "Mail Express", "Pune", "Lucknow", "21:00", "03:00", 1013, "Passenger", 1362.4);
 
addTrain(2544, "Shatabdi Express", "Mumbai", "Lucknow", "04:00", "13:45", 21, "Local", 435.6);

 addTrain(2545, "MEMU", "Delhi", "Pune", "00:30", "14:15", 1071, "Passenger", 1504.17);

  addTrain(2546, "Mail Express", "Bangalore", "Pune", "13:15", "04:15", 737, "Passenger", 75.56);

   addTrain(2547, "Suburban Local", "Pune", "Jaipur", "21:45", "01:45", 1644, "Passenger", 1593.19);

    addTrain(2548, "Garib Rath", "Mumbai", "Pune", "15:00", "15:45", 1139, "Express", 291.82);

addTrain(2549, "Rajdhani Express", "Lucknow", "Chennai", "22:45", "01:45", 238, "Express", 1482.2);
 
addTrain(2550, "Mail Express", "Kolkata", "Hyderabad", "07:00", "18:30", 966, "Passenger", 429.01);
 
addTrain(2551, "Shatabdi Express", "Jaipur", "Pune", "06:45", "02:00", 1338, "Local", 996.48);
 
addTrain(2552, "Duronto Express", "Chennai", "Pune", "01:30", "09:30", 547, "Express", 754.79);
 
addTrain(2553, "Superfast Express", "Bangalore", "Chennai", "09:45", "22:30", 90, "Local", 1137.8);
 
addTrain(2554, "Shatabdi Express", "Hyderabad", "Pune", "13:45", "09:45", 1543, "Passenger", 1711.56);
 
addTrain(2555, "Duronto Express", "Bangalore", "Mumbai", "10:30", "13:45", 1115, "Express", 1159.25);
 
addTrain(2556, "MEMU", "Bangalore", "Chennai", "22:30", "00:15", 927, "Express", 82.08);
 
addTrain(2557, "Shatabdi Express", "Chennai", "Ahmedabad", "18:00", "08:00", 906, "Passenger", 1270.39);
 
addTrain(2558, "Superfast Express", "Delhi", "Ahmedabad", "20:30", "19:45", 1529, "Passenger", 1842.3);
 
addTrain(2559, "Intercity Express", "Chennai", "Kolkata", "07:45", "23:45", 1811, "Local", 652.6);
 
addTrain(2560, "Rajdhani Express", "Hyderabad", "Lucknow", "13:15", "17:15", 1241, "Local", 1037.46);
 
addTrain(2561, "Suburban Local", "Pune", "Bangalore", "01:15", "21:15", 180, "Local", 1350.69);

 addTrain(2562, "Garib Rath", "Pune", "Bangalore", "08:15", "18:00", 814, "Express", 987.16); 

 addTrain(2563, "Duronto Express", "Lucknow", "Chennai", "02:45", "07:15", 165, "Passenger", 1860.09); 

 addTrain(2564, "Garib Rath", "Lucknow", "Mumbai", "00:30", "12:00", 1383, "Local", 1691.06); 

 addTrain(2565, "Intercity Express", "Lucknow", "Hyderabad", "02:45", "00:00", 1654, "Express", 701.4);

addTrain(2566, "Rajdhani Express", "Ahmedabad", "Mumbai", "05:45", "03:00", 1849, "Passenger", 470.2);
 
addTrain(2567, "Rajdhani Express", "Kolkata", "Bangalore", "19:30", "21:15", 1771, "Express", 1458.51);
 
addTrain(2568, "Intercity Express", "Lucknow", "Jaipur", "14:00", "09:15", 1130, "Local", 943.14);
 
addTrain(2569, "Suburban Local", "Jaipur", "Mumbai", "19:00", "13:45", 591, "Local", 913.5);
 
addTrain(2570, "Duronto Express", "Delhi", "Mumbai", "15:30", "23:30", 796, "Express", 629.49);
 
addTrain(2571, "Suburban Local", "Pune", "Lucknow", "19:00", "19:15", 614, "Express", 1761.2);
 
addTrain(2572, "Duronto Express", "Chennai", "Delhi", "19:00", "00:45", 1421, "Passenger", 1151.29);
 
addTrain(2573, "Garib Rath", "Lucknow", "Pune", "14:15", "07:30", 1129, "Passenger", 539.67);
 
addTrain(2574, "Garib Rath", "Delhi", "Kolkata", "18:15", "17:00", 136, "Passenger", 845.35);
 
addTrain(2575, "Superfast Express", "Hyderabad", "Mumbai", "00:15", "09:15", 1264, "Local", 1021.12);
 
addTrain(2576, "Garib Rath", "Pune", "Hyderabad", "22:45", "06:00", 1441, "Express", 1394.52);
 
addTrain(2577, "MEMU", "Ahmedabad", "Mumbai", "04:00", "04:15", 1872, "Passenger", 1682.9);

 addTrain(2578, "Superfast Express", "Kolkata", "Delhi", "04:15", "18:45", 532, "Passenger", 1241.73);

  addTrain(2579, "MEMU", "Chennai", "Bangalore", "05:15", "14:00", 1843, "Passenger", 1690.6);

   addTrain(2580, "Mail Express", "Chennai", "Mumbai", "21:00", "14:15", 1179, "Express", 1501.74);

    addTrain(2581, "Superfast Express", "Jaipur", "Ahmedabad", "05:15", "19:00", 1996, "Express", 1979.15);

addTrain(2582, "Duronto Express", "Ahmedabad", "Bangalore", "19:30", "02:30", 555, "Local", 950.8);
 
addTrain(2583, "MEMU", "Chennai", "Mumbai", "04:30", "11:30", 383, "Passenger", 1657.35);
 
addTrain(2584, "Jan Shatabdi", "Kolkata", "Delhi", "14:15", "05:15", 1521, "Express", 180.96);
 
addTrain(2585, "Intercity Express", "Bangalore", "Ahmedabad", "22:45", "11:00", 1664, "Express", 599.13);
 
addTrain(2586, "Duronto Express", "Hyderabad", "Chennai", "23:45", "14:30", 903, "Express", 243.12);
 
addTrain(2587, "Shatabdi Express", "Bangalore", "Lucknow", "08:45", "18:15", 80, "Express", 1103.18);
 
addTrain(2588, "Intercity Express", "Jaipur", "Kolkata", "17:15", "19:15", 206, "Local", 1012.5);
 
addTrain(2589, "Rajdhani Express", "Jaipur", "Delhi", "13:15", "00:30", 1343, "Passenger", 897.33);
 
addTrain(2590, "Intercity Express", "Mumbai", "Hyderabad", "14:30", "08:15", 1069, "Local", 688.55);
 
addTrain(2591, "Garib Rath", "Mumbai", "Pune", "11:15", "02:15", 926, "Local", 1552.13);
 
addTrain(2592, "Garib Rath", "Delhi", "Pune", "01:15", "19:30", 170, "Local", 133.72);
 
addTrain(2593, "MEMU", "Ahmedabad", "Pune", "15:45", "21:00", 534, "Express", 1387.8);
 
addTrain(2594, "Suburban Local", "Lucknow", "Chennai", "16:45", "11:30", 1262, "Passenger", 1312.03);

 addTrain(2595, "Jan Shatabdi", "Delhi", "Jaipur", "04:15", "15:30", 112, "Local", 1220.85);

  addTrain(2596, "Mail Express", "Delhi", "Jaipur", "03:30", "10:45", 69, "Passenger", 859.52); 

  addTrain(2597, "Jan Shatabdi", "Jaipur", "Delhi", "07:15", "11:15", 1214, "Local", 567.1); 

  addTrain(2598, "Duronto Express", "Ahmedabad", "Bangalore", "21:00", "09:45", 1594, "Passenger", 792.16);

addTrain(2599, "Mail Express", "Pune", "Delhi", "04:45", "20:30", 485, "Express", 95.12);
 
addTrain(2600, "Jan Shatabdi", "Jaipur", "Hyderabad", "04:30", "02:30", 1130, "Local", 1053.18);
 
addTrain(2601, "Intercity Express", "Chennai", "Kolkata", "01:45", "21:00", 1285, "Local", 83.06);
 
addTrain(2602, "MEMU", "Delhi", "Ahmedabad", "12:00", "07:00", 176, "Local", 1271.01);
 
addTrain(2603, "Shatabdi Express", "Kolkata", "Delhi", "04:00", "00:30", 668, "Express", 1335.61);
 
addTrain(2604, "Shatabdi Express", "Ahmedabad", "Mumbai", "02:30", "05:30", 52, "Local", 1059.97);
 
addTrain(2605, "Superfast Express", "Bangalore", "Mumbai", "22:00", "06:00", 776, "Express", 1191.4);
 
addTrain(2606, "Superfast Express", "Chennai", "Lucknow", "09:15", "05:45", 614, "Passenger", 1196.58);
 
addTrain(2607, "Garib Rath", "Ahmedabad", "Kolkata", "13:45", "08:00", 348, "Local", 964.33);
 
addTrain(2608, "Duronto Express", "Jaipur", "Pune", "15:45", "06:45", 622, "Local", 783.92);
 
addTrain(2609, "Shatabdi Express", "Chennai", "Bangalore", "11:45", "08:45", 910, "Local", 733.28);
 
addTrain(2610, "Duronto Express", "Kolkata", "Pune", "12:00", "17:15", 626, "Passenger", 1205.98);

 addTrain(2611, "MEMU", "Bangalore", "Jaipur", "22:15", "20:15", 102, "Express", 892.91); 

 addTrain(2612, "Garib Rath", "Delhi", "Ahmedabad", "08:45", "15:45", 1094, "Passenger", 392.88);

  addTrain(2613, "Mail Express", "Bangalore", "Kolkata", "09:30", "17:00", 350, "Local", 1834.4); 

  addTrain(2614, "Rajdhani Express", "Jaipur", "Lucknow", "15:45", "17:45", 1833, "Passenger", 1166.78);

addTrain(2615, "Duronto Express", "Kolkata", "Bangalore", "01:15", "07:30", 650, "Express", 69.09);
 
addTrain(2616, "Shatabdi Express", "Lucknow", "Bangalore", "04:30", "06:00", 1992, "Passenger", 1256.54);
 
addTrain(2617, "Mail Express", "Pune", "Ahmedabad", "13:00", "13:00", 1351, "Passenger", 1375.58);
 
addTrain(2618, "Garib Rath", "Delhi", "Pune", "16:00", "23:00", 1551, "Local", 546.0);
 
addTrain(2619, "Superfast Express", "Hyderabad", "Jaipur", "19:45", "21:00", 1130, "Express", 1919.6);
 
addTrain(2620, "MEMU", "Jaipur", "Ahmedabad", "20:15", "20:30", 671, "Passenger", 768.96);
 
addTrain(2621, "Duronto Express", "Hyderabad", "Kolkata", "07:00", "02:00", 1074, "Passenger", 566.55);
 
addTrain(2622, "Superfast Express", "Hyderabad", "Pune", "16:15", "23:00", 876, "Local", 355.86);
 
addTrain(2623, "Suburban Local", "Mumbai", "Kolkata", "06:30", "14:00", 1383, "Passenger", 88.74);
 
addTrain(2624, "Intercity Express", "Chennai", "Bangalore", "22:00", "00:45", 858, "Passenger", 153.17);
 
addTrain(2625, "Suburban Local", "Chennai", "Mumbai", "03:45", "07:45", 1574, "Express", 17.9);
 
addTrain(2626, "Mail Express", "Chennai", "Delhi", "12:15", "15:45", 1409, "Local", 1440.19);
 
addTrain(2627, "Mail Express", "Kolkata", "Hyderabad", "12:00", "07:00", 1242, "Local", 793.19); 

addTrain(2628, "Shatabdi Express", "Lucknow", "Delhi", "03:00", "18:15", 728, "Local", 1053.22); 

addTrain(2629, "Mail Express", "Chennai", "Lucknow", "08:15", "21:15", 1586, "Express", 378.23);

 addTrain(2630, "Mail Express", "Lucknow", "Pune", "21:00", "13:00", 706, "Express", 1078.4); 

 addTrain(2631, "Rajdhani Express", "Lucknow", "Kolkata", "19:30", "05:00", 1877, "Local", 490.09);

addTrain(2632, "Intercity Express", "Hyderabad", "Jaipur", "03:15", "00:15", 528, "Local", 616.76);
 
addTrain(2633, "Jan Shatabdi", "Lucknow", "Delhi", "04:30", "08:15", 39, "Passenger", 1630.11);
 
addTrain(2634, "Garib Rath", "Kolkata", "Mumbai", "10:45", "17:00", 804, "Local", 27.32);
 
addTrain(2635, "Jan Shatabdi", "Kolkata", "Hyderabad", "19:15", "17:45", 806, "Passenger", 1349.08);
 
addTrain(2636, "Rajdhani Express", "Bangalore", "Mumbai", "11:00", "04:15", 1840, "Express", 1181.96);
 
addTrain(2637, "Jan Shatabdi", "Delhi", "Lucknow", "01:00", "23:30", 192, "Express", 679.23);
 
addTrain(2638, "Jan Shatabdi", "Mumbai", "Chennai", "07:30", "09:45", 408, "Local", 1208.19);
 
addTrain(2639, "Intercity Express", "Delhi", "Kolkata", "12:00", "05:30", 803, "Express", 1903.77);
 
addTrain(2640, "Garib Rath", "Jaipur", "Ahmedabad", "13:15", "03:15", 178, "Express", 123.15);
 
addTrain(2641, "Jan Shatabdi", "Hyderabad", "Chennai", "16:00", "08:30", 269, "Passenger", 1920.64);
 
addTrain(2642, "Rajdhani Express", "Ahmedabad", "Delhi", "15:30", "02:00", 1240, "Passenger", 395.16);
 

addTrain(2643, "Suburban Local", "Kolkata", "Hyderabad", "05:45", "16:45", 1556, "Passenger", 1734.09);

 addTrain(2644, "Shatabdi Express", "Lucknow", "Chennai", "20:00", "13:00", 1525, "Express", 1961.71); 

 addTrain(2645, "Superfast Express", "Ahmedabad", "Jaipur", "18:15", "18:30", 929, "Local", 655.13);

  addTrain(2646, "Suburban Local", "Chennai", "Kolkata", "00:00", "01:15", 52, "Express", 703.1); 

  addTrain(2647, "Intercity Express", "Lucknow", "Chennai", "01:00", "19:00", 1140, "Local", 1708.2);

addTrain(2648, "Jan Shatabdi", "Mumbai", "Chennai", "09:00", "22:45", 431, "Express", 1465.18);
 
addTrain(2649, "Shatabdi Express", "Hyderabad", "Chennai", "00:45", "09:45", 1666, "Express", 1098.58);
 
addTrain(2650, "Duronto Express", "Pune", "Chennai", "18:45", "11:15", 980, "Express", 1349.2);
 
addTrain(2651, "Mail Express", "Mumbai", "Delhi", "15:30", "09:45", 379, "Passenger", 1082.0);
 
addTrain(2652, "Duronto Express", "Lucknow", "Pune", "03:00", "14:45", 1142, "Passenger", 952.67);
 
addTrain(2653, "Suburban Local", "Delhi", "Chennai", "23:00", "08:30", 1848, "Express", 1434.74);
 
addTrain(2654, "Jan Shatabdi", "Ahmedabad", "Kolkata", "13:15", "20:15", 485, "Express", 836.67);
 
addTrain(2655, "Garib Rath", "Bangalore", "Lucknow", "04:00", "12:00", 1544, "Passenger", 1992.39);
 
addTrain(2656, "Suburban Local", "Delhi", "Mumbai", "17:45", "06:15", 1907, "Passenger", 1269.13);
 
addTrain(2657, "Intercity Express", "Lucknow", "Hyderabad", "14:45", "00:30", 1332, "Passenger", 1970.47);
 
addTrain(2658, "Duronto Express", "Delhi", "Mumbai", "14:45", "15:30", 528, "Express", 1856.42);
 
addTrain(2659, "Superfast Express", "Jaipur", "Mumbai", "15:00", "08:30", 897, "Local", 679.58);
 
addTrain(2660, "Jan Shatabdi", "Mumbai", "Chennai", "01:45", "02:15", 339, "Passenger", 1242.19);

 addTrain(2661, "Duronto Express", "Mumbai", "Ahmedabad", "06:45", "00:45", 1704, "Local", 1758.32); 

 addTrain(2662, "Suburban Local", "Bangalore", "Hyderabad", "04:00", "04:45", 309, "Express", 481.46); 

 addTrain(2663, "Suburban Local", "Lucknow", "Jaipur", "04:45", "23:45", 985, "Local", 657.03); 

 addTrain(2664, "Garib Rath", "Pune", "Lucknow", "17:00", "01:45", 1979, "Express", 1867.08);

addTrain(2665, "Jan Shatabdi", "Jaipur", "Lucknow", "19:45", "16:00", 522, "Local", 194.45);
 
addTrain(2666, "Mail Express", "Bangalore", "Kolkata", "06:00", "21:45", 915, "Local", 909.04);
 
addTrain(2667, "Garib Rath", "Delhi", "Bangalore", "04:30", "04:00", 102, "Local", 1845.05);
 
addTrain(2668, "MEMU", "Kolkata", "Ahmedabad", "10:30", "12:15", 1890, "Local", 1365.48);
 
addTrain(2669, "Shatabdi Express", "Chennai", "Kolkata", "23:00", "07:30", 274, "Local", 1768.93);
 
addTrain(2670, "Duronto Express", "Bangalore", "Hyderabad", "19:45", "20:00", 322, "Express", 1855.64);
 
addTrain(2671, "MEMU", "Delhi", "Pune", "06:45", "22:30", 1883, "Local", 1729.73);
 
addTrain(2672, "Intercity Express", "Jaipur", "Mumbai", "18:15", "16:15", 1637, "Passenger", 1653.08);
 
addTrain(2673, "Duronto Express", "Hyderabad", "Lucknow", "01:00", "06:45", 441, "Express", 93.75);
 
addTrain(2674, "Duronto Express", "Lucknow", "Bangalore", "08:15", "06:45", 800, "Passenger", 1481.41);
 
addTrain(2675, "Superfast Express", "Hyderabad", "Bangalore", "14:00", "05:15", 1918, "Passenger", 813.91);
 
addTrain(2676, "Mail Express", "Delhi", "Kolkata", "19:45", "17:15", 1084, "Local", 1520.62);

 addTrain(2677, "Intercity Express", "Pune", "Mumbai", "02:45", "05:30", 1227, "Passenger", 56.33); 

 addTrain(2678, "Duronto Express", "Chennai", "Pune", "21:15", "01:00", 1440, "Local", 1590.94);

  addTrain(2679, "Suburban Local", "Pune", "Chennai", "16:30", "20:15", 548, "Express", 1063.61); 

  addTrain(2680, "Rajdhani Express", "Jaipur", "Ahmedabad", "03:45", "11:15", 825, "Express", 625.16);

addTrain(2681, "Rajdhani Express", "Chennai", "Jaipur", "04:15", "19:30", 1604, "Local", 1079.48);
 
addTrain(2682, "Duronto Express", "Mumbai", "Chennai", "05:30", "17:15", 1064, "Local", 919.02);
 
addTrain(2683, "Shatabdi Express", "Chennai", "Jaipur", "14:15", "00:30", 93, "Local", 1571.71);
 
addTrain(2684, "Superfast Express", "Jaipur", "Pune", "18:15", "23:30", 641, "Passenger", 62.27);
 
addTrain(2685, "Superfast Express", "Mumbai", "Chennai", "06:30", "02:30", 168, "Express", 652.19);
 
addTrain(2686, "Suburban Local", "Hyderabad", "Mumbai", "23:30", "08:30", 1765, "Local", 1008.37);
 
addTrain(2687, "Shatabdi Express", "Pune", "Chennai", "10:15", "11:30", 1632, "Passenger", 319.27);
 
addTrain(2688, "Intercity Express", "Ahmedabad", "Lucknow", "13:00", "04:30", 1168, "Local", 1973.82);
 
addTrain(2689, "Suburban Local", "Mumbai", "Lucknow", "12:15", "02:45", 839, "Local", 993.22);
 
addTrain(2690, "Rajdhani Express", "Pune", "Mumbai", "03:30", "12:30", 939, "Passenger", 288.25);
 
addTrain(2691, "Mail Express", "Mumbai", "Chennai", "20:15", "14:45", 621, "Local", 1963.21);
 
addTrain(2692, "Garib Rath", "Hyderabad", "Ahmedabad", "12:45", "16:00", 1563, "Express", 548.19);
 
addTrain(2693, "Suburban Local", "Chennai", "Lucknow", "05:00", "06:00", 1949, "Passenger", 1582.49);

addTrain(2694, "Shatabdi Express", "Pune", "Mumbai", "15:00", "02:00", 1635, "Passenger", 205.81);

 addTrain(2695, "Superfast Express", "Jaipur", "Delhi", "01:00", "09:00", 1859, "Local", 738.77); 

 addTrain(2696, "Suburban Local", "Mumbai", "Ahmedabad", "21:45", "01:30", 1724, "Passenger", 1733.18); 

 addTrain(2697, "Jan Shatabdi", "Delhi", "Pune", "01:15", "03:45", 83, "Express", 1643.08);

addTrain(2698, "Duronto Express", "Chennai", "Hyderabad", "18:45", "08:45", 916, "Local", 1074.76);
 
addTrain(2699, "Shatabdi Express", "Mumbai", "Delhi", "16:00", "00:45", 793, "Local", 316.07);
 
addTrain(2700, "Duronto Express", "Bangalore", "Hyderabad", "20:00", "18:00", 1957, "Local", 1939.66);
 
addTrain(2701, "Garib Rath", "Bangalore", "Delhi", "09:30", "08:15", 91, "Local", 1347.07);
 
addTrain(2702, "Suburban Local", "Chennai", "Jaipur", "09:30", "10:30", 1261, "Passenger", 797.29);
 
addTrain(2703, "Superfast Express", "Kolkata", "Pune", "03:15", "15:30", 1788, "Express", 810.18);
 
addTrain(2704, "Shatabdi Express", "Chennai", "Jaipur", "20:00", "23:00", 1986, "Express", 1558.18);
 
addTrain(2705, "MEMU", "Lucknow", "Ahmedabad", "01:45", "01:45", 458, "Express", 884.41);
 
addTrain(2706, "Rajdhani Express", "Ahmedabad", "Hyderabad", "07:30", "01:30", 1340, "Passenger", 1333.72);
 
addTrain(2707, "Mail Express", "Lucknow", "Kolkata", "06:30", "17:30", 1584, "Passenger", 647.48);
 
addTrain(2708, "Superfast Express", "Pune", "Hyderabad", "03:00", "01:15", 758, "Passenger", 1913.8);
 
addTrain(2709, "Suburban Local", "Lucknow", "Chennai", "18:45", "07:00", 1722, "Express", 95.74); 

addTrain(2710, "Duronto Express", "Delhi", "Kolkata", "10:45", "18:45", 845, "Local", 315.31);

 addTrain(2711, "Jan Shatabdi", "Jaipur", "Delhi", "22:30", "18:45", 744, "Express", 382.79);

  addTrain(2712, "Superfast Express", "Mumbai", "Kolkata", "15:30", "07:45", 1276, "Express", 1159.8); 

  addTrain(2713, "Mail Express", "Jaipur", "Ahmedabad", "12:30", "09:00", 1601, "Local", 98.75);

addTrain(2714, "Garib Rath", "Hyderabad", "Bangalore", "20:15", "05:30", 266, "Local", 571.55);
 
addTrain(2715, "Garib Rath", "Delhi", "Kolkata", "12:15", "05:00", 327, "Local", 98.77);
 
addTrain(2716, "Jan Shatabdi", "Hyderabad", "Mumbai", "15:45", "22:30", 1723, "Passenger", 649.53);
 
addTrain(2717, "MEMU", "Ahmedabad", "Chennai", "03:30", "22:15", 1611, "Express", 415.14);
 
addTrain(2718, "Shatabdi Express", "Chennai", "Delhi", "04:00", "00:45", 697, "Express", 1221.84);
 
addTrain(2719, "Intercity Express", "Mumbai", "Delhi", "10:15", "19:45", 1945, "Local", 379.53);
 
addTrain(2720, "Rajdhani Express", "Kolkata", "Ahmedabad", "11:00", "11:15", 1815, "Passenger", 1273.19);
 
addTrain(2721, "Duronto Express", "Chennai", "Jaipur", "05:15", "13:15", 571, "Passenger", 1349.19);
 
addTrain(2722, "Suburban Local", "Pune", "Ahmedabad", "02:45", "19:30", 99, "Express", 1229.13);
 
addTrain(2723, "Jan Shatabdi", "Bangalore", "Kolkata", "02:15", "19:00", 456, "Express", 176.84);
 
addTrain(2724, "Intercity Express", "Jaipur", "Mumbai", "05:45", "05:00", 1140, "Local", 450.18);
 
addTrain(2725, "MEMU", "Chennai", "Hyderabad", "05:15", "22:00", 1482, "Express", 1264.27);
 
addTrain(2726, "Intercity Express", "Jaipur", "Hyderabad", "01:15", "19:45", 1957, "Express", 1377.3);

 addTrain(2727, "Rajdhani Express", "Jaipur", "Bangalore", "01:15", "21:00", 1678, "Passenger", 1574.44); 

 addTrain(2728, "Intercity Express", "Jaipur", "Hyderabad", "05:45", "12:45", 938, "Express", 586.32); 

 addTrain(2729, "Duronto Express", "Hyderabad", "Delhi", "21:30", "13:15", 744, "Local", 580.48);

 addTrain(2730, "Mail Express", "Delhi", "Bangalore", "09:45", "19:00", 85, "Passenger", 595.3);

addTrain(2731, "Intercity Express", "Kolkata", "Delhi", "01:15", "15:15", 1971, "Express", 991.12);
 
addTrain(2732, "Rajdhani Express", "Kolkata", "Hyderabad", "17:00", "11:00", 1486, "Express", 825.35);
 
addTrain(2733, "Garib Rath", "Lucknow", "Bangalore", "21:00", "15:00", 1819, "Local", 324.94);
 
addTrain(2734, "Intercity Express", "Mumbai", "Bangalore", "23:00", "17:15", 1845, "Passenger", 1016.09);
 
addTrain(2735, "Jan Shatabdi", "Bangalore", "Jaipur", "23:00", "08:15", 1832, "Express", 735.88);
 
addTrain(2736, "Mail Express", "Chennai", "Delhi", "08:15", "06:15", 589, "Passenger", 1476.96);
 
addTrain(2737, "Duronto Express", "Mumbai", "Jaipur", "12:30", "08:15", 817, "Passenger", 1239.7);
 
addTrain(2738, "Shatabdi Express", "Jaipur", "Mumbai", "06:30", "10:30", 1372, "Local", 871.13);
 
addTrain(2739, "Duronto Express", "Bangalore", "Delhi", "20:00", "05:00", 1564, "Passenger", 942.85);
 
addTrain(2740, "Jan Shatabdi", "Jaipur", "Ahmedabad", "18:45", "17:15", 1072, "Passenger", 444.53);
 
addTrain(2741, "Duronto Express", "Pune", "Chennai", "14:15", "16:30", 1673, "Passenger", 1420.68);
 
addTrain(2742, "Jan Shatabdi", "Ahmedabad", "Hyderabad", "07:30", "02:30", 322, "Local", 319.19); 

addTrain(2743, "Jan Shatabdi", "Chennai", "Lucknow", "15:30", "06:45", 1706, "Passenger", 621.02);

 addTrain(2744, "MEMU", "Mumbai", "Pune", "20:15", "16:30", 1883, "Express", 609.19); 

 addTrain(2745, "Mail Express", "Delhi", "Kolkata", "20:15", "22:15", 1105, "Local", 1566.94); 

 addTrain(2746, "Rajdhani Express", "Pune", "Bangalore", "14:30", "08:15", 1181, "Passenger", 631.0);

addTrain(2747, "Intercity Express", "Lucknow", "Bangalore", "07:15", "02:30", 1525, "Passenger", 1561.65);
 
addTrain(2748, "MEMU", "Delhi", "Pune", "08:45", "02:00", 1476, "Passenger", 544.41);
 
addTrain(2749, "Jan Shatabdi", "Kolkata", "Lucknow", "12:45", "18:00", 499, "Local", 1551.33);
 
addTrain(2750, "Shatabdi Express", "Mumbai", "Lucknow", "00:00", "04:00", 1560, "Passenger", 310.95);
 
addTrain(2751, "Mail Express", "Pune", "Bangalore", "18:30", "23:15", 1379, "Passenger", 1219.64);
 
addTrain(2752, "Rajdhani Express", "Pune", "Delhi", "09:15", "04:15", 2000, "Local", 1994.48);
 
addTrain(2753, "Superfast Express", "Mumbai", "Pune", "19:30", "22:45", 1227, "Local", 227.73);
 
addTrain(2754, "Mail Express", "Lucknow", "Bangalore", "14:00", "02:15", 341, "Passenger", 144.9);
 
addTrain(2755, "Mail Express", "Hyderabad", "Bangalore", "23:15", "19:45", 1263, "Passenger", 1999.88);
 
addTrain(2756, "MEMU", "Mumbai", "Kolkata", "12:00", "06:15", 700, "Express", 51.28);
 
addTrain(2757, "Jan Shatabdi", "Lucknow", "Mumbai", "18:30", "01:15", 1494, "Local", 748.58);
 
addTrain(2758, "MEMU", "Lucknow", "Mumbai", "15:15", "00:15", 1118, "Express", 371.81);
 
addTrain(2759, "Rajdhani Express", "Mumbai", "Kolkata", "23:00", "11:45", 1793, "Express", 1182.23); 

addTrain(2760, "Superfast Express", "Ahmedabad", "Lucknow", "05:00", "01:30", 1270, "Passenger", 778.5); 

addTrain(2761, "Intercity Express", "Mumbai", "Lucknow", "17:15", "16:30", 1579, "Local", 1389.61);

 addTrain(2762, "MEMU", "Pune", "Delhi", "20:00", "12:00", 1265, "Local", 834.81);


  addTrain(2763, "MEMU", "Chennai", "Delhi", "06:00", "21:15", 1114, "Local", 561.04);

addTrain(2764, "Shatabdi Express", "Kolkata", "Ahmedabad", "01:45", "22:00", 1463, "Passenger", 1786.12);
 
addTrain(2765, "Shatabdi Express", "Chennai", "Lucknow", "13:00", "16:30", 1720, "Express", 1078.89);
 
addTrain(2766, "Jan Shatabdi", "Lucknow", "Bangalore", "00:45", "23:45", 1782, "Passenger", 1827.56);
 
addTrain(2767, "Rajdhani Express", "Ahmedabad", "Bangalore", "17:30", "00:30", 46, "Local", 597.33);
 
addTrain(2768, "Superfast Express", "Pune", "Bangalore", "14:00", "10:00", 189, "Passenger", 1719.66);
 
addTrain(2769, "Garib Rath", "Pune", "Lucknow", "13:00", "19:00", 1157, "Express", 466.72);
 
addTrain(2770, "Mail Express", "Kolkata", "Delhi", "02:15", "18:15", 43, "Passenger", 1665.5);
 
addTrain(2771, "Garib Rath", "Hyderabad", "Chennai", "08:00", "10:45", 959, "Passenger", 247.32);
 
addTrain(2772, "Jan Shatabdi", "Chennai", "Ahmedabad", "11:30", "03:45", 344, "Passenger", 928.22);
 
addTrain(2773, "Rajdhani Express", "Lucknow", "Pune", "19:30", "17:00", 1634, "Passenger", 880.33);
 
addTrain(2774, "Mail Express", "Ahmedabad", "Jaipur", "20:00", "22:30", 1482, "Passenger", 1648.54);
 
addTrain(2775, "MEMU", "Delhi", "Lucknow", "05:15", "05:00", 640, "Passenger", 361.24);

 addTrain(2776, "Shatabdi Express", "Bangalore", "Kolkata", "02:30", "03:15", 1660, "Passenger", 86.53);

  addTrain(2777, "Jan Shatabdi", "Chennai", "Delhi", "05:00", "17:30", 1020, "Express", 1183.21);

   addTrain(2778, "Intercity Express", "Mumbai", "Chennai", "03:00", "12:45", 200, "Express", 1711.53);

    addTrain(2779, "Shatabdi Express", "Kolkata", "Delhi", "00:30", "23:00", 970, "Passenger", 1196.71);

addTrain(2780, "Garib Rath", "Mumbai", "Chennai", "06:00", "02:00", 733, "Passenger", 1567.47);
 
addTrain(2781, "Suburban Local", "Bangalore", "Mumbai", "17:00", "20:15", 179, "Express", 1828.66);
 
addTrain(2782, "Intercity Express", "Ahmedabad", "Jaipur", "08:30", "13:15", 308, "Express", 178.93);
 
addTrain(2783, "MEMU", "Pune", "Bangalore", "02:00", "22:15", 515, "Passenger", 961.59);
 
addTrain(2784, "Superfast Express", "Kolkata", "Bangalore", "06:45", "16:30", 1444, "Express", 811.19);
 
addTrain(2785, "Rajdhani Express", "Pune", "Chennai", "06:45", "18:00", 1454, "Local", 1927.82);
 
addTrain(2786, "Duronto Express", "Ahmedabad", "Lucknow", "22:30", "12:45", 1448, "Passenger", 898.13);
 
addTrain(2787, "Garib Rath", "Bangalore", "Pune", "12:45", "15:15", 934, "Express", 969.46);
 
addTrain(2788, "Garib Rath", "Pune", "Delhi", "16:00", "11:15", 1283, "Local", 1999.65);
 
addTrain(2789, "Garib Rath", "Mumbai", "Hyderabad", "07:15", "08:00", 119, "Passenger", 1255.43);
 
addTrain(2790, "Rajdhani Express", "Mumbai", "Pune", "12:00", "06:00", 1500, "Express", 1884.27);
 
addTrain(2791, "Garib Rath", "Delhi", "Ahmedabad", "17:45", "01:00", 1658, "Express", 1012.23);
 
addTrain(2792, "Suburban Local", "Lucknow", "Mumbai", "15:00", "00:00", 799, "Express", 1314.27); 

addTrain(2793, "MEMU", "Bangalore", "Lucknow", "11:15", "08:00", 994, "Passenger", 813.39); 

addTrain(2794, "Garib Rath", "Ahmedabad", "Mumbai", "17:15", "12:45", 183, "Local", 842.68); 

addTrain(2795, "Superfast Express", "Hyderabad", "Delhi", "20:45", "07:00", 1940, "Local", 1233.35); 

addTrain(2796, "Superfast Express", "Kolkata", "Mumbai", "08:30", "03:15", 1808, "Passenger", 1242.05);

addTrain(2797, "Shatabdi Express", "Mumbai", "Chennai", "15:15", "14:45", 1703, "Express", 1481.82);
 
addTrain(2798, "Suburban Local", "Pune", "Lucknow", "22:45", "20:15", 601, "Passenger", 1034.23);
 
addTrain(2799, "Superfast Express", "Pune", "Lucknow", "09:45", "17:00", 912, "Express", 52.95);
 
addTrain(2800, "Intercity Express", "Jaipur", "Delhi", "19:15", "13:45", 798, "Local", 417.15);
 
addTrain(2801, "Duronto Express", "Pune", "Mumbai", "08:00", "19:15", 119, "Local", 493.15);
 
addTrain(2802, "Intercity Express", "Pune", "Chennai", "14:30", "00:30", 612, "Express", 655.67);
 
addTrain(2803, "Suburban Local", "Kolkata", "Delhi", "10:00", "15:30", 1234, "Passenger", 194.8);
 
addTrain(2804, "Shatabdi Express", "Bangalore", "Kolkata", "03:15", "06:30", 801, "Express", 359.44);
 
addTrain(2805, "Rajdhani Express", "Bangalore", "Mumbai", "01:45", "17:45", 1598, "Local", 1066.92);
 
addTrain(2806, "Suburban Local", "Ahmedabad", "Jaipur", "11:00", "16:15", 518, "Passenger", 1973.01);
 
addTrain(2807, "Shatabdi Express", "Bangalore", "Lucknow", "20:00", "08:45", 1284, "Passenger", 874.15);
 
addTrain(2808, "Duronto Express", "Pune", "Delhi", "15:00", "16:30", 730, "Local", 1873.48); 

addTrain(2809, "Jan Shatabdi", "Lucknow", "Delhi", "14:00", "08:15", 1224, "Express", 689.38); 

addTrain(2810, "Suburban Local", "Jaipur", "Lucknow", "22:45", "16:00", 1944, "Passenger", 625.82); 

addTrain(2811, "Garib Rath", "Lucknow", "Ahmedabad", "16:15", "17:15", 1085, "Passenger", 1606.15); 

addTrain(2812, "Intercity Express", "Chennai", "Bangalore", "13:45", "12:00", 624, "Passenger", 1045.02);

addTrain(2813, "Rajdhani Express", "Ahmedabad", "Delhi", "22:30", "18:45", 255, "Express", 944.14);
 
addTrain(2814, "MEMU", "Lucknow", "Bangalore", "20:00", "16:45", 708, "Passenger", 1823.35);
 
addTrain(2815, "Mail Express", "Mumbai", "Chennai", "22:45", "06:15", 328, "Local", 393.88);
 
addTrain(2816, "Mail Express", "Bangalore", "Ahmedabad", "12:15", "03:15", 81, "Express", 732.32);
 
addTrain(2817, "Jan Shatabdi", "Pune", "Delhi", "19:45", "02:00", 1843, "Local", 241.61);
 
addTrain(2818, "Intercity Express", "Pune", "Kolkata", "09:45", "22:15", 540, "Local", 1055.25);
 
addTrain(2819, "Garib Rath", "Lucknow", "Mumbai", "12:00", "17:30", 558, "Local", 1714.07);
 
addTrain(2820, "Garib Rath", "Delhi", "Hyderabad", "21:30", "02:30", 985, "Local", 493.01);
 
addTrain(2821, "Duronto Express", "Pune", "Mumbai", "12:00", "04:30", 872, "Passenger", 788.13);
 
addTrain(2822, "Garib Rath", "Chennai", "Hyderabad", "13:45", "08:30", 449, "Passenger", 659.46);
 
addTrain(2823, "MEMU", "Kolkata", "Lucknow", "23:15", "01:30", 619, "Express", 979.12);
 
addTrain(2824, "Shatabdi Express", "Jaipur", "Delhi", "02:45", "03:45", 1015, "Local", 1429.34);
 
addTrain(2825, "Jan Shatabdi", "Hyderabad", "Chennai", "10:15", "20:30", 453, "Express", 579.07);

 addTrain(2826, "Superfast Express", "Pune", "Jaipur", "13:45", "08:15", 1423, "Local", 1622.5); 

 addTrain(2827, "Shatabdi Express", "Hyderabad", "Pune", "11:45", "21:15", 749, "Passenger", 285.35);

  addTrain(2828, "Garib Rath", "Pune", "Delhi", "05:15", "09:00", 906, "Local", 1900.16);

  addTrain(2829, "Superfast Express", "Pune", "Bangalore", "06:00", "21:45", 1564, "Local", 929.31);

addTrain(2830, "Intercity Express", "Hyderabad", "Bangalore", "16:15", "03:15", 1685, "Local", 367.73);
 
addTrain(2831, "Duronto Express", "Chennai", "Delhi", "19:45", "19:15", 277, "Passenger", 1254.18);
 
addTrain(2832, "Shatabdi Express", "Mumbai", "Jaipur", "00:45", "06:30", 835, "Local", 1210.35);
 
addTrain(2833, "Superfast Express", "Bangalore", "Kolkata", "07:30", "01:30", 937, "Local", 305.06);
 
addTrain(2834, "Intercity Express", "Mumbai", "Chennai", "22:45", "09:30", 290, "Express", 182.29);
 
addTrain(2835, "Garib Rath", "Pune", "Jaipur", "07:00", "16:00", 1469, "Passenger", 462.18);
 
addTrain(2836, "Rajdhani Express", "Ahmedabad", "Mumbai", "05:45", "16:00", 592, "Passenger", 1181.85);
 
addTrain(2837, "Superfast Express", "Ahmedabad", "Bangalore", "17:45", "07:15", 1793, "Local", 984.19);
 
addTrain(2838, "Duronto Express", "Jaipur", "Delhi", "02:00", "02:45", 1002, "Passenger", 225.31);
 
addTrain(2839, "Suburban Local", "Pune", "Mumbai", "17:30", "15:00", 77, "Passenger", 462.01);
 
addTrain(2840, "Duronto Express", "Delhi", "Chennai", "16:15", "14:45", 820, "Passenger", 801.78);
 
addTrain(2841, "Duronto Express", "Pune", "Hyderabad", "07:15", "05:15", 1343, "Express", 246.09);

 addTrain(2842, "MEMU", "Lucknow", "Mumbai", "21:15", "07:30", 1172, "Passenger", 259.05);

  addTrain(2843, "Garib Rath", "Bangalore", "Kolkata", "10:15", "14:00", 377, "Passenger", 1811.32); 

  addTrain(2844, "MEMU", "Mumbai", "Bangalore", "11:15", "15:15", 1602, "Passenger", 1778.16);

   addTrain(2845, "Superfast Express", "Pune", "Mumbai", "07:45", "13:30", 607, "Express", 1311.73);

addTrain(2846, "Intercity Express", "Chennai", "Jaipur", "18:00", "01:15", 1378, "Express", 547.72);
 
addTrain(2847, "Mail Express", "Kolkata", "Pune", "21:45", "19:45", 376, "Express", 211.45);
 
addTrain(2848, "Duronto Express", "Jaipur", "Ahmedabad", "09:45", "04:30", 1068, "Local", 1420.66);
 
addTrain(2849, "Shatabdi Express", "Bangalore", "Lucknow", "11:15", "12:00", 1758, "Express", 612.91);
 
addTrain(2850, "Jan Shatabdi", "Delhi", "Kolkata", "09:45", "11:15", 815, "Local", 1122.62);
 
addTrain(2851, "Mail Express", "Lucknow", "Bangalore", "01:45", "02:15", 1572, "Passenger", 1705.82);
 
addTrain(2852, "Duronto Express", "Ahmedabad", "Jaipur", "08:15", "14:15", 1603, "Express", 1791.7);
 
addTrain(2853, "Suburban Local", "Jaipur", "Kolkata", "04:30", "04:30", 981, "Local", 296.53);
 
addTrain(2854, "Jan Shatabdi", "Pune", "Mumbai", "20:00", "22:15", 1266, "Express", 110.93);
 
addTrain(2855, "Suburban Local", "Delhi", "Lucknow", "01:45", "07:45", 77, "Express", 1100.11);
 
addTrain(2856, "Suburban Local", "Jaipur", "Hyderabad", "04:00", "06:00", 529, "Express", 1100.98);
 
addTrain(2857, "Mail Express", "Pune", "Mumbai", "21:00", "16:30", 575, "Local", 230.39);
 
addTrain(2858, "Jan Shatabdi", "Pune", "Jaipur", "04:45", "01:45", 726, "Local", 1603.56);

 addTrain(2859, "Duronto Express", "Ahmedabad", "Bangalore", "10:30", "14:15", 1949, "Passenger", 1102.6); 

 addTrain(2860, "Superfast Express", "Mumbai", "Delhi", "05:45", "06:45", 1655, "Passenger", 1828.15); 

 addTrain(2861, "Shatabdi Express", "Jaipur", "Hyderabad", "02:30", "19:00", 1820, "Express", 230.21); 

 addTrain(2862, "Shatabdi Express", "Hyderabad", "Kolkata", "06:30", "21:15", 1340, "Local", 1697.51);

addTrain(2863, "Rajdhani Express", "Pune", "Ahmedabad", "08:15", "15:00", 934, "Express", 1244.42);
 
addTrain(2864, "Intercity Express", "Hyderabad", "Jaipur", "11:30", "20:15", 1864, "Local", 1782.05);
 
addTrain(2865, "Intercity Express", "Hyderabad", "Jaipur", "11:30", "05:45", 1425, "Local", 945.95);
 
addTrain(2866, "Duronto Express", "Jaipur", "Ahmedabad", "05:30", "23:00", 924, "Express", 755.96);
 
addTrain(2867, "Duronto Express", "Jaipur", "Kolkata", "04:45", "04:00", 1208, "Express", 1601.54);
 
addTrain(2868, "Shatabdi Express", "Delhi", "Bangalore", "06:00", "08:45", 913, "Express", 941.33);
 
addTrain(2869, "MEMU", "Chennai", "Delhi", "02:15", "03:45", 545, "Local", 1571.46);
 
addTrain(2870, "Intercity Express", "Mumbai", "Pune", "01:00", "00:30", 1271, "Passenger", 1487.98);
 
addTrain(2871, "MEMU", "Bangalore", "Lucknow", "05:45", "02:15", 808, "Passenger", 1412.7);
 
addTrain(2872, "Garib Rath", "Chennai", "Hyderabad", "09:45", "07:45", 320, "Express", 935.82);
 
addTrain(2873, "MEMU", "Mumbai", "Kolkata", "08:30", "05:15", 1797, "Local", 1572.29);
 
addTrain(2874, "Shatabdi Express", "Chennai", "Bangalore", "05:30", "20:30", 1428, "Express", 304.56); 

addTrain(2875, "Intercity Express", "Kolkata", "Jaipur", "06:00", "01:30", 634, "Passenger", 938.67);

 addTrain(2876, "Superfast Express", "Chennai", "Hyderabad", "00:45", "02:30", 772, "Express", 1692.12); 

 addTrain(2878, "Superfast Express", "Hyderabad", "Chennai", "00:00", "08:00", 1392, "Passenger", 748.11);

addTrain(2879, "Jan Shatabdi", "Ahmedabad", "Bangalore", "04:30", "11:45", 125, "Local", 1274.55);
 
addTrain(2880, "Duronto Express", "Jaipur", "Pune", "00:00", "18:15", 1056, "Express", 111.46);
 
addTrain(2881, "Rajdhani Express", "Bangalore", "Chennai", "04:45", "04:45", 730, "Passenger", 900.93);
 
addTrain(2882, "Duronto Express", "Chennai", "Kolkata", "16:15", "17:45", 360, "Passenger", 399.95);
 
addTrain(2883, "Suburban Local", "Ahmedabad", "Mumbai", "14:00", "20:00", 1894, "Express", 1973.93);
 
addTrain(2884, "Intercity Express", "Mumbai", "Lucknow", "22:00", "19:45", 181, "Local", 1707.55);
 
addTrain(2885, "MEMU", "Lucknow", "Bangalore", "02:30", "06:30", 258, "Local", 1765.71);
 
addTrain(2886, "Rajdhani Express", "Mumbai", "Jaipur", "05:15", "11:45", 1036, "Passenger", 487.64);
 
addTrain(2887, "Shatabdi Express", "Pune", "Jaipur", "14:45", "15:45", 353, "Local", 1879.48);
 
addTrain(2888, "MEMU", "Mumbai", "Delhi", "00:00", "00:45", 525, "Express", 1989.76);
 
addTrain(2889, "MEMU", "Ahmedabad", "Kolkata", "12:30", "02:45", 267, "Local", 1358.0);
 
addTrain(2890, "MEMU", "Hyderabad", "Chennai", "10:45", "13:00", 1684, "Passenger", 1340.67);
 
addTrain(2891, "MEMU", "Bangalore", "Pune", "09:45", "20:45", 82, "Express", 671.77); 

addTrain(2892, "Garib Rath", "Pune", "Kolkata", "06:45", "14:30", 1493, "Local", 1401.69); 

addTrain(2893, "Mail Express", "Delhi", "Ahmedabad", "10:45", "20:30", 1106, "Local", 1986.53); 

addTrain(2894, "Intercity Express", "Kolkata", "Hyderabad", "01:15", "17:45", 822, "Local", 1126.69); 

addTrain(2895, "Rajdhani Express", "Bangalore", "Kolkata", "15:30", "03:15", 1404, "Express", 1200.12);

addTrain(2896, "Rajdhani Express", "Jaipur", "Ahmedabad", "21:00", "01:45", 1535, "Passenger", 1399.31);
 
addTrain(2897, "Suburban Local", "Delhi", "Pune", "09:15", "14:15", 235, "Passenger", 536.09);
 
addTrain(2898, "Garib Rath", "Pune", "Delhi", "12:45", "04:30", 1516, "Passenger", 934.99);
 
addTrain(2899, "Shatabdi Express", "Ahmedabad", "Pune", "10:00", "05:00", 839, "Passenger", 780.76);
 
addTrain(2900, "Shatabdi Express", "Chennai", "Lucknow", "09:45", "05:00", 1631, "Passenger", 60.96);
 
addTrain(2901, "Rajdhani Express", "Jaipur", "Ahmedabad", "11:30", "19:00", 666, "Local", 1483.0);
 
addTrain(2902, "Suburban Local", "Lucknow", "Delhi", "19:00", "02:45", 1688, "Passenger", 501.67);
 
addTrain(2903, "Garib Rath", "Hyderabad", "Mumbai", "21:00", "07:00", 764, "Local", 119.91);
 
addTrain(2904, "MEMU", "Lucknow", "Kolkata", "00:00", "23:00", 149, "Local", 740.88);
 
addTrain(2905, "Duronto Express", "Delhi", "Kolkata", "09:15", "21:00", 1686, "Passenger", 1434.61);
 
addTrain(2906, "Suburban Local", "Delhi", "Ahmedabad", "11:45", "21:45", 481, "Local", 1288.54);
 
addTrain(2907, "Mail Express", "Jaipur", "Mumbai", "21:00", "09:45", 900, "Express", 1688.58); 

addTrain(2908, "Garib Rath", "Lucknow", "Pune", "10:00", "10:00", 1843, "Express", 1819.18);

 addTrain(2909, "Mail Express", "Ahmedabad", "Kolkata", "07:00", "05:45", 1918, "Express", 185.32); 

 addTrain(2910, "Mail Express", "Delhi", "Hyderabad", "15:00", "01:00", 1753, "Passenger", 1018.91);

  addTrain(2911, "MEMU", "Chennai", "Mumbai", "23:00", "05:00", 463, "Express", 1692.3);

addTrain(2912, "Superfast Express", "Kolkata", "Ahmedabad", "00:15", "23:45", 1662, "Local", 104.25);
 
addTrain(2913, "Rajdhani Express", "Hyderabad", "Lucknow", "11:45", "13:15", 1288, "Express", 555.09);
 
addTrain(2914, "Jan Shatabdi", "Delhi", "Lucknow", "12:15", "09:15", 345, "Passenger", 985.85);
 
addTrain(2915, "Superfast Express", "Hyderabad", "Chennai", "19:45", "13:00", 1655, "Passenger", 383.37);
 
addTrain(2916, "Superfast Express", "Lucknow", "Delhi", "16:30", "15:45", 1606, "Passenger", 570.23);
 
addTrain(2917, "Garib Rath", "Pune", "Chennai", "16:15", "15:15", 1651, "Express", 1876.76);
 
addTrain(2918, "Jan Shatabdi", "Ahmedabad", "Mumbai", "04:00", "14:15", 960, "Passenger", 1468.74);
 
addTrain(2919, "Jan Shatabdi", "Chennai", "Pune", "19:15", "11:00", 1279, "Express", 20.2);
 
addTrain(2920, "Suburban Local", "Bangalore", "Hyderabad", "15:15", "16:30", 1232, "Express", 264.1);
 
addTrain(2921, "Shatabdi Express", "Ahmedabad", "Chennai", "02:30", "03:00", 1800, "Express", 586.97);
 
addTrain(2922, "Jan Shatabdi", "Pune", "Jaipur", "02:45", "01:15", 1155, "Local", 1919.01);
 
addTrain(2923, "MEMU", "Chennai", "Jaipur", "13:00", "20:45", 280, "Express", 144.15);
 
addTrain(2924, "MEMU", "Pune", "Delhi", "19:15", "18:45", 1775, "Local", 526.22);

 addTrain(2925, "Duronto Express", "Bangalore", "Chennai", "22:00", "03:15", 1968, "Express", 1235.94);

  addTrain(2926, "Duronto Express", "Pune", "Chennai", "05:45", "12:15", 1311, "Local", 1804.85); 

  addTrain(2927, "Duronto Express", "Jaipur", "Kolkata", "17:00", "06:15", 1639, "Express", 1147.4);

   addTrain(2928, "Superfast Express", "Hyderabad", "Mumbai", "23:30", "06:45", 1994, "Local", 1695.95);

addTrain(2929, "Rajdhani Express", "Hyderabad", "Bangalore", "02:30", "20:00", 1081, "Passenger", 618.41);
 
addTrain(2930, "MEMU", "Kolkata", "Chennai", "08:30", "01:15", 1926, "Passenger", 1809.2);
 
addTrain(2931, "MEMU", "Bangalore", "Pune", "11:45", "15:00", 590, "Local", 1666.09);
 
addTrain(2932, "Jan Shatabdi", "Jaipur", "Mumbai", "11:45", "23:15", 1378, "Express", 198.19);
 
addTrain(2933, "Mail Express", "Delhi", "Mumbai", "10:45", "19:00", 276, "Passenger", 457.29);
 
addTrain(2934, "Shatabdi Express", "Hyderabad", "Lucknow", "15:15", "06:30", 604, "Local", 1697.08);
 
addTrain(2935, "Garib Rath", "Mumbai", "Hyderabad", "22:30", "15:30", 1506, "Passenger", 1318.3);
 
addTrain(2936, "Garib Rath", "Jaipur", "Ahmedabad", "21:15", "19:30", 321, "Express", 142.11);
 
addTrain(2937, "Jan Shatabdi", "Delhi", "Bangalore", "11:15", "07:15", 978, "Passenger", 1637.52);
 
addTrain(2938, "Rajdhani Express", "Kolkata", "Lucknow", "09:30", "18:45", 1620, "Passenger", 889.04);
 
addTrain(2939, "Superfast Express", "Ahmedabad", "Jaipur", "15:45", "17:45", 684, "Express", 987.21);
 
addTrain(2940, "Garib Rath", "Chennai", "Delhi", "01:45", "15:15", 207, "Express", 1338.99);

 addTrain(2941, "Garib Rath", "Hyderabad", "Kolkata", "22:30", "20:45", 1614, "Express", 1501.47); 

 addTrain(2942, "Rajdhani Express", "Mumbai", "Ahmedabad", "14:45", "19:45", 1796, "Passenger", 1587.99);

  addTrain(2943, "Superfast Express", "Chennai", "Lucknow", "21:00", "09:30", 1860, "Passenger", 489.01);


   addTrain(2944, "Duronto Express", "Jaipur", "Lucknow", "08:15", "21:00", 106, "Local", 126.58);

addTrain(2945, "Rajdhani Express", "Ahmedabad", "Lucknow", "23:30", "17:30", 1747, "Express", 1686.4);

 
addTrain(2946, "Rajdhani Express", "Jaipur", "Ahmedabad", "03:30", "20:30", 1701, "Passenger", 291.03);
 
addTrain(2947, "Superfast Express", "Jaipur", "Chennai", "06:15", "13:45", 1055, "Express", 265.91);
 
addTrain(2948, "MEMU", "Pune", "Delhi", "12:30", "11:45", 1235, "Passenger", 1111.3);
 
addTrain(2949, "MEMU", "Ahmedabad", "Bangalore", "19:30", "07:30", 1841, "Passenger", 1786.55);
 
addTrain(2950, "Duronto Express", "Hyderabad", "Mumbai", "13:45", "00:30", 1902, "Local", 1178.72);
 
addTrain(2951, "MEMU", "Mumbai", "Jaipur", "08:15", "03:30", 53, "Passenger", 1573.9);
 
addTrain(2952, "Superfast Express", "Chennai", "Ahmedabad", "01:00", "13:00", 193, "Local", 455.76);
 
addTrain(2953, "MEMU", "Kolkata", "Pune", "15:00", "23:00", 1865, "Passenger", 926.05);
 
addTrain(2954, "Garib Rath", "Kolkata", "Pune", "23:00", "17:00", 1708, "Local", 400.88);
 
addTrain(2955, "Superfast Express", "Ahmedabad", "Pune", "06:15", "08:45", 1441, "Express", 1450.28);
 
addTrain(2956, "Intercity Express", "Ahmedabad", "Mumbai", "08:30", "05:45", 746, "Passenger", 29.83);
 
addTrain(2957, "Duronto Express", "Lucknow", "Chennai", "14:15", "07:30", 805, "Express", 1616.08);

 addTrain(2958, "Garib Rath", "Bangalore", "Hyderabad", "07:00", "02:00", 732, "Passenger", 1863.0); 

 addTrain(2959, "MEMU", "Ahmedabad", "Kolkata", "08:15", "19:15", 1339, "Passenger", 524.1);

  addTrain(2960, "Superfast Express", "Chennai", "Hyderabad", "02:00", "21:30", 578, "Local", 930.82); 

  addTrain(2961, "Rajdhani Express", "Pune", "Ahmedabad", "17:30", "01:45", 228, "Local", 1772.98);

addTrain(2962, "Rajdhani Express", "Chennai", "Bangalore", "05:00", "07:30", 1157, "Passenger", 1483.29);

 
addTrain(2963, "Shatabdi Express", "Delhi", "Chennai", "17:00", "16:15", 1068, "Local", 414.28);
 
addTrain(2964, "Shatabdi Express", "Chennai", "Lucknow", "01:45", "05:30", 490, "Passenger", 567.99);
 
addTrain(2965, "Garib Rath", "Lucknow", "Chennai", "14:30", "03:45", 1404, "Passenger", 1114.19);
 
addTrain(2966, "Shatabdi Express", "Hyderabad", "Jaipur", "07:15", "01:45", 1108, "Express", 1506.28);
 
addTrain(2967, "Duronto Express", "Chennai", "Ahmedabad", "09:00", "07:45", 479, "Local", 1352.07);
 
addTrain(2968, "Duronto Express", "Pune", "Ahmedabad", "05:45", "20:15", 1280, "Express", 337.21);
 
addTrain(2969, "Rajdhani Express", "Mumbai", "Jaipur", "11:15", "03:30", 680, "Local", 500.71);
 
addTrain(2970, "MEMU", "Kolkata", "Ahmedabad", "15:15", "04:30", 398, "Passenger", 394.81);
 
addTrain(2971, "Intercity Express", "Kolkata", "Jaipur", "05:00", "23:15", 607, "Passenger", 936.42);
 
addTrain(2972, "Jan Shatabdi", "Lucknow", "Hyderabad", "21:45", "03:15", 438, "Express", 1607.13);
 
addTrain(2973, "Garib Rath", "Jaipur", "Delhi", "16:15", "02:00", 167, "Express", 798.03); 

addTrain(2974, "Rajdhani Express", "Kolkata", "Jaipur", "15:15", "02:30", 1516, "Express", 572.36);

addTrain(2975, "MEMU", "Hyderabad", "Lucknow", "23:30", "23:30", 1975, "Local", 1829.44); 

addTrain(2976, "Jan Shatabdi", "Kolkata", "Ahmedabad", "23:45", "20:30", 158, "Passenger", 1108.36); 

addTrain(2977, "Suburban Local", "Bangalore", "Hyderabad", "07:00", "12:00", 1719, "Local", 597.14);

addTrain(2978, "MEMU", "Pune", "Ahmedabad", "17:30", "13:30", 1100, "Express", 806.51);
 
addTrain(2979, "Mail Express", "Kolkata", "Hyderabad", "16:30", "03:30", 1849, "Local", 88.58);
 
addTrain(2980, "Rajdhani Express", "Mumbai", "Lucknow", "11:00", "06:45", 1597, "Passenger", 1975.2);
 
addTrain(2981, "Jan Shatabdi", "Jaipur", "Pune", "13:45", "20:15", 1556, "Local", 1314.04);
 
addTrain(2982, "Jan Shatabdi", "Delhi", "Lucknow", "15:45", "23:45", 691, "Express", 1556.54);
 
addTrain(2983, "Garib Rath", "Chennai", "Lucknow", "16:45", "02:15", 707, "Passenger", 1125.95);
 
addTrain(2984, "Shatabdi Express", "Lucknow", "Kolkata", "11:30", "20:00", 51, "Local", 1513.58);
 
addTrain(2985, "Shatabdi Express", "Lucknow", "Mumbai", "05:30", "09:15", 1394, "Express", 1561.81);
 
addTrain(2986, "Superfast Express", "Mumbai", "Bangalore", "22:00", "15:30", 907, "Express", 1772.67);
 
addTrain(2987, "Garib Rath", "Lucknow", "Chennai", "07:45", "13:00", 744, "Express", 1817.22);
 
addTrain(2988, "MEMU", "Delhi", "Lucknow", "21:45", "14:30", 1639, "Local", 166.02);
 
addTrain(2989, "MEMU", "Mumbai", "Bangalore", "14:45", "14:45", 1769, "Passenger", 198.13);
 
addTrain(2990, "Rajdhani Express", "Lucknow", "Chennai", "18:30", "18:00", 1219, "Express", 613.61);

 addTrain(2991, "Jan Shatabdi", "Bangalore", "Mumbai", "00:30", "04:45", 953, "Local", 1339.3);

  addTrain(2992, "Shatabdi Express", "Delhi", "Chennai", "08:15", "05:15", 586, "Express", 670.85); 

  addTrain(2993, "Rajdhani Express", "Pune", "Kolkata", "17:15", "13:15", 844, "Express", 600.49); 

  addTrain(2994, "Superfast Express", "Mumbai", "Delhi", "05:15", "08:00", 725, "Express", 454.44);

addTrain(2995, "Shatabdi Express", "Chennai", "Jaipur", "08:30", "18:15", 1285, "Local", 798.5);
 
addTrain(2996, "Superfast Express", "Bangalore", "Chennai", "04:15", "04:15", 1977, "Local", 534.03);
 
addTrain(2997, "Mail Express", "Mumbai", "Ahmedabad", "10:45", "08:45", 1444, "Local", 1243.44);
 
addTrain(2998, "Intercity Express", "Chennai", "Jaipur", "09:30", "02:45", 772, "Local", 1675.27);
 
addTrain(2999, "Shatabdi Express", "Mumbai", "Bangalore", "14:30", "19:15", 280, "Express", 838.55);
 
addTrain(3000, "Superfast Express", "Mumbai", "Delhi", "04:00", "15:45", 227, "Passenger", 1673.65);
 
addTrain(3001, "Intercity Express", "Kolkata", "Hyderabad", "22:30", "10:15", 1062, "Express", 552.94);
 
addTrain(3002, "Superfast Express", "Ahmedabad", "Bangalore", "15:45", "14:00", 1033, "Passenger", 323.56);
 
addTrain(3003, "Jan Shatabdi", "Delhi", "Lucknow", "13:00", "02:30", 1508, "Express", 1908.5);
 
addTrain(3004, "Superfast Express", "Mumbai", "Delhi", "00:15", "23:30", 941, "Local", 1356.15);
 
addTrain(3005, "Duronto Express", "Delhi", "Ahmedabad", "09:00", "18:45", 466, "Local", 1288.03);
 
addTrain(3006, "MEMU", "Delhi", "Jaipur", "08:45", "15:30", 690, "Express", 286.8); 

addTrain(3007, "Mail Express", "Bangalore", "Chennai", "21:30", "00:15", 642, "Local", 1885.97); 

addTrain(3008, "MEMU", "Delhi", "Lucknow", "18:00", "17:15", 1721, "Passenger", 189.47);

 addTrain(3009, "Mail Express", "Mumbai", "Kolkata", "04:15", "21:45", 1840, "Passenger", 371.92);

  addTrain(3010, "Intercity Express", "Hyderabad", "Chennai", "23:00", "04:00", 281, "Express", 841.91);

addTrain(3011, "Intercity Express", "Jaipur", "Delhi", "06:15", "02:30", 1708, "Passenger", 1890.87);
 
addTrain(3012, "Rajdhani Express", "Chennai", "Hyderabad", "20:30", "13:30", 1289, "Passenger", 801.37);
 
addTrain(3013, "Mail Express", "Delhi", "Bangalore", "13:00", "10:45", 1288, "Passenger", 1491.81);
 
addTrain(3014, "Shatabdi Express", "Ahmedabad", "Lucknow", "12:45", "14:30", 1377, "Express", 1938.06);
 
addTrain(3015, "Intercity Express", "Mumbai", "Delhi", "05:30", "07:45", 1931, "Passenger", 116.82);
 
addTrain(3016, "Intercity Express", "Chennai", "Lucknow", "18:15", "12:15", 1281, "Local", 1160.38);
 
addTrain(3017, "MEMU", "Bangalore", "Delhi", "14:45", "05:45", 1692, "Express", 1513.53);
 
addTrain(3018, "Garib Rath", "Lucknow", "Pune", "15:00", "11:00", 1076, "Local", 249.78);
 
addTrain(3019, "Shatabdi Express", "Ahmedabad", "Hyderabad", "22:30", "10:15", 1369, "Express", 1109.09);
 
addTrain(3020, "Duronto Express", "Mumbai", "Delhi", "14:00", "11:00", 1754, "Local", 1629.76);
 
addTrain(3021, "Jan Shatabdi", "Lucknow", "Delhi", "01:45", "02:00", 515, "Passenger", 745.45);
 
addTrain(3022, "Jan Shatabdi", "Lucknow", "Ahmedabad", "19:45", "14:15", 1602, "Local", 1414.67);
 
addTrain(3023, "Superfast Express", "Pune", "Ahmedabad", "19:45", "01:00", 27, "Express", 198.83); 

addTrain(3024, "Duronto Express", "Jaipur", "Hyderabad", "06:45", "15:00", 1861, "Local", 54.19);

 addTrain(3025, "Shatabdi Express", "Kolkata", "Chennai", "07:30", "17:30", 676, "Local", 987.73);

  addTrain(3026, "Suburban Local", "Lucknow", "Delhi", "09:00", "12:45", 893, "Passenger", 618.54); 

  addTrain(3027, "MEMU", "Kolkata", "Delhi", "04:30", "17:45", 631, "Passenger", 1165.28);

addTrain(3028, "MEMU", "Hyderabad", "Ahmedabad", "15:15", "19:15", 1485, "Local", 1981.93);
 
addTrain(3029, "Suburban Local", "Jaipur", "Bangalore", "07:30", "10:30", 346, "Local", 1655.59);
 
addTrain(3030, "Suburban Local", "Lucknow", "Delhi", "14:00", "03:15", 1747, "Passenger", 379.53);
 
addTrain(3031, "Mail Express", "Chennai", "Hyderabad", "01:45", "02:45", 47, "Express", 1988.65);
 
addTrain(3032, "Duronto Express", "Mumbai", "Chennai", "19:30", "07:30", 1020, "Passenger", 603.01);
 
addTrain(3033, "Shatabdi Express", "Jaipur", "Hyderabad", "11:45", "04:30", 44, "Passenger", 789.58);
 
addTrain(3034, "Jan Shatabdi", "Pune", "Bangalore", "06:00", "01:00", 1517, "Passenger", 967.34);
 
addTrain(3035, "Jan Shatabdi", "Bangalore", "Lucknow", "06:15", "20:15", 243, "Express", 531.82);
 
addTrain(3036, "Rajdhani Express", "Kolkata", "Hyderabad", "20:30", "09:00", 754, "Express", 92.9);
 
addTrain(3037, "Duronto Express", "Pune", "Ahmedabad", "23:30", "12:45", 843, "Passenger", 1660.75);
 
addTrain(3038, "Duronto Express", "Hyderabad", "Delhi", "21:00", "10:15", 1145, "Express", 247.39);
 
addTrain(3039, "Superfast Express", "Chennai", "Lucknow", "17:45", "11:00", 1744, "Express", 973.09); 

addTrain(3040, "Intercity Express", "Lucknow", "Mumbai", "11:00", "20:45", 23, "Local", 1006.64);

 addTrain(3041, "Jan Shatabdi", "Hyderabad", "Chennai", "14:30", "12:45", 321, "Express", 1327.25);

  addTrain(3042, "Garib Rath", "Kolkata", "Chennai", "09:30", "03:15", 1857, "Express", 1183.66); 

  addTrain(3043, "Garib Rath", "Hyderabad", "Jaipur", "10:45", "08:15", 1213, "Passenger", 1962.91);

addTrain(3044, "MEMU", "Ahmedabad", "Delhi", "05:45", "20:45", 983, "Local", 59.5);

 
addTrain(3045, "Mail Express", "Chennai", "Ahmedabad", "11:30", "05:15", 337, "Passenger", 1231.36);
 
addTrain(3046, "Jan Shatabdi", "Hyderabad", "Ahmedabad", "11:45", "19:00", 1301, "Passenger", 1777.91);
 
addTrain(3047, "Garib Rath", "Mumbai", "Hyderabad", "06:15", "08:15", 1921, "Local", 1327.42);
 
addTrain(3048, "MEMU", "Bangalore", "Kolkata", "22:30", "19:00", 1007, "Passenger", 1910.19);
 
addTrain(3049, "Shatabdi Express", "Kolkata", "Mumbai", "02:30", "19:00", 1501, "Express", 1681.16);
 
addTrain(3050, "Superfast Express", "Mumbai", "Lucknow", "14:00", "09:45", 841, "Local", 1665.25);
 
addTrain(3051, "Shatabdi Express", "Jaipur", "Mumbai", "00:15", "00:15", 1505, "Express", 1121.95);
 
addTrain(3052, "Duronto Express", "Hyderabad", "Mumbai", "05:00", "12:45", 966, "Express", 421.08);
 
addTrain(3053, "MEMU", "Delhi", "Kolkata", "11:45", "18:30", 1135, "Express", 951.45);
 
addTrain(3054, "Rajdhani Express", "Pune", "Hyderabad", "20:15", "05:00", 978, "Passenger", 1486.87);
 
addTrain(3055, "Mail Express", "Chennai", "Bangalore", "19:00", "03:30", 1622, "Express", 426.45);
 
addTrain(3056, "Jan Shatabdi", "Delhi", "Ahmedabad", "14:00", "19:45", 41, "Local", 879.89); 

addTrain(3057, "Rajdhani Express", "Hyderabad", "Bangalore", "08:00", "03:45", 1827, "Express", 1347.47);

 addTrain(3058, "Duronto Express", "Chennai", "Hyderabad", "18:15", "07:15", 968, "Local", 1176.79);
 
addTrain(3059, "Duronto", "Bangalore", "Lucknow", "22:15", "14:15", 1429, "Local", 717.63); 

addTrain(3060, "MEMU", "Ahmedabad", "Pune", "12:00", "08:15", 90, "Passenger", 1222.49);

addTrain(3061, "Superfast Express", "Mumbai", "Jaipur", "13:00", "01:15", 1141, "Local", 108.73);
 
addTrain(3062, "Rajdhani Express", "Kolkata", "Mumbai", "01:30", "01:15", 306, "Local", 750.71);
 
addTrain(3063, "Garib Rath", "Delhi", "Pune", "17:15", "21:15", 393, "Express", 1175.16);
 
addTrain(3064, "Mail Express", "Ahmedabad", "Kolkata", "13:45", "04:00", 377, "Local", 561.0);
 
addTrain(3065, "Rajdhani Express", "Jaipur", "Hyderabad", "10:30", "00:00", 845, "Passenger", 664.55);
 
addTrain(3066, "MEMU", "Lucknow", "Hyderabad", "10:15", "01:45", 1801, "Express", 1182.08);
 
addTrain(3067, "Shatabdi Express", "Chennai", "Pune", "12:15", "13:30", 1927, "Passenger", 1575.93);
 
addTrain(3068, "Jan Shatabdi", "Hyderabad", "Mumbai", "04:45", "04:45", 897, "Passenger", 619.75);
 
addTrain(3069, "Jan Shatabdi", "Chennai", "Bangalore", "14:30", "13:15", 302, "Passenger", 91.46);
 
addTrain(3070, "Shatabdi Express", "Chennai", "Pune", "06:15", "23:15", 30, "Express", 167.51);
 
addTrain(3071, "Jan Shatabdi", "Ahmedabad", "Jaipur", "23:30", "00:00", 1174, "Local", 947.2);
 
addTrain(3072, "Intercity Express", "Ahmedabad", "Delhi", "08:00", "20:45", 94, "Local", 1764.12);

 addTrain(3073, "Duronto Express", "Ahmedabad", "Mumbai", "05:15", "00:15", 1245, "Express", 1083.02);

  addTrain(3074, "MEMU", "Lucknow", "Chennai", "11:45", "19:30", 1460, "Local", 1940.48);

addTrain(3075, "Mail Express", "Mumbai", "Hyderabad", "19:45", "18:45", 1893, "Local", 795.48);

 addTrain(3076, "Suburban Local", "Jaipur", "Chennai", "13:30", "01:45", 417, "Local", 655.12);

addTrain(3077, "Suburban Local", "Ahmedabad", "Bangalore", "19:45", "15:45", 1893, "Local", 1462.13);
 
addTrain(3078, "Rajdhani Express", "Mumbai", "Delhi", "17:15", "12:30", 359, "Express", 483.49);
 
addTrain(3079, "Jan Shatabdi", "Ahmedabad", "Lucknow", "05:15", "15:45", 1806, "Passenger", 1045.72);
 
addTrain(3080, "Garib Rath", "Ahmedabad", "Hyderabad", "14:45", "22:30", 1248, "Express", 860.51);
 
addTrain(3081, "Jan Shatabdi", "Bangalore", "Delhi", "10:30", "06:45", 1591, "Local", 1726.18);
 
addTrain(3082, "Garib Rath", "Ahmedabad", "Jaipur", "15:45", "20:45", 888, "Passenger", 435.59);
 
addTrain(3083, "Shatabdi Express", "Ahmedabad", "Delhi", "15:45", "21:30", 1515, "Express", 603.04);
 
addTrain(3084, "Superfast Express", "Mumbai", "Bangalore", "20:15", "04:30", 842, "Passenger", 533.72);
 
addTrain(3085, "Duronto Express", "Kolkata", "Delhi", "00:00", "08:00", 830, "Passenger", 356.79);
 
addTrain(3086, "Suburban Local", "Jaipur", "Pune", "08:45", "06:00", 1767, "Passenger", 46.28);
 
addTrain(3087, "Duronto Express", "Lucknow", "Chennai", "13:00", "11:15", 838, "Passenger", 1481.74);
 
addTrain(3088, "Suburban Local", "Kolkata", "Jaipur", "22:00", "02:30", 813, "Express", 1808.47);
 
addTrain(3089, "Jan Shatabdi", "Lucknow", "Ahmedabad", "09:45", "16:00", 1279, "Passenger", 1292.62);

 addTrain(3090, "Duronto Express", "Delhi", "Mumbai", "05:30", "22:00", 391, "Local", 757.16); 

 addTrain(3091, "Garib Rath", "Bangalore", "Kolkata", "10:30", "07:30", 148, "Local", 891.13); 

 addTrain(3092, "Duronto", "Pune", "Hyderabad", "18:30", "08:00", 1062, "Local", 81.02);

  addTrain(3093, "Suburban Local", "Bangalore", "Pune", "00:45", "13:45", 1600, "Local", 1512.89);

addTrain(3094, "Shatabdi Express", "Lucknow", "Jaipur", "12:00", "19:30", 591, "Local", 1276.04);
 
addTrain(3095, "Suburban Local", "Jaipur", "Ahmedabad", "19:15", "22:15", 626, "Local", 1699.79);
 
addTrain(3096, "Superfast Express", "Kolkata", "Bangalore", "11:45", "14:15", 1518, "Express", 979.76);
 
addTrain(3097, "Superfast Express", "Delhi", "Jaipur", "01:15", "19:15", 517, "Express", 1027.03);
 
addTrain(3098, "Mail Express", "Delhi", "Bangalore", "11:00", "02:45", 237, "Local", 713.13);
 
addTrain(3099, "Intercity Express", "Kolkata", "Hyderabad", "20:15", "17:00", 1544, "Passenger", 34.37);
 
addTrain(3100, "Shatabdi Express", "Mumbai", "Chennai", "16:00", "14:00", 398, "Passenger", 989.18);
 
addTrain(3101, "Garib Rath", "Lucknow", "Kolkata", "02:45", "08:15", 1337, "Local", 539.59);
 
addTrain(3102, "Suburban Local", "Jaipur", "Kolkata", "16:00", "01:00", 1814, "Local", 194.91);
 
addTrain(3103, "Superfast Express", "Mumbai", "Jaipur", "08:15", "20:30", 1519, "Local", 206.68);
 
addTrain(3104, "Jan Shatabdi", "Chennai", "Kolkata", "05:00", "10:45", 1901, "Passenger", 1613.26);
 
addTrain(3105, "Suburban Local", "Lucknow", "Pune", "22:15", "17:30", 715, "Passenger", 372.09); 

addTrain(3106, "Superfast Express", "Lucknow", "Mumbai", "23:00", "02:15", 1359, "Local", 1741.64); 

addTrain(3107, "Shatabdi Express", "Mumbai", "Pune", "21:45", "22:00", 897, "Express", 1833.07); 

addTrain(3108, "Duronto Express", "Kolkata", "Bangalore", "10:15", "10:00", 880, "Local", 1912.22);

 addTrain(3109, "Suburban Local", "Delhi", "Jaipur", "17:45", "12:30", 66, "Express", 808.41);

addTrain(3110, "MEMU", "Mumbai", "Delhi", "11:15", "06:00", 378, "Express", 1204.55);
 
addTrain(3111, "Suburban Local", "Delhi", "Mumbai", "00:30", "10:00", 818, "Passenger", 1499.42);
 
addTrain(3112, "Mail Express", "Chennai", "Pune", "22:30", "13:15", 505, "Passenger", 81.23);
 
addTrain(3113, "Shatabdi Express", "Hyderabad", "Pune", "12:45", "22:00", 1047, "Local", 467.56);
 
addTrain(3114, "MEMU", "Lucknow", "Bangalore", "12:45", "22:30", 1540, "Express", 1045.4);
 
addTrain(3115, "Superfast Express", "Lucknow", "Mumbai", "13:15", "10:00", 112, "Express", 421.88);
 
addTrain(3116, "MEMU", "Chennai", "Delhi", "09:30", "12:30", 1298, "Express", 1487.74);
 
addTrain(3117, "Rajdhani Express", "Jaipur", "Delhi", "22:45", "04:15", 373, "Local", 140.87);
 
addTrain(3118, "Mail Express", "Delhi", "Kolkata", "01:45", "09:00", 1189, "Passenger", 1443.83);
 
addTrain(3119, "Superfast Express", "Delhi", "Pune", "10:00", "20:30", 514, "Passenger", 808.02);
 
addTrain(3120, "Jan Shatabdi", "Ahmedabad", "Jaipur", "21:00", "16:30", 682, "Local", 1951.35);
 
addTrain(3121, "Garib Rath", "Lucknow", "Mumbai", "02:30", "00:15", 1298, "Express", 916.16);
 
addTrain(3122, "Superfast Express", "Chennai", "Lucknow", "01:45", "14:00", 621, "Local", 655.35); 

addTrain(3123, "Garib Rath", "Chennai", "Delhi", "22:00", "00:15", 1348, "Passenger", 1315.53); 

addTrain(3124, "Intercity Express", "Jaipur", "Ahmedabad", "04:30", "11:15", 393, "Express", 1351.5);

 addTrain(3125, "Intercity", "Lucknow", "Bangalore", "13:15", "15:00", 857, "Local", 1821.04); 

 addTrain(3126, "Duronto Express", "Hyderabad", "Chennai", "21:15", "07:15", 1050, "Express", 1249.57);

addTrain(3127, "Intercity Express", "Hyderabad", "Kolkata", "04:30", "06:45", 52, "Local", 673.74);
 
addTrain(3128, "MEMU", "Mumbai", "Kolkata", "12:45", "22:00", 903, "Passenger", 1238.04);
 
addTrain(3129, "Garib Rath", "Jaipur", "Pune", "19:45", "09:45", 1948, "Local", 671.04);
 
addTrain(3130, "Mail Express", "Chennai", "Delhi", "06:45", "18:15", 1640, "Passenger", 736.43);
 
addTrain(3131, "Mail Express", "Ahmedabad", "Pune", "09:45", "14:15", 830, "Passenger", 1532.7);
 
addTrain(3132, "Suburban Local", "Hyderabad", "Ahmedabad", "12:00", "11:15", 1480, "Express", 542.52);
 
addTrain(3133, "Jan Shatabdi", "Lucknow", "Jaipur", "10:30", "23:15", 301, "Passenger", 1733.98);
 
addTrain(3134, "Intercity Express", "Ahmedabad", "Jaipur", "00:45", "00:30", 609, "Local", 641.31);
 
addTrain(3135, "Mail Express", "Delhi", "Chennai", "09:45", "05:00", 696, "Express", 1334.35);
 
addTrain(3136, "Mail Express", "Kolkata", "Pune", "14:00", "03:30", 1069, "Local", 843.49);
 
addTrain(3137, "Duronto Express", "Kolkata", "Jaipur", "11:30", "16:15", 1388, "Local", 1513.48);
 
addTrain(3138, "Jan Shatabdi", "Bangalore", "Jaipur", "05:45", "05:00", 134, "Passenger", 852.39);

 addTrain(3139, "Mail Express", "Bangalore", "Pune", "17:30", "01:00", 1774, "Passenger", 489.71);
 
 addTrain(3140, "Rajdhani Express", "Kolkata", "Lucknow", "09:15", "06:00", 1222, "Local", 627.83); 

 addTrain(3141, "Suburban Local", "Delhi", "Pune", "03:45", "18:00", 78, "Passenger", 131.59);

  addTrain(3142, "Mail Express", "Jaipur", "Chennai", "16:00", "09:15", 1052, "Express", 1132.72);

addTrain(3143, "Mail Express", "Bangalore", "Lucknow", "09:45", "11:00", 1770, "Express", 336.82);
 
addTrain(3144, "Superfast Express", "Chennai", "Hyderabad", "05:00", "08:30", 313, "Passenger", 400.62);
 
addTrain(3145, "Intercity Express", "Delhi", "Ahmedabad", "20:45", "00:15", 959, "Passenger", 1788.27);
 
addTrain(3146, "Suburban Local", "Delhi", "Hyderabad", "04:45", "04:00", 1967, "Passenger", 1333.94);
 
addTrain(3147, "MEMU", "Jaipur", "Mumbai", "05:15", "22:30", 956, "Passenger", 1797.39);
 
addTrain(3148, "Suburban Local", "Bangalore", "Kolkata", "14:00", "17:30", 1836, "Express", 231.08);
 
addTrain(3149, "Garib Rath", "Lucknow", "Hyderabad", "02:30", "17:00", 908, "Local", 1517.08);
 
addTrain(3150, "Rajdhani Express", "Kolkata", "Jaipur", "13:30", "03:00", 883, "Local", 925.74);
 
addTrain(3151, "Superfast Express", "Pune", "Chennai", "19:30", "01:00", 1307, "Express", 451.93);
 
addTrain(3152, "Duronto Express", "Bangalore", "Delhi", "08:30", "17:30", 1141, "Passenger", 446.35);
 
addTrain(3153, "Suburban Local", "Lucknow", "Jaipur", "13:15", "16:15", 1815, "Passenger", 1483.35);
 
addTrain(3154, "Garib Rath", "Bangalore", "Mumbai", "08:45", "07:15", 72, "Local", 549.43);
 
addTrain(3155, "MEMU", "Lucknow", "Kolkata", "03:15", "09:45", 275, "Express", 1284.45);

 addTrain(3156, "Intercity Express", "Chennai", "Ahmedabad", "16:30", "12:15", 1091, "Local", 1948.39);

  addTrain(3157, "Jan Shatabdi", "Jaipur", "Pune", "23:15", "08:30", 1523, "Express", 75.23);
 
addTrain(3158, "Suburban Local", "Lucknow", "Chennai", "06:15", "06:15", 1356, "Passenger", 176.56);

 addTrain(3159, "Suburban Local", "Chennai", "Bangalore", "17:15", "00:00", 240, "Express", 95.62);

addTrain(3160, "Rajdhani Express", "Ahmedabad", "Hyderabad", "01:15", "17:30", 1687, "Local", 636.09);
 
addTrain(3161, "MEMU", "Hyderabad", "Pune", "02:00", "06:45", 1988, "Express", 99.31);
 
addTrain(3162, "Intercity Express", "Mumbai", "Lucknow", "20:30", "22:15", 899, "Express", 588.72);
 
addTrain(3163, "Jan Shatabdi", "Mumbai", "Bangalore", "14:00", "02:45", 1304, "Local", 898.69);
 
addTrain(3164, "Mail Express", "Jaipur", "Chennai", "20:30", "07:00", 1305, "Local", 1322.93);
 
addTrain(3165, "Jan Shatabdi", "Pune", "Ahmedabad", "22:30", "13:00", 1591, "Local", 712.91);
 
addTrain(3166, "Garib Rath", "Lucknow", "Delhi", "17:45", "19:30", 1426, "Local", 1693.03);
 
addTrain(3167, "Suburban Local", "Mumbai", "Ahmedabad", "19:30", "00:15", 52, "Passenger", 1922.48);
 
addTrain(3168, "Garib Rath", "Kolkata", "Hyderabad", "01:45", "23:30", 1049, "Express", 1724.21);
 
addTrain(3169, "Jan Shatabdi", "Bangalore", "Lucknow", "12:15", "17:15", 1950, "Local", 1649.7);
 
addTrain(3170, "Rajdhani Express", "Ahmedabad", "Jaipur", "18:15", "06:45", 1914, "Passenger", 1980.96);
 
addTrain(3171, "Superfast Express", "Mumbai", "Hyderabad", "00:15", "06:30", 521, "Passenger", 1966.86); 

addTrain(3172, "Intercity Express", "Chennai", "Hyderabad", "12:15", "04:30", 1485, "Express", 256.48);

 addTrain(3173, "Mail Express", "Chennai", "Pune", "16:15", "16:45", 117, "Express", 1030.22);

  addTrain(3174, "Shatabdi Express", "Ahmedabad", "Delhi", "17:15", "14:15", 960, "Local", 1240.27);

   addTrain(3175, "Intercity Express", "Mumbai", "Lucknow", "13:30", "13:45", 1651, "Local", 1229.38);

addTrain(3176, "Jan Shatabdi", "Lucknow", "Hyderabad", "18:45", "14:15", 1664, "Passenger", 1079.27);
 
addTrain(3177, "Mail Express", "Bangalore", "Chennai", "03:30", "22:45", 1354, "Local", 759.0);
 
addTrain(3178, "Shatabdi Express", "Hyderabad", "Lucknow", "21:45", "08:30", 1732, "Express", 457.47);
 
addTrain(3179, "Intercity Express", "Hyderabad", "Bangalore", "18:00", "17:15", 612, "Express", 265.63);
 
addTrain(3180, "Superfast Express", "Lucknow", "Ahmedabad", "12:15", "23:00", 850, "Passenger", 680.78);
 
addTrain(3181, "Garib Rath", "Bangalore", "Lucknow", "04:15", "20:15", 1158, "Passenger", 168.19);
 
addTrain(3182, "Rajdhani Express", "Delhi", "Lucknow", "14:30", "14:45", 1869, "Local", 1835.26);
 
addTrain(3183, "MEMU", "Bangalore", "Delhi", "01:45", "13:30", 745, "Passenger", 1314.18);
 
addTrain(3184, "Suburban Local", "Delhi", "Ahmedabad", "02:45", "12:15", 1624, "Local", 677.63);
 
addTrain(3185, "Superfast Express", "Pune", "Jaipur", "21:30", "07:15", 1055, "Passenger", 171.38);
 
addTrain(3186, "Garib Rath", "Mumbai", "Hyderabad", "09:45", "13:15", 730, "Express", 25.61);
 
addTrain(3187, "Intercity Express", "Delhi", "Mumbai", "04:00", "10:00", 899, "Express", 1275.94);
 
addTrain(3188, "Superfast Express", "Delhi", "Kolkata", "08:45", "12:15", 1657, "Passenger", 296.99); 

addTrain(3189, "MEMU", "Jaipur", "Ahmedabad", "12:00", "05:00", 623, "Express", 114.22); 

addTrain(3190, "MEMU", "Mumbai", "Hyderabad", "23:15", "19:00", 769, "Passenger", 1183.12); 

addTrain(3191, "Jan Shatabdi", "Chennai", "Pune", "11:45", "15:00", 785, "Passenger", 1187.27); 

addTrain(3192, "Garib Rath", "Jaipur", "Pune", "14:45", "00:00", 59, "Local", 1687.62);

addTrain(3193, "MEMU", "Jaipur", "Chennai", "10:30", "23:45", 850, "Passenger", 1422.72);
 
addTrain(3194, "MEMU", "Delhi", "Mumbai", "21:15", "13:30", 1919, "Local", 697.82);
 
addTrain(3195, "Mail Express", "Bangalore", "Ahmedabad", "16:30", "13:15", 1651, "Local", 21.06);
 
addTrain(3196, "Mail Express", "Bangalore", "Hyderabad", "23:30", "00:30", 408, "Local", 82.45);
 
addTrain(3197, "Shatabdi Express", "Kolkata", "Lucknow", "18:15", "16:00", 1119, "Express", 1990.46);
 
addTrain(3198, "Mail Express", "Bangalore", "Pune", "04:45", "01:30", 140, "Local", 428.29);
 
addTrain(3199, "MEMU", "Chennai", "Delhi", "10:30", "07:30", 1412, "Local", 124.69);
 
addTrain(3200, "Intercity Express", "Lucknow", "Chennai", "03:00", "05:15", 1984, "Express", 461.86);
 
addTrain(3201, "Shatabdi Express", "Lucknow", "Chennai", "02:30", "06:30", 1719, "Express", 1982.46);
 
addTrain(3202, "Superfast Express", "Lucknow", "Mumbai", "10:00", "19:45", 1223, "Passenger", 492.85);
 
addTrain(3203, "Intercity Express", "Chennai", "Hyderabad", "09:00", "06:45", 915, "Local", 1421.21);
 
addTrain(3204, "Mail Express", "Lucknow", "Bangalore", "01:15", "00:00", 193, "Passenger", 1878.98);

 addTrain(3205, "Rajdhani Express", "Pune", "Hyderabad", "04:00", "21:15", 1659, "Local", 1566.12); 

 addTrain(3206, "MEMU", "Kolkata", "Pune", "18:00", "06:45", 211, "Passenger", 1964.47); 

 addTrain(3207, "Intercity Express", "Delhi", "Lucknow", "03:45", "16:15", 1596, "Passenger", 34.58);

  addTrain(3208, "Rajdhani Express", "Jaipur", "Delhi", "12:00", "07:15", 1746, "Passenger", 1302.32);

addTrain(3209, "Rajdhani Express", "Pune", "Kolkata", "06:00", "01:15", 1489, "Local", 1270.77);
 
addTrain(3210, "Mail Express", "Chennai", "Delhi", "18:00", "10:45", 907, "Express", 818.67);
 
addTrain(3211, "Superfast Express", "Lucknow", "Ahmedabad", "02:00", "15:45", 300, "Passenger", 587.02);
 
addTrain(3212, "Jan Shatabdi", "Pune", "Delhi", "13:30", "08:00", 304, "Local", 355.58);
 
addTrain(3213, "Garib Rath", "Delhi", "Jaipur", "22:15", "09:45", 1580, "Passenger", 1595.93);
 
addTrain(3214, "Jan Shatabdi", "Ahmedabad", "Pune", "00:00", "06:15", 1873, "Local", 1423.58);
 
addTrain(3215, "Intercity Express", "Pune", "Lucknow", "15:00", "01:00", 221, "Express", 828.89);
 
addTrain(3216, "Suburban Local", "Hyderabad", "Bangalore", "09:15", "08:30", 1816, "Local", 597.61);
 
addTrain(3217, "MEMU", "Mumbai", "Delhi", "00:30", "17:30", 397, "Local", 1008.36);
 
addTrain(3218, "Jan Shatabdi", "Pune", "Chennai", "04:30", "12:15", 1927, "Passenger", 1368.72);
 
addTrain(3219, "Jan Shatabdi", "Ahmedabad", "Lucknow", "13:15", "05:30", 1021, "Local", 1288.82);
 
addTrain(3220, "MEMU", "Kolkata", "Jaipur", "03:30", "07:00", 1355, "Passenger", 998.14);
 
addTrain(3221, "MEMU", "Mumbai", "Hyderabad", "15:15", "10:45", 223, "Local", 75.75);

 addTrain(3222, "Rajdhani Express", "Chennai", "Pune", "18:45", "01:15", 973, "Express", 1017.06);

  addTrain(3223, "Rajdhani Express", "Jaipur", "Chennai", "09:00", "22:30", 1017, "Express", 1570.28); 

  addTrain(3224, "MEMU", "Lucknow", "Pune", "23:45", "11:00", 1536, "Local", 412.37);

   addTrain(3225, "Intercity Express", "Ahmedabad", "Lucknow", "13:00", "20:00", 494, "Local", 1831.28);

addTrain(3226, "Superfast Express", "Chennai", "Ahmedabad", "13:45", "16:45", 115, "Passenger", 398.39);
 
addTrain(3227, "Garib Rath", "Mumbai", "Kolkata", "15:30", "04:00", 793, "Local", 1384.78);
 
addTrain(3228, "Duronto Express", "Jaipur", "Hyderabad", "22:30", "00:15", 1698, "Passenger", 288.35);
 
addTrain(3229, "Shatabdi Express", "Bangalore", "Lucknow", "19:00", "18:15", 1977, "Local", 520.86);
 
addTrain(3230, "Intercity Express", "Jaipur", "Kolkata", "03:30", "18:30", 1864, "Express", 1013.47);
 
addTrain(3231, "Superfast Express", "Lucknow", "Ahmedabad", "21:15", "17:15", 243, "Express", 1698.27);
 
addTrain(3232, "Garib Rath", "Pune", "Lucknow", "10:00", "14:45", 1823, "Passenger", 1730.76);
 
addTrain(3233, "Garib Rath", "Delhi", "Chennai", "00:15", "09:45", 1683, "Passenger", 1940.59);
 
addTrain(3234, "Superfast Express", "Ahmedabad", "Kolkata", "07:30", "07:30", 648, "Express", 70.35);
 
addTrain(3235, "Mail Express", "Delhi", "Mumbai", "05:45", "17:15", 182, "Express", 229.47);
 
addTrain(3236, "Rajdhani Express", "Delhi", "Lucknow", "22:45", "05:15", 435, "Express", 1492.97);
 
addTrain(3237, "MEMU", "Kolkata", "Pune", "09:00", "14:45", 358, "Local", 424.57);

 addTrain(3238, "Suburban Local", "Mumbai", "Pune", "00:30", "19:45", 1246, "Express", 1486.16);

  addTrain(3239, "Mail Express", "Jaipur", "Bangalore", "23:30", "15:00", 123, "Passenger", 1823.94); 

  addTrain(3240, "Mail Express", "Jaipur", "Chennai", "21:15", "10:45", 1662, "Express", 1651.78);

   addTrain(3241, "Mail Express", "Mumbai", "Kolkata", "01:00", "11:30", 1250, "Passenger", 1740.76);

addTrain(3242, "Shatabdi Express", "Chennai", "Lucknow", "22:00", "23:45", 1386, "Express", 425.49);
 
addTrain(3243, "Mail Express", "Delhi", "Bangalore", "20:00", "18:30", 1443, "Express", 615.28);
 
addTrain(3244, "Rajdhani Express", "Pune", "Bangalore", "00:00", "05:00", 952, "Local", 1208.56);
 
addTrain(3245, "Mail Express", "Mumbai", "Kolkata", "01:00", "05:15", 680, "Passenger", 655.6);
 
addTrain(3246, "Rajdhani Express", "Hyderabad", "Jaipur", "19:45", "20:45", 1464, "Local", 1809.99);
 
addTrain(3247, "Shatabdi Express", "Jaipur", "Chennai", "13:00", "20:45", 1224, "Passenger", 1297.96);
 
addTrain(3248, "Shatabdi Express", "Chennai", "Jaipur", "17:45", "18:15", 1585, "Express", 484.63);
 
addTrain(3249, "Intercity Express", "Pune", "Chennai", "01:15", "05:00", 1607, "Passenger", 1524.17);
 
addTrain(3250, "Mail Express", "Bangalore", "Delhi", "14:45", "08:30", 710, "Passenger", 454.75);
 
addTrain(3251, "Superfast Express", "Jaipur", "Kolkata", "05:30", "16:00", 452, "Passenger", 811.78);
 
addTrain(3252, "Shatabdi Express", "Ahmedabad", "Pune", "04:15", "17:30", 1888, "Express", 982.39);
 
addTrain(3253, "Intercity Express", "Lucknow", "Mumbai", "07:15", "17:15", 1276, "Local", 1966.27);
 
addTrain(3254, "Shatabdi Express", "Lucknow", "Ahmedabad", "18:00", "22:00", 953, "Local", 1174.72);

 addTrain(3255, "Shatabdi Express", "Jaipur", "Kolkata", "13:15", "13:30", 1324, "Local", 466.4); 

 addTrain(3256, "Shatabdi Express", "Bangalore", "Hyderabad", "21:15", "15:45", 770, "Local", 838.41); 

 addTrain(3257, "Intercity Express", "Mumbai", "Hyderabad", "01:15", "18:45", 1919, "Express", 987.87);

  addTrain(3258, "MEMU", "Kolkata", "Delhi", "00:30", "14:15", 1968, "Express", 1531.25);

addTrain(3259, "MEMU", "Mumbai", "Chennai", "01:45", "09:45", 821, "Passenger", 1913.54);
 
addTrain(3260, "Intercity Express", "Hyderabad", "Delhi", "17:15", "12:45", 1469, "Express", 1104.14);
 
addTrain(3261, "MEMU", "Lucknow", "Kolkata", "22:15", "23:15", 730, "Local", 1026.89);
 
addTrain(3262, "Jan Shatabdi", "Chennai", "Hyderabad", "23:15", "09:30", 1473, "Express", 1801.37);
 
addTrain(3263, "Mail Express", "Hyderabad", "Chennai", "08:15", "18:15", 416, "Passenger", 525.29);
 
addTrain(3264, "Rajdhani Express", "Kolkata", "Delhi", "05:00", "07:15", 811, "Local", 509.69);
 
addTrain(3265, "Mail Express", "Bangalore", "Pune", "07:15", "17:45", 841, "Express", 1740.52);
 
addTrain(3266, "Jan Shatabdi", "Kolkata", "Bangalore", "19:00", "01:45", 886, "Local", 1719.23);
 
addTrain(3267, "Jan Shatabdi", "Mumbai", "Ahmedabad", "14:15", "22:00", 577, "Local", 68.62);
 
addTrain(3268, "MEMU", "Bangalore", "Chennai", "23:30", "01:15", 1566, "Passenger", 377.15);
 
addTrain(3269, "Suburban Local", "Hyderabad", "Lucknow", "03:30", "18:00", 1853, "Passenger", 1837.01);
 
addTrain(3270, "Duronto Express", "Lucknow", "Bangalore", "15:30", "01:45", 341, "Express", 338.28); 

addTrain(3271, "Mail Express", "Jaipur", "Mumbai", "12:15", "14:15", 401, "Express", 138.68); 

addTrain(3272, "Garib Rath", "Pune", "Hyderabad", "10:15", "04:15", 674, "Passenger", 962.3); 

addTrain(3273, "Superfast Express", "Kolkata", "Mumbai", "18:45", "20:15", 1174, "Passenger", 586.17); 

addTrain(3274, "Superfast Express", "Pune", "Bangalore", "04:30", "10:45", 1177, "Local", 1677.51);

addTrain(3275, "Shatabdi Express", "Ahmedabad", "Bangalore", "01:15", "12:00", 965, "Express", 806.9);
 
addTrain(3276, "Intercity Express", "Bangalore", "Mumbai", "22:00", "06:15", 662, "Local", 1901.52);
 
addTrain(3277, "Jan Shatabdi", "Delhi", "Chennai", "07:15", "18:00", 984, "Local", 1102.05);
 
addTrain(3278, "MEMU", "Pune", "Lucknow", "09:45", "08:30", 1779, "Local", 845.69);
 
addTrain(3279, "Rajdhani Express", "Ahmedabad", "Kolkata", "07:15", "19:15", 1752, "Local", 1711.38);
 
addTrain(3280, "MEMU", "Lucknow", "Mumbai", "14:45", "14:30", 1195, "Passenger", 334.77);
 
addTrain(3281, "MEMU", "Kolkata", "Jaipur", "19:45", "02:00", 1093, "Express", 1042.1);
 
addTrain(3282, "Jan Shatabdi", "Lucknow", "Mumbai", "10:30", "07:45", 702, "Express", 1226.01);
 
addTrain(3283, "Superfast Express", "Chennai", "Jaipur", "04:45", "20:45", 1503, "Local", 588.42);
 
addTrain(3284, "MEMU", "Lucknow", "Chennai", "17:45", "12:00", 1884, "Express", 1874.1);
 
addTrain(3285, "Shatabdi Express", "Jaipur", "Chennai", "20:30", "02:45", 1476, "Express", 240.02);
 
addTrain(3286, "Intercity Express", "Mumbai", "Hyderabad", "07:00", "01:30", 1567, "Local", 1008.9);
 
addTrain(3287, "Jan Shatabdi", "Mumbai", "Chennai", "08:15", "20:15", 228, "Local", 1367.48);

 addTrain(3288, "Superfast Express", "Lucknow", "Hyderabad", "11:45", "07:15", 1379, "Express", 112.88); 

 addTrain(3289, "MEMU", "Jaipur", "Bangalore", "02:30", "16:45", 1371, "Local", 558.0);

addTrain(3290, "Rajdhani Express", "Jaipur", "Lucknow", "00:45", "03:45", 1414, "Local", 1112.67); 

addTrain(3291, "Garib Rath", "Delhi", "Ahmedabad", "12:15", "01:00", 158, "Passenger", 374.67);

addTrain(3292, "Mail Express", "Lucknow", "Jaipur", "10:15", "20:30", 1188, "Local", 206.27);
 
addTrain(3293, "Intercity Express", "Lucknow", "Delhi", "13:00", "14:00", 1753, "Local", 1423.22);
 
addTrain(3294, "MEMU", "Chennai", "Pune", "14:15", "21:15", 1777, "Passenger", 761.4);
 
addTrain(3295, "Jan Shatabdi", "Kolkata", "Jaipur", "13:15", "17:30", 1014, "Passenger", 369.17);
 
addTrain(3296, "Intercity Express", "Mumbai", "Chennai", "13:45", "19:15", 1690, "Local", 1020.66);
 
addTrain(3297, "MEMU", "Delhi", "Kolkata", "12:45", "07:00", 1141, "Passenger", 1482.5);
 
addTrain(3298, "Shatabdi Express", "Mumbai", "Kolkata", "22:30", "13:30", 104, "Passenger", 1816.78);
 
addTrain(3299, "Garib Rath", "Lucknow", "Kolkata", "15:30", "19:45", 1770, "Local", 81.07);
 
addTrain(3300, "Jan Shatabdi", "Hyderabad", "Bangalore", "09:00", "03:15", 415, "Passenger", 1459.66);
 
addTrain(3301, "Mail Express", "Mumbai", "Lucknow", "17:15", "06:30", 801, "Express", 187.41);
 
addTrain(3302, "Superfast Express", "Ahmedabad", "Hyderabad", "03:15", "09:30", 540, "Local", 1761.31);
 
addTrain(3303, "Superfast Express", "Delhi", "Hyderabad", "08:45", "13:15", 1548, "Express", 1884.77); 

addTrain(3304, "Garib Rath", "Mumbai", "Ahmedabad", "09:30", "18:30", 803, "Passenger", 1215.45); 

addTrain(3305, "Garib Rath", "Bangalore", "Chennai", "08:30", "04:30", 587, "Local", 1622.38);

 addTrain(3306, "Shatabdi Express", "Hyderabad", "Lucknow", "03:30", "06:30", 240, "Passenger", 238.2);

  addTrain(3307, "Jan Shatabdi", "Hyderabad", "Lucknow", "11:15", "12:15", 1661, "Express", 24.49);

addTrain(3308, "MEMU", "Chennai", "Pune", "12:15", "10:15", 945, "Express", 738.02);
 
addTrain(3309, "Duronto Express", "Kolkata", "Bangalore", "02:00", "04:15", 1568, "Passenger", 915.75);
 
addTrain(3310, "Rajdhani Express", "Bangalore", "Ahmedabad", "23:45", "07:45", 338, "Passenger", 732.45);
 
addTrain(3311, "Rajdhani Express", "Mumbai", "Kolkata", "13:30", "19:00", 1145, "Express", 1593.09);
 
addTrain(3312, "Shatabdi Express", "Ahmedabad", "Hyderabad", "13:30", "15:15", 323, "Local", 32.41);
 
addTrain(3313, "Mail Express", "Pune", "Kolkata", "09:45", "10:30", 1003, "Passenger", 1546.34);
 
addTrain(3314, "Intercity Express", "Bangalore", "Hyderabad", "22:30", "09:45", 1859, "Local", 1561.95);
 
addTrain(3315, "MEMU", "Mumbai", "Jaipur", "11:15", "21:00", 1226, "Passenger", 852.88);
 
addTrain(3316, "Shatabdi Express", "Mumbai", "Bangalore", "13:15", "12:00", 284, "Passenger", 617.59);
 
addTrain(3317, "Intercity Express", "Hyderabad", "Chennai", "11:45", "09:30", 1182, "Passenger", 1458.47);
 
addTrain(3318, "Rajdhani Express", "Mumbai", "Pune", "15:45", "14:45", 71, "Local", 1467.28);
 
addTrain(3319, "Duronto Express", "Lucknow", "Jaipur", "18:00", "08:00", 433, "Local", 14.17);
 
addTrain(3320, "Duronto Express", "Chennai", "Pune", "15:45", "08:45", 1669, "Express", 419.24); 

addTrain(3321, "Suburban Local", "Delhi", "Kolkata", "05:00", "07:00", 397, "Passenger", 1254.75); 

addTrain(3322, "MEMU", "Chennai", "Pune", "19:45", "13:00", 1027, "Express", 1988.26); 

addTrain(3323, "Shatabdi Express", "Bangalore", "Kolkata", "10:15", "08:15", 1144, "Local", 1807.01);

 addTrain(3324, "Suburban Local", "Chennai", "Hyderabad", "19:00", "20:15", 1734, "Express", 1807.21);

addTrain(3325, "Suburban Local", "Chennai", "Ahmedabad", "01:15", "20:30", 363, "Local", 1424.24);
 
addTrain(3326, "Superfast Express", "Pune", "Delhi", "02:15", "04:30", 525, "Express", 1925.03);
 
addTrain(3327, "Mail Express", "Chennai", "Hyderabad", "08:30", "15:15", 1531, "Passenger", 1557.43);
 
addTrain(3328, "Mail Express", "Pune", "Lucknow", "02:45", "12:15", 1260, "Passenger", 149.02);
 
addTrain(3329, "Intercity Express", "Kolkata", "Pune", "23:15", "22:30", 996, "Local", 832.61);
 
addTrain(3330, "Rajdhani Express", "Lucknow", "Ahmedabad", "16:15", "18:45", 672, "Passenger", 1805.21);
 
addTrain(3331, "Jan Shatabdi", "Lucknow", "Pune", "16:00", "23:30", 222, "Local", 1889.46);
 
addTrain(3332, "Duronto Express", "Hyderabad", "Ahmedabad", "01:30", "06:45", 464, "Local", 180.68);
 
addTrain(3333, "Shatabdi Express", "Ahmedabad", "Pune", "22:30", "01:15", 302, "Passenger", 1298.45);
 
addTrain(3334, "Garib Rath", "Hyderabad", "Chennai", "14:15", "23:15", 1177, "Express", 1443.25);
 
addTrain(3335, "Mail Express", "Pune", "Ahmedabad", "13:45", "07:15", 766, "Passenger", 1010.51);
 
addTrain(3336, "Jan Shatabdi", "Kolkata", "Bangalore", "09:30", "00:30", 629, "Express", 1111.04);

 addTrain(3337, "Shatabdi Express", "Pune", "Chennai", "20:00", "07:15", 1142, "Express", 185.74); 

 addTrain(3338, "Suburban Local", "Chennai", "Pune", "19:15", "17:30", 938, "Express", 621.14);

  addTrain(3339, "MEMU", "Mumbai", "Bangalore", "16:30", "00:15", 546, "Passenger", 829.7);

   addTrain(3340, "MEMU", "Ahmedabad", "Kolkata", "16:30", "19:15", 1723, "Passenger", 510.69);

addTrain(3341, "Mail Express", "Delhi", "Pune", "03:00", "12:45", 1703, "Local", 1968.56);
 
addTrain(3342, "Intercity Express", "Lucknow", "Hyderabad", "05:15", "11:15", 1410, "Local", 787.47);
 
addTrain(3343, "MEMU", "Chennai", "Hyderabad", "06:00", "19:15", 561, "Local", 1137.27);
 
addTrain(3344, "Rajdhani Express", "Pune", "Hyderabad", "01:15", "16:15", 928, "Local", 1192.59);
 
addTrain(3345, "MEMU", "Bangalore", "Delhi", "06:30", "08:00", 1381, "Local", 1220.06);
 
addTrain(3346, "Mail Express", "Jaipur", "Mumbai", "12:45", "16:45", 1104, "Passenger", 919.03);
 
addTrain(3347, "Mail Express", "Ahmedabad", "Chennai", "08:45", "21:15", 679, "Passenger", 712.83);
 
addTrain(3348, "MEMU", "Delhi", "Ahmedabad", "03:45", "10:00", 1306, "Local", 715.29);
 
addTrain(3349, "Garib Rath", "Pune", "Delhi", "07:15", "04:45", 543, "Passenger", 599.35);
 
addTrain(3350, "Suburban Local", "Lucknow", "Delhi", "22:15", "18:45", 1151, "Local", 1834.37);
 
addTrain(3351, "Superfast Express", "Chennai", "Pune", "20:45", "16:30", 437, "Local", 1390.11);
 
addTrain(3352, "Mail Express", "Mumbai", "Ahmedabad", "19:30", "03:45", 1175, "Express", 1463.11);
 
addTrain(3353, "MEMU", "Mumbai", "Ahmedabad", "13:00", "14:30", 877, "Express", 1333.43); 

addTrain(3354, "Superfast Express", "Mumbai", "Bangalore", "20:00", "12:00", 195, "Express", 569.67); 

addTrain(3355, "Duronto Express", "Ahmedabad", "Kolkata", "17:45", "05:30", 1003, "Passenger", 857.82);

 addTrain(3356, "Jan Shatabdi", "Jaipur", "Delhi", "07:15", "15:00", 1770, "Passenger", 229.43);

  addTrain(3357, "Mail Express", "Mumbai", "Lucknow", "07:45", "01:45", 1568, "Express", 975.13);

addTrain(3358, "Rajdhani Express", "Kolkata", "Bangalore", "14:45", "11:00", 729, "Local", 1816.27);
 
addTrain(3359, "Rajdhani Express", "Jaipur", "Mumbai", "21:15", "11:00", 481, "Express", 1981.01);
 
addTrain(3360, "Mail Express", "Hyderabad", "Mumbai", "06:00", "21:30", 1493, "Express", 1253.78);
 
addTrain(3361, "Mail Express", "Jaipur", "Hyderabad", "12:15", "01:00", 1271, "Express", 69.47);
 
addTrain(3362, "Shatabdi Express", "Delhi", "Pune", "17:00", "20:45", 763, "Local", 1026.5);
 
addTrain(3363, "Rajdhani Express", "Lucknow", "Pune", "23:45", "22:45", 1593, "Express", 1556.28);
 
addTrain(3364, "Mail Express", "Mumbai", "Pune", "17:15", "18:00", 1767, "Passenger", 1885.62);
 
addTrain(3365, "Shatabdi Express", "Jaipur", "Bangalore", "05:15", "02:45", 88, "Passenger", 1230.57);
 
addTrain(3366, "Jan Shatabdi", "Delhi", "Lucknow", "05:30", "18:45", 1575, "Local", 208.6);
 
addTrain(3367, "Shatabdi Express", "Chennai", "Ahmedabad", "11:30", "21:15", 1104, "Local", 1967.76);
 
addTrain(3368, "Duronto Express", "Jaipur", "Lucknow", "18:45", "17:45", 1093, "Passenger", 1989.66);
 
addTrain(3369, "Shatabdi Express", "Chennai", "Ahmedabad", "09:00", "06:00", 1634, "Local", 1030.42); 

addTrain(3370, "Jan Shatabdi", "Pune", "Bangalore", "04:00", "05:30", 715, "Passenger", 660.87);

 addTrain(3371, "Jan Shatabdi", "Lucknow", "Hyderabad", "08:15", "11:00", 1392, "Express", 1458.23);
 
addTrain(3372, "Rajdhani", "Delhi", "Mumbai", "17:45", "13:45", 1428, "Passenger", 1201.19);

addTrain(3373, "Rajdhani Express", "Lucknow", "Kolkata", "17:15", "13:15", 945, "Local", 975.87);

addTrain(3374, "Garib Rath", "Chennai", "Pune", "11:00", "05:15", 1815, "Express", 1725.27);
 
addTrain(3375, "Rajdhani Express", "Chennai", "Mumbai", "02:15", "03:15", 1065, "Local", 1541.1);
 
addTrain(3376, "Garib Rath", "Pune", "Lucknow", "13:15", "13:30", 780, "Express", 237.36);
 
addTrain(3377, "Shatabdi Express", "Kolkata", "Bangalore", "00:45", "21:45", 813, "Express", 1230.87);
 
addTrain(3378, "Superfast Express", "Kolkata", "Bangalore", "04:00", "14:45", 264, "Express", 263.14);
 
addTrain(3379, "Intercity Express", "Bangalore", "Hyderabad", "13:45", "18:00", 1194, "Passenger", 33.29);
 
addTrain(3380, "Intercity Express", "Jaipur", "Bangalore", "12:00", "17:00", 177, "Passenger", 958.8);
 
addTrain(3381, "Shatabdi Express", "Hyderabad", "Bangalore", "13:45", "16:00", 662, "Passenger", 1394.43);
 
addTrain(3382, "Superfast Express", "Lucknow", "Pune", "17:45", "09:45", 1524, "Passenger", 1557.37);
 
addTrain(3383, "Suburban Local", "Pune", "Delhi", "05:00", "18:45", 125, "Express", 158.2);
 
addTrain(3384, "Shatabdi Express", "Lucknow", "Jaipur", "01:15", "16:30", 1869, "Passenger", 1493.0);
 
addTrain(3385, "Shatabdi Express", "Jaipur", "Delhi", "20:45", "07:30", 115, "Local", 1426.42);
 
addTrain(3386, "Rajdhani Express", "Kolkata", "Ahmedabad", "09:00", "00:15", 617, "Local", 337.88);

 addTrain(3387, "Jan Shatabdi", "Lucknow", "Jaipur", "08:00", "09:15", 1649, "Local", 526.05);

  addTrain(3388, "MEMU", "Bangalore", "Ahmedabad", "14:30", "09:15", 829, "Passenger", 434.57); 

  addTrain(3389, "MEMU", "Hyderabad", "Pune", "11:30", "08:15", 1331, "Local", 722.79);

   addTrain(3390, "Mail Express", "Mumbai", "Kolkata", "07:15", "18:45", 930, "Passenger", 767.6);

addTrain(3391, "Jan Shatabdi", "Pune", "Kolkata", "05:15", "08:00", 1973, "Passenger", 1516.81);
 
addTrain(3392, "Superfast Express", "Bangalore", "Chennai", "02:30", "23:30", 1390, "Local", 569.27);
 
addTrain(3393, "Rajdhani Express", "Delhi", "Pune", "11:30", "20:00", 658, "Express", 99.33);
 
addTrain(3394, "Garib Rath", "Pune", "Ahmedabad", "23:45", "12:30", 238, "Passenger", 1714.48);
 
addTrain(3395, "Mail Express", "Chennai", "Mumbai", "03:45", "05:00", 103, "Local", 951.24);
 
addTrain(3396, "Rajdhani Express", "Chennai", "Kolkata", "19:45", "21:30", 478, "Express", 1100.8);
 
addTrain(3397, "Intercity Express", "Pune", "Lucknow", "14:15", "02:45", 211, "Express", 608.72);
 
addTrain(3398, "Shatabdi Express", "Bangalore", "Ahmedabad", "03:15", "19:45", 1024, "Express", 1360.05);
 
addTrain(3399, "Mail Express", "Kolkata", "Chennai", "07:30", "13:45", 640, "Local", 1403.48);
 
addTrain(3400, "Rajdhani Express", "Ahmedabad", "Chennai", "00:15", "19:30", 1004, "Express", 1064.87);
 
addTrain(3401, "Intercity Express", "Mumbai", "Ahmedabad", "20:30", "10:15", 1481, "Express", 997.9);
 
addTrain(3402, "Mail Express", "Pune", "Chennai", "23:30", "02:30", 969, "Local", 1806.12);

 addTrain(3403, "Rajdhani Express", "Jaipur", "Hyderabad", "09:45", "00:15", 1411, "Local", 345.13);

  addTrain(3404, "Shatabdi Express", "Lucknow", "Ahmedabad", "19:45", "08:15", 89, "Passenger", 1820.37); 

  addTrain(3405, "Duronto", "Bangalore", "Kolkata", "01:15", "23:45", 1423, "Local", 906.48); 

  addTrain(3406, "Mail Express", "Jaipur", "Bangalore", "05:45", "12:45", 587, "Express", 1196.85);

addTrain(3407, "Superfast Express", "Mumbai", "Bangalore", "14:45", "21:30", 1933, "Express", 230.75);
 
addTrain(3408, "Duronto Express", "Bangalore", "Ahmedabad", "18:45", "09:00", 1439, "Passenger", 1647.61);
 
addTrain(3409, "Superfast Express", "Chennai", "Delhi", "21:00", "22:30", 1704, "Local", 33.98);
 
addTrain(3410, "Mail Express", "Lucknow", "Delhi", "12:30", "17:15", 1841, "Express", 1720.0);
 
addTrain(3411, "Duronto Express", "Hyderabad", "Bangalore", "05:00", "02:30", 1724, "Express", 652.8);
 
addTrain(3412, "Duronto Express", "Hyderabad", "Delhi", "22:00", "18:00", 981, "Passenger", 1566.85);
 
addTrain(3413, "Mail Express", "Kolkata", "Delhi", "01:00", "05:00", 1830, "Express", 1370.55);
 
addTrain(3414, "Rajdhani Express", "Kolkata", "Mumbai", "23:15", "05:30", 1098, "Local", 1284.23);
 
addTrain(3415, "Shatabdi Express", "Bangalore", "Chennai", "16:00", "00:15", 1008, "Passenger", 1444.18);
 
addTrain(3416, "Suburban Local", "Jaipur", "Lucknow", "20:00", "08:45", 458, "Local", 1074.48);
 
addTrain(3417, "Jan Shatabdi", "Hyderabad", "Kolkata", "13:45", "02:30", 25, "Express", 1455.17);
 
addTrain(3418, "Rajdhani Express", "Mumbai", "Chennai", "05:15", "17:15", 1094, "Passenger", 181.91);
 
addTrain(3419, "Mail Express", "Kolkata", "Ahmedabad", "22:30", "15:15", 1936, "Local", 1989.83);

 addTrain(3420, "Jan Shatabdi", "Pune", "Lucknow", "08:15", "11:45", 1908, "Local", 434.45); 


 addTrain(3421, "Jan Shatabdi", "Chennai", "Kolkata", "15:30", "13:45", 1039, "Express", 171.0);

  addTrain(3422, "Superfast Express", "Chennai", "Hyderabad", "15:30", "16:30", 395, "Local", 1200.51);

   addTrain(3423, "Mail Express", "Kolkata", "Bangalore", "20:30", "01:45", 1942, "Passenger", 1435.47);

addTrain(3424, "Rajdhani Express", "Delhi", "Mumbai", "05:45", "14:45", 948, "Passenger", 676.42);
 
addTrain(3425, "Shatabdi Express", "Ahmedabad", "Pune", "02:00", "14:15", 1848, "Express", 1315.56);
 
addTrain(3426, "Garib Rath", "Mumbai", "Lucknow", "16:15", "06:45", 156, "Local", 338.64);
 
addTrain(3427, "Mail Express", "Kolkata", "Hyderabad", "22:30", "23:15", 1253, "Local", 881.3);
 
addTrain(3428, "Rajdhani Express", "Hyderabad", "Ahmedabad", "20:00", "17:15", 887, "Express", 1198.96);
 
addTrain(3429, "Intercity Express", "Delhi", "Jaipur", "00:45", "21:30", 535, "Passenger", 1917.77);
 
addTrain(3430, "Mail Express", "Ahmedabad", "Lucknow", "06:30", "09:30", 535, "Express", 1079.47);
 
addTrain(3431, "Suburban Local", "Kolkata", "Bangalore", "20:15", "19:00", 650, "Passenger", 1105.43);
 
addTrain(3432, "Intercity Express", "Delhi", "Chennai", "01:45", "01:00", 1620, "Express", 452.16);
 
addTrain(3433, "Duronto Express", "Kolkata", "Pune", "17:00", "08:30", 517, "Passenger", 1952.01);
 
addTrain(3434, "Mail Express", "Mumbai", "Pune", "13:45", "11:15", 511, "Local", 600.01);
 
addTrain(3435, "Shatabdi Express", "Mumbai", "Kolkata", "05:00", "10:45", 229, "Passenger", 1508.16);

 addTrain(3436, "Mail Express", "Delhi", "Ahmedabad", "02:00", "21:15", 780, "Express", 1527.66);

  addTrain(3437, "MEMU", "Mumbai", "Delhi", "14:45", "17:15", 1891, "Local", 1776.95);

addTrain(3438, "Rajdhani", "Hyderabad", "Delhi", "11:15", "14:15", 792, "Local", 378.79); 

addTrain(3439, "Shatabdi Express", "Jaipur", "Ahmedabad", "11:30", "00:30", 1808, "Local", 72.21);

addTrain(3440, "Duronto Express", "Lucknow", "Chennai", "21:15", "05:00", 1709, "Express", 1699.73);
 
addTrain(3441, "Shatabdi Express", "Hyderabad", "Pune", "11:00", "07:45", 1181, "Passenger", 1039.2);
 
addTrain(3442, "Suburban Local", "Mumbai", "Bangalore", "08:00", "12:15", 92, "Local", 1998.64);
 
addTrain(3443, "Superfast Express", "Chennai", "Bangalore", "05:30", "00:15", 1560, "Express", 1924.14);
 
addTrain(3444, "Superfast Express", "Kolkata", "Mumbai", "02:15", "06:45", 203, "Local", 1895.87);
 
addTrain(3445, "Garib Rath", "Jaipur", "Kolkata", "19:15", "13:00", 1103, "Local", 275.36);
 
addTrain(3446, "Garib Rath", "Chennai", "Mumbai", "09:30", "21:00", 1152, "Passenger", 1704.99);
 
addTrain(3447, "MEMU", "Lucknow", "Ahmedabad", "05:45", "23:30", 731, "Passenger", 1924.01);
 
addTrain(3448, "Jan Shatabdi", "Hyderabad", "Pune", "14:45", "04:30", 1346, "Express", 518.24);
 
addTrain(3449, "Rajdhani Express", "Bangalore", "Hyderabad", "12:15", "03:30", 881, "Express", 535.55);
 
addTrain(3450, "Rajdhani Express", "Chennai", "Mumbai", "02:30", "19:15", 1185, "Passenger", 36.86);
 
addTrain(3451, "Rajdhani Express", "Bangalore", "Delhi", "12:15", "11:45", 545, "Express", 718.91);
 
addTrain(3452, "Shatabdi Express", "Ahmedabad", "Lucknow", "13:15", "03:15", 129, "Express", 1658.69);

 addTrain(3453, "Suburban Local", "Kolkata", "Hyderabad", "05:15", "06:30", 1025, "Passenger", 1816.87);

  addTrain(3454, "MEMU", "Jaipur", "Delhi", "18:15", "10:45", 1811, "Passenger", 517.02);

addTrain(3455, "Shatabdi Express", "Lucknow", "Ahmedabad", "06:45", "04:45", 496, "Local", 478.16);

 addTrain(3456, "MEMU", "Chennai", "Pune", "21:45", "17:45", 618, "Local", 734.29);

addTrain(3457, "Garib Rath", "Delhi", "Jaipur", "14:45", "18:45", 1265, "Passenger", 342.23);
 
addTrain(3458, "MEMU", "Delhi", "Hyderabad", "21:30", "13:00", 1141, "Passenger", 1227.31);
 
addTrain(3459, "Duronto Express", "Delhi", "Chennai", "02:00", "08:00", 195, "Local", 427.44);
 
addTrain(3460, "Superfast Express", "Lucknow", "Bangalore", "13:30", "09:45", 1485, "Passenger", 341.65);
 
addTrain(3461, "Superfast Express", "Ahmedabad", "Kolkata", "00:15", "03:45", 1592, "Express", 912.91);
 
addTrain(3462, "MEMU", "Delhi", "Chennai", "03:15", "00:30", 1827, "Local", 1043.28);
 
addTrain(3463, "Jan Shatabdi", "Ahmedabad", "Pune", "09:15", "20:15", 1744, "Passenger", 576.03);
 
addTrain(3464, "Intercity Express", "Lucknow", "Hyderabad", "17:15", "20:45", 1577, "Passenger", 1378.7);
 
addTrain(3465, "Intercity Express", "Mumbai", "Hyderabad", "10:45", "20:00", 400, "Express", 450.6);
 
addTrain(3466, "MEMU", "Mumbai", "Chennai", "00:45", "19:15", 710, "Passenger", 1319.75);
 
addTrain(3467, "Duronto Express", "Pune", "Ahmedabad", "00:45", "04:00", 1929, "Local", 14.7);
 
addTrain(3468, "Suburban Local", "Lucknow", "Delhi", "00:45", "22:15", 1904, "Express", 815.24); 

addTrain(3469, "MEMU", "Delhi", "Bangalore", "16:15", "14:15", 1684, "Local", 1029.24); 

addTrain(3470, "Duronto Express", "Kolkata", "Delhi", "16:30", "17:45", 291, "Passenger", 1573.66);

 addTrain(3471, "Shatabdi", "Jaipur", "Pune", "12:45", "07:30", 1808, "Passenger", 1263.21); 

 addTrain(3472, "Duronto Express", "Ahmedabad", "Kolkata", "14:00", "09:15", 1377, "Passenger", 1096.32);

addTrain(3473, "MEMU", "Ahmedabad", "Jaipur", "03:00", "22:15", 1589, "Passenger", 133.69);
 
addTrain(3474, "Duronto Express", "Chennai", "Lucknow", "12:45", "15:30", 1045, "Local", 418.23);
 
addTrain(3475, "Superfast Express", "Jaipur", "Lucknow", "15:00", "14:45", 421, "Express", 298.83);
 
addTrain(3476, "Rajdhani Express", "Pune", "Delhi", "10:15", "21:00", 1523, "Local", 181.74);
 
addTrain(3477, "Suburban Local", "Lucknow", "Jaipur", "21:00", "17:30", 977, "Local", 1954.88);
 
addTrain(3478, "Rajdhani Express", "Kolkata", "Ahmedabad", "07:00", "10:15", 148, "Express", 344.3);
 
addTrain(3479, "Shatabdi Express", "Mumbai", "Bangalore", "04:15", "15:00", 956, "Local", 1867.07);
 
addTrain(3480, "Mail Express", "Jaipur", "Chennai", "10:00", "10:45", 1587, "Local", 1413.58);
 
addTrain(3481, "Duronto Express", "Kolkata", "Pune", "12:00", "03:00", 1421, "Local", 1480.9);
 
addTrain(3482, "Mail Express", "Lucknow", "Delhi", "13:45", "03:30", 799, "Passenger", 1266.78);
 
addTrain(3483, "Mail Express", "Mumbai", "Ahmedabad", "10:00", "20:45", 1133, "Express", 562.01);
 
addTrain(3484, "Intercity Express", "Delhi", "Bangalore", "17:15", "18:45", 1812, "Passenger", 1829.67);
 
addTrain(3485, "Duronto Express", "Chennai", "Hyderabad", "15:00", "04:00", 1136, "Local", 1948.79); 

addTrain(3486, "Suburban Local", "Mumbai", "Bangalore", "20:15", "02:30", 1775, "Passenger", 686.23);

addTrain(3487, "Mail Express", "Delhi", "Lucknow", "01:45", "23:45", 1366, "Local", 1294.11);

 addTrain(3488, "Jan Shatabdi", "Delhi", "Kolkata", "11:45", "03:00", 1868, "Local", 324.2); 

 addTrain(3489, "Mail Express", "Bangalore", "Lucknow", "03:00", "00:30", 1662, "Passenger", 1229.67);

addTrain(3490, "Duronto Express", "Lucknow", "Bangalore", "02:45", "02:45", 223, "Express", 919.93);
 
addTrain(3491, "MEMU", "Hyderabad", "Bangalore", "12:15", "23:00", 977, "Passenger", 1239.95);
 
addTrain(3492, "Jan Shatabdi", "Pune", "Lucknow", "03:15", "10:45", 813, "Passenger", 294.79);
 
addTrain(3493, "MEMU", "Kolkata", "Mumbai", "17:45", "19:00", 879, "Passenger", 868.04);
 
addTrain(3494, "Garib Rath", "Hyderabad", "Kolkata", "14:30", "18:30", 505, "Express", 445.43);
 
addTrain(3495, "Mail Express", "Jaipur", "Ahmedabad", "01:30", "14:45", 1360, "Local", 1710.52);
 
addTrain(3496, "Intercity Express", "Chennai", "Lucknow", "15:15", "10:45", 543, "Express", 572.52);
 
addTrain(3497, "Rajdhani Express", "Chennai", "Jaipur", "19:15", "13:30", 1079, "Local", 1434.83);
 
addTrain(3498, "MEMU", "Chennai", "Pune", "06:00", "15:30", 588, "Local", 1809.13);
 
addTrain(3499, "Duronto Express", "Jaipur", "Hyderabad", "04:45", "14:30", 1639, "Local", 1094.25);
 
addTrain(3500, "MEMU", "Chennai", "Kolkata", "05:00", "17:45", 586, "Express", 920.15);
 
addTrain(3501, "Jan Shatabdi", "Ahmedabad", "Hyderabad", "06:15", "05:00", 1198, "Express", 573.83); 

addTrain(3502, "Intercity Express", "Lucknow", "Delhi", "23:30", "07:45", 1697, "Passenger", 1128.87); 

addTrain(3503, "Superfast Express", "Pune", "Delhi", "13:45", "03:45", 1405, "Local", 1365.17);
 
addTrain(3504, "Superfast Express", "Pune", "Bangalore", "11:15", "05:45", 563, "Passenger", 1225.73); 

addTrain(3505, "Duronto Express", "Hyderabad", "Bangalore", "19:30", "02:30", 929, "Express", 1785.99);

addTrain(3506, "Rajdhani Express", "Kolkata", "Bangalore", "02:00", "14:45", 20, "Passenger", 1759.31);
 
addTrain(3507, "Duronto Express", "Ahmedabad", "Lucknow", "14:15", "12:15", 1960, "Local", 1328.64);
 
addTrain(3508, "Intercity Express", "Mumbai", "Kolkata", "04:45", "09:00", 1526, "Express", 225.37);
 
addTrain(3509, "Rajdhani Express", "Kolkata", "Hyderabad", "07:30", "11:00", 1545, "Local", 673.97);
 
addTrain(3510, "Jan Shatabdi", "Chennai", "Mumbai", "20:30", "17:15", 1875, "Local", 1461.88);
 
addTrain(3511, "MEMU", "Chennai", "Jaipur", "00:30", "14:30", 972, "Passenger", 152.24);
 
addTrain(3512, "MEMU", "Chennai", "Jaipur", "16:00", "15:30", 306, "Local", 1027.1);
 
addTrain(3513, "Rajdhani Express", "Jaipur", "Ahmedabad", "14:45", "22:45", 1826, "Express", 1180.11);
 
addTrain(3514, "Intercity Express", "Delhi", "Kolkata", "16:30", "07:00", 1148, "Express", 1093.17);
 
addTrain(3515, "Superfast Express", "Hyderabad", "Lucknow", "05:30", "02:45", 1635, "Express", 1604.24);
 
addTrain(3516, "Rajdhani Express", "Chennai", "Jaipur", "09:45", "00:45", 1625, "Passenger", 35.8);
 
addTrain(3517, "Suburban Local", "Bangalore", "Mumbai", "17:15", "21:30", 749, "Passenger", 1408.58);
 
addTrain(3518, "Rajdhani Express", "Hyderabad", "Delhi", "08:30", "23:00", 1139, "Passenger", 1879.09);

 addTrain(3519, "Garib Rath", "Delhi", "Mumbai", "05:15", "17:15", 247, "Local", 1553.35);

  addTrain(3520, "Garib Rath", "Ahmedabad", "Pune", "10:15", "15:15", 306, "Express", 1469.59);

   addTrain(3521, "Superfast Express", "Hyderabad", "Delhi", "15:00", "15:00", 302, "Express", 1425.96); 

   addTrain(3522, "Superfast Express", "Ahmedabad", "Mumbai", "20:15", "10:00", 577, "Local", 1221.87);

addTrain(3523, "Superfast Express", "Chennai", "Lucknow", "18:45", "06:00", 659, "Local", 1327.02);
 
addTrain(3524, "Duronto Express", "Chennai", "Jaipur", "03:30", "11:15", 1487, "Express", 398.36);
 
addTrain(3525, "Rajdhani Express", "Bangalore", "Hyderabad", "03:45", "20:15", 1386, "Passenger", 1867.04);
 
addTrain(3526, "MEMU", "Mumbai", "Delhi", "02:00", "01:45", 1569, "Local", 1527.53);
 
addTrain(3527, "Suburban Local", "Bangalore", "Hyderabad", "21:45", "05:15", 1781, "Passenger", 1655.28);
 
addTrain(3528, "Rajdhani Express", "Chennai", "Delhi", "20:15", "15:15", 59, "Express", 310.12);
 
addTrain(3529, "Shatabdi Express", "Lucknow", "Kolkata", "18:30", "16:30", 1118, "Local", 504.89);
 
addTrain(3530, "Mail Express", "Chennai", "Kolkata", "16:45", "10:00", 1904, "Passenger", 1331.85);
 
addTrain(3531, "Rajdhani Express", "Pune", "Jaipur", "00:00", "06:45", 369, "Local", 907.28);
 
addTrain(3532, "Jan Shatabdi", "Lucknow", "Jaipur", "21:30", "22:15", 1142, "Local", 1562.56);
 
addTrain(3533, "Mail Express", "Mumbai", "Hyderabad", "11:45", "20:45", 55, "Passenger", 1007.14);
 
addTrain(3534, "Intercity Express", "Bangalore", "Jaipur", "07:30", "10:00", 917, "Passenger", 664.36);

 addTrain(3535, "Jan Shatabdi", "Ahmedabad", "Chennai", "09:30", "22:45", 1624, "Express", 1346.67); 

 addTrain(3536, "Superfast Express", "Lucknow", "Delhi", "23:00", "17:30", 1100, "Local", 1001.51); 

 addTrain(3537, "Suburban Local", "Jaipur", "Ahmedabad", "14:15", "14:00", 1906, "Local", 878.96); 

 addTrain(3538, "Suburban Local", "Jaipur", "Chennai", "14:00", "00:15", 860, "Passenger", 726.13);

addTrain(3539, "Intercity Express", "Kolkata", "Bangalore", "19:45", "06:15", 468, "Local", 1679.49);
 
addTrain(3540, "Garib Rath", "Delhi", "Bangalore", "10:45", "13:00", 1235, "Local", 1681.19);
 
addTrain(3541, "Garib Rath", "Delhi", "Lucknow", "12:00", "07:15", 1002, "Passenger", 1842.55);
 
addTrain(3542, "Shatabdi Express", "Pune", "Ahmedabad", "12:30", "07:00", 315, "Passenger", 1293.35);
 
addTrain(3543, "Mail Express", "Jaipur", "Hyderabad", "03:30", "03:15", 1582, "Local", 550.21);
 
addTrain(3544, "Intercity Express", "Hyderabad", "Lucknow", "05:15", "15:30", 902, "Local", 1950.48);
 
addTrain(3545, "Garib Rath", "Mumbai", "Jaipur", "22:45", "10:45", 319, "Local", 311.59);
 
addTrain(3546, "Intercity Express", "Pune", "Mumbai", "23:15", "00:45", 1498, "Passenger", 383.74);
 
addTrain(3547, "MEMU", "Ahmedabad", "Kolkata", "15:15", "01:45", 582, "Local", 1978.5);
 
addTrain(3548, "Suburban Local", "Kolkata", "Chennai", "20:45", "09:00", 941, "Express", 927.68);
 
addTrain(3549, "Shatabdi Express", "Hyderabad", "Jaipur", "02:15", "14:45", 1665, "Local", 874.95);
 
addTrain(3550, "Duronto Express", "Ahmedabad", "Delhi", "14:45", "16:00", 54, "Passenger", 598.68);
 
addTrain(3551, "Duronto Express", "Lucknow", "Pune", "05:00", "12:00", 1407, "Passenger", 1705.35);

 addTrain(3552, "Mail Express", "Hyderabad", "Mumbai", "19:45", "13:00", 106, "Passenger", 1016.79);

  addTrain(3553, "Shatabdi Express", "Mumbai", "Jaipur", "10:45", "13:15", 1754, "Express", 1767.12);

   addTrain(3554, "Garib Rath", "Ahmedabad", "Chennai", "11:00", "03:30", 607, "Express", 1771.94);

    addTrain(3555, "Garib Rath", "Ahmedabad", "Mumbai", "07:45", "02:15", 1402, "Local", 707.43);

addTrain(3556, "Intercity Express", "Bangalore", "Hyderabad", "20:15", "12:45", 540, "Local", 1513.5);
 
addTrain(3557, "Suburban Local", "Jaipur", "Delhi", "19:30", "22:30", 1482, "Express", 1037.6);
 
addTrain(3558, "Mail Express", "Hyderabad", "Chennai", "04:15", "01:15", 1378, "Local", 1201.58);
 
addTrain(3559, "Garib Rath", "Jaipur", "Hyderabad", "21:30", "02:00", 1564, "Express", 716.15);
 
addTrain(3560, "MEMU", "Delhi", "Hyderabad", "10:30", "23:45", 115, "Passenger", 1394.11);
 
addTrain(3561, "Rajdhani Express", "Ahmedabad", "Mumbai", "14:30", "23:30", 1935, "Express", 96.86);
 
addTrain(3562, "Duronto Express", "Delhi", "Jaipur", "16:30", "04:30", 1367, "Express", 282.48);
 
addTrain(3563, "Jan Shatabdi", "Lucknow", "Delhi", "21:15", "20:30", 97, "Express", 927.5);
 
addTrain(3564, "Duronto Express", "Bangalore", "Hyderabad", "23:30", "15:45", 1708, "Express", 1675.39);
 
addTrain(3565, "Duronto Express", "Ahmedabad", "Lucknow", "01:30", "14:30", 1574, "Express", 367.47);
 
addTrain(3566, "Superfast Express", "Pune", "Jaipur", "21:30", "05:15", 744, "Local", 1804.42);
 
addTrain(3567, "MEMU", "Ahmedabad", "Jaipur", "08:00", "14:45", 1025, "Passenger", 545.78); 

addTrain(3568, "Jan Shatabdi", "Kolkata", "Ahmedabad", "14:15", "05:00", 1755, "Passenger", 1286.42); 

addTrain(3569, "Suburban Local", "Pune", "Jaipur", "11:00", "10:45", 1116, "Express", 1845.02);

 addTrain(3570, "Shatabdi Express", "Delhi", "Jaipur", "19:45", "21:30", 144, "Local", 1150.97); 
 
 addTrain(3571, "Duronto Express", "Kolkata", "Hyderabad", "19:00", "18:45", 1834, "Express", 959.84);

addTrain(3572, "Intercity Express", "Delhi", "Ahmedabad", "04:45", "11:30", 972, "Local", 947.11);
 
addTrain(3573, "Rajdhani Express", "Chennai", "Jaipur", "05:45", "17:15", 1062, "Passenger", 1163.68);
 
addTrain(3574, "Mail Express", "Delhi", "Ahmedabad", "14:15", "10:45", 1671, "Local", 1875.49);
 
addTrain(3575, "Intercity Express", "Mumbai", "Hyderabad", "00:45", "13:30", 1278, "Express", 1593.55);
 
addTrain(3576, "Suburban Local", "Jaipur", "Mumbai", "21:45", "02:30", 1878, "Passenger", 1334.21);
 
addTrain(3577, "Jan Shatabdi", "Hyderabad", "Ahmedabad", "03:45", "12:00", 760, "Express", 807.92);
 
addTrain(3578, "Suburban Local", "Ahmedabad", "Mumbai", "20:00", "13:00", 1221, "Passenger", 1513.08);
 
addTrain(3579, "Mail Express", "Ahmedabad", "Bangalore", "00:45", "06:15", 1110, "Passenger", 1865.09);
 
addTrain(3580, "Jan Shatabdi", "Chennai", "Jaipur", "16:30", "23:15", 187, "Passenger", 1535.58);
 
addTrain(3581, "Intercity Express", "Delhi", "Hyderabad", "17:45", "03:30", 1170, "Express", 1355.56);
 
addTrain(3582, "Duronto Express", "Delhi", "Jaipur", "07:45", "21:15", 1276, "Local", 177.47);
 
addTrain(3583, "MEMU", "Delhi", "Kolkata", "20:15", "18:15", 1430, "Express", 362.44);
 
addTrain(3584, "Shatabdi Express", "Hyderabad", "Mumbai", "09:00", "14:30", 609, "Express", 1009.36);

 addTrain(3585, "Garib Rath", "Chennai", "Ahmedabad", "13:30", "05:30", 1696, "Local", 1999.7); 

 addTrain(3586, "Rajdhani Express", "Jaipur", "Chennai", "18:45", "12:00", 1836, "Express", 789.99);

  addTrain(3587, "Intercity Express", "Pune", "Delhi", "10:30", "05:45", 1871, "Passenger", 1806.54);

   addTrain(3588, "Duronto Express", "Kolkata", "Chennai", "23:30", "09:00", 1589, "Local", 1865.07);

addTrain(3589, "Suburban Local", "Lucknow", "Kolkata", "09:00", "21:00", 1675, "Passenger", 298.18);
 
addTrain(3590, "Rajdhani Express", "Mumbai", "Ahmedabad", "17:00", "09:45", 703, "Express", 749.06);
 
addTrain(3591, "Mail Express", "Mumbai", "Delhi", "07:30", "13:15", 1248, "Passenger", 715.58);
 
addTrain(3592, "Shatabdi Express", "Mumbai", "Pune", "08:00", "02:00", 1185, "Express", 1718.81);
 
addTrain(3593, "Superfast Express", "Pune", "Chennai", "00:45", "11:15", 1289, "Express", 1002.54);
 
addTrain(3594, "Jan Shatabdi", "Lucknow", "Mumbai", "23:45", "11:30", 491, "Local", 940.21);
 
addTrain(3595, "Garib Rath", "Kolkata", "Bangalore", "00:00", "21:15", 625, "Passenger", 1614.14);
 
addTrain(3596, "Suburban Local", "Bangalore", "Mumbai", "20:30", "16:15", 1198, "Local", 283.15);
 
addTrain(3597, "Suburban Local", "Bangalore", "Lucknow", "03:15", "04:30", 766, "Passenger", 603.09);
 
addTrain(3598, "Duronto Express", "Pune", "Jaipur", "12:30", "21:15", 836, "Local", 1190.64);
 
addTrain(3599, "Mail Express", "Delhi", "Bangalore", "16:15", "00:30", 1798, "Express", 1749.85);
 
addTrain(3600, "Garib Rath", "Lucknow", "Chennai", "12:00", "13:45", 315, "Local", 856.33);

 addTrain(3601, "Superfast Express", "Pune", "Chennai", "06:15", "17:45", 373, "Express", 1622.6);

  addTrain(3602, "Superfast Express", "Chennai", "Mumbai", "02:15", "18:00", 400, "Express", 1753.95);

   addTrain(3603, "Mail Express", "Pune", "Kolkata", "14:00", "18:45", 241, "Passenger", 632.45); 

   addTrain(3604, "Superfast Express", "Mumbai", "Lucknow", "01:00", "07:45", 139, "Express", 1983.64);

addTrain(3605, "MEMU", "Bangalore", "Delhi", "17:00", "04:00", 93, "Express", 653.53);
 
addTrain(3606, "Rajdhani Express", "Pune", "Bangalore", "02:00", "07:45", 702, "Passenger", 1690.2);
 
addTrain(3607, "Duronto Express", "Ahmedabad", "Delhi", "17:15", "05:45", 1284, "Local", 950.9);
 
addTrain(3608, "MEMU", "Ahmedabad", "Jaipur", "17:00", "11:15", 1547, "Express", 1598.98);
 
addTrain(3609, "Rajdhani Express", "Lucknow", "Delhi", "12:00", "22:00", 185, "Passenger", 933.76);
 
addTrain(3610, "Superfast Express", "Ahmedabad", "Jaipur", "11:15", "15:00", 1227, "Local", 835.54);
 
addTrain(3611, "Shatabdi Express", "Kolkata", "Delhi", "23:00", "17:00", 524, "Local", 1146.49);
 
addTrain(3612, "MEMU", "Chennai", "Hyderabad", "14:30", "02:15", 1315, "Local", 1259.12);
 
addTrain(3613, "MEMU", "Ahmedabad", "Chennai", "01:45", "02:45", 927, "Local", 957.27);
 
addTrain(3614, "Suburban Local", "Chennai", "Mumbai", "10:15", "06:30", 1612, "Local", 837.67);
 
addTrain(3615, "Shatabdi Express", "Jaipur", "Lucknow", "06:15", "08:15", 778, "Local", 1732.69);
 
addTrain(3616, "Rajdhani Express", "Mumbai", "Lucknow", "11:30", "03:15", 1171, "Passenger", 286.19);
 
addTrain(3617, "Rajdhani Express", "Hyderabad", "Lucknow", "00:15", "16:00", 583, "Express", 730.25);

 addTrain(3618, "Duronto Express", "Delhi", "Hyderabad", "20:30", "03:15", 98, "Express", 487.26);

  addTrain(3619, "Duronto Express", "Delhi", "Ahmedabad", "18:15", "11:45", 1454, "Local", 1891.53); 

  addTrain(3620, "MEMU", "Lucknow", "Jaipur", "13:30", "19:00", 1805, "Local", 1041.29);

   addTrain(3621, "Duronto Express", "Ahmedabad", "Delhi", "05:30", "07:45", 1546, "Passenger", 550.55);

addTrain(3622, "Duronto Express", "Kolkata", "Mumbai", "21:00", "12:45", 1911, "Local", 780.42);
 
addTrain(3623, "Garib Rath", "Jaipur", "Chennai", "00:15", "04:00", 23, "Passenger", 1438.24);
 
addTrain(3624, "Intercity Express", "Mumbai", "Pune", "09:45", "01:15", 573, "Local", 1496.59);
 
addTrain(3625, "Garib Rath", "Pune", "Bangalore", "12:45", "12:30", 1030, "Local", 1346.87);
 
addTrain(3626, "Shatabdi Express", "Delhi", "Lucknow", "10:15", "12:45", 584, "Local", 886.64);
 
addTrain(3627, "Intercity Express", "Delhi", "Pune", "11:15", "12:15", 841, "Express", 525.23);
 
addTrain(3628, "Rajdhani Express", "Pune", "Delhi", "17:30", "09:00", 1274, "Local", 109.0);
 
addTrain(3629, "Shatabdi Express", "Kolkata", "Delhi", "02:45", "04:30", 1541, "Express", 1669.95);
 
addTrain(3630, "MEMU", "Jaipur", "Ahmedabad", "01:45", "23:00", 851, "Express", 153.55);
 
addTrain(3631, "Garib Rath", "Lucknow", "Kolkata", "12:15", "12:30", 681, "Local", 1210.13);
 
addTrain(3632, "Intercity Express", "Lucknow", "Ahmedabad", "20:45", "02:00", 1678, "Local", 880.86);
 
addTrain(3633, "Shatabdi Express", "Bangalore", "Hyderabad", "09:45", "18:15", 977, "Express", 1809.7);

 addTrain(3634, "Superfast Express", "Lucknow", "Bangalore", "08:00", "09:00", 933, "Express", 1315.36); 

 addTrain(3635, "Duronto Express", "Ahmedabad", "Hyderabad", "20:45", "03:00", 586, "Passenger", 1029.35); 

 addTrain(3636, "Shatabdi Express", "Lucknow", "Hyderabad", "17:30", "14:00", 1423, "Passenger", 305.61);

  addTrain(3637, "Jan Shatabdi", "Bangalore", "Mumbai", "07:45", "19:00", 1848, "Express", 643.83);

addTrain(3638, "Duronto Express", "Delhi", "Lucknow", "22:45", "12:00", 149, "Local", 1703.33);

 
addTrain(3639, "Suburban Local", "Bangalore", "Pune", "10:15", "04:00", 1669, "Express", 1994.44);
 
addTrain(3640, "Rajdhani Express", "Mumbai", "Lucknow", "19:00", "07:45", 1896, "Local", 1874.32);
 
addTrain(3641, "Mail Express", "Bangalore", "Mumbai", "18:15", "20:15", 159, "Express", 892.0);
 
addTrain(3642, "Rajdhani Express", "Delhi", "Chennai", "06:00", "15:00", 1319, "Local", 636.52);
 
addTrain(3643, "Intercity Express", "Pune", "Jaipur", "22:00", "11:00", 923, "Local", 1203.06);
 
addTrain(3644, "Shatabdi Express", "Chennai", "Hyderabad", "21:30", "02:30", 1311, "Local", 1153.56);
 
addTrain(3645, "Suburban Local", "Pune", "Ahmedabad", "20:30", "17:30", 1674, "Local", 1669.82);
 
addTrain(3646, "Suburban Local", "Delhi", "Bangalore", "19:45", "16:45", 1073, "Local", 1917.97);
 
addTrain(3647, "Superfast Express", "Pune", "Ahmedabad", "19:45", "06:00", 1421, "Express", 691.95);
 
addTrain(3648, "Mail Express", "Jaipur", "Chennai", "23:00", "06:15", 1527, "Express", 113.22);
 
addTrain(3649, "Rajdhani Express", "Delhi", "Bangalore", "09:15", "07:45", 233, "Express", 1674.38);
 
addTrain(3650, "Duronto Express", "Bangalore", "Ahmedabad", "20:00", "21:45", 893, "Express", 1025.44);

 addTrain(3651, "Duronto Express", "Bangalore", "Kolkata", "02:15", "18:30", 1579, "Passenger", 132.89);

  addTrain(3652, "MEMU", "Bangalore", "Lucknow", "15:00", "01:00", 1539, "Passenger", 1222.7); 

  addTrain(3653, "Mail Express", "Kolkata", "Bangalore", "04:00", "14:15", 1111, "Express", 990.73);

   addTrain(3654, "Shatabdi Express", "Mumbai", "Kolkata", "18:45", "15:15", 772, "Express", 1570.23);

addTrain(3655, "MEMU", "Chennai", "Pune", "20:45", "01:00", 520, "Passenger", 1170.93);
 
addTrain(3656, "Suburban Local", "Ahmedabad", "Delhi", "21:45", "03:00", 1474, "Passenger", 671.36);
 
addTrain(3657, "Intercity Express", "Bangalore", "Chennai", "21:30", "11:15", 1333, "Local", 1004.16);
 
addTrain(3658, "Jan Shatabdi", "Jaipur", "Delhi", "19:30", "00:15", 731, "Passenger", 121.49);
 
addTrain(3659, "Jan Shatabdi", "Lucknow", "Hyderabad", "13:45", "00:30", 840, "Local", 514.06);
 
addTrain(3660, "Duronto Express", "Pune", "Lucknow", "17:45", "18:30", 1183, "Express", 664.54);
 
addTrain(3661, "Suburban Local", "Kolkata", "Delhi", "00:30", "05:30", 1075, "Passenger", 1546.17);
 
addTrain(3662, "Garib Rath", "Lucknow", "Pune", "06:15", "01:45", 1000, "Express", 1714.23);
 
addTrain(3663, "Intercity Express", "Ahmedabad", "Delhi", "02:30", "17:30", 125, "Local", 1019.18);
 
addTrain(3664, "Superfast Express", "Bangalore", "Hyderabad", "18:45", "22:45", 829, "Express", 850.66);
 
addTrain(3665, "Duronto Express", "Mumbai", "Jaipur", "17:45", "16:15", 635, "Local", 17.84);
 

addTrain(3666, "Duronto Express", "Delhi", "Hyderabad", "14:45", "01:30", 1745, "Passenger", 397.48);

addTrain(3667, "Suburban Local", "Chennai", "Lucknow", "03:00", "09:15", 1260, "Express", 1804.93);

addTrain(3668, "Garib Rath", "Pune", "Lucknow", "00:15", "16:30", 1960, "Express", 484.95);

 addTrain(3669, "Garib Rath", "Jaipur", "Ahmedabad", "11:45", "06:15", 95, "Local", 1932.24); 

 addTrain(3670, "Shatabdi Express", "Mumbai", "Kolkata", "02:30", "15:30", 1138, "Express", 953.37);

addTrain(3671, "Intercity Express", "Ahmedabad", "Lucknow", "15:15", "14:15", 1569, "Local", 10.05);
 
addTrain(3672, "Duronto Express", "Kolkata", "Ahmedabad", "07:45", "12:00", 623, "Express", 186.42);
 
addTrain(3673, "Suburban Local", "Jaipur", "Delhi", "01:30", "01:15", 676, "Express", 1149.56);
 
addTrain(3674, "Jan Shatabdi", "Jaipur", "Pune", "09:15", "13:00", 260, "Local", 1282.56);
 
addTrain(3675, "Suburban Local", "Hyderabad", "Lucknow", "23:45", "15:15", 1490, "Local", 1302.4);
 
addTrain(3676, "Rajdhani Express", "Lucknow", "Delhi", "13:00", "00:30", 630, "Passenger", 1108.07);
 
addTrain(3677, "MEMU", "Pune", "Chennai", "11:30", "05:45", 316, "Passenger", 1794.17);
 
addTrain(3678, "Mail Express", "Kolkata", "Mumbai", "02:45", "20:15", 1189, "Express", 591.24);
 
addTrain(3679, "Mail Express", "Hyderabad", "Mumbai", "21:30", "23:30", 658, "Passenger", 1689.2);
 
addTrain(3680, "Intercity Express", "Jaipur", "Ahmedabad", "13:30", "14:30", 616, "Local", 1359.37);
 
addTrain(3681, "Intercity Express", "Bangalore", "Lucknow", "02:00", "09:00", 1150, "Local", 905.36);
 
addTrain(3682, "MEMU", "Bangalore", "Jaipur", "21:30", "05:15", 1869, "Local", 427.17);
 
addTrain(3683, "Shatabdi Express", "Mumbai", "Ahmedabad", "04:45", "21:30", 1638, "Local", 774.76); 

addTrain(3684, "Mail Express", "Chennai", "Jaipur", "10:30", "16:15", 585, "Passenger", 1589.3); 

addTrain(3685, "MEMU", "Pune", "Ahmedabad", "05:30", "04:15", 1679, "Express", 1329.9); 

addTrain(3686, "Garib Rath", "Mumbai", "Hyderabad", "23:00", "12:00", 1572, "Passenger", 1042.05); 

addTrain(3687, "Jan Shatabdi", "Mumbai", "Delhi", "08:15", "19:45", 751, "Express", 1662.39);

addTrain(3688, "Intercity Express", "Delhi", "Pune", "02:45", "13:00", 865, "Passenger", 976.34);
 
addTrain(3689, "Shatabdi Express", "Kolkata", "Bangalore", "05:30", "17:15", 1502, "Passenger", 29.97);
 
addTrain(3690, "Superfast Express", "Pune", "Ahmedabad", "15:30", "18:00", 560, "Passenger", 1111.35);
 
addTrain(3691, "Superfast Express", "Hyderabad", "Mumbai", "05:30", "13:30", 1855, "Passenger", 82.32);
 
addTrain(3692, "Mail Express", "Jaipur", "Mumbai", "05:00", "12:00", 820, "Express", 2000.0);
 
addTrain(3693, "Duronto Express", "Jaipur", "Bangalore", "16:00", "03:45", 1858, "Express", 1635.68);
 
addTrain(3694, "Mail Express", "Bangalore", "Ahmedabad", "19:00", "05:30", 1219, "Local", 741.71);
 
addTrain(3695, "Rajdhani Express", "Mumbai", "Chennai", "00:00", "05:45", 1643, "Passenger", 671.47);
 
addTrain(3696, "Mail Express", "Hyderabad", "Pune", "03:00", "20:00", 1614, "Passenger", 1104.95);
 
addTrain(3697, "MEMU", "Pune", "Delhi", "16:45", "04:45", 1517, "Passenger", 1224.29);
 
addTrain(3698, "Duronto Express", "Kolkata", "Ahmedabad", "01:30", "05:00", 472, "Passenger", 449.58);
 
addTrain(3699, "Suburban Local", "Jaipur", "Delhi", "07:30", "13:00", 1009, "Local", 516.26);

 addTrain(3700, "Superfast Express", "Pune", "Ahmedabad", "08:30", "07:30", 163, "Express", 1464.75); 

 addTrain(3701, "Intercity Express", "Ahmedabad", "Bangalore", "14:15", "08:30", 1721, "Express", 517.04);

  addTrain(3702, "Intercity Express", "Mumbai", "Chennai", "06:00", "04:45", 1516, "Express", 699.43); 

  addTrain(3703, "Duronto Express", "Kolkata", "Jaipur", "10:30", "01:30", 1675, "Passenger", 534.39);

addTrain(3704, "Suburban Local", "Kolkata", "Chennai", "12:00", "16:15", 1637, "Local", 761.41);
 
addTrain(3705, "Duronto Express", "Pune", "Lucknow", "11:15", "17:00", 784, "Local", 243.98);
 
addTrain(3706, "Garib Rath", "Pune", "Mumbai", "06:45", "21:00", 1284, "Passenger", 1084.67);
 
addTrain(3707, "Rajdhani Express", "Ahmedabad", "Delhi", "12:00", "05:30", 211, "Express", 1877.42);
 
addTrain(3708, "Superfast Express", "Kolkata", "Chennai", "07:45", "22:00", 759, "Passenger", 138.35);
 
addTrain(3709, "Jan Shatabdi", "Bangalore", "Jaipur", "10:00", "09:30", 1075, "Local", 1496.7);
 
addTrain(3710, "Shatabdi Express", "Lucknow", "Delhi", "15:45", "13:00", 302, "Passenger", 1971.37);
 
addTrain(3711, "Rajdhani Express", "Hyderabad", "Kolkata", "04:15", "15:30", 473, "Local", 1054.61);
 
addTrain(3712, "Suburban Local", "Delhi", "Pune", "15:15", "22:45", 490, "Express", 648.25);
 
addTrain(3713, "Superfast Express", "Jaipur", "Lucknow", "16:30", "19:45", 563, "Express", 1580.07);
 
addTrain(3714, "Duronto Express", "Chennai", "Kolkata", "20:30", "12:15", 1516, "Express", 962.29);
 
addTrain(3715, "Rajdhani Express", "Bangalore", "Kolkata", "06:00", "16:00", 1447, "Local", 1146.73);
 
addTrain(3716, "Suburban Local", "Jaipur", "Delhi", "19:00", "08:45", 1876, "Passenger", 1156.18);

 addTrain(3717, "MEMU", "Chennai", "Ahmedabad", "20:00", "13:45", 766, "Express", 1961.87); 
 
 addTrain(3718, "Intercity Express", "Delhi", "Pune", "17:45", "09:15", 1967, "Local", 169.52); 

 addTrain(3719, "Superfast Express", "Kolkata", "Hyderabad", "11:15", "08:30", 1081, "Express", 1641.32);

  addTrain(3720, "Shatabdi Express", "Pune", "Jaipur", "04:30", "03:45", 859, "Passenger", 145.09);

addTrain(3721, "MEMU", "Chennai", "Ahmedabad", "04:00", "05:45", 56, "Express", 1401.36);
 
addTrain(3722, "Rajdhani Express", "Delhi", "Lucknow", "10:15", "15:30", 1428, "Local", 441.03);
 
addTrain(3723, "Intercity Express", "Ahmedabad", "Kolkata", "23:45", "16:15", 65, "Passenger", 838.26);
 
addTrain(3724, "Garib Rath", "Lucknow", "Chennai", "19:00", "23:45", 1195, "Express", 1078.93);
 
addTrain(3725, "Shatabdi Express", "Delhi", "Ahmedabad", "21:45", "10:45", 1191, "Passenger", 243.65);
 
addTrain(3726, "Superfast Express", "Ahmedabad", "Jaipur", "07:45", "16:45", 1013, "Local", 52.01);
 
addTrain(3727, "Superfast Express", "Bangalore", "Chennai", "03:30", "04:15", 416, "Passenger", 1470.63);
 
addTrain(3728, "Intercity Express", "Mumbai", "Bangalore", "17:00", "15:15", 1285, "Express", 1448.01);
 
addTrain(3729, "Suburban Local", "Ahmedabad", "Jaipur", "13:30", "17:30", 1499, "Local", 1417.84);
 
addTrain(3730, "Jan Shatabdi", "Mumbai", "Hyderabad", "18:15", "16:15", 560, "Local", 358.51);
 
addTrain(3731, "Suburban Local", "Jaipur", "Mumbai", "19:15", "15:30", 1937, "Passenger", 1852.45);
 
addTrain(3732, "Intercity Express", "Ahmedabad", "Chennai", "09:30", "14:45", 1998, "Local", 276.28); 

addTrain(3733, "Superfast Express", "Mumbai", "Chennai", "16:00", "05:45", 962, "Local", 1160.03); 

addTrain(3734, "Shatabdi Express", "Hyderabad", "Kolkata", "10:15", "22:00", 778, "Local", 979.7);

 addTrain(3735, "Duronto Express", "Hyderabad", "Kolkata", "21:00", "22:00", 906, "Express", 490.41);

  addTrain(3736, "Jan Shatabdi", "Chennai", "Ahmedabad", "15:45", "17:15", 231, "Passenger", 1229.89);

addTrain(3737, "MEMU", "Delhi", "Jaipur", "13:30", "19:45", 279, "Express", 266.4);
 
addTrain(3738, "Jan Shatabdi", "Jaipur", "Mumbai", "07:30", "01:15", 161, "Local", 1921.66);
 
addTrain(3739, "Mail Express", "Lucknow", "Pune", "04:45", "12:15", 1393, "Local", 513.6);
 
addTrain(3740, "MEMU", "Lucknow", "Pune", "17:00", "16:15", 452, "Express", 44.1);
 
addTrain(3741, "Duronto Express", "Jaipur", "Mumbai", "04:00", "10:30", 1473, "Passenger", 417.9);
 
addTrain(3742, "Jan Shatabdi", "Ahmedabad", "Delhi", "10:30", "08:45", 42, "Express", 779.85);
 
addTrain(3743, "MEMU", "Delhi", "Lucknow", "01:45", "06:00", 1251, "Local", 1911.17);
 
addTrain(3744, "Duronto Express", "Ahmedabad", "Jaipur", "03:15", "19:00", 138, "Express", 1366.39);
 
addTrain(3745, "Mail Express", "Mumbai", "Chennai", "01:00", "20:30", 1378, "Local", 1417.6);
 
addTrain(3746, "Shatabdi Express", "Hyderabad", "Kolkata", "02:00", "07:45", 1815, "Passenger", 1225.12);
 
addTrain(3747, "Shatabdi Express", "Jaipur", "Kolkata", "06:45", "09:00", 525, "Local", 361.96);
 
addTrain(3748, "Shatabdi Express", "Delhi", "Kolkata", "12:00", "10:15", 461, "Local", 539.72);
 
addTrain(3749, "Duronto Express", "Kolkata", "Pune", "23:45", "12:30", 1067, "Passenger", 163.82);

 addTrain(3750, "Shatabdi Express", "Pune", "Chennai", "22:00", "15:00", 833, "Express", 841.94);

  addTrain(3751, "Jan Shatabdi", "Kolkata", "Ahmedabad", "04:30", "15:00", 187, "Passenger", 1613.68);

   addTrain(3752, "Garib Rath", "Delhi", "Bangalore", "10:15", "05:30", 835, "Express", 416.43); 

   addTrain(3753, "Jan Shatabdi", "Chennai", "Ahmedabad", "11:45", "10:45", 656, "Passenger", 1900.61);

addTrain(3754, "Suburban Local", "Hyderabad", "Delhi", "11:15", "01:30", 917, "Local", 338.83);
 
addTrain(3755, "Jan Shatabdi", "Pune", "Chennai", "14:45", "05:15", 1703, "Local", 559.98);
 
addTrain(3756, "Superfast Express", "Hyderabad", "Delhi", "08:15", "17:30", 450, "Passenger", 509.34);
 
addTrain(3757, "Garib Rath", "Kolkata", "Pune", "17:45", "17:45", 231, "Express", 51.26);
 
addTrain(3758, "Garib Rath", "Delhi", "Bangalore", "14:30", "10:15", 1336, "Local", 1655.74);
 
addTrain(3759, "Garib Rath", "Jaipur", "Lucknow", "11:30", "11:15", 1810, "Local", 973.89);
 
addTrain(3760, "Jan Shatabdi", "Kolkata", "Lucknow", "23:30", "06:45", 251, "Express", 70.08);
 
addTrain(3761, "Intercity Express", "Kolkata", "Pune", "16:15", "12:45", 296, "Passenger", 503.97);
 
addTrain(3762, "Mail Express", "Ahmedabad", "Hyderabad", "03:15", "04:00", 1829, "Express", 607.85);
 
addTrain(3763, "Superfast Express", "Mumbai", "Hyderabad", "03:45", "05:30", 38, "Local", 1219.03);
 
addTrain(3764, "Jan Shatabdi", "Ahmedabad", "Bangalore", "04:45", "23:45", 724, "Express", 887.38);
 
addTrain(3765, "Superfast Express", "Mumbai", "Bangalore", "20:30", "10:45", 1172, "Local", 605.47);

 addTrain(3766, "Jan Shatabdi", "Ahmedabad", "Pune", "22:00", "08:45", 768, "Express", 1502.05); 

 addTrain(3767, "Mail Express", "Delhi", "Chennai", "04:00", "08:00", 558, "Express", 197.77); 

 addTrain(3768, "Shatabdi Express", "Hyderabad", "Bangalore", "11:30", "19:15", 1600, "Passenger", 179.93);

  addTrain(3769, "Garib Rath", "Mumbai", "Kolkata", "10:45", "17:00", 596, "Passenger", 994.11);

addTrain(3770, "Duronto Express", "Chennai", "Kolkata", "20:15", "12:45", 1311, "Express", 1901.47);
 
addTrain(3771, "Mail Express", "Delhi", "Mumbai", "16:45", "21:15", 946, "Local", 1793.62);
 
addTrain(3772, "Mail Express", "Hyderabad", "Bangalore", "18:00", "20:00", 1314, "Express", 548.21);
 
addTrain(3773, "Intercity Express", "Pune", "Bangalore", "06:15", "10:45", 970, "Express", 19.79);
 
addTrain(3774, "Duronto Express", "Kolkata", "Pune", "04:45", "07:15", 79, "Express", 641.42);
 
addTrain(3775, "Garib Rath", "Delhi", "Mumbai", "09:15", "21:45", 1411, "Local", 471.11);
 
addTrain(3776, "Garib Rath", "Mumbai", "Delhi", "11:30", "20:30", 467, "Express", 758.51);
 
addTrain(3777, "Garib Rath", "Ahmedabad", "Mumbai", "02:45", "05:00", 101, "Express", 1755.71);
 
addTrain(3778, "Intercity Express", "Ahmedabad", "Bangalore", "19:00", "20:45", 783, "Passenger", 951.04);
 
addTrain(3779, "MEMU", "Bangalore", "Jaipur", "03:15", "20:15", 1607, "Local", 592.97);
 
addTrain(3780, "Suburban Local", "Delhi", "Chennai", "05:15", "16:45", 1083, "Passenger", 587.57);
 
addTrain(3781, "Shatabdi Express", "Bangalore", "Lucknow", "08:45", "09:15", 405, "Passenger", 276.75);
 
addTrain(3782, "Rajdhani Express", "Bangalore", "Mumbai", "00:30", "02:45", 329, "Passenger", 1594.95);

 addTrain(3783, "Intercity Express", "Lucknow", "Kolkata", "13:15", "04:15", 1073, "Express", 1001.44);

  addTrain(3784, "Rajdhani Express", "Chennai", "Delhi", "09:00", "21:30", 1266, "Express", 1553.91);

   addTrain(3785, "Mail Express", "Lucknow", "Bangalore", "09:45", "23:00", 1809, "Express", 1688.23);

    addTrain(3786, "Intercity Express", "Hyderabad", "Delhi", "14:15", "12:15", 1277, "Local", 471.58);

addTrain(3787, "Jan Shatabdi", "Jaipur", "Bangalore", "03:30", "02:45", 602, "Passenger", 1760.22);
 
addTrain(3788, "Jan Shatabdi", "Pune", "Bangalore", "21:00", "22:00", 469, "Passenger", 116.45);
 
addTrain(3789, "Shatabdi Express", "Kolkata", "Hyderabad", "05:15", "02:30", 838, "Express", 901.58);
 
addTrain(3790, "Duronto Express", "Delhi", "Hyderabad", "14:45", "05:45", 1958, "Passenger", 1646.99);
 
addTrain(3791, "Mail Express", "Lucknow", "Jaipur", "21:00", "00:30", 589, "Passenger", 531.52);
 
addTrain(3792, "Superfast Express", "Lucknow", "Ahmedabad", "10:15", "08:45", 1724, "Local", 1785.41);
 
addTrain(3793, "Superfast Express", "Chennai", "Hyderabad", "18:45", "14:30", 727, "Express", 1342.25);
 
addTrain(3794, "Superfast Express", "Kolkata", "Ahmedabad", "21:30", "15:45", 1578, "Local", 1122.17);
 
addTrain(3795, "Duronto Express", "Lucknow", "Chennai", "14:00", "17:15", 557, "Express", 1795.88);
 
addTrain(3796, "MEMU", "Pune", "Bangalore", "06:00", "06:15", 1809, "Local", 331.98);
 
addTrain(3797, "Superfast Express", "Ahmedabad", "Jaipur", "12:30", "17:45", 447, "Local", 50.59);
 
addTrain(3798, "Intercity Express", "Mumbai", "Delhi", "21:15", "07:45", 441, "Passenger", 1810.01);

 addTrain(3799, "MEMU", "Chennai", "Mumbai", "09:45", "21:00", 1261, "Passenger", 749.06);

  addTrain(3800, "MEMU", "Jaipur", "Lucknow", "09:30", "18:45", 1706, "Passenger", 1355.37);

   addTrain(3801, "Superfast Express", "Lucknow", "Kolkata", "21:00", "05:15", 150, "Passenger", 575.28); 

   addTrain(3802, "Jan Shatabdi", "Kolkata", "Pune", "10:30", "20:45", 207, "Passenger", 468.78);

addTrain(3803, "Mail Express", "Kolkata", "Bangalore", "16:15", "08:30", 819, "Express", 1834.47);
 
addTrain(3804, "Intercity Express", "Jaipur", "Delhi", "17:00", "21:15", 1876, "Passenger", 1914.06);
 
addTrain(3805, "Jan Shatabdi", "Lucknow", "Mumbai", "15:15", "20:00", 165, "Passenger", 1454.47);
 
addTrain(3806, "Duronto Express", "Pune", "Ahmedabad", "21:30", "01:15", 1253, "Passenger", 453.93);
 
addTrain(3807, "Garib Rath", "Ahmedabad", "Chennai", "01:15", "03:45", 710, "Express", 961.7);
 
addTrain(3808, "MEMU", "Lucknow", "Jaipur", "22:00", "20:30", 219, "Passenger", 234.81);
 
addTrain(3809, "Shatabdi Express", "Lucknow", "Bangalore", "13:45", "13:45", 1288, "Express", 1009.88);
 
addTrain(3810, "Rajdhani Express", "Kolkata", "Mumbai", "15:15", "22:30", 793, "Express", 1677.52);
 
addTrain(3811, "Rajdhani Express", "Delhi", "Mumbai", "21:45", "12:00", 29, "Passenger", 101.31);
 
addTrain(3812, "Rajdhani Express", "Hyderabad", "Lucknow", "13:00", "23:15", 327, "Passenger", 1026.9);
 
addTrain(3813, "Duronto Express", "Kolkata", "Mumbai", "21:45", "21:45", 1378, "Passenger", 1039.84);
 
addTrain(3814, "Jan Shatabdi", "Kolkata", "Bangalore", "10:45", "08:00", 1176, "Local", 1405.55);
 
addTrain(3815, "Rajdhani Express", "Bangalore", "Chennai", "00:30", "22:15", 453, "Local", 344.25); 

addTrain(3816, "Garib Rath", "Bangalore", "Jaipur", "13:45", "13:30", 1996, "Passenger", 732.8); 

addTrain(3817, "Garib Rath", "Kolkata", "Hyderabad", "01:45", "12:30", 1057, "Local", 1745.72);

 addTrain(3818, "Duronto Express", "Chennai", "Ahmedabad", "00:00", "09:30", 1171, "Express", 1718.56); 

 addTrain(3819, "Intercity Express", "Ahmedabad", "Bangalore", "04:15", "09:00", 1233, "Express", 353.4);

addTrain(3820, "Mail Express", "Bangalore", "Chennai", "16:45", "12:15", 174, "Local", 1773.05);
 
addTrain(3821, "Rajdhani Express", "Hyderabad", "Lucknow", "18:00", "16:30", 807, "Local", 24.04);
 
addTrain(3822, "Duronto Express", "Ahmedabad", "Kolkata", "18:15", "01:15", 419, "Passenger", 1207.29);
 
addTrain(3823, "Mail Express", "Delhi", "Kolkata", "17:30", "15:30", 1841, "Express", 1211.52);
 
addTrain(3824, "Rajdhani Express", "Kolkata", "Mumbai", "08:15", "06:30", 508, "Passenger", 305.45);
 
addTrain(3825, "Duronto Express", "Delhi", "Pune", "01:00", "21:30", 1179, "Passenger", 1244.37);
 
addTrain(3826, "Intercity Express", "Pune", "Bangalore", "09:30", "21:15", 1737, "Passenger", 1000.46);
 
addTrain(3827, "Intercity Express", "Pune", "Ahmedabad", "03:15", "20:00", 429, "Express", 1009.39);
 
addTrain(3828, "Jan Shatabdi", "Lucknow", "Kolkata", "20:30", "03:00", 1189, "Local", 1881.75);
 
addTrain(3829, "Suburban Local", "Mumbai", "Ahmedabad", "15:30", "08:15", 1355, "Passenger", 914.92);
 
addTrain(3830, "Superfast Express", "Bangalore", "Delhi", "13:30", "19:15", 1321, "Passenger", 1879.86);
 
addTrain(3831, "Shatabdi Express", "Pune", "Ahmedabad", "00:00", "21:30", 142, "Express", 981.51);

 addTrain(3832, "Suburban Local", "Chennai", "Kolkata", "11:30", "14:00", 416, "Passenger", 1500.55);

  addTrain(3833, "Duronto Express", "Bangalore", "Jaipur", "16:00", "19:00", 1965, "Local", 811.62);

   addTrain(3834, "Superfast Express", "Hyderabad", "Bangalore", "22:45", "13:00", 1177, "Local", 427.31);

    addTrain(3835, "Suburban Local", "Jaipur", "Pune", "05:00", "06:00", 601, "Passenger", 1204.58);

addTrain(3836, "MEMU", "Ahmedabad", "Hyderabad", "14:15", "22:45", 1657, "Express", 1480.5);
 
addTrain(3837, "Rajdhani Express", "Jaipur", "Chennai", "09:00", "20:30", 50, "Express", 1491.68);
 
addTrain(3838, "MEMU", "Mumbai", "Delhi", "06:00", "16:45", 276, "Express", 1847.13);
 
addTrain(3839, "Superfast Express", "Lucknow", "Hyderabad", "12:45", "06:45", 1696, "Express", 978.41);
 
addTrain(3840, "Garib Rath", "Pune", "Lucknow", "20:30", "04:15", 149, "Express", 426.41);
 
addTrain(3841, "Jan Shatabdi", "Mumbai", "Pune", "11:30", "09:30", 625, "Passenger", 1581.06);
 
addTrain(3842, "Jan Shatabdi", "Kolkata", "Chennai", "23:15", "04:00", 958, "Express", 300.58);
 
addTrain(3843, "MEMU", "Delhi", "Kolkata", "17:30", "02:00", 56, "Local", 1177.25);
 
addTrain(3844, "Rajdhani Express", "Chennai", "Ahmedabad", "23:30", "15:00", 556, "Passenger", 655.63);
 
addTrain(3845, "Rajdhani Express", "Hyderabad", "Lucknow", "08:45", "05:15", 789, "Express", 1114.65);
 
addTrain(3846, "Garib Rath", "Chennai", "Bangalore", "11:00", "10:30", 1282, "Express", 1265.16);
 
addTrain(3847, "Intercity Express", "Kolkata", "Delhi", "03:00", "16:30", 1432, "Passenger", 1482.12);
 
addTrain(3848, "MEMU", "Kolkata", "Chennai", "05:45", "07:00", 1247, "Passenger", 240.27); 

addTrain(3849, "MEMU", "Delhi", "Hyderabad", "08:00", "11:45", 1355, "Express", 1530.86); 

addTrain(3850, "Superfast Express", "Delhi", "Lucknow", "14:15", "23:45", 73, "Express", 1747.86);

 addTrain(3851, "Suburban Local", "Mumbai", "Bangalore", "06:45", "02:30", 610, "Local", 988.78);

  addTrain(3852, "Duronto Express", "Kolkata", "Lucknow", "00:45", "10:30", 1613, "Local", 1652.36);

addTrain(3853, "Rajdhani Express", "Mumbai", "Jaipur", "17:30", "05:15", 129, "Local", 1909.81);
 
addTrain(3854, "Mail Express", "Ahmedabad", "Jaipur", "14:45", "10:00", 1856, "Local", 412.28);
 
addTrain(3855, "Suburban Local", "Pune", "Ahmedabad", "23:30", "20:00", 1744, "Local", 654.87);
 
addTrain(3856, "Superfast Express", "Jaipur", "Pune", "08:00", "08:30", 1154, "Local", 561.07);
 
addTrain(3857, "MEMU", "Ahmedabad", "Hyderabad", "11:30", "18:00", 80, "Local", 139.55);
 
addTrain(3858, "Mail Express", "Chennai", "Mumbai", "10:00", "19:00", 1370, "Express", 834.65);
 
addTrain(3859, "Shatabdi Express", "Lucknow", "Mumbai", "12:15", "04:30", 548, "Passenger", 700.55);
 
addTrain(3860, "Shatabdi Express", "Hyderabad", "Kolkata", "19:45", "14:15", 704, "Passenger", 561.45);
 
addTrain(3861, "Garib Rath", "Hyderabad", "Chennai", "14:15", "01:45", 1756, "Express", 1218.23);
 
addTrain(3862, "Duronto Express", "Bangalore", "Lucknow", "03:45", "21:15", 1247, "Local", 1762.38);
 
addTrain(3863, "Superfast Express", "Lucknow", "Kolkata", "00:15", "08:15", 985, "Express", 984.82);
 
addTrain(3864, "Rajdhani Express", "Kolkata", "Hyderabad", "19:45", "10:15", 1818, "Express", 567.21);

 addTrain(3865, "Jan Shatabdi", "Kolkata", "Delhi", "18:45", "10:45", 1087, "Local", 762.11);

  addTrain(3866, "Mail Express", "Ahmedabad", "Chennai", "09:45", "06:30", 958, "Local", 141.02); 

  addTrain(3867, "Suburban Local", "Chennai", "Pune", "13:30", "04:30", 1008, "Express", 119.0); 

  addTrain(3868, "Shatabdi Express", "Kolkata", "Pune", "07:15", "03:30", 386, "Passenger", 1221.2);

addTrain(3869, "Rajdhani Express", "Jaipur", "Lucknow", "00:45", "08:15", 837, "Passenger", 1021.62);
 
addTrain(3870, "Intercity Express", "Bangalore", "Chennai", "01:15", "20:00", 230, "Local", 1214.57);
 
addTrain(3871, "Intercity Express", "Hyderabad", "Ahmedabad", "08:00", "16:30", 181, "Express", 1576.99);
 
addTrain(3872, "Intercity Express", "Mumbai", "Bangalore", "19:30", "11:45", 927, "Passenger", 563.32);
 
addTrain(3873, "Suburban Local", "Delhi", "Lucknow", "12:30", "07:30", 1472, "Local", 1538.6);
 
addTrain(3874, "Garib Rath", "Lucknow", "Mumbai", "11:00", "11:15", 202, "Express", 588.8);
 
addTrain(3875, "Shatabdi Express", "Hyderabad", "Mumbai", "19:45", "14:45", 1585, "Local", 892.62);
 
addTrain(3876, "Suburban Local", "Pune", "Chennai", "11:00", "14:30", 1106, "Passenger", 957.11);
 
addTrain(3877, "Duronto Express", "Mumbai", "Delhi", "07:45", "04:15", 1958, "Express", 1809.16);
 
addTrain(3878, "Intercity Express", "Mumbai", "Kolkata", "21:00", "15:30", 228, "Passenger", 908.66);
 
addTrain(3879, "Garib Rath", "Ahmedabad", "Hyderabad", "09:00", "09:30", 1814, "Passenger", 455.43);
 
addTrain(3880, "Suburban Local", "Kolkata", "Ahmedabad", "19:30", "17:15", 1492, "Express", 1142.49);
 
addTrain(3881, "Jan Shatabdi", "Delhi", "Jaipur", "04:45", "09:45", 1835, "Express", 114.82);

 addTrain(3882, "Suburban Local", "Ahmedabad", "Jaipur", "03:00", "04:00", 1007, "Express", 146.29);

  addTrain(3883, "Mail Express", "Mumbai", "Chennai", "08:00", "21:30", 400, "Passenger", 884.53); 

  addTrain(3884, "Intercity Express", "Lucknow", "Jaipur", "22:15", "07:30", 1222, "Passenger", 1863.66);

   addTrain(3885, "MEMU", "Bangalore", "Ahmedabad", "12:15", "11:15", 1530, "Passenger", 1790.71);

addTrain(3886, "Shatabdi Express", "Kolkata", "Hyderabad", "00:30", "10:45", 1490, "Express", 1647.48);
 
addTrain(3887, "Mail Express", "Ahmedabad", "Kolkata", "02:45", "20:15", 1397, "Passenger", 1399.12);
 
addTrain(3888, "Rajdhani Express", "Pune", "Lucknow", "11:15", "05:45", 1362, "Passenger", 374.25);
 
addTrain(3889, "Intercity Express", "Chennai", "Ahmedabad", "21:00", "06:00", 1212, "Local", 965.73);
 
addTrain(3890, "Mail Express", "Ahmedabad", "Chennai", "02:45", "08:45", 1039, "Express", 1611.45);
 
addTrain(3891, "Mail Express", "Chennai", "Pune", "04:15", "22:30", 767, "Local", 1910.55);
 
addTrain(3892, "Mail Express", "Delhi", "Lucknow", "03:00", "22:45", 1713, "Express", 1864.94);
 
addTrain(3893, "Intercity Express", "Jaipur", "Bangalore", "04:45", "02:00", 1211, "Express", 1823.62);
 
addTrain(3894, "Garib Rath", "Ahmedabad", "Kolkata", "21:00", "22:30", 1334, "Local", 289.99);
 
addTrain(3895, "Garib Rath", "Bangalore", "Kolkata", "03:15", "03:00", 1721, "Passenger", 1432.92);
 
addTrain(3896, "Superfast Express", "Chennai", "Kolkata", "23:30", "04:00", 161, "Passenger", 1498.78);
 
addTrain(3897, "Mail Express", "Delhi", "Hyderabad", "07:30", "18:45", 723, "Passenger", 1281.25);

 addTrain(3898, "Rajdhani Express", "Jaipur", "Pune", "01:30", "01:15", 1428, "Passenger", 1671.04);

  addTrain(3899, "Suburban Local", "Mumbai", "Ahmedabad", "15:45", "01:30", 1916, "Local", 365.44);

   addTrain(3900, "Duronto Express", "Pune", "Ahmedabad", "05:15", "06:45", 1224, "Local", 1912.64);

   addTrain(3901, "Intercity Express", "Jaipur", "Pune", "10:30", "03:00", 710, "Local", 137.68);

addTrain(3902, "Shatabdi Express", "Chennai", "Mumbai", "02:00", "21:15", 1550, "Express", 1786.61);
 
addTrain(3903, "Suburban Local", "Hyderabad", "Bangalore", "04:45", "05:15", 405, "Passenger", 130.77);
 
addTrain(3904, "Suburban Local", "Lucknow", "Kolkata", "11:00", "00:15", 138, "Express", 519.44);
 
addTrain(3905, "Intercity Express", "Bangalore", "Pune", "14:45", "12:15", 765, "Passenger", 1525.89);
 
addTrain(3906, "Rajdhani Express", "Hyderabad", "Mumbai", "01:00", "04:15", 309, "Local", 1150.45);
 
addTrain(3907, "Intercity Express", "Ahmedabad", "Bangalore", "20:00", "18:45", 1471, "Passenger", 1600.49);
 
addTrain(3908, "Mail Express", "Hyderabad", "Lucknow", "14:45", "18:45", 630, "Passenger", 1074.02);
 
addTrain(3909, "MEMU", "Mumbai", "Delhi", "07:00", "21:00", 1873, "Express", 712.33);
 
addTrain(3910, "Shatabdi Express", "Kolkata", "Hyderabad", "06:00", "00:00", 889, "Express", 952.03);
 
addTrain(3911, "Shatabdi Express", "Chennai", "Bangalore", "16:15", "18:00", 448, "Express", 527.82);
 
addTrain(3912, "Mail Express", "Delhi", "Lucknow", "17:45", "19:45", 1272, "Express", 706.99);
 
addTrain(3913, "Garib Rath", "Pune", "Lucknow", "21:15", "19:45", 1348, "Express", 987.07);
 
addTrain(3914, "Suburban Local", "Kolkata", "Hyderabad", "02:45", "05:30", 373, "Local", 1759.5);

 addTrain(3915, "Jan Shatabdi", "Kolkata", "Bangalore", "02:45", "09:30", 390, "Passenger", 872.69); 

 addTrain(3916, "MEMU", "Ahmedabad", "Delhi", "01:15", "10:00", 558, "Passenger", 1923.26);

  addTrain(3917, "Superfast Express", "Jaipur", "Hyderabad", "01:30", "03:15", 1416, "Passenger", 1400.31); 
  
  addTrain(3918, "Duronto Express", "Lucknow", "Chennai", "02:30", "16:15", 1335, "Passenger", 1151.7);

addTrain(3919, "Duronto Express", "Mumbai", "Lucknow", "16:15", "03:15", 1914, "Express", 1483.35);
 
addTrain(3920, "Shatabdi Express", "Mumbai", "Hyderabad", "14:30", "23:30", 370, "Passenger", 1867.59);
 
addTrain(3921, "Shatabdi Express", "Mumbai", "Delhi", "06:45", "05:30", 849, "Express", 93.46);
 
addTrain(3922, "Duronto Express", "Hyderabad", "Ahmedabad", "05:15", "18:15", 1242, "Passenger", 664.69);
 
addTrain(3923, "Garib Rath", "Chennai", "Mumbai", "17:00", "09:45", 551, "Local", 590.32);
 
addTrain(3924, "Mail Express", "Chennai", "Lucknow", "20:30", "15:45", 1398, "Express", 234.79);
 
addTrain(3925, "Duronto Express", "Jaipur", "Kolkata", "00:45", "04:15", 1003, "Passenger", 1200.2);
 
addTrain(3926, "Mail Express", "Bangalore", "Ahmedabad", "06:15", "15:00", 813, "Express", 1756.22);
 
addTrain(3927, "Mail Express", "Chennai", "Hyderabad", "10:15", "08:30", 1951, "Express", 596.25);
 
addTrain(3928, "Duronto Express", "Lucknow", "Jaipur", "00:00", "08:00", 1963, "Local", 746.89);
 
addTrain(3929, "Intercity Express", "Chennai", "Hyderabad", "16:45", "12:00", 1675, "Express", 413.18);
 
addTrain(3930, "Garib Rath", "Mumbai", "Chennai", "22:30", "21:15", 1049, "Local", 466.34); 

addTrain(3931, "MEMU", "Hyderabad", "Lucknow", "21:00", "18:45", 994, "Express", 494.94);

 addTrain(3932, "Shatabdi Express", "Jaipur", "Chennai", "11:30", "13:15", 1016, "Local", 1301.58); 

 addTrain(3933, "Rajdhani Express", "Mumbai", "Delhi", "05:00", "08:15", 1969, "Local", 1975.36); 

 addTrain(3934, "Rajdhani Express", "Bangalore", "Chennai", "20:30", "18:15", 524, "Passenger", 406.99);

addTrain(3935, "Shatabdi Express", "Lucknow", "Pune", "20:30", "19:30", 526, "Local", 70.64);
 
addTrain(3936, "Suburban Local", "Lucknow", "Bangalore", "04:30", "02:30", 1078, "Express", 531.68);
 
addTrain(3937, "Duronto Express", "Jaipur", "Delhi", "19:15", "06:15", 1733, "Local", 1479.35);
 
addTrain(3938, "Mail Express", "Mumbai", "Pune", "21:30", "19:15", 1263, "Express", 1479.68);
 
addTrain(3939, "Superfast Express", "Kolkata", "Lucknow", "15:30", "03:15", 1578, "Passenger", 1763.5);
 
addTrain(3940, "MEMU", "Pune", "Mumbai", "17:15", "19:00", 1581, "Passenger", 1451.2);
 
addTrain(3941, "MEMU", "Delhi", "Pune", "01:15", "22:15", 1680, "Local", 1438.26);
 
addTrain(3942, "Garib Rath", "Ahmedabad", "Jaipur", "07:30", "14:30", 1989, "Passenger", 630.04);
 
addTrain(3943, "Shatabdi Express", "Pune", "Kolkata", "22:45", "11:15", 768, "Express", 1644.48);
 
addTrain(3944, "Shatabdi Express", "Pune", "Ahmedabad", "14:00", "12:00", 1283, "Express", 649.13);
 
addTrain(3945, "Duronto Express", "Hyderabad", "Mumbai", "00:45", "13:30", 36, "Local", 44.98);
 
addTrain(3946, "Suburban Local", "Chennai", "Lucknow", "19:45", "03:45", 1489, "Passenger", 1727.5);
 
addTrain(3947, "MEMU", "Pune", "Delhi", "04:15", "23:45", 379, "Passenger", 583.92);

 addTrain(3948, "Shatabdi Express", "Kolkata", "Bangalore", "03:15", "15:45", 1284, "Local", 1896.02);

  addTrain(3949, "Garib Rath", "Mumbai", "Jaipur", "09:30", "19:30", 1205, "Express", 1207.87);

   addTrain(3950, "MEMU", "Ahmedabad", "Bangalore", "22:15", "05:45", 845, "Passenger", 887.35); 

   addTrain(3951, "Suburban Local", "Hyderabad", "Delhi", "04:45", "13:45", 790, "Express", 1212.91);

addTrain(3952, "MEMU", "Lucknow", "Hyderabad", "06:45", "22:30", 603, "Passenger", 781.12);
 
addTrain(3953, "Superfast Express", "Delhi", "Pune", "04:15", "08:30", 132, "Express", 809.98);
 
addTrain(3954, "Shatabdi Express", "Pune", "Lucknow", "03:15", "19:45", 211, "Local", 1154.53);
 
addTrain(3955, "Shatabdi Express", "Kolkata", "Bangalore", "17:15", "09:00", 1395, "Local", 1623.73);
 
addTrain(3956, "Suburban Local", "Mumbai", "Bangalore", "17:00", "20:45", 129, "Express", 1652.59);
 
addTrain(3957, "Intercity Express", "Jaipur", "Hyderabad", "00:45", "08:00", 496, "Express", 1559.26);
 
addTrain(3958, "Mail Express", "Chennai", "Ahmedabad", "11:15", "15:30", 1423, "Passenger", 434.5);
 
addTrain(3959, "Intercity Express", "Kolkata", "Jaipur", "18:30", "05:45", 83, "Local", 625.41);
 
addTrain(3960, "Intercity Express", "Bangalore", "Jaipur", "07:30", "05:15", 714, "Local", 1003.2);
 
addTrain(3961, "Garib Rath", "Kolkata", "Bangalore", "23:30", "06:45", 483, "Local", 1529.81);
 
addTrain(3962, "Garib Rath", "Hyderabad", "Pune", "14:45", "07:30", 1107, "Express", 1043.19);
 
addTrain(3963, "Mail Express", "Delhi", "Hyderabad", "10:30", "02:45", 923, "Local", 1608.72);

 addTrain(3964, "Jan Shatabdi", "Hyderabad", "Ahmedabad", "15:00", "07:00", 629, "Local", 317.22);

  addTrain(3965, "Mail Express", "Delhi", "Bangalore", "20:45", "21:30", 719, "Passenger", 1980.98);

   addTrain(3966, "Shatabdi Express", "Ahmedabad", "Lucknow", "00:00", "17:15", 688, "Passenger", 1457.09);

    addTrain(3967, "Mail Express", "Mumbai", "Hyderabad", "07:45", "20:45", 1895, "Passenger", 1600.01);

addTrain(3968, "Suburban Local", "Mumbai", "Lucknow", "14:15", "18:15", 103, "Express", 1544.48);
 
addTrain(3969, "Shatabdi Express", "Lucknow", "Delhi", "10:45", "20:30", 1531, "Local", 1730.38);
 
addTrain(3970, "Suburban Local", "Mumbai", "Lucknow", "07:30", "12:45", 1497, "Passenger", 657.41);
 
addTrain(3971, "Jan Shatabdi", "Bangalore", "Ahmedabad", "14:15", "10:30", 295, "Local", 677.57);
 
addTrain(3972, "Intercity Express", "Chennai", "Kolkata", "09:30", "10:00", 655, "Express", 1306.18);
 
addTrain(3973, "Rajdhani Express", "Hyderabad", "Ahmedabad", "06:45", "18:00", 1139, "Passenger", 204.94);
 
addTrain(3974, "Garib Rath", "Lucknow", "Ahmedabad", "02:15", "15:30", 1993, "Express", 1892.9);
 
addTrain(3975, "Intercity Express", "Kolkata", "Chennai", "11:00", "18:00", 1168, "Local", 1788.18);
 
addTrain(3976, "Shatabdi Express", "Mumbai", "Chennai", "03:15", "13:45", 857, "Passenger", 496.05);
 
addTrain(3977, "Mail Express", "Mumbai", "Ahmedabad", "11:15", "23:45", 440, "Passenger", 191.17);
 
addTrain(3978, "MEMU", "Mumbai", "Hyderabad", "17:45", "19:00", 1167, "Local", 363.15);
 
addTrain(3979, "MEMU", "Chennai", "Kolkata", "18:30", "01:30", 1179, "Express", 844.82);
 
addTrain(3980, "Mail Express", "Chennai", "Delhi", "20:00", "08:45", 622, "Express", 216.33); 

addTrain(3981, "Intercity Express", "Lucknow", "Delhi", "12:00", "07:15", 639, "Local", 1080.93); 

addTrain(3982, "Duronto Express", "Lucknow", "Ahmedabad", "23:15", "18:30", 476, "Express", 753.94);

 addTrain(3983, "Duronto Express", "Delhi", "Ahmedabad", "18:45", "17:00", 291, "Passenger", 1165.84);

  addTrain(3984, "Superfast Express", "Lucknow", "Pune", "16:30", "15:45", 851, "Local", 707.33);

addTrain(3985, "Mail Express", "Chennai", "Hyderabad", "13:15", "15:45", 1596, "Local", 1872.68);

 
addTrain(3986, "Shatabdi Express", "Chennai", "Bangalore", "02:30", "04:00", 1500, "Local", 700.7);
 
addTrain(3987, "Shatabdi Express", "Chennai", "Pune", "10:00", "01:45", 80, "Express", 1606.64);
 
addTrain(3988, "Mail Express", "Pune", "Chennai", "23:00", "18:45", 401, "Passenger", 1813.28);
 
addTrain(3989, "MEMU", "Hyderabad", "Mumbai", "15:30", "03:00", 1636, "Local", 1871.2);
 
addTrain(3990, "Garib Rath", "Mumbai", "Chennai", "20:00", "08:30", 81, "Local", 1364.11);
 
addTrain(3991, "Garib Rath", "Chennai", "Mumbai", "23:15", "04:30", 956, "Passenger", 326.25);
 
addTrain(3992, "Superfast Express", "Hyderabad", "Mumbai", "23:15", "03:30", 1078, "Local", 1668.25);
 
addTrain(3993, "Intercity Express", "Lucknow", "Jaipur", "02:30", "23:45", 898, "Local", 848.98);
 
addTrain(3994, "Superfast Express", "Kolkata", "Bangalore", "04:45", "15:00", 1822, "Passenger", 687.11);
 
addTrain(3995, "Suburban Local", "Pune", "Jaipur", "01:15", "14:45", 676, "Local", 1722.6);
 
addTrain(3996, "Shatabdi Express", "Jaipur", "Lucknow", "12:15", "13:45", 1430, "Passenger", 255.35);

 addTrain(3997, "Duronto Express", "Lucknow", "Jaipur", "07:30", "22:30", 1797, "Local", 1769.69); 

 addTrain(3998, "MEMU", "Hyderabad", "Ahmedabad", "06:00", "16:00", 1818, "Local", 660.28);

  addTrain(3999, "MEMU", "Jaipur", "Lucknow", "13:00", "20:45", 711, "Express", 349.99);
 
  }
 
 
  void displayAllTrains() const {
 
        cout << left << setw(15) << "Train Number"
 
             << setw(25) << "Train Name"
 
             << setw(20) << "Source"
 
             << setw(20) << "Destination"
 
             << setw(15) << "Departure"
 
             << setw(15) << "Arrival"
 
             << setw(10) << "Distance"
 
       << setw(15) << "Type"
       << setw(10) << "Price" << endl;

  cout << string(150, '-') << endl;

  for (const auto& train : trains) {
          train.display();
        }
 
    }
 
  const Train* searchTrainByNumber(int number) const {
 
        for (const auto& train : trains) {
 
            if (train.trainNumber == number) {
 
                return &train;
 
            }
 
        }
 
        return nullptr;
 
    }
 
 
  vector<Train> searchTrainByRoute(const string& source, const string& destination) const {
    vector<Train> matchingTrains;
        for (const auto& train : trains) {
 
            if (train.source == source && train.destination == destination) {
 
                matchingTrains.push_back(train);
 
            }
 
        }
 
        return matchingTrains;
 
    }
 
 bool removeTrainByNumber(int trainNumber) {
 
        auto it = std::find_if(trains.begin(), trains.end(), 
 
                               [trainNumber](const Train& train) {
 
                                   return train.trainNumber == trainNumber;
 
                               });
 
        if (it != trains.end()) {
 
      trains.erase(it);
      return true;
  }
  return false;
  }
 
 
 const Train* findTrain(int trainNumber) const {
 
        for (const auto& train : trains) {
 
            if (train.trainNumber == trainNumber) {
 
                return &train;
 
            }
 
        }
 
        return nullptr;
 
    }
 
 
  void searchTrains(const string& src, const string& dest) const {
 
        cout << "Searching for trains from " << src << " to " << dest << "...\n";
      bool found = false;
    for (const auto& train : trains) {
            if (train.source == src && train.destination == dest) {
 
                train.display();
 
                found = true;
 
            }
 
        }
 
        if (!found) {
 
            cout << "No trains found for the specified route.\n";
 
        }
 
    }
 
 
 // Add this method to search trains by distance
  vector<Train> searchTrainsByDistance(int minDistance) const {
 
        vector<Train> matchingTrains;
 
        for (const auto& train : trains) {
 
      if (train.distance >= minDistance) {
          matchingTrains.push_back(train);
      }
  }
    return matchingTrains;
    }
 
};
 
 class Booking {
 
public:
 
    int bookingId;
 
    string passengerName;
 
    int trainNumber;
 
    string seatClass; 
 
    int numTickets;
 
    double ticketPrice;
 
 
  
Booking() : bookingId(0), passengerName(""), trainNumber(0), seatClass(""), numTickets(0), ticketPrice(0.0) {}   Booking(int id, const string& name, int tNumber, const string& sClass, int tickets, double price)
 
        : bookingId(id), passengerName(name), trainNumber(tNumber), seatClass(sClass), numTickets(tickets), ticketPrice(price) {}
 
 };
 
 
 
class BookingSystem {
 
 private:
 
    TrainDatabase& trainDB;
 
    map<int, Booking> bookings;
 
    int nextBookingID;
 
 
 
public:
 
    BookingSystem(TrainDatabase& db) : trainDB(db), nextBookingID(1) {}
 
 
void bookTicket() {
  string src, dest;
  cout << "Enter source station: ";
    cin >> src;
        cout << "Enter destination station: ";
 
        cin >> dest;
 
 
 
        trainDB.searchTrains(src, dest);
 
 
 
        int trainNumber;
 
        cout << "Enter the train number to book: ";
 
        cin >> trainNumber;
 
 
 
        const Train* train = trainDB.findTrain(trainNumber);
 
        if (!train) {
 
            cout << "Invalid train number. Booking failed.\n";
          return;
    }
 
 
    string passengerName, seatClass;
 
    int numTickets;
 
        cout << "Enter passenger name: ";
 
        cin.ignore(); // To ignore the newline character left by the previous input
 
        getline(cin, passengerName);
 
        cout << "Enter seat class (e.g., First Class, Second Class): ";
 
        getline(cin, seatClass);
 
        cout << "Enter number of tickets: ";
 
        cin >> numTickets;
 
 
 
        double ticketPrice = train->price * numTickets;
 
        bookings[nextBookingID] = Booking(nextBookingID, passengerName, trainNumber, seatClass, numTickets, ticketPrice );
 
        cout << "Booking successful! Your booking ID is " << nextBookingID << ".\n";
 
        nextBookingID++;
 
  }
 
 
void viewBooking(int bookingId) const {
    auto it = bookings.find(bookingId);
        if (it == bookings.end()) {
 
            cout << "No booking found with ID " << bookingId << ".\n";
 
            return;
 
        }
 
 
 
        const Booking& booking = it->second;
 
        cout << "Booking ID: " << booking.bookingId << "\n"
 
             << "Passenger Name: " << booking.passengerName << "\n"
 
             << "Train Number: " << booking.trainNumber << "\n"
 
             << "Seat Class: " << booking.seatClass << "\n"
 
             << "Number of Tickets: " << booking.numTickets << "\n"
 
             << "Total Price: " << fixed << setprecision(2) << booking.ticketPrice << "\n";
 
  }
 
 
void cancelBooking(int bookingId) {
    auto it = bookings.find(bookingId);
 
    if (it == bookings.end()) {
 
            cout << "No booking found with ID " << bookingId << ".\n";
 
            return;
 
        }
 
 
 
        bookings.erase(it);
 
        cout << "Booking ID " << bookingId << " has been canceled.\n";
 
    }
 
 };
 
 
bool kmpMatch1(const string& text, const string& pattern) { int m = pattern.size();
int n = text.size();
 
 
    vector<int> lps(m, 0);
 
    int j = 0;
 
 
 
    for (int i = 1; i < m; i++) {
 
        if (pattern[i] == pattern[j]) {
 
            lps[i] = ++j;
 
        } else if (j > 0) {
 
            j = lps[j - 1];
 
            i--;
 
        }
 
    }
 
 
 
  j = 0; for (int i = 0; i < n; i++) {     if (text[i] == pattern[j]) {
        j++;
 
        if (j == m) return true;
 
        } else if (j > 0) {
 
            j = lps[j - 1];
 
            i--;
 
        }
 
    }
 
 
 
    return false;
 
}
 
 
 
string getHiddenPassword1() {
 
    string password = "";
 
char ch;
while ((ch = getch()) != '\r') {     if (ch == '\b') {
        if (!password.empty()) {
                cout << "\b \b";
 
                password.pop_back();
 
            }
 
        } else {
 
            password.push_back(ch);
 
            cout << "*";
 
        }
 
    }
 
    cout << endl;
 
    return password;
 
}
 
 
 void admin_portal() {
TrainDatabase db; db.initializeDatabase();
 
 
string admin_name;
 
    string password;
 
    const string default_password = "admin123";
 
 
 
    cout << "Enter Admin Name: ";
 
    cin >> admin_name;
 
 
 
    cout << "Enter Password: ";
 
    password = getHiddenPassword1();
 
 
 
    if ((admin_name == "harshit" || admin_name == "vaibhav" || 
 
         admin_name == "samarth" || admin_name == "abhishek") && kmpMatch1(password, default_password)) {
 
    int choice;
    do {
        system("cls");
        cout << "Welcome " << admin_name << " to the Admin Portal!\n";
 
 
            cout << "\n\n\t\t--------Admin Portal--------\n";
 
            cout << "1. Display All Trains\n";
 
            cout << "2. Search Train by Number\n";
 
            cout << "3. Search Train by Source and Destination\n";
 
            cout << "4. Remove Train By Number\n";
 
            cout << "5. Exit\n";
 
 
 
            cout << "\nEnter your choice: ";
 
            cin >> choice;
 
 
 
            switch (choice) {
 
            case 1:
 
                db.displayAllTrains();
            break;
        case 2: {
            int trainNumber;
            cout << "Enter Train Number to Search: ";
 
                cin >> trainNumber;
 
                const Train* train = db.searchTrainByNumber(trainNumber);
 
                if (train) {
 
                    cout << "Train Details:\n";
 
                    train->display();
 
                } else {
 
                    cout << "Train not found!\n";
 
                }
 
                break;
 
            }
 
 case 3: {
 
string source, destination; cout << "Enter Source Station: "; cin >> source;
cout << "Enter Destination Station: "; cin >> destination;
 
 
    vector<Train> results = db.searchTrainByRoute(source, destination);
 
    if (!results.empty()) {
 
        cout << "Trains Available from " << source << " to " << destination << ":\n";
 
        for (const auto& train : results) {
 
            train.display();
 
            cout << "-----------------------------\n";  
        }
 
    } else {
 
        cout << "No trains found between " << source << " and " << destination << "!\n";
 
    }
 
    break;
 
}
case 4: {
            int trainNumber;
            cout << "Enter Train Number to Remove: ";
            cin >> trainNumber;
 
                if (db.removeTrainByNumber(trainNumber)) {
 
                    cout << "Train successfully removed.\n";
 
                } else {
 
                    cout << "Train not found or could not be removed.\n";
 
                }
 
                break;
 
            }
 
            case 5:
 
                cout << "Exiting Admin Portal...\n";
 
                break;
 
            default:
 
            cout << "Invalid Choice. Try again!\n";
 
        }
 
 
        cout << "\nPress Enter to continue...";
        cin.ignore(numeric_limits<streamsize>::max(), '\n');
            cin.get();
 
        } while (choice != 5);
 
    } else {
 
        cout << "Access Denied! Unauthorized Admin or Incorrect Password.\n";
 
    }
 
}
 
 
 string toLowerCase(string str);
 void registerUser() {
 
    string name, dob, password, gender, address;
 
    int age;
 
    long long phone, aadhar;
 
 
cout << "Enter your name: "; cin.ignore();
getline(cin, name);
 
    cout << "Enter your age: ";
 
    cin >> age;
 
    cout << "Enter your date of birth (DD/MM/YYYY): ";
 
    cin >> dob;
 
 
 
    // Validate phone number
 
    while (true) {
 
        cout << "Enter your phone number: ";
 
        cin >> phone;
 
 
 
        ifstream file("users.txt");
 
    string line;
 
    bool phoneExists = false;
 
 
    while (getline(file, line)) {
        size_t pos = 0;
            string data[8];
 
            int i = 0;
 
            while ((pos = line.find(',')) != string::npos && i < 7) {
 
                data[i++] = line.substr(0, pos);
 
                line.erase(0, pos + 1);
 
            }
 
            data[7] = line; // Last field is password
 
 
 
            long long existingPhone = stoll(data[3]);
 
            if (phone == existingPhone) {
 
                phoneExists = true;
 
                break;
 
            }
 
        }
    file.close();
 
 
    if (phoneExists) {
 
            cout << "Error: Phone number already registered. Please enter a different phone number.\n";
 
        } else {
 
            break;
 
        }
 
    }
 
 
 
    // Validate Aadhar number
 
    while (true) {
 
        cout << "Enter your Aadhar number: ";
 
        cin >> aadhar;
 
 
 
    ifstream file("users.txt");
    string line;
    bool aadharExists = false;
 
 
    while (getline(file, line)) {
 
            size_t pos = 0;
 
            string data[8];
 
            int i = 0;
 
            while ((pos = line.find(',')) != string::npos && i < 7) {
 
                data[i++] = line.substr(0, pos);
 
                line.erase(0, pos + 1);
 
            }
 
            data[7] = line; // Last field is password
 
 
 
            long long existingAadhar = stoll(data[4]);
 
            if (aadhar == existingAadhar) {
 
                aadharExists = true;
 
                break;
 
            }
    }
        file.close();
 
 
 
        if (aadharExists) {
 
            cout << "Error: Aadhar number already registered. Please enter a different Aadhar number.\n";
 
        } else {
 
            break;
 
        }
 
    }
 
 
 
    cout << "Enter your gender (M/F/O): ";
 
    cin >> gender;
 
    cout << "Enter your address: ";
 
    cin.ignore();
 
getline(cin, address); cout << "Create your password: "; password = getHiddenPassword1();   // Convert name to lowercase for consistency
 
    name = toLowerCase(name);
 
 
 
    // Save user data
 
    ofstream outFile("users.txt", ios::app);
 
    if (outFile.is_open()) {
 
        outFile << name << "," << age << "," << dob << "," << phone << "," << aadhar << "," << gender << "," << address << "," << password << endl;
 
        outFile.close();
 
        cout << "Registration successful!\n";
 
    } else {
 
        cerr << "Error: Unable to open file.\n";
 
    }
 
}
 
 
string toLowerCase(string str);
 
void loginUser() {
 
    string name, inputPassword, line, storedName, storedPassword;
 
 
 
    cout << "Enter your name: ";
 
    cin.ignore();
 
    getline(cin, name);
 
    cout << "Enter your password: ";
 
    inputPassword = getHiddenPassword1();
 
 
  name = toLowerCase(name);
 
 
 ifstream file("users.txt"); if (file.is_open()) {
        bool loginSuccessful = false;
 
        while (getline(file, line)) {
 
            size_t pos = 0;
 
            string data[8];
 
            int i = 0;
 
            while ((pos = line.find(',')) != string::npos && i < 7) {
 
                data[i++] = line.substr(0, pos);
 
                line.erase(0, pos + 1);
 
            }
 
            data[7] = line; 
 
 
 
            storedName = data[0];
 
            storedPassword = data[7];
 
 
 
            if (storedName == name && storedPassword.size() == inputPassword.size() && kmpMatch1(storedPassword, inputPassword))
 
 {
                loginSuccessful = true;
 
                cout << "Login Successful!\n";
 
                file.close();
 
                passengerMenu();
 
return;
 
                
 
            }
 
        }
 
        file.close();
 
 
 
        if (!loginSuccessful) {
 
            cout << "Invalid name or password. Please try again.\n";
 
        }
 
    } else {
 
      cerr << "Error: Unable to open file.\n";
  }
}
 
 string toLowerCase(string str); // Function prototype
 
 void forgotPassword() {
 
    string name, line;
 
    long long phone, storedPhone;
 
 
 
    cout << "Enter your name: ";
 
    cin.ignore();
 
    getline(cin, name);
 
    cout << "Enter your registered phone number: ";
 
    cin >> phone;
 
 
    name = toLowerCase(name);
 
 
 
    ifstream file("users.txt");
 
    ofstream tempFile("temp.txt");
 
 
 
    bool found = false;
 
 
 
    if (file.is_open() && tempFile.is_open()) {
 
        while (getline(file, line)) {
 
            size_t pos = 0;
 
            string data[8];
 
            int i = 0;
 
            while ((pos = line.find(',')) != string::npos && i < 7) {
 
                data[i++] = line.substr(0, pos);
 
                line.erase(0, pos + 1);
 
            }
 
            data[7] = line; 
 
 
            storedPhone = stoll(data[3]);
 
 
 
            if (toLowerCase(data[0]) == name && storedPhone == phone) {
 
                found = true;
 
                cout << "User found. Enter new password: ";
 
 
 
                string newPassword = getHiddenPassword1();
 
                tempFile << data[0] << "," << data[1] << "," << data[2] << "," << data[3] << "," << data[4] << "," << data[5] << "," << data[6] << "," << newPassword << endl;
 
                cout << "Password reset successfully!\n";
 
            } else {
 
                tempFile << data[0] << "," << data[1] << "," << data[2] << "," << data[3] << "," << data[4] << "," << data[5] << "," << data[6] << "," << data[7] << endl;
 
            }
 
        }
 
        file.close();
 
        tempFile.close();
 
 
        remove("users.txt");
 
        rename("temp.txt", "users.txt");
 
 
 
        if (!found) {
 
            cout << "User not found or phone number incorrect.\n";
 
        }
 
    } else {
 
        cerr << "Error: Unable to open file.\n";
 
    }
 
}
 
 
 
string toLowerCase(string str) {
 
    transform(str.begin(), str.end(), str.begin(), ::tolower);
  return str;
}
 
 // void adminMenu() {
 
   
 
// }
 
class RatingFeedback {
 
private:
 
    struct Feedback {
 
        int userId;
 
        double rating;
 
        std::string comment;
 
 
 
        Feedback(int userId, double rating, const std::string& comment)
 
          : userId(userId), rating(rating), comment(comment) {}
 
  };
 
 
    std::vector<Feedback> feedbackList; // List of feedback from users
 
    double totalRating; // Sum of all ratings
 
    int feedbackCount;  // Total number of feedbacks
 
 
 
public:
 
    RatingFeedback() : totalRating(0), feedbackCount(0) {}
 
 
 
    void giveFeedback(int userId) {
 
        double rating;
 
        std::string comment;
 
 
 
        std::cout << "Enter your rating (1.0 to 5.0): ";
 
        std::cin >> rating;
 
        while (rating < 1.0 || rating > 5.0) {
    std::cout << "Invalid rating. Please enter a rating between 1.0 and 5.0: ";
    std::cin >> rating;
        }
 
 
 
        std::cin.ignore(); // To clear the newline character left in the input buffer
 
        std::cout << "Enter your feedback comment: ";
 
        std::getline(std::cin, comment);
 
 
 
        feedbackList.emplace_back(userId, rating, comment);
 
        totalRating += rating;
 
        feedbackCount++;
 
 
 
        std::cout << "Thank you for your feedback!\n";
 
    }
 
 
 
    void displayAverageRating() const {
 
      if (feedbackCount == 0) {
          std::cout << "No feedback available yet.\n";
      } else {
            double average = totalRating / feedbackCount;
 
            std::cout << std::fixed << std::setprecision(2);
 
            std::cout << "Average Rating: " << average << "/5.0\n";
 
        }
 
    }
 
 
 
    void displayAllFeedback() const {
 
        if (feedbackList.empty()) {
 
            std::cout << "No feedback available yet.\n";
 
        } else {
 
            std::cout << "Feedback List:\n";
 
            for (const auto& feedback : feedbackList) {
 
                std::cout << "User ID: " << feedback.userId
 
                          << " | Rating: " << feedback.rating
                  << " | Comment: " << feedback.comment << "\n";
    }
        }
 
    }
 
 
 
    void saveFeedbackToFile(const std::string& filename = "feedback.txt") const {
 
        std::ofstream file(filename);
 
        if (file.is_open()) {
 
            for (const auto& feedback : feedbackList) {
 
                file << "User ID: " << feedback.userId
 
                     << " | Rating: " << feedback.rating
 
                     << " | Comment: " << feedback.comment << "\n";
 
            }
 
            file.close();
 
            std::cout << "Feedback saved to " << filename << " successfully.\n";
 
        } else {
 
          std::cerr << "Error: Unable to open file " << filename << ".\n";
      }
  }
};
 
 
 
 
void passengerMenu() {
 
    int choice;
 
    do {
 
        cout << "\n---------------------------------";
 
        cout << "\n          Passenger Menu          ";
 
        cout << "\n---------------------------------";
 
        cout << "\n     1. Book Ticket               ";
 
        cout << "\n     2. Track Train               ";
 
        cout << "\n     3. Rate Service              ";
 
        cout << "\n     4. Logout                    ";
 
        cout << "\n---------------------------------";
cout << "\nEnter your choice: "; cin >> choice;
    switch (choice) {
            case 1:
 
                bookTicket();
 
                break;
 
            case 2:
 
                trackTrain();
 
                break;
 
            case 3:
 
                rateService();
 
                break;
 
            case 4:
 
                cout << "Logging out...\n";
 
                break;  
      default:
          cout << "Invalid choice. Please try again.\n";
  }
  } while (choice != 4);
}
 
void rateService() {
 
    RatingFeedback  feedback; // Use the updated class name
 
    int choice;
 
    int userId = 1; // Simulated user ID generator
 
 
 
    do {
 
        std::cout << "\nRating and Feedback System\n";
 
        std::cout << "1. Give Feedback\n";
 
        std::cout << "2. Display Average Rating\n";
 
        std::cout << "3. Display All Feedback\n";
 
        std::cout << "4. Save Feedback to File\n";
 
        std::cout << "5. Exit\n";
std::cout << "Enter your choice: "; std::cin >> choice;
    switch (choice) {
            case 1:
 
                feedback.giveFeedback(userId++);
 
                break;
 
            case 2:
 
                feedback.displayAverageRating();
 
                break;
 
            case 3:
 
                feedback.displayAllFeedback();
 
                break;
 
            case 4:
 
                feedback.saveFeedbackToFile();
 
                break;  
      case 5:
          std::cout << "Exiting the system. Goodbye!\n";
          break;
          default:
                std::cout << "Invalid choice. Please try again.\n";
 
                break;
 
        }
 
    } while (choice != 5);
 
}
 
void manageTrainSchedule() {
 
 }
 
 
 
 
 
void bookTicket()
 {

    TrainDatabase db;

    db.initializeDatabase(); // Initialize the database with some train data

    BookingSystem bookingSystem(db); // Initialize the booking system with the train database

    int choice;

    do 
    {

        cout << "\n1. Display All Trains\n";

        cout << "2. Search Trains\n";

        cout << "3. Book Ticket\n";

        cout << "4. View Booking\n";

        cout << "5. Cancel Booking\n";

        cout << "6. Exit\n";

        cout << "Enter your choice: ";

        cin >> choice;

        switch (choice) 
        {
        case 1:

            db.displayAllTrains();

            break;

        case 2: 
        {
            string src, dest;

            cout << "Enter source station: ";

            cin >> src;

            cout << "Enter destination station: ";

            cin >> dest;

            db.searchTrains(src, dest);

            break;
        }
        case 3:

            bookingSystem.bookTicket();

            break;

        case 4: 
        {
            int bookingId;

            cout << "Enter booking ID to view: ";

            cin >> bookingId;

            bookingSystem.viewBooking(bookingId);

            break;
        }
        case 5:
         {

            int bookingId;

            cout << "Enter booking ID to cancel: ";

            cin >> bookingId;

            bookingSystem.cancelBooking(bookingId);

            break;
        }
        case 6:

            cout << "Exiting program.\n";

            break;

        default:

            cout << "Invalid choice. Please try again.\n";
        
        }
    } 
    
    while (choice != 6);
    
}
 
 
 
void trackTrain() {
 
    TrainDatabase db;
 
    db.initializeDatabase(); // Initialize the database with some train data
 
 
 
    string source, destination;
 
    cout << "Enter source station: ";
 
    cin >> source;
 
    cout << "Enter destination station: ";
 
    cin >> destination;
 
 
 
    vector<Train> trains = db.searchTrainByRoute(source, destination); if (!trains.empty()) {
  // Find the train with the shortest distance
auto shortestTrain = min_element(trains.begin(), trains.end(), [](const Train& a, const Train& b) {     return a.distance < b.distance;
  });
 
 
 
        cout << "Shortest distance train from " << source << " to " << destination << ":\n";
 
        cout << left << setw(15) << "Train Number"
 
             << setw(25) << "Train Name"
 
             << setw(20) << "Source"
 
             << setw(20) << "Destination"
 
             << setw(15) << "Departure"
 
             << setw(15) << "Arrival"
 
             << setw(10) << "Distance"
 
             << setw(15) << "Type"
 
             << setw(10) << "Price" << endl;
 
      cout << string(150, '-') << endl;
      shortestTrain->display();
  } else {
    cout << "No trains found from " << source << " to " << destination << ".\n";
    }
 
}
 
 
 
 
 
void user_portal() {
 
    int choice;
 
    do {
 
        system("cls"); // Clear the screen (works on Windows; for Linux/Mac use "clear")
 
        cout << "\n========================================\n";
 
        cout << "           WELCOME TO USER PORTAL        \n";
 
        cout << "========================================\n";
 
        cout << "\nPlease choose an option:\n";
 
        cout << "----------------------------------------\n";
cout << setw(4) << " " << "1. Register User\n"; cout << setw(4) << " " << "2. Login User\n"; cout << setw(4) << " " << "3. Forgot Password\n"; cout << setw(4) << " " << "4. Exit\n";
  cout << "----------------------------------------\n";  
        cout << "Enter your choice: ";
 
        cin >> choice;
 
 
 
        switch (choice) {
 
            case 1:
 
                system("cls");
 
                cout << "========== USER REGISTRATION ==========\n";
 
                registerUser();
 
                break;
 
            case 2:
 
                system("cls");
 
              cout << "========== USER LOGIN ==========\n";
              loginUser();
              break;
        case 3:
                system("cls");
 
                cout << "========== FORGOT PASSWORD ==========\n";
 
                forgotPassword();
 
                break;
 
            case 4:
 
                system("cls");
 
                cout << "Thank you for using the User Portal. Exiting...\n";
 
                break;
 
            default:
 
                cout << "Invalid choice. Please try again.\n";
 
        }
 
 
 
        if (choice != 4) {
    cout << "\nPress Enter to return to the menu...";
    cin.ignore(numeric_limits<streamsize>::max(), '\n');
    cin.get();
  }
 
 
    } while (choice != 4);
 
}
 
 
void main_menu() {
 
    while (true) {
 
         cout << "\n=========================================" << endl;
 
    cout << "         INDIAN RAILWAY BOOKING SYSTEM    " << endl;
 
    cout << "=========================================" << endl;
 
    cout << "               MAIN MENU                  " << endl;
 
    cout << "=========================================" << endl;
 
 cout << "1. User Portal" << endl;
      cout << "2. Admin Portal" << endl;
      cout << "3. Exit" << endl;
cout << "=========================================" << endl;
 
 
       
 
 
 
        int choice;
 
        cout << "Enter your choice (1-3): ";
 
        cin >> choice;
 
 
 
        switch (choice) {
 
            case 1:
 
                user_portal();
 
                break;
 
            case 2:
 
                admin_portal();         break;     case 3:
        cout << "Exiting... Thank you!" << endl;
          return;
            default:
 
                cout << "Invalid choice. Please try again." << endl;
 
        }
 
    }
 
}
 
 
 
int main() {
 
    main_menu();
 
    return 0;
 
}

