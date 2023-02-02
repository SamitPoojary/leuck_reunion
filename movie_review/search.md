{% include review.html %}



<button id="add-activity-btn">Add Activity</button>
<table>
  <tr>
    <th>Date</th>
    <th>Action</th>
    <th>User</th>
    <th>Item</th>
    <th>Quantity</th>
  </tr>
<style>
  table {
    width: 100%;
    border-collapse: collapse;
  }

  th, td {
    border: 1px solid black;
    padding: 8px;
    text-align: left;
  }

  th {
    background-color: #f2f2f2;
  }
</style>
</table>


<script>
const addActivityBtn = document.getElementById('add-activity-btn');
const table = document.querySelector('table');
const form = document.createElement('form');

form.innerHTML = `
  <label>Date: <input type="text" id="date"></label>
  <label>Action: <input type="text" id="action"></label>
  <label>User: <input type="text" id="user"></label>
  <label>Item: <input type="text" id="item"></label>
  <label>Quantity: <input type="text" id="quantity"></label>
  <button type="submit">Add</button>
`;



form.style.display = 'none';
document.body.appendChild(form);

addActivityBtn.addEventListener('click', event => {
  event.preventDefault();
  form.style.display = 'block';
});

form.addEventListener('submit', event => {
  event.preventDefault();
  const date = document.getElementById('date').value;
  const action = document.getElementById('action').value;
  const user = document.getElementById('user').value;
  const item = document.getElementById('item').value;
  const quantity = document.getElementById('quantity').value;

  const newRow = document.createElement('tr');
  newRow.style.border = '1px solid black';
  newRow.innerHTML = `
    <td style="border: 1px solid black; padding: 8px;">${date}</td>
    <td style="border: 1px solid black; padding: 8px;">${action}</td>
    <td style="border: 1px solid black; padding: 8px;">${user}</td>
    <td style="border: 1px solid black; padding: 8px;">${item}</td>
    <td style="border: 1px solid black; padding: 8px;">${quantity}</td>
  `;

  table.appendChild(newRow);
  form.style.display = 'none';
});
</script>




