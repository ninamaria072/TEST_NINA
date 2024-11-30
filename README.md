<html>
<!-- LEAFLET CSS -->
    <link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />
	<style>
	#map{
            width: 100%;
            height: 100vh;
        }
	</style>
	<body>
		<div id="map"></div>
	</body>
<!-- LEAFLET JAVASCRIPT -->
<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js" integrity="sha256-20nQCchB9co0qIjJZRGuk2/Z9VM+kNiyxNV1lvTlZBo=" crossorigin=""></script>
<script>
    <!-- LOKASI KAJIAN -->
    var map = L.map('map').setView([-5.367016, 105.317890], 15);
    <!-- BASEMAP OPENSTREETMAP -->
    var osm = L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
     attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
     });
     osm.addTo(map);
	 <!-- BASEMAP ESRI -->
var Esri_WorldImagery = L.tileLayer('https://server.arcgisonline.com/ArcGIS/rest/services/World_Imagery/MapServer/tile/{z}/{y}/{x}', {
    attribution: 'Tiles &copy; Esri &mdash; Source: Esri, i-cubed, USDA, USGS, AEX, GeoEye, Getmapping, Aerogrid, IGN, IGP, UPR-EGP, and the GIS User Community'
    });
Esri_WorldImagery.addTo(map);
<!-- POSISI GEDUNG E -->
L.marker([ -5.3600342,105.3152115]).addTo(map);
<!-- POSISI EMBUNG A -->
L.marker([ -5.3580216,105.3126642]).addTo(map);
<!-- POSISI EMBUNG SUMATERA -->
L.marker([ -5.3697126,105.3107433]).addTo(map);
<!-- POSISI GERBANG UTAMA -->
L.marker([ -5.357593, 105.314863]).addTo(map);
<!-- POSISI GERBANG BARAT -->
L.marker([ -5.363155, 105.308453]).addTo(map);
<!-- POSISI GEDUNG A -->
L.marker([ -5.357942, 105.314393]).addTo(map);
<!-- POSISI GEDUNG B -->
L.marker([ -5.357914, 105.315298]).addTo(map);
<!-- POSISI GEDUNG C dan D -->
L.marker([ -5.358701, 105.313515]).addTo(map);
<!-- POSISI GEDUNG  F -->
L.marker([ -5.361355, 105.31363]).addTo(map);
<!-- POSISI KANTIN RK -->
L.marker([ -5.359478, 105.312600]).addTo(map);
<!-- POSISI KANTIN BKL-->
L.marker([ -5.357599, 105.316446]).addTo(map);
<!-- POSISI MASJID BAITUL ILMI -->
L.marker([ -5.361516,105.310534]).addTo(map);
<!-- POSISI MASJID AT TANWIR -->
L.marker([ -5.356787, 105.318796]).addTo(map);
<!-- POSISI LABTEK 1 -->
L.marker([ -5.360279, 105.310162]).addTo(map);
<!-- POSISI LABTEK 2 -->
L.marker([ -5.361455, 105.310458]).addTo(map);
<!-- POSISI LABTEK 3 -->
L.marker([ -5.360301, 105.309108]).addTo(map);
<!-- POSISI GEDUNG GKU 1 -->
L.marker([ -5.360896, 105.310527]).addTo(map);
<!-- POSISI GEDUNG GKU 2 -->
L.marker([ -5.360327, 105.313873]).addTo(map);
<!-- POSISI GEDUNG OZT -->
L.marker([ -5.362045, 105.310575]).addTo(map);
<!-- POSISI EMBUNG B -->
L.marker([ -5.365038, 105.316463]).addTo(map);
<!-- POSISI EMBUNG C -->
L.marker([ -5.359394, 105.313672]).addTo(map);
<!-- POSISI EMBUNG D -->
L.marker([ -5.360289, 105.320607]).addTo(map);
<!-- POSISI Embung E-->
L.marker([ -5.368733, 105.319746]).addTo(map);
<!-- POSISI LABIRIN  -->
L.marker([ -5.369615, 105.312159]).addTo(map);
<!-- POSISI GEDUNG  Asrama TB1 -->
L.marker([ -5.358420, 105.317433]).addTo(map);
<!-- POSISI GEDUNG  Asrama TB2 -->
L.marker([ -5.358472, 105.319384]).addTo(map);
<!-- POSISI GEDUNG  Asrama TB3 -->
L.marker([ -5.359148, 105.318997]).addTo(map);
<!-- POSISI GEDUNG  Asrama TB4 -->
L.marker([ -5.359139, 105.317433]).addTo(map);
<!-- POSISI GEDUNG  Asrama TB5 -->
L.marker([ -5.358442, 105.318395]).addTo(map);
<!-- POSISI GEDUNG  GSG -->
L.marker([ -5.362413, 105.318956]).addTo(map);
<!-- POSISI GEDUNG  RIMA -->
L.marker([ -5.358616, 105.321095]).addTo(map);
<!-- POSISI GEDUNG  POLIKLINIK ITERA -->
L.marker([ -5.357726, 105.315971]).addTo(map);
<!-- POSISI GEDUNG  ATM ITERA -->
L.marker([ -5.357587, 105.315271]).addTo(map);
<!-- POSISI GEDUNG  GALERI1 -->
L.marker([ -5.357906,105.315573]).addTo(map);
<!-- POSISI PLTS -->
L.marker([ -5.360565, 105.311889]).addTo(map);

<!-- BUNDARAN YANG SERING SAYA LANGGAR ATURAN SAAT BERLALU LINTAS DI ITERA -->
var bundaranF = L.circle([ -5.363156, 105.312634], {
    color: 'red',
    fillColor: '#f03',
    fillOpacity: 0.5,
    radius: 20
}).addTo(map);
<!-- BUNDARAN INI JUGA SERING SAYA LANGGAR SETELAH SELESAI KULIAH DI GKU 2 -->
var bundaranGKU2 = L.circle([-5.360813, 105.314847], {
    color: 'green',
    fillColor: '#f03',
    fillOpacity: 0.5,
    radius: 35
}).addTo(map);

<!-- POLIGON BANGUNAN  GEDUNG F -->
var polygon = L.polygon([
    [-5.359799, 105.315831],
    [-5.359957, 105.315831],
    [-5.359957, 105.315571],
    [-5.360474, 105.315571],
    [-5.360474, 105.315401],
    [-5.359635, 105.315401],
    [-5.359635, 105.315571],
    [-5.359799, 105.315571]
]).addTo(map);
<!-- POLIGON BANGUNAN GEDUNG A-->
var polygon = L.polygon([
    [-5.357727, 105.314514],
    [-5.358071, 105.314513],
    [-5.358075, 105.314334],
    [-5.357731, 105.314337],
]).addTo(map);
<!-- POLIGON BANGUNAN GEDUNG B-->
var polygon = L.polygon([
    [-5.357732, 105.315236],
    [-5.357732, 105.315409],
    [-5.358065, 105.315420],
    [-5.358068, 105.315237],
]).addTo(map);
<!-- POLIGON BANGUNAN GEDUNG C dan D-->
var polygon = L.polygon([
    [-5.358311, 105.314144],
    [-5.358466, 105.313992],
    [-5.358466, 105.313606],
    [-5.358912, 105.313606],
    [-5.359070, 105.313450],
    [-5.358466, 105.313444],
    [-5.35846, 105.313321],
    [-5.358327, 105.313329],
]).addTo(map);
<!-- POLIGON BANGUNAN GEDUNG E-->
var polygon = L.polygon([
    [-5.359608, 105.315463],
    [-5.359611, 105.315637],
    [-5.359743, 105.315634],
    [-5.359731, 105.315899],
    [-5.359911, 105.315897],
    [-5.359892, 105.315633],
    [-5.360464, 105.315611],
    [-5.360469, 105.315452],
]).addTo(map);
<!-- POLIGON BANGUNAN KANTIN BKL-->
var polygon = L.polygon([
    [-5.357503, 105.316644],
    [-5.357704, 105.316659],
    [-5.357711, 105.316367],
    [-5.357517, 105.316354],
]).addTo(map);
<!-- POLIGON BANGUNAN KANTIN RK-->
var polygon = L.polygon([
    [-5.359288, 105.312453],
    [-5.359270, 105.312825],
    [-5.359599, 105.312846],
    [-5.359612, 105.312461],
]).addTo(map);
<!-- POLIGON BANGUNAN MASJID BAITUL ILMI-->
var polygon = L.polygon([
    [-5.358936, 105.312553],
    [-5.359028, 105.312764],
    [-5.359215, 105.312667],
    [-5.359115, 105.312468],
]).addTo(map);
<!-- POLIGON MASJID AT TANWIR-->
var polygon = L.polygon([
    [-5.356599, 105.318750],
    [-5.356732, 105.318997],
    [-5.356970, 105.318871],
    [-5.356881, 105.318654],
    [-5.356830, 105.318696],
    [-5.356821, 105.318642],
]).addTo(map);
<!-- POLIGON BANGUNAN GEUDNG ASRAMA TB1-->
var polygon = L.polygon([
    [-5.358325, 105.317176],
    [-5.358329, 105.317705],
    [-5.358502, 105.317713],
    [-5.358514, 105.317201],
]).addTo(map);
<!-- POLIGON BANGUNAN GEDUNG ASRAMA TB2-->
var polygon = L.polygon([
    [-5.358374, 105.319180],
    [-5.358386, 105.319676],
    [-5.358546, 105.319692],
    [-5.358551, 105.319192],
]).addTo(map);
<!-- POLIGON BANGUNAN GEDUNG ASRAMA TB3-->
var polygon = L.polygon([
    [-5.359052, 105.318767],
    [-5.359055, 105.319384],
    [-5.359183, 105.319376],
    [-5.359185, 105.318771],
]).addTo(map);
<!-- POLIGON BANGUNAN GEDUNG ASRAMA TB4-->
var polygon = L.polygon([
    [-5.359084, 105.317169],
    [-5.359084, 105.317770],
    [-5.359203, 105.317777],
    [-5.359211, 105.317166],
]).addTo(map);
<!-- POLIGON BANGUNAN GEDUNG ASRAMA TB5-->
var polygon = L.polygon([
    [-5.358381, 105.318201],
    [-5.358369, 105.318715],
    [-5.358530, 105.318699],
    [-5.358543, 105.318217],
]).addTo(map);
<!-- POLIGON BANGUNAN GEDUNG RIMA ITERA-->
var polygon = L.polygon([
    [-5.358509, 105.321045],
    [-5.358507, 105.321154],
    [-5.358620, 105.321205],
    [-5.358731, 105.321156],
    [-5.358755, 105.321059],
    [-5.358679, 105.320960],
    [-5.358578, 105.320965],
]).addTo(map);
<!-- POLIGON BANGUNAN GEDUNG GSG ITERA-->
var polygon = L.polygon([
    [-5.362225, 105.318844],
    [-5.362225, 105.319039],
    [-5.362617, 105.319049],
    [-5.362627, 105.318847],
]).addTo(map);
<!-- POLIGON BANGUNAN GEDUNG POLIKLINIK ITERA-->
var polygon = L.polygon([
    [-5.357661, 105.315921],
    [-5.357782, 105.315920],
    [-5.357780, 105.316015],
    [-5.357686, 105.316003],
    [-5.357680, 105.315960],
    [-5.357662, 105.315948],
]).addTo(map);
<!-- POLIGON BANGUNAN GEDUNG LABTEK 3-->
var polygon = L.polygon([
    [-5.360215, 105.308793],
    [-5.360196, 105.309448],
    [-5.360418, 105.309447],
    [-5.360422, 105.308776],
]).addTo(map);
<!-- POLIGON BANGUNAN GEDUNG LABTEK 1-->
var polygon = L.polygon([
    [-5.360214, 105.309954],
    [-5.360190, 105.310524],
    [-5.360453, 105.310515],
    [-5.360449, 105.309979],
]).addTo(map);
<!-- POLIGON BANGUNAN GEDUNG LABTEK 2-->
var polygon = L.polygon([
    [-5.361449, 105.309987],
    [-5.361433, 105.310971],
    [-5.361619, 105.310959],
    [-5.361607, 105.310003],
]).addTo(map);
<!-- POLIGON BANGUNAN GEDUNG GKU1-->
var polygon = L.polygon([
    [-5.360793, 105.309983],
    [-5.360817, 105.311000],
    [-5.361032, 105.311004],
    [-5.361040, 105.309966],
]).addTo(map);
<!-- POLIGON BANGUNAN GEDUNG OZT-->
var polygon = L.polygon([
    [-5.361955, 105.310353],
    [-5.361955, 105.311004],
    [-5.362142, 105.310995],
    [-5.362138, 105.310349],
]).addTo(map);

<!-- MENAMPILKAN NAMA GEDUNG E -->
    var GEDUNGE = L.marker([-5.3600342,105.3152115]);
    var namagedunge = GEDUNGE.bindPopup("GEDUNG E").openPopup()
    namagedunge.addTo(map);
<!-- MENAMPILKAN NAMA EMBUNG A -->
    var EMBUNGA = L.marker([-5.3580216,105.3126642]);
    var namaembunga = EMBUNGA.bindPopup("EMBUNG A").openPopup()
    namaembunga.addTo(map);
<!-- MENAMPILKAN NAMA EMBUNG SUMATERA -->
    var EMBUNGSUMATERA = L.marker([-5.3697126,105.3107433]);
    var namaembungsumatera = EMBUNGSUMATERA.bindPopup("EMBUNG SUMATERA").openPopup()
    namaembungsumatera.addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG GKU 1 -->
    var GKU1 = L.marker([-5.360896, 105.310527]);
    var namagku1 = GKU1.bindPopup("Gedung GKU 1").openPopup()
    namagku1.addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG Laboratorium OZT -->
    var LaboratoriumOZT = L.marker([-5.362045, 105.310575]);
    var namaLaboratoriumOZT = LaboratoriumOZT.bindPopup("Laboratorium OZT").openPopup()
    namaLaboratoriumOZT.addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG GKU 2 -->
    var GKU2 = L.marker([-5.360327, 105.313873]);
    var namagku2 = GKU2.bindPopup("Gedung GKU 2").openPopup()
    namagku2.addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG A -->
    var A = L.marker([-5.357942, 105.314393]);
    var namaA = A.bindPopup("Gedung A").openPopup()
    namaA.addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG B -->
    var B = L.marker([-5.357914, 105.315298]);
    var namaB = B.bindPopup("Gedung B").openPopup()
    namaB.addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG C dan D -->
    var CdanD = L.marker([-5.358701, 105.313515]);
    var namaCdanD = CdanD.bindPopup("Gedung C dan D").openPopup()
    namaCdanD.addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG Laboratorium 1 -->
    var Laboratorium1 = L.marker([-5.360279, 105.310162]);
    var namaLaboratorium1 = Laboratorium1.bindPopup("Laboratorium 1").openPopup()
    namaLaboratorium1.addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG Laboratorium 2 -->
    var Laboratorium2 = L.marker([-5.361455, 105.310458]);
    var namaLaboratorium2 = Laboratorium2.bindPopup("Laboratorium 2").openPopup()
    namaLaboratorium2.addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG Laboratorium 3 -->
    var Laboratorium3 = L.marker([-5.360301, 105.309108]);
    var namaLaboratorium3 = Laboratorium3.bindPopup("Laboratorium 3").openPopup()
    namaLaboratorium3.addTo(map);
<!-- MENAMPILKAN NAMA Embung B -->
    var EmbungB = L.marker([-5.365038, 105.316463]);
    var namaEmbungB = EmbungB.bindPopup("Embung B").openPopup()
    namaEmbungB.addTo(map);
<!-- MENAMPILKAN NAMA Embung C -->
    var EmbungC = L.marker([-5.359394, 105.313672]);
    var namaEmbungC = EmbungC.bindPopup("Embung C").openPopup()
    namaEmbungC.addTo(map);
<!-- MENAMPILKAN NAMA Embung D -->
    var EmbungD = L.marker([-5.360289, 105.320607]);
    var namaEmbungD = EmbungD.bindPopup("Embung D").openPopup()
    namaEmbungD.addTo(map);
<!-- MENAMPILKAN NAMA Embung E -->
    var EmbungE = L.marker([-5.368733, 105.319746]);
    var namaEmbungE = EmbungE.bindPopup("Embung E").openPopup()
    namaEmbungE.addTo(map);
<!-- MENAMPILKAN NAMA LABIRIN -->
    var Labirin = L.marker([-5.369615, 105.312159]);
    var namaLabirin = Labirin.bindPopup("LABIRIN").openPopup()
    namaLabirin.addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG Kantin BKL -->
    var KantinBKL = L.marker([-5.357599, 105.316446]);
    var namaKantinBKL = KantinBKL.bindPopup("Kantin BKL").openPopup()
    namaKantinBKL.addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG Kantin RK -->
    var KantinRK = L.marker([-5.359478, 105.312600]);
    var namaKantinRK = KantinRK.bindPopup("Kantin RK").openPopup()
    namaKantinRK.addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG RIMA -->
    var RIMA = L.marker([-5.362413, 105.318956]);
    var namaRIMA = RIMA.bindPopup("Rumah Ibadah Multi Agama").openPopup()
    namaRIMA.addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG Masjid Raya At Tanwir -->
    var MasjidRayaAtTanwir = L.marker([-5.356787, 105.318796]);
    var namaMasjidRayaAtTanwir = MasjidRayaAtTanwir.bindPopup("Masjid Raya At-Tanwir").openPopup()
    namaMasjidRayaAtTanwir.addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG Masjid Baitul Ilmi -->
    var MasjidBaitulIlmi = L.marker([-5.359091, 105.312621]);
    var namaMasjidBaitulIlmi = MasjidBaitulIlmi.bindPopup("Masjid Baitul Ilmi").openPopup()
    namaMasjidBaitulIlmi.addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG Asrama TB1 -->
    var AsramaTB1 = L.marker([-5.358420, 105.317433]);
    var namaAsramaTB1 = AsramaTB1.bindPopup("Asrama TB1").openPopup()
    namaAsramaTB1.addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG Asrama TB2 -->
    var AsramaTB2 = L.marker([-5.358472, 105.319384]);
    var namaAsramaTB2 = AsramaTB2.bindPopup("Asrama TB2").openPopup()
    namaAsramaTB2.addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG Asrama TB3 -->
    var AsramaTB3 = L.marker([-5.359148, 105.318997]);
    var namaAsramaTB3 = AsramaTB3.bindPopup("Asrama TB3").openPopup()
    namaAsramaTB3.addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG Asrama TB4 -->
    var AsramaTB4 = L.marker([-5.359139, 105.317433]);
    var namaAsramaTB4 = AsramaTB4.bindPopup("Asrama TB4").openPopup()
    namaAsramaTB4.addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG Asrama TB5 -->
    var AsramaTB5 = L.marker([-5.358442, 105.318395]);
    var namaAsramaTB5 = AsramaTB5.bindPopup("Asrama TB5").openPopup()
    namaAsramaTB4.addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG GSG -->
    var GSG = L.marker([-5.362413, 105.318956]);
    var namaGSG = GSG.bindPopup("Gedung Serba Guna").openPopup()
    namaGSG.addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG Poliklinik ITERA -->
    var PoliklinikITERA = L.marker([ -5.357726, 105.315971]);
    var namaPoliklinikITERA = PoliklinikITERA.bindPopup("Poliklinik ITERA").openPopup()
    namaPoliklinikITERA.addTo(map);
<!-- MENAMPILKAN NAMA ATM ITERA -->
    var ATM_Itera = L.marker([-5.357587, 105.315271]);
    var namaATM_Itera = ATM_Itera.bindPopup("ATM ITERA").openPopup()
    namaATM_Itera.addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG GALERI1 -->
    var Galeri1 = L.marker([-5.357906,105.315573]);
    var namaGaleri1 = Galeri1.bindPopup("Galeri 1 ITERA").openPopup()
    namaGaleri1.addTo(map);
<!-- MENAMPILKAN NAMA PLTS -->
    var PLTS = L.marker([-5.360565, 105.311889]);
    var namaPLTS = PLTS.bindPopup("PLTS ITERA").openPopup()
    namaPLTS.addTo(map);
<!-- MENAMPILKAN NAMA GEDUNG F -->
    var GEDUNG_F = L.marker([-5.361346, 105.313842]);
    var namagedungf = GEDUNG_F.bindPopup("Gedung F").openPopup()
    namagedungf.addTo(map);
    var baseMaps = {
	"OSM":osm,
	"ESRI":Esri_WorldImagery,
};
var overlayMaps = {
	"GEDUNG E" : GEDUNGE,
    "EMBUNG A": EMBUNGA,
    "Bundaran F": bundaranF,
    "Bundaran GKU": bundaranGKU2,
    "EMBUNG SUMATERA": EMBUNGSUMATERA,
	"Gedung GKU 1" : GKU1,
    "Laboratorium OZT": LaboratoriumOZT,
	"Gedung GKU 2": GKU2,
	"Gedung A" : A,
	"Gedung B" : B,
	"Gedung C dan D" : CdanD,  
    "Laboratorium 1": Laboratorium1,
	"Laboratorium 2": Laboratorium2,
	"Laboratorium 3": Laboratorium3,
	"Embung B": EmbungB ,
	"Embung C": EmbungC ,
	"Embung D": EmbungD ,
	"Embung E": EmbungE ,
    "LABIRIN" : Labirin ,
    "Kantin BKL": KantinBKL ,
	"Kantin RK": KantinRK ,
	"Rumah Ibadah Multi Agama" : RIMA ,
	"Masjid Raya At-Tanwir" : MasjidRayaAtTanwir ,
	"Masjid Baitul Ilmi" : MasjidBaitulIlmi ,
	"Asrama TB1" : AsramaTB1 ,
	"Asrama TB2" : AsramaTB2 ,
	"Asrama TB3" : AsramaTB3 ,
	"Asrama TB4" : AsramaTB4 ,
	"Asrama TB5" : AsramaTB5 ,
	"Gedung Serba Guna": GSG  ,
	"Poliklinik ITERA" : PoliklinikITERA  ,
    "ATM ITERA": ATM_Itera  ,
	"PLTS ITERA": PLTS   ,
	"Gedung F":GEDUNG_F,

};
map.removeLayer(GEDUNGE)
map.removeLayer(EMBUNGA)
map.removeLayer(bundaranF)
map.removeLayer(bundaranGKU2)
map.removeLayer(EMBUNGSUMATERA)
map.removeLayer(GKU1)
map.removeLayer(LaboratoriumOZT)
map.removeLayer(GKU2)
map.removeLayer(A)
map.removeLayer(B)
map.removeLayer(CdanD)
map.removeLayer(Laboratorium1)
map.removeLayer(Laboratorium2)
map.removeLayer(Laboratorium3)
map.removeLayer(EmbungB)
map.removeLayer(EmbungC)
map.removeLayer(EmbungD)
map.removeLayer(EmbungE)
map.removeLayer(Labirin)
map.removeLayer(KantinBKL)
map.removeLayer(KantinRK)
map.removeLayer(RIMA)
map.removeLayer(MasjidRayaAtTanwir)
map.removeLayer(MasjidBaitulIlmi)
map.removeLayer(AsramaTB1)
map.removeLayer(AsramaTB2)
map.removeLayer(AsramaTB3)
map.removeLayer(AsramaTB4)
map.removeLayer(AsramaTB5)
map.removeLayer(GSG)
map.removeLayer(PoliklinikITERA)
map.removeLayer(ATM_Itera)
map.removeLayer(PLTS)
map.removeLayer(GEDUNG_F)
L.control.layers(baseMaps,overlayMaps, {collapsed : false}).addTo(map);
