{% include review.html %}

<form id="inventory-form">
  <div>
    <label for="date">Date:</label>
    <input type="text" id="date" name="date">
  </div>
  <div>
    <label for="action">Action:</label>
    <input type="text" id="action" name="action">
  </div>
  <div>
    <label for="user">User:</label>
    <input type="text" id="user" name="user">
  </div>
  <div>
    <label for="item">Item:</label>
    <input type="text" id="item" name="item">
  </div>
  <div>
    <label for="quantity">Quantity:</label>
    <input type="text" id="quantity" name="quantity">
  </div>
  <button type="submit" id="add-activity-btn">Add Activity</button>

<style>
  #inventory-form {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 20px;
  }

  #inventory-form div {
    display: flex;
    flex-direction: column;
    margin-bottom: 10px;
  }

  label {
    font-weight: bold;
    margin-bottom: 5px;
  }

  input[type="text"] {
    padding: 10px;
    font-size: 16px;
    border-radius: 5px;
    border: 1px solid gray;
  }

  #add-activity-btn {
    padding: 10px 20px;
    background-color: #4CAF50;
    color: white;
    border-radius: 5px;
    border: none;
    cursor: pointer;
    font-size: 16px;
    margin-top: 20px;
  }

  #inventory-table {
    border-collapse: collapse;
    width: 100%;
  }

  #inventory-table th, td {
    border: 1px solid black;
    padding: 8px;
    text-align: left;
  }

  #inventory-table th {
    background-color: lightgray;
  }
</style>

</form>

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
const form = document.getElementById('inventory-form');
const table = document.getElementById('inventory-table');

form.addEventListener('submit', function(event) {
  event.preventDefault();

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
});
</script>

