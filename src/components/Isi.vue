<template>
    <div>
        <v-app-bar app color="light-blue" class="mainHeader" flat>
            <v-toolbar-title>Bernadette Chrestella</v-toolbar-title>
            <v-toolbar-items>
                <v-btn text><router-link tag="btn" to="/isi" id="home">Home</router-link></v-btn>
                <v-btn text><router-link tag="btn" to="/isi" id="about-me">About Me</router-link></v-btn>
                <v-btn text><router-link tag="btn" to="/isi" id="work-experience">Work Experiences</router-link></v-btn>
                <v-btn text><router-link tag="btn" to="/isi" id="education">Education</router-link></v-btn>
                <v-btn text><router-link tag="btn" to="/isi" id="skills">Skills</router-link></v-btn>
                <v-btn text><router-link tag="btn" to="/isi" id="contact-me">Contact Me</router-link></v-btn>
                <v-btn text><router-link tag="btn" to="/isi" id="footer">Footer</router-link></v-btn>
            </v-toolbar-items>
        </v-app-bar>
        <br />

        <v-container>
        <v-row wrap class="d-flex align-start mb-6">
            <v-col cols="5">
                <section class="text-center" id="profile">
                    <v-img
                    :src="require('../assets/BernadetteChrestella.jpg')"
                    contain
                    height="150"/>
                    <h1>Bernadette Chrestella</h1>
                    <h5 class="h5">Jalan Tahiti, RT 02, Rw02, Bintuni Timur, Bintuni, Papua Barat</h5>
                    <h5 class="h5">bernadettechrestella@gmail.com</h5>
                    <h5 class="h5">081248002829</h5>

                    <ul class="list-inline">
                        <i class="fab fa-linkedin"></i>
                        <li class="list-inline-item"><a href="https://www.linkedin.com/in/bernadette-chrestella-2785b6106/" target="_blank">LinkedIn</a></li>
                        <i class="fab fa-instagram-square"></i>
                        <li class="list-inline-item"><a href="https://www.instagram.com/bernadette.chrestella/" target="_blank">Instagram</a></li>
                        <i class="fab fa-github-square"></i>
                        <li class="list-inline-item"><a href="https://github.com/bernadettechrestella/" target="_blank">Github</a></li>
                    </ul>
                </section>
            </v-col>
            <v-col>
                <section id="about-me">
                    <h1 class="p-3 mb-2 bg-info text-dark"><i class="fas fa-user"></i> About Me</h1>
                    <v-divider></v-divider>
                    <p class="text-center">Nama panggilan saya Stella. Saya adalah alumni Universitas Sanata Dharma yang lulus di tahun 2020. Saya mengambil jurusan Informatika. Saya adalah pribadi yang tertarik dengan tantangan berupa hal-hal baru yang dapat dipelajari.</p>
                </section><br>

                <section id="education">
                    <h1 class="p-3 mb-2 bg-info text-dark"><i class="fas fa-user-graduate"></i> Education</h1>
                    <v-divider></v-divider>
                    <h4  class="text-center">Universitas Sanata Dharma</h4>
                    <h5  class="text-center">Informatika</h5>
                    <h5  class="text-center">2016-2020</h5>
                </section><br>
                                                    
                <section id="work-experience">
                    <h1 class="p-3 mb-2 bg-info text-dark"><i class="fas fa-briefcase"></i> Work Experience</h1><br>
                    <v-divider></v-divider>
                    <v-simple-table>
                        <template v-slot:default>
                            <thead>
                                <tr>
                                    <th class="text-left">Company</th>
                                    <th class="text-left">Role</th>
                                    <th class="text-left">Status</th>
                                    <th class="text-left">Period</th>
                                </tr>
                            </thead>
                            <tbody>
                                <tr>
                                    <td>You Want Coffe Cafe</td>
                                    <td>Barista</td>
                                    <td>Part Time</td>
                                    <td>July-August 2019</td>
                                </tr>
                            </tbody>
                        </template>
                    </v-simple-table>
                    <br />
                </section>

                <section id="skills">
                    <h1 class="p-3 mb-2 bg-info text-dark"><i class="fas fa-cogs"></i> Skills</h1>
                    <v-divider></v-divider>
                    <br>
                    <ol class="row align-items-start">
                        <div class="col">
                            <li><a>Java Programming</a></li>
                            <li><a>HTML</a></li>
                            <li><a>CSS</a></li>
                            <li><a>JavaScript</a></li>
                            <li><a>Mikrotik</a></li>
                            <li><a>Cisco</a></li>
                            <li><a>Core System Administration</a></li>
                            <li><a>Adobe Illustrator</a></li>
                        </div>
                    </ol>
                </section>
            </v-col>
        </v-row>

        <section id="contact-me">
        <h1 class="p-3 mb-2 bg-info text-dark"><i class="fas fa-envelope"></i> Contact Me</h1><br />
        <v-divider></v-divider>
            <v-form v-model="valid">
                <v-container>
                    <v-row>
                        <v-col cols="12" md="4">
                            <v-text-field
                                v-model="firstname"
                                :rules="nameRules"
                                :counter="15"
                                label="First Name"
                                required>
                            </v-text-field>
                        </v-col>
                        <v-col cols="12" md="4">
                            <v-text-field
                                v-model="lastname"
                                :rules="nameRules"
                                :counter="15"
                                label="Last Name"
                                required>
                            </v-text-field>
                        </v-col>
                        <v-col cols="12" md="4">
                            <v-text-field
                                v-model="email"
                                :rules="emailRules"
                                label="E-mail"
                                required>
                            </v-text-field>
                        </v-col>
                    </v-row>
                </v-container>
            </v-form>
            <v-container id="dropdown-example-3">
                <v-overflow-btn
                    class="my-2"
                    :items="dropdown_edit"
                    label="Select your country"
                    counter
                    item-value="text">
                </v-overflow-btn>
            </v-container>
            <v-textarea
                v-model="message"
                auto-grow
                filled
                color="white"
                label="Write your messages here"
                rows="1">
            </v-textarea>
            <v-btn
                text
                @click="$refs.form.reset()">
                Clear
            </v-btn>
            <v-btn
                :loading="isLoading"
                class="black--text"
                color="white"
                depressed>
                Submit
            </v-btn>
        </section>
        </v-container>

        <v-footer padless color="blue" class="footer">
            <v-col
            class="text-center"
            cols="12"
            >
            {{ new Date().getFullYear() }} — <strong>Bernadette Chrestella</strong>
            </v-col>
        </v-footer>
    </div>
</template>

<script>
export default {
    name: "Isi",
    data: () => ({
        valid: false,
        firstname: '',
        lastname: '',
        nameRules: [
            v => !!v || 'Name is required',
            v => v.length <= 15 || 'name must be less than 15 characters'
        ],
        email: '',
        emailRules: [
            v => !!v || 'Email is required',
            v => /.+@.+/.test(v) || 'Email must be valid'
        ],
        dropdown_edit: [
            {text: 'Indonesia'},
            {text: 'USA'},
            {text: 'Canada'},
        ]
    }),
}
</script>