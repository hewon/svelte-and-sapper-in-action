<script>
  let password = '';
  let username = '';

  const login = () => alert('You pressed Login.');
  const signup = () => alert('You pressed Signup.');
</script>

<section>
  <form on:submit|preventDefault={login}> <!-- |preventDefault 로 데이터 전송을 막음-->
    <label>
      Username
      <input required bind:value={username} /> <!-- required 속성-->
    </label>
    <label>
      Password
      <input type="password" required bind:value={password} />
    </label>
    <div class="buttons">
      <button>Login</button>
      <!-- ▲ 버튼 요소의 기본형은 submit이다( type="submit" ). 
           폼에  단하나의 전송 버튼만 만들기 위해 명시적으로 type을 button으로 지정 ▼ -->
      <button type="button" on:click={signup}>Sign Up</button> 
    </div>
  </form>
</section>

<style>
  .buttons {
    display: flex;
    justify-content: space-between;

    font-size: 1.5rem;
    margin-top: 1rem;
  }

  form {
    display: inline-block;
  }

  input {
    display: block;
    margin-top: 0.3rem;
  }

  label {
    color: white;
    display: block;
    font-size: 1.5rem;
    margin-top: 0.5rem;
  }
</style>
