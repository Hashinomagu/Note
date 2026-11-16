  

async function loadCSV(path) {

const response = await fetch(path);

const text = await response.text();

// 改行コード（\r\n または \n）で分割して二次元配列に変換

const data = text.trim().split(/\r\n|\n/).map(line => line.split(','));

return data;

}
