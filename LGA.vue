<template>
    <div class="container">
        <div class="row">
            <div class="form-group col-md-6">
                <label for="state" class="form-label">State of Origin</label>
                <select type="text1" id="state" v-model="origin" class="form-control gaminators" @change="selectState()">
                    <option :value="null" disabled selected>� Select State �</option>
                    <option value='Abia'>Abia</option>
                    <option value='Adamawa'>Adamawa</option>
                    <option value='AkwaIbom'>AkwaIbom</option>
                    <option value='Anambra'>Anambra</option>
                    <option value='Bauchi'>Bauchi</option>
                    <option value='Bayelsa'>Bayelsa</option>
                    <option value='Benue'>Benue</option>
                    <option value='Borno'>Borno</option>
                    <option value='Cross River'>Cross River</option>
                    <option value='Delta'>Delta</option>
                    <option value='Ebonyi'>Ebonyi</option>
                    <option value='Edo'>Edo</option>
                    <option value='Ekiti'>Ekiti</option>
                    <option value='Enugu'>Enugu</option>
                    <option value='FCT'>FCT</option>
                    <option value='Gombe'>Gombe</option>
                    <option value='Imo'>Imo</option>
                    <option value='Jigawa'>Jigawa</option>
                    <option value='Kaduna'>Kaduna</option>
                    <option value='Kano'>Kano</option>
                    <option value='Katsina'>Katsina</option>
                    <option value='Kebbi'>Kebbi</option>
                    <option value='Kogi'>Kogi</option>
                    <option value='Kwara'>Kwara</option>
                    <option value='Lagos'>Lagos</option>
                    <option value='Nasarawa'>Nasarawa</option>
                    <option value='Niger'>Niger</option>
                    <option value='Ogun'>Ogun</option>
                    <option value='Ondo'>Ondo</option>
                    <option value='Osun'>Osun</option>
                    <option value='Oyo'>Oyo</option>
                    <option value='Plateau'>Plateau</option>
                    <option value='Rivers'>Rivers</option>
                    <option value='Sokoto'>Sokoto</option>
                    <option value='Taraba'>Taraba</option>
                    <option value='Yobe'>Yobe</option>
                    <option value='Zamfara'>Zamafara</option>
                </select>
            </div>
            <div class="form-group col-md-6">
                <label for="lga" class="form-label">Local Government Area</label>
                <select name="lga" v-model="lga" id="lga" class="form-control gaminators" required>
                    <option :value="null" selected>-- Select L.G.A. --</option>
                </select>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            origin:null,
            lga:null
        }
    },
    methods: {
        selectState(){
            var select = document.getElementById("lga");
            var length = select.options.length;
            for (i = 0; i < length; i++) {
                if (i != 0) {
                    select.options[i] = null;
                } 
            }
            var state = this.origin
            switch (state) {
            case "Abia":
            var data = ['Aba North', 'Aba South', 'Arochukwu', 'Bende', 'Ikwuano', 'Isiala Ngwa North', 'Isiala Ngwa South', 'Isuikwuato', 'Obi Ngwa', 'Ohafia', 'Osisioma', 'Ugwunagbo', 'Ukwa East', 'Ukwa West', 'Umuahia North', 'muahia South', 'Umu Nneochi']; 
            var geo = "South East"
            break;

            case "Adamawa":
            var data = ['Demsa', 'Fufure', 'Ganye', 'Gayuk', 'Gombi', 'Grie', 'Hong', 'Jada', 'Larmurde', 'Madagali', 'Maiha', 'Mayo Belwa', 'Michika', 'Mubi North', 'Mubi South', 'Numan', 'Shelleng', 'Song', 'Toungo', 'Yola North', 'Yola South'];
            var geo = "North East"
            break;

            case "AkwaIbom":
            var data = ['Abak', 'Eastern Obolo', 'Eket', 'Esit Eket', 'Essien Udim', 'Etim Ekpo', 'Etinan', 'Ibeno', 'Ibesikpo Asutan', 'Ibiono-Ibom', 'Ika', 'Ikono', 'Ikot Abasi', 'Ikot Ekpene', 'Ini', 'Itu', 'Mbo', 'Mkpat-Enin', 'Nsit-Atai', 'Nsit-Ibom', 'Nsit-Ubium', 'Obot Akara', 'Okobo', 'Onna', 'Oron', 'Oruk Anam', 'Udung-Uko', 'Ukanafun', 'Uruan', 'Urue-Offong Oruko', 'Uyo'];
            var geo = "South South"
            break;

            case "Anambra":
            var data = ['Aguata', 'Anambra East', 'Anambra West', 'Anaocha', 'Awka North', 'Awka South', 'Ayamelum', 'Dunukofia', 'Ekwusigo', 'Idemili North', 'Idemili South', 'Ihiala', 'Njikoka', 'Nnewi North', 'Nnewi South', 'Ogbaru', 'Onitsha North', 'Onitsha South', 'Orumba North', 'Orumba South', 'Oyi'];
            var geo = "South East"
            break;

            case "Bauchi":
            var data = ['Alkaleri', 'Bauchi', 'Bogoro', 'Damban', 'Darazo', 'Dass', 'Gamawa', 'Ganjuwa', 'Giade', 'Itas-Gadau', 'Jama are', 'Katagum', 'Kirfi', 'Misau', 'Ningi', 'Shira', 'Tafawa Balewa', ' Toro', ' Warji', ' Zaki'];
            var geo = "North East"
            break;
            
            case "Bayelsa":
            var data = ['Brass', 'Ekeremor', 'Kolokuma Opokuma', 'Nembe', 'Ogbia', 'Sagbama', 'Southern Ijaw', 'Yenagoa'];
            var geo = "South South"
            break;

            case "Benue":
            var geo = "North Central"
            var data = ['Agatu', 'Apa', 'Ado', 'Buruku', 'Gboko', 'Guma', 'Gwer East', 'Gwer West', 'Katsina-Ala', 'Konshisha', 'Kwande', 'Logo', 'Makurdi', 'Obi', 'Ogbadibo', 'Ohimini', 'Oju', 'Okpokwu', 'Oturkpo', 'Tarka', 'Ukum', 'Ushongo', 'Vandeikya'];
            break;

            case "Borno":
            var data =  ['Abadam', 'Askira-Uba', 'Bama', 'Bayo', 'Biu', 'Chibok', 'Damboa', 'Dikwa', 'Gubio', 'Guzamala', 'Gwoza', 'Hawul', 'Jere', 'Kaga', 'Kala-Balge', 'Konduga', 'Kukawa', 'Kwaya Kusar', 'Mafa', 'Magumeri', 'Maiduguri', 'Marte', 'Mobbar', 'Monguno', 'Ngala', 'Nganzai', 'Shani'];
            var geo = "North East"
            break;

            case "Cross River":
            var data =  ['Abi', 'Akamkpa', 'Akpabuyo', 'Bakassi', 'Bekwarra', 'Biase', 'Boki', 'Calabar Municipal', 'Calabar South', 'Etung', 'Ikom', 'Obanliku', 'Obubra', 'Obudu', 'Odukpani', 'Ogoja', 'Yakuur', 'Yala'];
            var geo = "South South"
            break;
            
            case "Delta":
            var data =  ['Aniocha North', 'Aniocha South', 'Bomadi', 'Burutu', 'Ethiope East', 'Ethiope West', 'Ika North East', 'Ika South', 'Isoko North', 'Isoko South', 'Ndokwa East', 'Ndokwa West', 'Okpe', 'Oshimili North', 'Oshimili South', 'Patani', 'Sapele', 'Udu', 'Ughelli North', 'Ughelli South', 'Ukwuani', 'Uvwie', 'Warri North', 'Warri South', 'Warri South West'];
            var geo = "South South"
            break;
            
            case "Ebonyi":
            var data = ['Abakaliki', 'Afikpo North', 'Afikpo South', 'Ebonyi', 'Ezza North', 'Ezza South', 'Ikwo', 'Ishielu', 'Ivo', 'Izzi', 'Ohaozara', 'Ohaukwu', 'Onicha'];
            var geo = "South East"
            break;

            case "Edo":
            var data = ['Akoko-Edo', 'Egor', 'Esan Central', 'Esan North-East', 'Esan South-East', 'Esan West', 'Etsako Central', 'Etsako East', 'Etsako West', 'Igueben', 'Ikpoba Okha', 'Orhionmwon', 'Oredo', 'Ovia North-East', 'Ovia South-West', 'Owan East', 'Owan West', 'Uhunmwonde'];
            var geo = "South South"
            break;
            
            case "Ekiti":
            var data = ['Ado Ekiti', 'Efon', 'Ekiti East', 'Ekiti South-West', 'Ekiti West', 'Emure', 'Gbonyin', 'Ido Osi', 'Ijero', 'Ikere', 'Ikole', 'Ilejemeje', 'Irepodun-Ifelodun', 'Ise-Orun', 'Moba', 'Oye'];
            var geo = "South West"
            break;

            case "Rivers":
            var data = ['Port Harcourt', 'Obio-Akpor', 'Okrika', 'Ogu�Bolo', 'Eleme', 'Tai', 'Gokana', 'Khana', 'Oyigbo', 'Opobo�Nkoro', 'Andoni', 'Bonny', 'Degema', 'Asari-Toru', 'Akuku-Toru', 'Abua�Odual', 'Ahoada West', 'Ahoada East', 'Ogba�Egbema�Ndoni', 'Emohua', 'Ikwerre', 'Etche', 'Omuma'];
            var geo = "South South"
            break;

            case "Enugu":
            var data =  ['Aninri', 'Awgu', 'Enugu East', 'Enugu North', 'Enugu South', 'Ezeagu', 'Igbo Etiti', 'Igbo Eze North', 'Igbo Eze South', 'Isi Uzo', 'Nkanu East', 'Nkanu West', 'Nsukka', 'Oji River', 'Udenu', 'Udi', 'Uzo Uwani'];
            var geo = "South East"
            break;

            case "FCT":
            var data =  ['Abaji', 'Bwari', 'Gwagwalada', 'Kuje', 'Kwali', 'Municipal Area Council'];
            var geo = "North Central"
            break;

            case "Gombe":
            var data =   ['Akko', 'Balanga', 'Billiri', 'Dukku', 'Funakaye', 'Gombe', 'Kaltungo', 'Kwami', 'Nafada', 'Shongom', 'Yamaltu-Deba'];
            var geo = "North East"
            break;
            
            case "Imo":
            var data =   ['Aboh Mbaise', 'Ahiazu Mbaise', 'Ehime Mbano', 'Ezinihitte', 'Ideato North', 'Ideato South', 'Ihitte-Uboma', 'Ikeduru', 'Isiala Mbano', 'Isu', 'Mbaitoli', 'Ngor Okpala', 'Njaba', 'Nkwerre', 'Nwangele', 'Obowo', 'Oguta', 'Ohaji-Egbema', 'Okigwe', 'Orlu', 'Orsu', 'Oru East', 'Oru West', 'Owerri Municipal', 'Owerri North', 'Owerri West', 'Unuimo'];
            var geo = "South East"
            break;

            case "Jigawa":
            var data =   ['Auyo', 'Babura', 'Biriniwa', 'Birnin Kudu', 'Buji', 'Dutse', 'Gagarawa', 'Garki', 'Gumel', 'Guri', 'Gwaram', 'Gwiwa', 'Hadejia', 'Jahun', 'Kafin Hausa', 'Kazaure', 'Kiri Kasama', 'Kiyawa', 'Kaugama', 'Maigatari', 'Malam Madori', 'Miga', 'Ringim', 'Roni', 'Sule Tankarkar', 'Taura', 'Yankwashi'];
            var geo = "North West"
            break;

            case "Kaduna":
            var data =  ['Birnin Gwari', 'Chikun', 'Giwa', 'Igabi', 'Ikara', 'Jaba', 'Jema a', 'Kachia', 'Kaduna North', 'Kaduna South', 'Kagarko', 'Kajuru', 'Kaura', 'Kauru', 'Kubau', 'Kudan', 'Lere', 'Makarfi', 'Sabon Gari', 'Sanga', 'Soba', 'Zangon Kataf', 'Zaria'];
            var geo = "North West"
            break;

            case "Kano":
            var data = ['Ajingi', 'Albasu', 'Bagwai', 'Bebeji', 'Bichi', 'Bunkure', 'Dala', 'Dambatta', 'Dawakin Kudu', 'Dawakin Tofa', 'Doguwa', 'Fagge', 'Gabasawa', 'Garko', 'Garun Mallam', 'Gaya', 'Gezawa', 'Gwale', 'Gwarzo', 'Kabo', 'Kano Municipal', 'Karaye', 'Kibiya', 'Kiru', 'Kumbotso', 'Kunchi', 'Kura', 'Madobi', 'Makoda', 'Minjibir', 'Nasarawa', 'Rano', 'Rimin Gado', 'Rogo', 'Shanono', 'Sumaila', 'Takai', 'Tarauni', 'Tofa', 'Tsanyawa', 'Tudun Wada', 'Ungogo', 'Warawa', 'Wudil'];
            var geo = "North West"
            break;

            case "Katsina":
            var data = ['Bakori', 'Batagarawa', 'Batsari', 'Baure', 'Bindawa', 'Charanchi', 'Dandume', 'Danja', 'Dan Musa', 'Daura', 'Dutsi', 'Dutsin Ma', 'Faskari', 'Funtua', 'Ingawa', 'Jibia', 'Kafur', 'Kaita', 'Kankara', 'Kankia', 'Katsina', 'Kurfi', 'Kusada', 'Mai Adua', 'Malumfashi', 'Mani', 'Mashi', 'Matazu', 'Musawa', 'Rimi', 'Sabuwa', 'Safana', 'Sandamu', 'Zango'];
            var geo = "North West"
            break;

            case "Kebbi":
            var data =  ['Aleiro', 'Arewa Dandi', 'Argungu', 'Augie', 'Bagudo', 'Birnin Kebbi', 'Bunza', 'Dandi', 'Fakai', 'Gwandu', 'Jega', 'Kalgo', 'Koko Besse', 'Maiyama', 'Ngaski', 'Sakaba', 'Shanga', 'Suru', 'Wasagu Danko', 'Yauri', 'Zuru'];
            var geo = "North West"
            break;

            case "Kogi":
            var data =  ['Adavi', 'Ajaokuta', 'Ankpa', 'Bassa', 'Dekina', 'Ibaji', 'Idah', 'Igalamela Odolu', 'Ijumu', 'Kabba Bunu', 'Kogi', 'Lokoja', 'Mopa Muro', 'Ofu', 'Ogori Magongo', 'Okehi', 'Okene', 'Olamaboro', 'Omala', 'Yagba East', 'Yagba West'];
            var geo = "North Central"
            break;

            case "Kwara":
            var data =  ['Asa', 'Baruten', 'Edu', 'Ekiti', 'Ifelodun', 'Ilorin East', 'Ilorin South', 'Ilorin West', 'Irepodun', 'Isin', 'Kaiama', 'Moro', 'Offa', 'Oke Ero', 'Oyun', 'Pategi'];
            var geo = "North Central"
            break;

            case "Lagos":
            var data = ['Agege', 'Ajeromi-Ifelodun', 'Alimosho', 'Amuwo-Odofin', 'Apapa', 'Badagry', 'Epe', 'Eti Osa', 'Ibeju-Lekki', 'Ifako-Ijaiye', 'Ikeja', 'Ikorodu', 'Kosofe', 'Lagos Island', 'Lagos Mainland', 'Mushin', 'Ojo', 'Oshodi-Isolo', 'Shomolu', 'Surulere'];
            var geo = "South West"
            break;

            case "Nasarawa":
            var data = ['Akwanga', 'Awe', 'Doma', 'Karu', 'Keana', 'Keffi', 'Kokona', 'Lafia', 'Nasarawa', 'Nasarawa Egon', 'Obi', 'Toto', 'Wamba'];
            var geo = "North Central"
            break;

            case "Niger":
            var data = ['Agaie', 'Agwara', 'Bida', 'Borgu', 'Bosso', 'Chanchaga', 'Edati', 'Gbako', 'Gurara', 'Katcha', 'Kontagora', 'Lapai', 'Lavun', 'Magama', 'Mariga', 'Mashegu', 'Mokwa', 'Moya', 'Paikoro', 'Rafi', 'Rijau', 'Shiroro', 'Suleja', 'Tafa', 'Wushishi'];
            var geo = "North Central"
            break;

            case "Ogun":
            var data = ['Abeokuta North', 'Abeokuta South', 'Ado-Odo Ota', 'Egbado North', 'Egbado South', 'Ewekoro', 'Ifo', 'Ijebu East', 'Ijebu North', 'Ijebu North East', 'Ijebu Ode', 'Ikenne', 'Imeko Afon', 'Ipokia', 'Obafemi Owode', 'Odeda', 'Odogbolu', 'Ogun Waterside', 'Remo North', 'Shagamu'];
            var geo = "South West"
            break;

            case "Ondo":
            var data = ['Akoko North-East', 'Akoko North-West', 'Akoko South-West', 'Akoko South-East', 'Akure North', 'Akure South', 'Ese Odo', 'Idanre', 'Ifedore', 'Ilaje', 'Ile Oluji-Okeigbo', 'Irele', 'Odigbo', 'Okitipupa', 'Ondo East', 'Ondo West', 'Ose', 'Owo'];
            var geo = "South West"
            break;

            case "Osun":
            var data = ['Atakunmosa East', 'Atakunmosa West', 'Aiyedaade', 'Aiyedire', 'Boluwaduro', 'Boripe', 'Ede North', 'Ede South', 'Ife Central', 'Ife East', 'Ife North', 'Ife South', 'Egbedore', 'Ejigbo', 'Ifedayo', 'Ifelodun', 'Ila', 'Ilesa East', 'Ilesa West', 'Irepodun', 'Irewole', 'Isokan', 'Iwo', 'Obokun', 'Odo Otin', 'Ola Oluwa', 'Olorunda', 'Oriade', 'Orolu', 'Osogbo'];
            var geo = "South West"
            break;

            case "Oyo":
            var data = ['Afijio', 'Akinyele', 'Atiba', 'Atisbo', 'Egbeda', 'Ibadan North', 'Ibadan North-East', 'Ibadan North-West', 'Ibadan South-East', 'Ibadan South-West', 'Ibarapa Central', 'Ibarapa East', 'Ibarapa North', 'Ido', 'Irepo', 'Iseyin', 'Itesiwaju', 'Iwajowa', 'Kajola', 'Lagelu', 'Ogbomosho North', 'Ogbomosho South', 'Ogo Oluwa', 'Olorunsogo', 'Oluyole', 'Ona Ara', 'Orelope', 'Ori Ire', 'Oyo', 'Oyo East', 'Saki East', 'Saki West', 'Surulere'];
           var geo = "South West"
           break;

            case "Plateau":
            var data = ['Bokkos', 'Barkin Ladi', 'Bassa', 'Jos East', 'Jos North', 'Jos South', 'Kanam', 'Kanke', 'Langtang South', 'Langtang North', 'Mangu', 'Mikang', 'Pankshin', 'Qua an Pan', 'Riyom', 'Shendam', 'Wase'];
           var geo = "North Central"
           break;

            case "Sokoto":
            var data = ['Binji', 'Bodinga', 'Dange Shuni', 'Gada', 'Goronyo', 'Gudu', 'Gwadabawa', 'Illela', 'Isa', 'Kebbe', 'Kware', 'Rabah', 'Sabon Birni', 'Shagari', 'Silame', 'Sokoto North', 'Sokoto South', 'Tambuwal', 'Tangaza', 'Tureta', 'Wamako', 'Wurno', 'Yabo'];
            var geo = "North West"
            break;

            case "Taraba":
            var data =  ['Ardo Kola', 'Bali', 'Donga', 'Gashaka', 'Gassol', 'Ibi', 'Jalingo', 'Karim Lamido', 'Kumi', 'Lau', 'Sardauna', 'Takum', 'Ussa', 'Wukari', 'Yorro', 'Zing'];
            var geo = "North East"
            break;

            case "Yobe":
            var data =   ['Bade', 'Bursari', 'Damaturu', 'Fika', 'Fune', 'Geidam', 'Gujba', 'Gulani', 'Jakusko', 'Karasuwa', 'Machina', 'Nangere', 'Nguru', 'Potiskum', 'Tarmuwa', 'Yunusari', 'Yusufari'];
            var geo = "North East"
            break;

            case "Zamfara":
            var data =   ['Anka', 'Bakura', 'Birnin Magaji Kiyaw', 'Bukkuyum', 'Bungudu', 'Gummi', 'Gusau', 'Kaura Namoda', 'Maradun', 'Maru', 'Shinkafi', 'Talata Mafara', 'Chafe', 'Zurmi'];
            var geo = "North West"
            }
            var i;
            var html = [];
            //loop through the array
            for (var i = 0; i < data.length; i++) {//begin for loop
                //add the option elements to the html array
                html.push("<option>" + data[i] + "</option>")
            }//end for loop

            //add the option values to the select list with an id of lga
            document.getElementById("lga").innerHTML = html.join('');
            document.getElementById("geo").value = geo;
        }
    },
}
</script>