  

async function loadCSV(path) {

const response = await fetch(path);

const text = await response.text();

// 改行コード（\r\n または \n）で分割して二次元配列に変換

const data = text.trim().split(/\r\n|\n/).map(line => line.split(','));

return data;

}






const dater=loadCSV("schedule.csv");
dater.then(data => {
console.log(data[0][0]); // ID
console.log(data[0][1]); // 名前
});