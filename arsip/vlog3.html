<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Manajemen Akun Gmail</title>
<style>
  body { font-family: Arial, sans-serif; margin: 20px; }
  h1 { text-align: center; }
  .phone { border: 1px solid #ccc; padding: 10px; margin-bottom: 10px; }
  .phone h2 { margin: 0; cursor: pointer; }
  .accounts { margin-top: 5px; display: none; }
  .account { padding: 5px; margin: 2px 0; border-bottom: 1px solid #eee; display: flex; justify-content: space-between; align-items: center; }
  .status { padding: 2px 5px; border-radius: 4px; color: #fff; font-size: 12px; margin-right: 5px; }
  .tersedia { background-color: green; }
  .terjual { background-color: gray; }
  .ditolak { background-color: red; }
  button { margin-left: 5px; }
  form { margin-bottom: 20px; }
</style>
</head>
<body>

<h1>Manajemen Akun Gmail</h1>

<!-- Form tambah HP -->
<form id="addPhoneForm">
  <input type="text" id="phoneName" placeholder="Nama HP baru" required>
  <button type="submit">Tambah HP</button>
</form>

<!-- Form tambah akun -->
<form id="addAccountForm">
  <select id="selectPhone" required>
    <option value="">Pilih HP</option>
  </select>
  <input type="email" id="accountEmail" placeholder="Email Gmail" required>
  <select id="accountSource" required>
    <option value="">Asal Akun</option>
    <option value="buat sendiri">Buat Sendiri</option>
    <option value="beli">Beli</option>
  </select>
  <select id="accountStatus" required>
    <option value="">Status</option>
    <option value="tersedia">Tersedia</option>
    <option value="ditolak">Ditolak</option>
  </select>
  <button type="submit">Tambah Akun</button>
</form>

<div id="phonesContainer"></div>

<script>
// ======== DATA & LOCALSTORAGE ========
let data = JSON.parse(localStorage.getItem('gmailManager')) || { phones: [] };

// ======== HELPER FUNCTIONS ========
function saveData() {
  localStorage.setItem('gmailManager', JSON.stringify(data));
}

function renderPhones() {
  const container = document.getElementById('phonesContainer');
  container.innerHTML = '';
  
  data.phones.forEach((phone, pIndex) => {
    const phoneDiv = document.createElement('div');
    phoneDiv.className = 'phone';

    const phoneHeader = document.createElement('h2');
    phoneHeader.textContent = phone.name;
    phoneHeader.onclick = () => {
      const accDiv = phoneDiv.querySelector('.accounts');
      accDiv.style.display = accDiv.style.display === 'none' ? 'block' : 'none';
    };
    phoneDiv.appendChild(phoneHeader);

    const accountsDiv = document.createElement('div');
    accountsDiv.className = 'accounts';

    phone.accounts.forEach((acc, aIndex) => {
      const accDiv = document.createElement('div');
      accDiv.className = 'account';

      const info = document.createElement('div');
      const statusSpan = document.createElement('span');
      statusSpan.className = 'status ' + acc.status;
      statusSpan.textContent = acc.status;
      info.appendChild(statusSpan);
      info.innerHTML += ` ${acc.email} (${acc.source})`;

      const btnDiv = document.createElement('div');

      if (acc.status === 'tersedia') {
        const sellBtn = document.createElement('button');
        sellBtn.textContent = 'Terjual';
        sellBtn.onclick = () => {
          // hapus akun jika terjual
          data.phones[pIndex].accounts.splice(aIndex, 1);
          saveData();
          renderPhones();
        };
        btnDiv.appendChild(sellBtn);
      }

      accDiv.appendChild(info);
      accDiv.appendChild(btnDiv);
      accountsDiv.appendChild(accDiv);
    });

    phoneDiv.appendChild(accountsDiv);
    container.appendChild(phoneDiv);
  });

  // Update select HP untuk tambah akun
  const selectPhone = document.getElementById('selectPhone');
  selectPhone.innerHTML = '<option value="">Pilih HP</option>';
  data.phones.forEach((phone, index) => {
    const opt = document.createElement('option');
    opt.value = index;
    opt.textContent = phone.name;
    selectPhone.appendChild(opt);
  });
}

// ======== EVENT LISTENERS ========
document.getElementById('addPhoneForm').addEventListener('submit', e => {
  e.preventDefault();
  const name = document.getElementById('phoneName').value.trim();
  if (!name) return;
  data.phones.push({ name: name, accounts: [] });
  saveData();
  renderPhones();
  e.target.reset();
});

document.getElementById('addAccountForm').addEventListener('submit', e => {
  e.preventDefault();
  const phoneIndex = document.getElementById('selectPhone').value;
  const email = document.getElementById('accountEmail').value.trim();
  const source = document.getElementById('accountSource').value;
  const status = document.getElementById('accountStatus').value;
  if (phoneIndex === '' || !email || !source || !status) return;

  data.phones[phoneIndex].accounts.push({ email, source, status });
  saveData();
  renderPhones();
  e.target.reset();
});

// ======== INITIAL RENDER ========
renderPhones();
</script>

</body>
</html>