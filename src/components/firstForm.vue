<template>
<form>
    <h1><b>आपले शिवमुद्रा मध्ये स्वागत आहे 🙏 </b></h1>
    <!-- प्राथमिक माहिती  -->
    <h2>प्राथमिक माहिती</h2>
    <lable>
        <h3>नाव :</h3>
    </lable>
    <input type="text" placeholder="पहिले नाव " v-model="dataofForm.firstName">
    <input type="text" placeholder="मधले नाव " v-model="dataofForm.middleName">
    <input type="text" placeholder="आडनाव " v-model="dataofForm.lastName">
    <br>
    <lable>
        <h3>टोपण नाव :</h3>
    </lable>
    <input type="text" placeholder="टोपण नाव " v-model="dataofForm.nickName">
    <br>
    <lable>
        <h3>जन्म तारीख :</h3>
    </lable>
    <input type="date" placeholder="टोपण नाव " v-model="dataofForm.dob">
    <lable>
        <h3>लिंग :</h3>
    </lable>
    <label for=male>पुरुष </label>
    <input type="radio" id="male" name="gender" value="पुरुष" v-model="dataofForm.gender">
    <br>
    <label for="female">स्त्री </label>
    <input type="radio" value="स्त्री" id="female" name="gender" v-model="dataofForm.gender">
    <br>
    <label>
        <h3> रक्तगट </h3>
    </label>
    <select v-model="dataofForm.blood">
        <option>O+</option>
        <option>O-</option>
        <option>A+</option>
        <option>A-</option>
        <option>B+</option>
        <option>B-</option>
        <option>AB+</option>
        <option>AB-</option>
    </select>
    <label>
        <h3>वैवाहिक स्थिति :</h3>
        <select v-model="dataofForm.marriageStatus">
            <option>अविवाहित </option>
            <option>विवाहित </option>
            <option>इतर </option>
        </select>
    </label>
    <br><br><br><br>

    <!-- संपर्क माहिती  -->
    <h2>संपर्क माहीती :</h2>
    <lable>
        <h3>Whatsapp Number :</h3>
    </lable>
    <input type="text" placeholder="Whatsapp नंबर " v-model="dataofForm.whatsapp">
    <lable>
        <h3>द्वितीय मोबाइल नंबर :</h3>
    </lable>
    <input type="text" placeholder="नसल्यास 0 टाका" v-model="dataofForm.secondaryNumber">
    <br>
    <label>
        <h3>E-mail :</h3>
    </label>
    <input type="email" placeholder="आपला ईमेल टाका " v-model="dataofForm.email">
    <br>
    <label>
        <h3>सध्याचा पत्ता :</h3>
    </label>
    <textarea rows="6" cols="40" placeholder="          आपला राहता पत्ता टाका" v-model="dataofForm.address"></textarea>
    <br>
    <label>
        <h3>राज्य :</h3>
    </label>
    <select v-model="dataofForm.state">
        <option value="Andhra Pradesh">Andhra Pradesh</option>
        <option value="Andaman and Nicobar Islands">Andaman and Nicobar Islands</option>
        <option value="Arunachal Pradesh">Arunachal Pradesh</option>
        <option value="Assam">Assam</option>
        <option value="Bihar">Bihar</option>
        <option value="Chandigarh">Chandigarh</option>
        <option value="Chhattisgarh">Chhattisgarh</option>
        <option value="Dadar and Nagar Haveli">Dadar and Nagar Haveli</option>
        <option value="Daman and Diu">Daman and Diu</option>
        <option value="Delhi">Delhi</option>
        <option value="Lakshadweep">Lakshadweep</option>
        <option value="Puducherry">Puducherry</option>
        <option value="Goa">Goa</option>
        <option value="Gujarat">Gujarat</option>
        <option value="Haryana">Haryana</option>
        <option value="Himachal Pradesh">Himachal Pradesh</option>
        <option value="Jammu and Kashmir">Jammu and Kashmir</option>
        <option value="Jharkhand">Jharkhand</option>
        <option value="Karnataka">Karnataka</option>
        <option value="Kerala">Kerala</option>
        <option value="Madhya Pradesh">Madhya Pradesh</option>
        <option value="Maharashtra">Maharashtra</option>
        <option value="Manipur">Manipur</option>
        <option value="Meghalaya">Meghalaya</option>
        <option value="Mizoram">Mizoram</option>
        <option value="Nagaland">Nagaland</option>
        <option value="Odisha">Odisha</option>
        <option value="Punjab">Punjab</option>
        <option value="Rajasthan">Rajasthan</option>
        <option value="Sikkim">Sikkim</option>
        <option value="Tamil Nadu">Tamil Nadu</option>
        <option value="Telangana">Telangana</option>
        <option value="Tripura">Tripura</option>
        <option value="Uttar Pradesh">Uttar Pradesh</option>
        <option value="Uttarakhand">Uttarakhand</option>
        <option value="West Bengal">West Bengal</option>
    </select>
    <br>
    <label>
        <h3>जिल्हा </h3>
    </label>
    <input type="text" placeholder="आपला राहता जिल्हा टाका" v-model="dataofForm.districts">
    <label>
        <h3>तालुका </h3>
    </label>
    <input type="text" placeholder="आपला राहता तालुका टाका" v-model="dataofForm.taluka">
    <br>
    <label>
        <h3>गावचा पत्ता :</h3>
    </label>
    <textarea rows="6" cols="40" placeholder="          आपला गावचा पत्ता टाका" v-model="dataofForm.gavAdd"></textarea>
    <br><br><br><br>
    <!-- शैक्षणिक माहिती  -->
    <h2>शैक्षणिक माहिती</h2>
    <label>
        <h3>शिक्षण</h3>
    </label>
    <select v-model="dataofForm.edu">
        <option>PhD</option>
        <option>पदव्युत्तर (डिग्रीनंतर)</option>
        <option>पदवीधर (१५ वी / इतर डिग्री) </option>
        <option>पदविका (ITI / डिप्लोमा)</option>
        <option>उच्च माध्यमिक (९ - १४)</option>
        <option>माध्यमिक (१ - ८)</option>
        <option>अशिक्षित</option>
    </select>
    <label>
        <h3>शाखा :</h3>
    </label>
    <input type="text" placeholder="उदा. कला/वाणिज्य/विज्ञान" v-model="dataofForm.branch">
    <br>
    <label>
        <h3>तुम्ही स्पर्धा परीक्षेची तयारी करत आहे का?</h3>
    </label>
    <label for=yes>होय </label>
    <input type="radio" id="yes" name="serviceExam" value="स्पर्धा-होय " v-model="dataofForm.civilServices">
    <br>
    <label for="no">नाही </label>
    <input type="radio" value="स्पर्धा-नाही" id="no" name="serviceExam" v-model="dataofForm.civilServices">
    <br>
    <label>
        <h3>स्पर्धा परीक्षेचा प्रकार :</h3>
    </label>
    <input type="text" placeholder="उदा. MPSC, UPSC, Railway" v-model="dataofForm.civilType">
    <br><br><br><br>
    <!-- व्यावसायीक माहिती  -->
    <h2>व्यावसायीक माहिती</h2>
    <label>
        <h3>व्यावसायाचा प्रकार :</h3>
    </label>
    <select v-model="dataofForm.incomeSource">
        <option></option>
        <option>स्वतःचा व्यवसाय / व्यापार</option>
        <option>नोकरी</option>
        <option>शेती</option>
        <option>काहीही नाही </option>
    </select>
    <br>
    <label>
        <h3>व्यावसाय/नोकरीचे क्षेत्र :</h3>
    </label>
    <input type="text" placeholder="उदा. शिक्षक, फळ व्यापारी " v-model="dataofForm.jobType">
    <br>

</form>
<div>
    {{dataofForm}}
</div>
</template>

<script>
export default {
    name: 'firstForm',
    data(){
        return{
            dataofForm:{
                firstName: "",
                middleName: "",
                lastName: "",
                nickName: "",
                dob:"",
                gender:"",
                blood: "",
                marriageStatus: "",
                whatsapp: "",
                secondaryNumber:"",
                email: "",
                address: "",
                state: "",
                districts: "",
                taluka: "",
                gavAdd: "",
                edu: "",
                branch: "",
                civilServices: "",
                civilType: "",
                incomeSource: "",
                jobType: "",
            }

        }
    }
}
</script>

<style>
h1 {
    color: tomato;
}

h2 {
    color: palegoldenrod;
    background-color: rgb(184, 63, 163);
    margin: auto;
    width: 50%;
    border: 3px solid rgb(47, 5, 124);
    padding: 10px;
}
</style>
