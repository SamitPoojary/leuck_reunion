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


addActivityBtn.addEventListener('click', function() {
  form.style.display = 'block';
});

form.addEventListener('submit', function(event) {
  event.preventDefault();

  const date = form.querySelector('#date').value;
  const action = form.querySelector('#action').value;
  const user = form.querySelector('#user').value;
  const item = form.querySelector('#item').value;
  const quantity = form.querySelector('#quantity').value;

  const row = document.createElement('tr');
  row.innerHTML = `
    <td>${date}</td>
    <td>${action}</td>
    <td>${user}</td>
    <td>${item}</td>
    <td>${quantity}</td>
  `;

  table.appendChild(row);

  form.reset();
  form.style.display = 'none';
});
</script>



