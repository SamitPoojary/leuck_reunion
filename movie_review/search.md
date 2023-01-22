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
  newRow.innerHTML = `
    <td>${date}</td>
    <td>${action}</td>
    <td>${user}</td>
    <td>${item}</td>
    <td>${quantity}</td>
  `;

  table.appendChild(newRow);
  form.style.display = 'none';
});
</script>


