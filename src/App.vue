<script setup lang="ts">
import {reactive} from 'vue'
import PaginationVue from './components/Paginations.vue';
let layout = "total,sizes,prev, pager, next, jumper, ->, slot"; //分页组件会展示的功能项
let page = reactive({
    // 放置页码及相关数据
    pageNum: 1, //当前页
    pageSize: 30, //每页条目数
    total: 30, // 记录总数
    totalPage: 0, //页数
});
const pageFunc = (data) => {
    page.pageSize = 30; //每页条数
    page.pageNum = data.pageNum; //多少页
    //query(page.pageSize, page.pageNum);; 数据分页请求方法
};
const list= [
            {
                "date": "2023-06-14",
                "4": "53.812200",
                "5": "211.630000",
                "6": "0.860000",
                "7": "2.230000",
                "8": "66.324600",
                "10": "57.785600",
                "11": "14.640000",
                "14": "46.224600",
                "15": "49.620000",
                "16": "6.740000",
                "19": "0.000000",
                "24": "0.040000",
                "33": "81.059196",
                "35": "20.850000",
                "total": 611.8161960000001
            },
            {
                "date": "2023-06-13",
                "1": "11.300000",
                "4": "74.827800",
                "5": "204.530000",
                "7": "25.350000",
                "8": "360.970600",
                "9": "6.501400",
                "10": "99.279400",
                "11": "49.100000",
                "14": "40.295800",
                "15": "11.550000",
                "17": "0.680000",
                "20": "0.060000",
                "24": "0.190000",
                "31": "0.170000",
                "33": "148.366211",
                "35": "4.100000",
                "total": 1037.2712109999998
            },
            {
                "date": "2023-06-12",
                "4": "54.902500",
                "5": "261.000000",
                "6": "14.200000",
                "7": "14.010000",
                "8": "170.587600",
                "9": "2.661400",
                "10": "49.424000",
                "11": "11.950000",
                "14": "48.688800",
                "15": "4.920000",
                "17": "1.230000",
                "20": "11.380000",
                "24": "0.840000",
                "25": "2.206702",
                "31": "0.370000",
                "33": "78.987462",
                "35": "3.960000",
                "total": 731.318464
            },
            {
                "date": "2023-06-11",
                "4": "128.357300",
                "5": "208.200000",
                "6": "2.380000",
                "7": "11.800000",
                "8": "43.922200",
                "9": "11.706400",
                "10": "90.577000",
                "11": "36.420000",
                "14": "8.727210",
                "15": "9.780000",
                "19": "1.470000",
                "20": "7.060000",
                "24": "1.290000",
                "25": "1.700142",
                "31": "1.300000",
                "33": "55.212318",
                "35": "0.220000",
                "total": 620.1225699999999
            },
            {
                "date": "2023-06-10",
                "4": "43.433400",
                "5": "58.940000",
                "7": "0.000000",
                "8": "79.397100",
                "9": "3.835800",
                "10": "66.680000",
                "11": "20.020000",
                "14": "4.248200",
                "15": "13.260000",
                "24": "0.990000",
                "25": "1.285396",
                "31": "1.460000",
                "33": "126.726400",
                "35": "0.340000",
                "total": 420.616296
            },
            {
                "date": "2023-06-09",
                "4": "28.691424",
                "5": "142.350000",
                "6": "50.210000",
                "7": "18.130000",
                "8": "63.738100",
                "9": "5.652600",
                "10": "207.991600",
                "11": "1.730000",
                "14": "34.023790",
                "15": "19.060000",
                "19": "35.610000",
                "20": "3.380000",
                "24": "3.730000",
                "31": "0.740000",
                "33": "44.677183",
                "35": "4.520000",
                "total": 664.234697
            },
            {
                "date": "2023-06-08",
                "4": "74.458800",
                "5": "294.390000",
                "6": "1.510000",
                "7": "1.180000",
                "8": "239.643400",
                "9": "30.303500",
                "10": "20.450000",
                "11": "10.540000",
                "14": "36.830600",
                "15": "8.660000",
                "19": "0.760000",
                "20": "39.870000",
                "24": "2.650000",
                "31": "1.290000",
                "33": "106.939804",
                "35": "4.690000",
                "total": 874.1661039999999
            },
            {
                "date": "2023-06-07",
                "4": "45.315400",
                "5": "95.420000",
                "7": "38.580000",
                "8": "291.700300",
                "9": "5.506000",
                "10": "184.484000",
                "11": "32.650000",
                "14": "6.950000",
                "15": "0.030000",
                "19": "5.950000",
                "20": "19.570000",
                "23": "0.750000",
                "24": "1.260000",
                "31": "0.950000",
                "33": "202.387630",
                "35": "25.220000",
                "total": 956.7233300000003
            },
            {
                "date": "2023-06-06",
                "4": "60.117800",
                "5": "62.910000",
                "7": "17.600000",
                "8": "319.849000",
                "9": "4.145290",
                "10": "33.350000",
                "11": "2.840000",
                "14": "9.902720",
                "15": "4.720000",
                "20": "24.650000",
                "24": "2.360000",
                "31": "1.120000",
                "33": "126.201306",
                "35": "23.420000",
                "total": 693.186116
            },
            {
                "date": "2023-06-05",
                "4": "95.066000",
                "5": "119.340000",
                "7": "37.550000",
                "8": "101.153300",
                "9": "6.498792",
                "10": "87.957400",
                "11": "19.860000",
                "14": "47.623600",
                "15": "16.860000",
                "20": "6.600000",
                "24": "0.590000",
                "31": "2.810000",
                "33": "117.883712",
                "35": "8.150000",
                "total": 667.9428039999999
            },
            {
                "date": "2023-06-04",
                "4": "21.174400",
                "5": "76.330000",
                "6": "15.580000",
                "7": "0.720000",
                "8": "126.558500",
                "9": "24.659200",
                "10": "41.270000",
                "11": "32.220000",
                "14": "13.855800",
                "15": "28.420000",
                "20": "26.190000",
                "24": "0.530000",
                "31": "0.960000",
                "33": "102.073350",
                "35": "0.630000",
                "total": 511.17125
            },
            {
                "date": "2023-06-03",
                "4": "4.225200",
                "5": "202.420000",
                "6": "17.030000",
                "7": "2.820000",
                "8": "100.538600",
                "9": "9.509400",
                "10": "129.107440",
                "11": "11.030000",
                "14": "71.569200",
                "15": "12.890000",
                "19": "0.010000",
                "20": "5.200000",
                "24": "0.480000",
                "25": "1.942341",
                "31": "1.190000",
                "33": "60.186133",
                "35": "1.240000",
                "total": 631.3883140000002
            },
            {
                "date": "2023-06-02",
                "4": "39.237993",
                "5": "128.810000",
                "7": "2.720000",
                "8": "141.605700",
                "9": "3.903490",
                "10": "137.109000",
                "11": "0.000000",
                "14": "9.084000",
                "15": "36.470000",
                "20": "25.500000",
                "23": "10.030000",
                "24": "1.600000",
                "31": "1.960000",
                "33": "106.108827",
                "35": "12.000000",
                "total": 656.13901
            },
            {
                "date": "2023-06-01",
                "4": "82.596811",
                "5": "336.870000",
                "6": "2.900000",
                "7": "0.800000",
                "8": "62.788100",
                "9": "4.772106",
                "10": "140.890000",
                "11": "3.590000",
                "14": "52.106420",
                "15": "14.780000",
                "20": "3.770000",
                "23": "0.750000",
                "24": "0.760000",
                "31": "1.620000",
                "33": "62.761912",
                "35": "31.770000",
                "total": 803.525349
            },
            {
                "date": "2023-05-31",
                "4": "18.326200",
                "5": "109.670000",
                "6": "24.170000",
                "7": "6.900000",
                "8": "97.958400",
                "9": "2.882890",
                "10": "42.050000",
                "11": "27.650000",
                "14": "42.019200",
                "15": "39.370000",
                "19": "0.070000",
                "20": "28.530000",
                "24": "1.370000",
                "31": "1.870000",
                "33": "203.081245",
                "35": "33.500000",
                "total": 679.4179349999999
            },
            {
                "date": "2023-05-30",
                "4": "25.107000",
                "5": "134.730000",
                "6": "2.450000",
                "7": "45.440000",
                "8": "169.004400",
                "9": "5.627400",
                "10": "67.646000",
                "11": "227.000000",
                "14": "23.636000",
                "15": "2.590000",
                "19": "0.000000",
                "20": "4.740000",
                "24": "0.950000",
                "31": "1.780000",
                "33": "235.011230",
                "35": "1.060000",
                "total": 946.7720300000001
            },
            {
                "date": "2023-05-29",
                "4": "46.536000",
                "5": "121.600000",
                "6": "0.000000",
                "7": "8.880000",
                "8": "136.743800",
                "9": "6.505600",
                "10": "81.192000",
                "11": "30.650000",
                "14": "129.478200",
                "15": "15.240000",
                "17": "0.060000",
                "19": "9.730000",
                "20": "15.670000",
                "24": "1.160000",
                "31": "2.040000",
                "33": "124.958907",
                "35": "0.430000",
                "total": 730.8745069999998
            },
            {
                "date": "2023-05-28",
                "4": "4.658400",
                "5": "57.410000",
                "6": "2.510000",
                "7": "7.890000",
                "8": "466.195100",
                "9": "11.044400",
                "10": "37.210000",
                "11": "14.550000",
                "14": "36.972380",
                "15": "10.300000",
                "16": "3.400000",
                "20": "49.630000",
                "24": "0.400000",
                "31": "1.130000",
                "33": "95.119308",
                "35": "1.620000",
                "total": 800.039588
            },
            {
                "date": "2023-05-27",
                "4": "59.623400",
                "5": "940.460000",
                "6": "4.950000",
                "7": "33.730000",
                "8": "57.348000",
                "9": "10.891500",
                "10": "53.050000",
                "11": "2.000000",
                "14": "21.879600",
                "15": "12.410000",
                "20": "14.550000",
                "24": "0.690000",
                "31": "0.710000",
                "33": "114.543858",
                "35": "13.840000",
                "total": 1340.676358
            },
            {
                "date": "2023-05-26",
                "4": "88.880200",
                "5": "138.410000",
                "6": "2.810000",
                "7": "6.550000",
                "8": "70.115500",
                "9": "7.156600",
                "10": "13.071400",
                "11": "13.270000",
                "14": "1.882000",
                "15": "17.260000",
                "17": "3.680000",
                "20": "24.870000",
                "24": "0.850000",
                "31": "0.980000",
                "33": "131.852506",
                "35": "5.410000",
                "total": 527.048206
            },
            {
                "date": "2023-05-25",
                "1": "1.750000",
                "4": "34.636800",
                "5": "171.140000",
                "6": "3.570000",
                "7": "6.900000",
                "8": "93.248600",
                "9": "2.315800",
                "10": "111.180000",
                "11": "28.420000",
                "15": "7.450000",
                "17": "0.170000",
                "20": "16.600000",
                "24": "0.630000",
                "25": "2.692683",
                "31": "1.670000",
                "33": "56.850953",
                "35": "4.780000",
                "total": 544.004836
            },
            {
                "date": "2023-05-24",
                "1": "1.270000",
                "4": "38.752600",
                "5": "155.980000",
                "6": "76.010000",
                "7": "24.420000",
                "8": "116.555800",
                "9": "0.888000",
                "10": "261.340000",
                "11": "28.560000",
                "14": "5.112000",
                "15": "7.500000",
                "16": "51.220000",
                "17": "5.660000",
                "19": "0.000000",
                "20": "39.810000",
                "24": "0.420000",
                "31": "0.210000",
                "33": "128.168694",
                "35": "35.890000",
                "total": 977.7670939999998
            },
            {
                "date": "2023-05-23",
                "4": "53.453332",
                "5": "79.800000",
                "6": "188.570000",
                "7": "2.740000",
                "8": "168.122800",
                "9": "1.420000",
                "10": "11.170000",
                "11": "22.790000",
                "14": "22.899800",
                "15": "21.770000",
                "17": "2.770000",
                "19": "1.290000",
                "20": "12.970000",
                "24": "0.310000",
                "31": "0.560000",
                "33": "134.041922",
                "35": "22.090000",
                "total": 746.7678539999999
            },
            {
                "date": "2023-05-22",
                "1": "18.830000",
                "4": "81.868000",
                "5": "99.240000",
                "6": "249.170000",
                "7": "18.300000",
                "8": "121.788800",
                "9": "0.883400",
                "10": "9.640000",
                "11": "47.120000",
                "14": "29.341200",
                "15": "5.670000",
                "17": "3.390000",
                "19": "0.000000",
                "20": "5.110000",
                "24": "0.130000",
                "31": "0.460000",
                "33": "138.284016",
                "35": "3.010000",
                "total": 832.235416
            },
            {
                "date": "2023-05-21",
                "1": "1.870000",
                "4": "20.386800",
                "5": "108.360000",
                "6": "100.380000",
                "7": "25.160000",
                "8": "94.242500",
                "9": "2.271000",
                "10": "4.220000",
                "11": "36.230000",
                "14": "13.780000",
                "15": "10.230000",
                "17": "0.160000",
                "19": "0.000000",
                "20": "32.300000",
                "24": "0.030000",
                "31": "0.300000",
                "33": "41.292232",
                "35": "6.470000",
                "total": 497.68253200000015
            },
            {
                "date": "2023-05-20",
                "4": "32.125800",
                "5": "60.990000",
                "6": "318.910000",
                "7": "11.340000",
                "8": "230.261300",
                "9": "0.411400",
                "10": "9.980000",
                "11": "25.160000",
                "14": "38.056200",
                "15": "0.360000",
                "17": "1.240000",
                "19": "0.720000",
                "20": "1.180000",
                "24": "0.150000",
                "33": "90.163000",
                "35": "5.480000",
                "total": 826.5276999999999
            },
            {
                "date": "2023-05-19",
                "1": "0.000000",
                "4": "23.232400",
                "5": "51.510000",
                "6": "240.280000",
                "7": "57.840000",
                "8": "68.017800",
                "9": "1.180000",
                "10": "7.660000",
                "11": "32.230000",
                "14": "19.780400",
                "15": "34.390000",
                "17": "21.310000",
                "20": "61.050000",
                "24": "0.560000",
                "31": "0.280000",
                "33": "95.362632",
                "35": "82.630000",
                "total": 797.3132319999997
            },
            {
                "date": "2023-05-18",
                "1": "0.090000",
                "4": "59.174400",
                "5": "52.930000",
                "6": "264.910000",
                "7": "17.720000",
                "8": "121.580700",
                "9": "1.768800",
                "10": "19.778400",
                "11": "41.980000",
                "14": "6.336680",
                "15": "17.040000",
                "16": "12.600000",
                "17": "3.490000",
                "20": "71.310000",
                "24": "0.260000",
                "31": "0.200000",
                "33": "127.734686",
                "35": "38.780000",
                "total": 857.6836660000001
            },
            {
                "date": "2023-05-17",
                "1": "0.000000",
                "4": "39.864000",
                "5": "111.520000",
                "6": "517.200000",
                "7": "16.530000",
                "8": "147.102800",
                "9": "2.985600",
                "10": "19.020000",
                "11": "259.550000",
                "14": "24.336000",
                "16": "77.900000",
                "17": "1.100000",
                "19": "1.970000",
                "20": "3.090000",
                "23": "7.840000",
                "24": "0.050000",
                "31": "0.450000",
                "33": "67.617324",
                "35": "25.150000",
                "total": 1323.275724
            },
            {
                "date": "2023-05-16",
                "1": "0.170000",
                "4": "59.395800",
                "5": "117.010000",
                "6": "211.550000",
                "7": "12.800000",
                "8": "76.712400",
                "9": "2.220400",
                "10": "16.190000",
                "11": "96.490000",
                "14": "57.188000",
                "15": "5.350000",
                "17": "0.390000",
                "20": "39.200000",
                "24": "1.080000",
                "31": "0.490000",
                "33": "47.468100",
                "35": "10.650000",
                "total": 754.3547000000001
            },
            {
                "date": "2023-05-15",
                "1": "0.060000",
                "4": "109.892000",
                "5": "56.240000",
                "6": "419.810000",
                "7": "29.520000",
                "8": "80.906900",
                "9": "1.996200",
                "10": "20.562000",
                "11": "149.390000",
                "14": "0.000000",
                "16": "56.460000",
                "17": "1.350000",
                "20": "9.930000",
                "24": "0.780000",
                "31": "0.110000",
                "33": "112.829890",
                "35": "0.610000",
                "total": 1050.44699
            }
        ]
</script>

<template>
    <el-table :data="list" style="width: 100%" max-height="600px">
    <el-table-column label="" v-for="(item,index) in list" :key="index" :prop="index"></el-table-column>
  </el-table>
        <pagination-vue :layout="layout" :current-page="page.pageNum" :pageTotal="page.total"
            @pageFunc="pageFunc"></pagination-vue>
</template>

<style scoped>
</style>
