---

layout: default
permalink: /comp-serial
title: Comp Serialization PoC
description: crude demo
robots: "NOINDEX, NOFOLLOW"
sitemap: false

---

<input id="poc-url" style="width:100%;" />
Search:
<input id="search" style="width:100%;" />
<div id="queries"></div>
Results:
<ul id="results"></ul>
Comp:
<textarea id="poc-json" style="width:100%; height:600px">

</textarea>

<script type="text/javascript">

// https://stackoverflow.com/questions/14733374/how-to-generate-an-md5-file-hash-in-javascript-node-js
var MD5 = function(d){var r = M(V(Y(X(d),8*d.length)));return r.toLowerCase()};function M(d){for(var _,m="0123456789ABCDEF",f="",r=0;r<d.length;r++)_=d.charCodeAt(r),f+=m.charAt(_>>>4&15)+m.charAt(15&_);return f}function X(d){for(var _=Array(d.length>>2),m=0;m<_.length;m++)_[m]=0;for(m=0;m<8*d.length;m+=8)_[m>>5]|=(255&d.charCodeAt(m/8))<<m%32;return _}function V(d){for(var _="",m=0;m<32*d.length;m+=8)_+=String.fromCharCode(d[m>>5]>>>m%32&255);return _}function Y(d,_){d[_>>5]|=128<<_%32,d[14+(_+64>>>9<<4)]=_;for(var m=1732584193,f=-271733879,r=-1732584194,i=271733878,n=0;n<d.length;n+=16){var h=m,t=f,g=r,e=i;f=md5_ii(f=md5_ii(f=md5_ii(f=md5_ii(f=md5_hh(f=md5_hh(f=md5_hh(f=md5_hh(f=md5_gg(f=md5_gg(f=md5_gg(f=md5_gg(f=md5_ff(f=md5_ff(f=md5_ff(f=md5_ff(f,r=md5_ff(r,i=md5_ff(i,m=md5_ff(m,f,r,i,d[n+0],7,-680876936),f,r,d[n+1],12,-389564586),m,f,d[n+2],17,606105819),i,m,d[n+3],22,-1044525330),r=md5_ff(r,i=md5_ff(i,m=md5_ff(m,f,r,i,d[n+4],7,-176418897),f,r,d[n+5],12,1200080426),m,f,d[n+6],17,-1473231341),i,m,d[n+7],22,-45705983),r=md5_ff(r,i=md5_ff(i,m=md5_ff(m,f,r,i,d[n+8],7,1770035416),f,r,d[n+9],12,-1958414417),m,f,d[n+10],17,-42063),i,m,d[n+11],22,-1990404162),r=md5_ff(r,i=md5_ff(i,m=md5_ff(m,f,r,i,d[n+12],7,1804603682),f,r,d[n+13],12,-40341101),m,f,d[n+14],17,-1502002290),i,m,d[n+15],22,1236535329),r=md5_gg(r,i=md5_gg(i,m=md5_gg(m,f,r,i,d[n+1],5,-165796510),f,r,d[n+6],9,-1069501632),m,f,d[n+11],14,643717713),i,m,d[n+0],20,-373897302),r=md5_gg(r,i=md5_gg(i,m=md5_gg(m,f,r,i,d[n+5],5,-701558691),f,r,d[n+10],9,38016083),m,f,d[n+15],14,-660478335),i,m,d[n+4],20,-405537848),r=md5_gg(r,i=md5_gg(i,m=md5_gg(m,f,r,i,d[n+9],5,568446438),f,r,d[n+14],9,-1019803690),m,f,d[n+3],14,-187363961),i,m,d[n+8],20,1163531501),r=md5_gg(r,i=md5_gg(i,m=md5_gg(m,f,r,i,d[n+13],5,-1444681467),f,r,d[n+2],9,-51403784),m,f,d[n+7],14,1735328473),i,m,d[n+12],20,-1926607734),r=md5_hh(r,i=md5_hh(i,m=md5_hh(m,f,r,i,d[n+5],4,-378558),f,r,d[n+8],11,-2022574463),m,f,d[n+11],16,1839030562),i,m,d[n+14],23,-35309556),r=md5_hh(r,i=md5_hh(i,m=md5_hh(m,f,r,i,d[n+1],4,-1530992060),f,r,d[n+4],11,1272893353),m,f,d[n+7],16,-155497632),i,m,d[n+10],23,-1094730640),r=md5_hh(r,i=md5_hh(i,m=md5_hh(m,f,r,i,d[n+13],4,681279174),f,r,d[n+0],11,-358537222),m,f,d[n+3],16,-722521979),i,m,d[n+6],23,76029189),r=md5_hh(r,i=md5_hh(i,m=md5_hh(m,f,r,i,d[n+9],4,-640364487),f,r,d[n+12],11,-421815835),m,f,d[n+15],16,530742520),i,m,d[n+2],23,-995338651),r=md5_ii(r,i=md5_ii(i,m=md5_ii(m,f,r,i,d[n+0],6,-198630844),f,r,d[n+7],10,1126891415),m,f,d[n+14],15,-1416354905),i,m,d[n+5],21,-57434055),r=md5_ii(r,i=md5_ii(i,m=md5_ii(m,f,r,i,d[n+12],6,1700485571),f,r,d[n+3],10,-1894986606),m,f,d[n+10],15,-1051523),i,m,d[n+1],21,-2054922799),r=md5_ii(r,i=md5_ii(i,m=md5_ii(m,f,r,i,d[n+8],6,1873313359),f,r,d[n+15],10,-30611744),m,f,d[n+6],15,-1560198380),i,m,d[n+13],21,1309151649),r=md5_ii(r,i=md5_ii(i,m=md5_ii(m,f,r,i,d[n+4],6,-145523070),f,r,d[n+11],10,-1120210379),m,f,d[n+2],15,718787259),i,m,d[n+9],21,-343485551),m=safe_add(m,h),f=safe_add(f,t),r=safe_add(r,g),i=safe_add(i,e)}return Array(m,f,r,i)}function md5_cmn(d,_,m,f,r,i){return safe_add(bit_rol(safe_add(safe_add(_,d),safe_add(f,i)),r),m)}function md5_ff(d,_,m,f,r,i,n){return md5_cmn(_&m|~_&f,d,_,r,i,n)}function md5_gg(d,_,m,f,r,i,n){return md5_cmn(_&f|m&~f,d,_,r,i,n)}function md5_hh(d,_,m,f,r,i,n){return md5_cmn(_^m^f,d,_,r,i,n)}function md5_ii(d,_,m,f,r,i,n){return md5_cmn(m^(_|~f),d,_,r,i,n)}function safe_add(d,_){var m=(65535&d)+(65535&_);return(d>>16)+(_>>16)+(m>>16)<<16|65535&m}function bit_rol(d,_){return d<<_|d>>>32-_}


var comp = {
	title: 'demo title',
	bots: [
		{name: "barrie", ai: [1,0,1,0,0]},
		{name: "nozzle", ai: [1,0,1,1,1]},
		{name: "inkjet", ai: [1,0,0,0,0]},
		{name: "lobbie", ai: [1,1,1,0,0]},
		{name: "slash", ai: [1,0,1,1,0]},
		{name: "icicool", ai: [0,0,0,0,0]}
	],
	abilities: [
		"ball-lightning",
		"hasty-ground",
		"proximity-translocator",
		"shield-field"
	],
	boosters: [
		"bot-health-rare",
		"corrupted-power-generation-epic",
		"power-generation-epic",
		"power-generation-epic"
	]
};

function serialize(comp){
	let bots = comp.bots.map(bot=>{
		let id = lookup.bot2key[bot.name];
		let ai = aiEncode(bot.ai)
		return id + ai
	}).join('');
	let abilities = comp.abilities.map(ability=>{
		return lookup.ability2key[ability];
	}).join('');
	let boosters = comp.boosters.map(booster=>{
		return lookup.booster2key[booster];
	}).join('');
	let title = comp.title.replaceAll(' ','-'); //todo proper url prep
	return [bots,abilities,boosters,title].join('-')
}

function unserialize(str){
	let [bots, abilities, boosters, ...title] = str.split('-');
	title = title.join(' ');
	try {
		bots = bots.match(/.{1,4}/g).map(bot=>{
			let [id, ai] = [bot.substr(0,3),bot.substr(3,1)];
			return {name: lookup.key2bot[id], ai: aiDecode(ai)}
		})
	} catch (e) { bots = []; }
	try {
		abilities = abilities.match(/.{1,3}/g).map(id=>lookup.key2ability[id])
	} catch (e) { abilities = []; }
	try {
		boosters = boosters.match(/.{1,3}/g).map(id=>lookup.key2booster[id])
	} catch (e) { boosters = []; }

	return comp = {
		title: title,
		bots: bots,
		abilities: abilities,
		boosters: boosters
	}
}

// mapping the array of 0,1 ai values to binary
// result is base 36 encoded in a single char (2^5 = 32 ai combinations)
function aiEncode(array){
	return Number.parseInt(array.join(''),2).toString(36); // array to bin to decimal to b36
}
function aiDecode(str){
	return Number.parseInt(str, 36).toString(2).padEnd(5,'0').split('')
}


const OVERRIDES = {
	// SUGAR
	// bots
	"barrie":"Bar", "beat":"Bea", "berserker":"Ber", "bigshot":"Big", "bombee":"Bom", "brute":"Bru", "bullseye":"BuE", "bullwark":"BuW", "chainer":"Cha", "chomp":"Cho", "comet":"Com", "dune-bug":"Dun", "flamer":"Fla", "fork":"For", "froggy":"Frg", "frosty":"Frs", "gusto":"Gus", "halo":"Hal", "hornet":"Hor", "icicool":"Ici", "inkjet":"Ink", "ko":"KOx", "link":"Lin", "lobbie":"Lob", "longshot":"Lon", "mort":"Mor", "nibbles":"Nib", "nozzle":"Noz", "phantom":"Pha", "pluggie":"Plu", "pupil":"Pup", "ram":"Ram", "rocketeer":"Roc", "scatter":"Sca", "sheller":"She", "shuffle":"Shu", "slash":"Sla", "slicer":"Sli", "tether":"Tet", "thump":"Thu", "virus":"Vir", "yanky":"Yan",
	// abilities
	"gust":"Gus",
	"hypercharge":"HCh",
	"hyperdrain":"HDr",
	"icewall":"IcW",
	"deep-freeze":"DFr",
	"supercharged-chaos-translocator": "SCT",
	"chaos-translocator": "CTr",
	"explosive-proximity-translocator":"EPT",
	"proximity-translocator": "PTr",
	"gravity-surge":"GSu",
	// boosters
	"ult-cooldowns-rare":"UCD",
	"ult-charge-special":"UCh",
	"faerie's-blessing":"FBl",
	"sub-zero":"SZ0",
	"power-start-epic":"PwS",
	"power-generation-epic":"PwG",
	"corrupted-power-generation-epic":"cPw",
	// COLLISIONS
	//'ram': 'RAM', // bullseye
	'corrupted-sharpshooter-range-epic': 'cSR', // brawler-lifesteal-common
	'energy-resistance-epic': 'EnR', // bot-damage-common
}


var db, lookup = {};

function genLookups(dbCollection){
	let key2entity = {};
	let entity2key = {};
	for (let id in dbCollection){
		const fallback = MD5(id).substr(0,3);
		const key = OVERRIDES[id] || fallback; 
		if (entity2key[id]){ alert('collision: ' + id + ' and ' + entity2key[id]) }; 
		key2entity[fallback] = id; //so serial payloads shared before an override was added stay supported
		key2entity[key] = id;
		entity2key[id] = key;
	}
	return [key2entity, entity2key]
}


const $output = document.querySelector('#poc-json');
const $url = document.querySelector('#poc-url');
	
function init(json){
	db = json;
	const [key2bot, bot2key] = genLookups(db.bots);
	const [key2ability, ability2key] = genLookups(db.abilities);
	const [key2booster, booster2key] = genLookups(db.boosters);

	lookup = {
		key2bot: key2bot, bot2key: bot2key,
		key2ability: key2ability, ability2key: ability2key,
		key2booster: key2booster, booster2key: booster2key,
		list: Object.keys(bot2key).concat(Object.keys(ability2key), Object.keys(booster2key))
	}

	if (anchor = document.location.hash){
	    // If yes, get the app state out of it
		comp = unserialize(anchor.slice(1));
	}

	$url.value = document.location;
	$output.value = JSON.stringify(comp, null, 2);


	$output.addEventListener('keyup', ()=>{
		document.location.hash = '#'+serialize(JSON.parse($output.value));
		$url.value = document.location;
	});

}



//fetch("comp-serial.json")
fetch("/assets/js/comp-serial.json")
  .then(response => response.json())
  .then(json => init(json));


var collection = [
	'ChakLobnMorgVirsNozmFor0-GusDFrSCTHCh-cPwPwSSZ0UCD-arena-chainer-meta',
	'Big0-00a-da0da0-Bigshot-fever',
	'Com0-SCT-da0da0SZ0PwS-sky-pony-boom',
	'Ici0Roc0Lob0-GusHDrGSu-EnREnREnREnR-karts-special',
	'Bar0Lob0Dun0Yan0Roc0Ici0-Gus28c-UChUch28282-Pix-pauper',
	'Cha0Lob0-GusIcW-SZ0UCDPwScPG-Pix-CC-shell'
];


const $search = document.querySelector('#search');
const $queries = document.querySelector('#queries');
const $results = document.querySelector('#results');

function loadCompFromStr(str){
	comp = unserialize(str);
	$output.value = JSON.stringify(comp, null, 2);
}

function loadResults(arr){
	$results.innerHTML = '';
	arr.map((e)=>{
		let $entry = document.createElement('li')
		let $link = document.createElement('a');
		$link.innerText = e;
		$link.href = '#'+e;
		$link.addEventListener('click', ()=>loadCompFromStr(e));
		$entry.append($link);
		$results.append($entry);
	})
}

loadResults(collection);

$search.addEventListener('keyup', ()=>{
	const query = $search.value.toLowerCase().replaceAll(' ','-');
	const expandedQuery = lookup.list.filter(e=>e.startsWith(query));
	const keys = [query].concat(expandedQuery.map(e=>lookup.bot2key[e]||lookup.ability2key[e]||lookup.booster2key[e]));
	console.log(keys);
	
	if (query) {$queries.innerText = expandedQuery;}
	else {$queries.innerText = '';}

	let matching = collection.filter(e=>{
		return (keys.filter(k=>e.includes(k))).length
	})
	loadResults(matching);
});

</script>
