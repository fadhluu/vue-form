<template>
  <div class="container">
    <form>
      <div class="row mt-4">
        <div class="col-lg-6 col-md-8 col-sm-12 mx-auto">
          <h1>File a complaint</h1>
          <!-- email -->
          <div class="form-group">
            <label for="email"><b>Email</b></label>
            <input
              type="email"
              name="email"
              id="email"
              class="form-control"
              v-model.lazy="userData.email"
            />
          </div>
          <!-- password -->
          <div class="form-group">
            <label for="password"><b>Password</b></label>
            <input
              type="password"
              name="password"
              id="password"
              class="form-control"
              v-model.lazy="userData.password"
            />
          </div>
          <!-- age -->
          <div class="form-group">
            <label for="age"><b>Age</b></label>
            <input
              type="number"
              name="age"
              id="age"
              class="form-control"
              v-model.lazy="userData.age"
            />
          </div>
          <!-- gender -->
          <div class="form-group">
            <label for=""><b>Gender</b></label><br>
            <div class="form-check form-check-inline">
              <input
                class="form-check-input"
                type="radio"
                id="male"
                value="Male"
                v-model="userData.gender"
              />
              <label class="form-check-label" for="male">Male</label>
            </div>
            <div class="form-check form-check-inline">
              <input
                class="form-check-input"
                type="radio"
                id="female"
                value="Female"
                v-model="userData.gender"
              />
              <label class="form-check-label" for="female">Female</label>
            </div>
          </div>
          <!-- message -->
          <div class="form-group">
            <label for="message"><b>Message</b></label>
            <textarea
              name="message"
              id="message"
              cols="30"
              rows="3"
              class="form-control"
              v-model.lazy="message"
            ></textarea>
          </div>
          <!-- mailing -->
          <div class="form-group">
            <div class="form-check form-check-inline">
              <input class="form-check-input"
              type="checkbox"
              id="send_main"
              v-model="mailing"
              value="send_mail"/>
              <label class="form-check-label" for="send_main"
                ><b>Send Mail</b></label
              >
            </div>
            <div class="form-check form-check-inline">
              <input
                class="form-check-input"
                type="checkbox"
                id="send_infomail"
                value="send_infomail"
                v-model="mailing"
              />
              <label class="form-check-label" for="send_infomail"
                ><b>Send Infomail</b></label
              >
            </div>
          </div>
          <!-- priority -->
          <div class="form-group">
            <label for="priority"><b>Priority</b></label>
            <select class="custom-select" id="priority" v-model="selectedPriority">
              <option v-for="priority in priorities"
              :selected="priority == 'Medium'">
              {{priority}}
              </option>
            </select>
          </div>
          <!-- submit -->
          <div class="form-group">
            <button class="btn btn-primary">Submit</button>
          </div>
        </div>
        <div class="col-lg-6">
          <h1>Form Data</h1>
          <div class="card">
            <div class="card-header">
              User Data
            </div>
            <div class="card-body">
              <p class="card-text">Email: {{ userData.email }}</p>
              <p class="card-text">Password: {{ userData.password }}</p>
              <p class="card-text">Age: {{ userData.age }}</p>
              <p class="card-text">Message: {{ message }}</p>
              <p class="card-text">
                Mailing:
                <ul>
                  <li v-for="item in mailing">{{item}}</li>
                </ul>
              </p>
              <p class="card-text">
                Gender: {{userData.gender}}
              </p>
              <p class="card-text">
                Priority: {{selectedPriority}}
              </p>
            </div>
          </div>
        </div>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      userData: {
        email: '',
        password: '',
        age: '',
        gender: 'Male',
      },
      message: '',
      mailing: [],
      priorities: ['Low', 'Medium', 'High'],
      selectedPriority: 'High',
    };
  },
};
</script>

<style></style>
