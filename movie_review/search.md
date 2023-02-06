{% include review.html %}

<button id="add-activity-btn">Add Activity</button>
<table id="inventory-table">
  <tr>
    <th>Date</th>
    <th>Action</th>
    <th>User</th>
    <th>Item</th>
    <th>Quantity</th>
  </tr>
</table>

<script>
const table = document.getElementById('inventory-table');

function addInventory() {
  const date = document.getElementById('date').value;
  const action = document.getElementById('action').value;
  const user = document.getElementById('user').value;
  const item = document.getElementById('item').value;
  const quantity = document.getElementById('quantity').value;

  const row = table.insertRow();
  const dateCell = row.insertCell(0);
  const actionCell = row.insertCell(1);
  const userCell = row.insertCell(2);
  const itemCell = row.insertCell(3);
  const quantityCell = row.insertCell(4);

  dateCell.innerHTML = date;
  actionCell.innerHTML = action;
  userCell.innerHTML = user;
  itemCell.innerHTML = item;
  quantityCell.innerHTML = quantity;
}

document.getElementById('add-activity-btn').addEventListener('click', addInventory);
</script>
