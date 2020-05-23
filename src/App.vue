<template>
  <div class="container">
    <form>
      <div class="row mt-4">
        <div class="col-lg-6 col-md-8 col-sm-12 mx-auto">
          <h1>File a complaint</h1>
          <!-- email -->
          <div class="form-group">
            <label for="email"><b>Email</b></label>
            <input type="email" name="email" id="email" class="form-control" />
          </div>
          <!-- password -->
          <div class="form-group">
            <label for="password"><b>Password</b></label>
            <input
              type="password"
              name="password"
              id="password"
              class="form-control"
            />
          </div>
          <!-- age -->
          <div class="form-group">
            <label for="age"><b>Age</b></label>
            <input type="number" name="age" id="age" class="form-control" />
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
            ></textarea>
          </div>
          <!-- mailing -->
          <div class="form-group">
            <div class="form-check form-check-inline">
              <input class="form-check-input" type="checkbox" id="send_main" />
              <label class="form-check-label" for="send_main"
                ><b>Send Mail</b></label
              >
            </div>
            <div class="form-check form-check-inline">
              <input
                class="form-check-input"
                type="checkbox"
                id="send_infomail"
                value="option2"
              />
              <label class="form-check-label" for="send_infomail"
                ><b>Send Infomail</b></label
              >
            </div>
          </div>
          <!-- gender -->
          <div class="form-group">
            <div class="form-check form-check-inline">
              <input
                class="form-check-input"
                type="radio"
                name="gender"
                id="male"
              />
              <label class="form-check-label" for="male"><b>Male</b></label>
            </div>
            <div class="form-check form-check-inline">
              <input
                class="form-check-input"
                type="radio"
                name="gender"
                id="female"
              />
              <label class="form-check-label" for="female"><b>Female</b></label>
            </div>
          </div>
          <!-- priority -->
          <div class="form-group">
            <label for="priority"><b>Priority</b></label>
            <select class="custom-select" id="priority">
              <option value="low">Low</option>
              <option value="medium">Medium</option>
              <option value="high">High</option>
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
              <p class="card-text">
                Email:
                <hr>
                Password:
                <hr>
                Age:
                <hr>
                Message:
                <hr>
                Mailing:
                <hr>
                Gender:
                <hr>
                Priority:
              </p>
            </div>
          </div>
        </div>
      </div>
    </form>
  </div>
</template>

<script>
export default {};
</script>

<style></style>
