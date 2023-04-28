 <script setup>

      import { ref } from 'vue'
      const nome = ref('');
      const email = ref('');
      const senha = ref('');
      const senha2 = ref('')
      const confirmarUsuario = ref(false);
      const nascimento = ref('');
      const bio = ref('');
      const endereco = ref('');
      const estados = ref('');
      const lingProg = ref('');
      const hobbies = ref('');
      
      </script>
      
      <template>
        <div class="div1">
        <form @submit.prevent="confirmarUsuario=confirma()" class="formulario">
          <div class="menu">
          <p>Nome: </p><input v-model="nome" placeholder="Nome" minlength="3" maxlength="20" required />
          <p>Email: </p><input type="email" v-model="email" placeholder="Email" required />
          <p>Senha: </p><input type="password" v-model="senha" required />
          <p>Confirmação de senha: </p><input type="password" v-model="senha2" required />
          <p>Nascimento: </p><input type="date" name="Data nascimento" id="nascimento" v-model="nascimento"> 
          <p>Cidade: </p><input type="text" v-model="cidade" required />
          <p>Endereço: </p><input type="text" v-model="endereco" required />
         
          
          <p>Estado: </p><select v-model="estados">
            <option value=" Acre">AC</option>
            <option value="Alagoas">AL</option>
            <option value="Amapá">AP</option>
            <option value="Amazonas">AM</option>
            <option value="Bahia">BA</option>
            <option value="Ceará">CE</option>
            <option value="Distrito Federal">DF</option>
            <option value="Espírito Santo">ES</option>
            <option value="Goiás">GO</option>
            <option value="Maranhão">MA</option>
            <option value="Mato Grosso">MT</option>
            <option value="Mato Grosso do Sul">MS</option>
            <option value="Minas Gerais">MG</option>
            <option value="Pará">PA</option>
            <option value="Paraíba">PB</option>
            <option value="Paraná">PR</option>
            <option value="Pernambuco">PE</option>
            <option value="Piauí">PI</option>
            <option value="Rio de Janeiro">RJ</option>
            <option value="Rio Grande do Norte">RN</option>
            <option value="Rio Grande do Sul">RS</option>
            <option value="Rondônia">RO</option>
            <option value="Roraima">RR</option>
            <option value="Santa Catarina">SC</option>
            <option value="São Paulo">SP</option>
            <option value="Sergipe">SE</option>
            <option value="Tocantins">TO</option>
          </select>
          <p>Hobbies: </p><textarea v-model="hobbies" cols="20" rows="5"></textarea>
          <p>Linguagens de programação: </p><textarea v-model="lingProg" cols="20" rows="5"></textarea>
          <p>Biografia: </p><textarea v-model="bio" cols="20" rows="5"></textarea>
          <button type="submit" class="button">Enviar</button>
        </div>
      </form> 
      
      <div v-if="confirmarUsuario" class="formulario2">
        
        <div class="usuario">
          <p>Usúario</p>
          <p>Nome: {{ nome }}</p>
          <p>Email: {{ email }}</p>
          <p>Senha: {{ senha }}</p>
          <p>Data de nascimento: {{ nascimento }}</p>
          <p>Endereço: {{ endereco }}</p>
          <p>Cidade: {{ cidade }}</p>
          <p>Estado: {{ estados }}</p>
          <p>Hobbies: {{ hobbies }}</p>
          <p>Linguagens de programação: {{ lingProg }}</p>
          <p>Biografia: {{ bio }}</p>
        </div>
        
      </div>
      
      </div>
      </template>
      
      <style scoped>
      .formulario{
        color: rgb(115, 184, 245);
          background-color: #0E4459;
          border-radius: 20px;
          margin-left: 23%;
        }
        .formulario2{
        color: rgb(144, 196, 242);
          background-color: #0E4459;
          border-radius: 20px;
          margin-left: 23%;
        }
        .menu{
          margin: 50px 50px 50px 90px;
        
        }
        
        .button{
          font-size: 15px;
          color: rgb(152, 201, 244);
          background-color: #07748d;
          border: solid 1px #3d43e9;
          border-radius: 20px;
          margin: 20px 10px 10px 0px
        }
       
       .div1{
          display: grid;
          grid-template-columns: 50% 50%;
        }
      
       
        .usuario{
          color: rgb(12, 217, 245);
          background-color: #0E4459;
          margin: 10px 60px 60px 100px;
     
        }
       
      
      
      
        </style>
      

      
