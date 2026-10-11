<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Job registration, school and college admission, and international travel application forms. Print, save as PDF and share.">
<meta name="theme-color" content="#102b50">
<title>Global Registration Center</title>

<style>
*{box-sizing:border-box}
body{
  margin:0;font-family:Arial,sans-serif;
  background:#f2f5fa;color:#17243b
}
header{
  background:#102b50;color:white;
  padding:25px 16px;text-align:center
}
header h1{margin:0 0 8px;font-size:27px}
header p{margin:0;color:#dce7f7}
.container{max-width:850px;margin:22px auto;padding:0 14px}
.notice{
  background:#fff4d6;padding:13px;border-radius:10px;
  font-size:14px;margin-bottom:18px
}
.cards{display:grid;grid-template-columns:repeat(3,1fr);gap:10px}
.card{
  background:white;padding:16px 8px;border-radius:12px;
  text-align:center;border:1px solid #dce4ef
}
.card h3{font-size:16px}
button,.btn{
  border:0;border-radius:8px;padding:12px 14px;
  background:#155eef;color:white;font-size:14px;
  cursor:pointer;text-decoration:none;display:inline-block
}
.card button{width:100%}
.card p{font-size:13px;color:#64748b}
.panel{
  display:none;background:white;padding:20px;
  margin-top:20px;border-radius:12px;
  box-shadow:0 3px 16px #102b5010
}
.panel.active{display:block}
.panel h2{margin-top:0;color:#102b50}
label{display:block;font-weight:bold;font-size:14px;margin:13px 0 6px}
input,select,textarea{
  width:100%;padding:12px;border:1px solid #cbd5e1;
  border-radius:7px;font-size:16px;background:white
}
textarea{min-height:80px;resize:vertical}
.grid{display:grid;grid-template-columns:1fr 1fr;gap:0 14px}
.actions{display:flex;flex-wrap:wrap;gap:9px;margin-top:20px}
.secondary{background:#475569}
.green{background:#087443}
footer{text-align:center;padding:25px;color:#64748b;font-size:13px}
.small{font-size:12px;color:#64748b}
@media(max-width:560px){
 .cards{grid-template-columns:1fr}
 .card{padding:12px}
 .grid{grid-template-columns:1fr}
 header h1{font-size:23px}
}
@media print{
 body{background:white}
 header,.notice,.cards,footer,.actions,.small{display:none!important}
 .container{margin:0;padding:0;max-width:none}
 .panel{display:none!important;box-shadow:none;padding:0;margin:0}
 .panel.active{display:block!important}
 input,select,textarea{
   border:0;border-bottom:1px solid #aaa;
   border-radius:0;padding:5px 0;font-size:12pt;
   appearance:none;background:white
 }
 label{margin-top:12px}
 h2{font-size:20pt}
}
</style>
</head>
<body>

<header>
  <h1>Global Registration Center</h1>
  <p>Job • Education • International Travel</p>
  <p style="margin-top:10px;font-size:13px">
    Registration Forms | درخواست فارم
  </p>
</header>

<main class="container">
  <div class="notice">
    <strong>Important / اہم اطلاع:</strong>
    These are general application forms, not official government,
    visa or employer forms. Submitting a form here does not guarantee
    a job, admission or visa.
  </div>

  <h2>Choose Your Form / اپنا فارم منتخب کریں</h2>

  <div class="cards">
    <div class="card">
      <h3>💼 Job Registration</h3>
      <p>نوکری کے لیے درخواست</p>
      <button onclick="showForm('job')">Open Job Form</button>
    </div>
    <div class="card">
      <h3>🎓 Admission</h3>
      <p>اسکول یا کالج میں داخلہ</p>
      <button onclick="showForm('admission')">Open Admission Form</button>
    </div>
    <div class="card">
      <h3>🌍 International</h3>
      <p>بیرونِ ملک درخواست</p>
      <button onclick="showForm('travel')">Open Travel Form</button>
    </div>
  </div>

  <section id="job" class="panel">
    <h2>Job Registration Form</h2>
    <p>نوکری کے لیے درخواست فارم</p>
    <form>
      <div class="grid">
        <div><label>Full Name / پورا نام *</label><input name="name" required autocomplete="name"></div>
        <div><label>Father / Guardian Name</label><input name="guardian"></div>
        <div><label>Email / ای میل</label><input type="email" name="email" autocomplete="email"></div>
        <div><label>Phone / رابطہ نمبر *</label><input type="tel" name="phone" required autocomplete="tel"></div>
        <div><label>City / شہر</label><input name="city" autocomplete="address-level2"></div>
        <div><label>Country / ملک</label><input name="country"></div>
        <div><label>Education / تعلیم *</label>
          <select name="education" required>
            <option value="">Select education</option>
            <option>Middle</option><option>Matric</option>
            <option>Intermediate</option><option>Bachelor</option>
            <option>Master</option><option>Other</option>
          </select>
        </div>
        <div><label>Job Title / نوکری</label><input name="job"></div>
        <div><label>Experience / تجربہ</label>
          <select name="experience">
            <option>No experience</option><option>Less than 1 year</option>
            <option>1–3 years</option><option>3+ years</option>
          </select>
        </div>
        <div><label>Preferred Work Location</label><input name="worklocation"></div>
      </div>
      <label>Skills / مہارتیں</label><textarea name="skills"></textarea>
      <label>Additional Information</label><textarea name="details"></textarea>
      <p class="small">Review your information before printing.</p>
      <div class="actions">
        <button type="button" onclick="printForm()">Print / Save PDF</button>
        <button type="button" class="green" onclick="sharePage()">Share Form</button>
      </div>
    </form>
  </section>

  <section id="admission" class="panel">
    <h2>School / College Admission Form</h2>
    <p>تعلیمی ادارے میں داخلے کا درخواست فارم</p>
    <form>
      <div class="grid">
        <div><label>Student Full Name *</label><input name="student" required></div>
        <div><label>Father / Guardian Name *</label><input name="guardian" required></div>
        <div><label>Date of Birth</label><input type="date" name="dob"></div>
        <div><label>Contact Number *</label><input type="tel" name="phone" required></div>
        <div><label>Email</label><input type="email" name="email"></div>
        <div><label>City / Country</label><input name="location"></div>
        <div><label>School / College Name *</label><input name="institution" required></div>
        <div><label>Class / Course *</label><input name="course" required></div>
        <div><label>Last Qualification</label><input name="qualification"></div>
        <div><label>Last Exam Marks / Grade</label><input name="marks"></div>
      </div>
      <label>Home Address</label><textarea name="address"></textarea>
      <label>Other Information</label><textarea name="details"></textarea>
      <div class="actions">
        <button type="button" onclick="printForm()">Print / Save PDF</button>
        <button type="button" class="green" onclick="sharePage()">Share Form</button>
      </div>
    </form>
  </section>

  <section id="travel" class="panel">
    <h2>International Travel Application</h2>
    <p>بیرونِ ملک سفر، تعلیم یا ملازمت کے لیے ابتدائی فارم</p>
    <form>
      <div class="grid">
        <div><label>Full Name *</label><input name="name" required></div>
        <div><label>Contact Number *</label><input type="tel" name="phone" required></div>
        <div><label>Email</label><input type="email" name="email"></div>
        <div><label>Current Country *</label><input name="country" required></div>
        <div><label>Destination Country *</label><input name="destination" required></div>
        <div><label>Purpose *</label>
          <select name="purpose" required>
            <option value="">Choose purpose</option>
            <option>Employment</option><option>Education</option>
            <option>Tourism</option><option>Family Visit</option>
            <option>Other</option>
          </select>
        </div>
        <div><label>Expected Travel Date</label><input type="date" name="date"></div>
        <div><label>Passport Status</label>
          <select name="passport">
            <option>Prefer not to say</option>
            <option>Valid passport available</option>
            <option>Need to apply for passport</option>
          </select>
        </div>
      </div>
      <label>Relevant Qualifications or Details</label><textarea name="details"></textarea>
      <p class="small">Do not enter your passport number, passport scan, or other sensitive identity information into this demo form.</p>
      <div class="actions">
        <button type="button" onclick="printForm()">Print / Save PDF</button>
        <button type="button" class="green" onclick="sharePage()">Share Form</button>
      </div>
    </form>
  </section>

  <p class="small" style="margin-top:18px">
    Demo version: the information entered is not uploaded or saved to a
    server. Printing creates a paper copy or lets you save it as PDF.
  </p>
</main>

<footer>
  Global Registration Center · General-purpose application templates
</footer>

<script>
function showForm(id){
  document.querySelectorAll('.panel').forEach(p=>{
    p.classList.remove('active');
  });
  const panel=document.getElementById(id);
  panel.classList.add('active');
  panel.scrollIntoView({behavior:'smooth',block:'start'});
}

function printForm(){
  const active=document.querySelector('.panel.active');
  if(!active){
    alert('Please open a form first.');
    return;
  }
  const form=active.querySelector('form');
  if(!form.reportValidity()) return;
  window.print();
}

async function sharePage(){
  const url=window.location.href;
  const title='Global Registration Center';
  const data={title:title,text:'Open the registration forms here:',url:url};
  try{
    if(navigator.share){
      await navigator.share(data);
    }else if(navigator.clipboard && window.isSecureContext){
      await navigator.clipboard.writeText(url);
      alert('Page link copied. You can share it on WhatsApp or IMO.');
    }else{
      prompt('Copy this page link:',url);
    }
  }catch(e){
    if(e.name!=='AbortError'){
      prompt('Copy this page link:',url);
    }
  }
}
</script>
</body>
</html>
