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

addActivityBtn.addEventListener('click', () => {
  form.style.display = 'block';
});

form.addEventListener('submit', (event) => {
  event.preventDefault();

  const date = document.getElementById('date').value;
  const action = document.getElementById('action').value;
  const user = document.getElementById('user').value;
  const item = document.getElementById('item').value;
  const quantity = document.getElementById('quantity').value;

  const newRow = table.insertRow();
  const dateCell = newRow.insertCell(0);
  const actionCell = newRow.insertCell(1);
  const userCell = newRow.insertCell(2);
  const itemCell = newRow.insertCell(3);
  const quantityCell = newRow.insertCell(4);

  dateCell.innerHTML = date;
  actionCell.innerHTML = action;
  userCell.innerHTML = user;
  itemCell.innerHTML = item;
  quantityCell.innerHTML = quantity;

  form.reset();
});
</script>




