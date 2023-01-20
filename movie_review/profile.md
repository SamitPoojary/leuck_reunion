{% include review.html %}

<div id="profile-tab-content" class="tab-content">
  <h2>Profile</h2>
  <div id="profile-info">
    <p>Username: <span id="username"></span></p>
    <p>Email: <span id="email"></span></p>
    <button id="edit-profile-btn">Edit Profile</button>
  </div>
  <form id="edit-profile-form" style="display: none;">
    <label>
      New Username:
      <input type="text" id="new-username">
    </label>
    <br>
    <label>
      New Email:
      <input type="email" id="new-email">
    </label>
    <br>
    <button type="submit">Save Changes</button>
    <button type="button" id="cancel-edit-btn">Cancel</button>
  </form>
</div>

<style>
#profile-tab-content {
  text-align: center;
}

#profile-info {
  margin: 20px 0;
}

#edit-profile-form {
  margin-top: 20px;
}
</style>



<script>
const editProfileBtn = document.getElementById('edit-profile-btn');
const cancelEditBtn = document.getElementById('cancel-edit-btn');
const editProfileForm = document.getElementById('edit-profile-form');
const usernameSpan = document.getElementById('username');
const emailSpan = document.getElementById('email');

editProfileBtn.addEventListener('click', event => {
  editProfileForm.style.display = 'block';
  profileInfoDiv.style.display = 'none';
});

cancelEditBtn.addEventListener('click', event => {
  editProfileForm.style.display = 'none';
  profileInfoDiv.style.display = 'block';
});

editProfileForm.addEventListener('submit', event => {
  event.preventDefault();
  const newUsername = document.getElementById('new-username').value;
  const newEmail = document.getElementById('new-email').value;
  
  usernameSpan.innerText = newUsername;
  emailSpan.innerText = newEmail;

  editProfileForm.style.display = 'none';
  profileInfoDiv.style.display = 'block';
});
</script>

