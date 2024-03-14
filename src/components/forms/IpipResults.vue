<template>
	<div class="main">
		<div class="chart-container is-flex is-horizontal-center ">
			<bar-chart 
				v-if="loaded"
				:chart-data="datacollection" 
						:options="options">
			</bar-chart>
		</div>

		<section>
			
			<div class="container">
				<h1 class="title">ΑΝΤΙΛΗΨΗ ΧΩΡΟΥ</h1>
				<p>Μερικά επαγγέλματα που η άσκησή τους προϋποθέτει να λύνεις με ευκολία  τέτοιου είδους προβλήματα: τοπογράφος, πολιτικός μηχανικός, αρχιτέκτων,  σκηνογράφος, ναυπηγός, γραφίστας, διακοσμητής, σχεδιαστής τεχνικού σχεδίου κλπ.</p> 

				<div>
					<div id="emoji-block" class="is-flex is-horizontal-center">
						<figure class="image is-128x128">
							<img class="purple-theme" src="./../../assets/ah.svg" alt="">
						</figure>
					</div>
					<h2 class="is-size-6 has-text-centered has-text-weight-bold">Το σκορ σου: {{ ah_score }} / 100</h2>
				</div>
			</div>

			
			<div class="container">
				<h1 class="title">ΑΡΙΘΜΗΤΙΚΗ ΙΚΑΝΟΤΗΤΑ</h1>
				<p>Μερικά επαγγέλματα που η άσκησή τους προϋποθέτει να έχεις ανεπτυγμένη την αριθμητική ικανότητα: λογιστής, ταμίας, στέλεχος εμπορικών επιχειρήσεων, υπάλληλος ξενοδοχείου, ασφαλιστής, υπάλληλος τραπέζης, έμπορος.</p> 
				<div>
					<div id="emoji-block" class="is-flex is-horizontal-center">
						<figure class="image is-128x128">
							<img class="purple-theme" src="./../../assets/ai.svg" alt="">
						</figure>
					</div>
					<h2 class="is-size-6 has-text-centered has-text-weight-bold">Το σκορ σου: {{ ai_score }} / 100</h2>
				</div>
			</div>
		
			<div class="container">
				<h1 class="title">ΑΦΑΙΡΕΤΙΚΗ ΣΚΕΨΗ</h1>
				<p>Γενικά, η αφαιρετική σκέψη χρειάζεται σε όσους σκέπτονται να ακολουθήσουν μακροχρόνιες σπουδές και να εξασκήσουν επιστημονικά επαγγέλματα.</p> 
				<div>
					<div id="emoji-block" class="is-flex is-horizontal-center">
						<figure class="image is-128x128">
							<img class="purple-theme" src="./../../assets/as.svg" alt="">
						</figure>
					</div>
					<h2 class="is-size-6 has-text-centered has-text-weight-bold">Το σκορ σου: {{ as_score }} / 100</h2>
				</div>
			</div>

			<div class="container">
				<h1 class="title">ΓΛΩΣΣΙΚΗ ΙΚΑΝΟΤΗΤΑ</h1>
				<p>Μερικά επαγγέλματα που η άσκησή τους προϋποθέτει να έχεις αναπτυγμένη γλωσσική ικανότητα: δικηγόρος, δημοσιογράφος, διπλωμάτης, διερμηνέας, δάσκαλος, καθηγητής, ψυχολόγος, ξεναγός, γραμματέας, υπάλληλος γραφείου.</p> 
				<div>
					<div id="emoji-block" class="is-flex is-horizontal-center">
						<figure class="image is-128x128">
							<img class="purple-theme" src="./../../assets/gi.svg" alt="">
						</figure>
					</div>
					<h2 class="is-size-6 has-text-centered has-text-weight-bold">Το σκορ σου: {{ gi_score }} / 100</h2>
				</div>
			</div>

			<div class="container">
			<h1 class="title">ΙΚΑΝΟΤΗΤΑ ΔΙΑΠΡΟΣΩΠΙΚΗΣ ΕΠΑΦΗΣ</h1>
			<p>Μερικά επαγγέλματα που η άσκησή τους προϋποθέτει να έχεις αναπτυγμένη ικανότητα διαπροσωπικής επαφής: γιατρός, νοσοκόμος, καθηγητής, ψυχολόγος, παιδαγωγός, κοινωνικός λειτουργός.</p> 
				<div>
					<div id="emoji-block" class="is-flex is-horizontal-center">
						<figure class="image is-128x128">
							<img class="purple-theme" src="./../../assets/ide.svg" alt="">
						</figure>
					</div>
					<h2 class="is-size-6 has-text-centered has-text-weight-bold">Το σκορ σου: {{ ide_score }} / 100</h2>
				</div>
			</div>

			<div class="container">
			<h1 class="title">ΚΑΤΑΝΟΗΣΗ ΜΗΧΑΝΙΚΩΝ ΚΑΙ ΤΕΧΝΙΚΩΝ ΠΡΟΒΛΗΜΑΤΩΝ</h1>
			<p>Μερικά επαγγέλματα που η άσκησή τους προϋποθέτει να κατανοείς μηχανικά και τεχνικά προβλήματα: ηλεκτρολόγος, μηχανικός, μηχανολόγος, τεχνολόγος κλπ.</p> 
				<div>
					<div id="emoji-block" class="is-flex is-horizontal-center">
						<figure class="image is-128x128">
							<img class="purple-theme" src="./../../assets/kmtp.svg" alt="">
						</figure>
					</div>
					<h2 class="is-size-6 has-text-centered has-text-weight-bold">Το σκορ σου: {{ kmtp_score }} / 100</h2>
				</div>
			</div>

			<div class="container">
			<h1 class="title">ΟΡΓΑΝΩΤΙΚΕΣ ΔΕΞΙΟΤΗΤΕΣ</h1>
			<p>Μερικά επαγγέλματα που η άσκησή τους προϋποθέτει να έχεις ανεπτυγμένη αυτή τη δεξιότητα είναι: συμβολαιογράφος, βιβλιοθηκάριος, λογιστής, διοικητικός υπάλληλος, γραμματέας, δημοσιογράφος, οικονομολόγος, διαφημιστής, διευθυντής ξενοδοχείου κλπ.</p> 
				<div>
					<div id="emoji-block" class="is-flex is-horizontal-center">
						<figure class="image is-128x128">
							<img class="purple-theme" src="./../../assets/od.svg" alt="">
						</figure>
					</div>
					<h2 class="is-size-6 has-text-centered has-text-weight-bold">Το σκορ σου: {{ od_score }} / 100</h2>
				</div>
			</div>

			<div class="container">
			<h1 class="title">ΕΥΕΛΙΞΙΑ - ΠΡΟΣΑΡΜΟΣΤΙΚΟΤΗΤΑ</h1>
			<p>Μερικά επαγγέλματα που η άσκησή τους προϋποθέτει να έχεις ανεπτυγμένη αυτή τη δεξιότητα είναι: Υπάλληλος Τουριστικού Γραφείο, Τουριστικός Αντιπρόσωπος, Πωλητής Λιανικής, Στέλεχος Εξαγωγικού Εμπορίου.</p> 
				<div>
					<div id="emoji-block" class="is-flex is-horizontal-center">
						<figure class="image is-128x128">
							<img class="purple-theme" src="./../../assets/ep.svg" alt="">
						</figure>
					</div>
					<h2 class="is-size-6 has-text-centered has-text-weight-bold">Το σκορ σου: {{ ep_score }} / 100</h2>
				</div>
			</div>

			<div class="container">
			<h1 class="title">ΣΩΜΑΤΙΚΗ ΑΝΤΟΧΗ ΚΑΙ ΔΥΝΑΜΗ</h1>
			<p>Μερικά επαγγέλματα που η άσκησή τους προϋποθέτει να έχεις ανεπτυγμένη αυτή τη δεξιότητα είναι: Στέλεχος Αποθήκης, Τεχνικός Παραγωγής, Τεχνικός Συντήρησης Εγκαταστάσεων, Σκίπερ.</p> 
				<div>
					<div id="emoji-block" class="is-flex is-horizontal-center">
						<figure class="image is-128x128">
							<img class="purple-theme" src="./../../assets/sad.svg" alt="">
						</figure>
					</div>
					<h2 class="is-size-6 has-text-centered has-text-weight-bold">Το σκορ σου: {{ sad_score }} / 100</h2>
				</div>
			</div>

			<div class="container">
			<h1 class="title">ΤΑΧΥΤΗΤΑ ΚΑΙ ΑΚΡΙΒΕΙΑ</h1>
			<p>Μερικά επαγγέλματα που η άσκησή τους προϋποθέτει να έχεις ανεπτυγμένη αυτή τη δεξιότητα είναι:  Υπάλληλος Γραφείου, Βοηθός Λογιστή, Ταμίας, Στέλεχος Διαχείρισης Εφοδιαστικής Αλυσίδας, Στέλεχος Διαχείρισης Ασφάλειας Τροφίμων.</p> 
				<div>
					<div id="emoji-block" class="is-flex is-horizontal-center">
						<figure class="image is-128x128">
							<img class="purple-theme" src="./../../assets/ta.svg" alt="">
						</figure>
					</div>
					<h2 class="is-size-6 has-text-centered has-text-weight-bold">Το σκορ σου: {{ ta_score }} / 100</h2>
				</div>
			</div>

			<div class="container">
			<h1 class="title">ΦΑΝΤΑΣΙΑ - ΔΗΜΙΟΥΡΓΙΚΟΤΗΤΑ</h1>
			<p>Μερικά επαγγέλματα που η άσκησή τους προϋποθέτει να έχεις ανεπτυγμένη αυτή τη δεξιότητα είναι: Διακοσμητής, Ειδικός Σχεδιασμού Ιστοσελίδων και Εφαρμογών, Σεφ, Ζαχαροπλάστης, Μεταποιητής Ενδυμάτων.</p> 
				<div>
					<div id="emoji-block" class="is-flex is-horizontal-center">
						<figure class="image is-128x128">
							<img class="purple-theme" src="./../../assets/fd.svg" alt="">
						</figure>
					</div>
					<h2 class="is-size-6 has-text-centered has-text-weight-bold">Το σκορ σου: {{ fd_score }} / 100</h2>
				</div>
			</div>

			<div class="container">
			<h1 class="title">ΤΕΧΝΟΛΟΓΙΑ ΤΗΣ ΠΛΗΡΟΦΟΡΙΑΣ</h1>
			<p>Μερικά επαγγέλματα που η άσκησή τους προϋποθέτει να έχεις ανεπτυγμένη αυτή τη δεξιότητα είναι:  Υπάλληλος Γραφείου, Προγραμματιστής, Ειδικός Σχεδιασμού Ιστοσελίδων και Εφαρμογών.</p> 
				<div>
					<div id="emoji-block" class="is-flex is-horizontal-center">
						<figure class="image is-128x128">
							<img class="purple-theme" src="./../../assets/tp.svg" alt="">
						</figure>
					</div>
					<h2 class="is-size-6 has-text-centered has-text-weight-bold">Το σκορ σου: {{ tp_score }} / 100</h2>
				</div>
			</div>
		</section>

		<!-- <section>
			<i>Πηγή: <a href="https://jrounds.weebly.com/onet-interest-profiler-short-form.html">O*NET Interest Profiler Short Form</a></i>
		</section> -->

	</div>
</template>

<script>

import IpipChart from './IpipChart.vue'
// import IpipReferenceData from '../../assets/sample_features.json'

var maximumValue = 5;

export default {
	components: {
		'bar-chart': IpipChart
	},
	props: ['formName'],
	data() {
    return {
    //   ipipReference: IpipReferenceData,
			formData: [],
			datacollection : null, 
			loaded: false,
			options:
			{
				scales: {
					yAxes: [
						{
							ticks: {
								suggestedMin:20,
								suggestedMax:100,
								stepSize: 20
							}
						}
					]
				},
				responsive: true,
				maintainAspectRatio: false
			},
		
		}
	},
	async mounted () {
		this.fetchData()
	},
	methods: {
		fetchData() {
			let retrievedFormData = localStorage.getItem('formData');
			this.formData = JSON.parse(retrievedFormData);
			this.fillData();
			this.loaded = true;

			// const database = 'https://open-bigfive-ipip100.firebaseio.com/ipip100/';
			// const id = this.formName;
			// const query = database + id + '.json';
			// this.$http.get(query)
			// 	.then(response => {
			// 		return response.json()
			// 	})
			// 	.then(data => {
			// 		this.formData = data;
			// 		this.fillData();
			// 		this.loaded = true;
			// 	})
		},
		fillData() {
			this.datacollection = {
				labels: ['ΑΝΤΙΛΗΨΗ ΧΩΡΟΥ', 'ΑΡΙΘΜΗΤΙΚΗ ΙΚΑΝΟΤΗΤΑ', 'ΑΦΑΙΡΕΤΙΚΗ ΣΚΕΨΗ',
					'ΓΛΩΣΣΙΚΗ ΙΚΑΝΟΤΗΤΑ', 'ΙΚΑΝΟΤΗΤΑ ΔΙΑΠΡΟΣΩΠΙΚΗΣ ΕΠΑΦΗΣ', 'ΔΙΟΙΚΗΤΙΚΟ ΚΑΙ ΕΠΙΧΕΙΡΗΜΑΤΙΚΟ ΠΝΕΥΜΑ', 'ΚΑΤΑΝΟΗΣΗ ΜΗΧΑΝΙΚΩΝ ΚΑΙ ΤΕΧΝΙΚΩΝ ΠΡΟΒΛΗΜΑΤΩΝ', 'ΟΡΓΑΝΩΤΙΚΕΣ ΔΕΞΙΟΤΗΤΕΣ', 'ΕΥΕΛΙΞΙΑ ΠΡΟΣΑΡΜΟΣΤΙΚΟΤΗΤΑ', 'ΣΩΜΑΤΙΚΗ ΑΝΤΟΧΗ ΚΑΙ ΔΥΝΑΜΗ', 'ΤΑΧΥΤΗΤΑ ΚΑΙ ΑΚΡΙΒΕΙΑ', 'ΦΑΝΤΑΣΙΑ ΔΗΜΙΟΥΡΓΙΚΟΤΗΤΑ', 'ΤΕΧΝΟΛΟΓΙΑ ΤΗΣ ΠΛΗΡΟΦΟΡΙΑΣ'],
				datasets: [
					{
						label: 'Το σκορ σου',
						backgroundColor: '#7957d5',
						data: [this.ah_score, this.ai_score, this.as_score,
								this.gi_score, this.ide_score, this.dep_score,
								this.kmtp_score, this.od_score, this.ep_score,
								this.sad_score, this.ta_score, this.fd_score, this.tp_score]
					},
			// 		{
			// 			label: 'Μέσος όρος ερωτηθέντων',
			// 			backgroundColor: 'hsl(48, 100%, 67%)',
            // data: [this.ipipReference.f_one.mean,
            //   this.ipipReference.f_two.mean,
            //   this.ipipReference.f_three.mean,
            //   this.ipipReference.f_four.mean,
            //   this.ipipReference.f_five.mean]
			// 		}
				]
			}
		},
		getMultiplier(factor)
		{
			return 100 /
				(this.formData.filter(item => item.factor == factor).length
					* maximumValue)
		},
		getScore(factor)
		{
			return Math.round(this.formData
				.filter(item => item.factor == factor)
				.reduce( (Sum, item) => parseInt(item.value,10) + Sum, 0) * this.getMultiplier(factor))
		}
	},
	computed: {
		ah_score() {
			return this.getScore('ΑΝΤΙΛΗΨΗ ΧΩΡΟΥ')
		},
		ai_score() {
			return this.getScore('ΑΡΙΘΜΗΤΙΚΗ ΙΚΑΝΟΤΗΤΑ')
		},
		as_score() {
			return this.getScore('ΑΦΑΙΡΕΤΙΚΗ ΣΚΕΨΗ')
		},
		gi_score() {
			return this.getScore('ΓΛΩΣΣΙΚΗ ΙΚΑΝΟΤΗΤΑ')
		},
		ide_score() {
			return this.getScore('ΙΚΑΝΟΤΗΤΑ ΔΙΑΠΡΟΣΩΠΙΚΗΣ ΕΠΑΦΗΣ')
		},
		dep_score() {
			return this.getScore('ΔΙΟΙΚΗΤΙΚΟ ΚΑΙ ΕΠΙΧΕΙΡΗΜΑΤΙΚΟ ΠΝΕΥΜΑ')
		},
		kmtp_score() {
			return this.getScore('ΚΑΤΑΝΟΗΣΗ ΜΗΧΑΝΙΚΩΝ ΚΑΙ ΤΕΧΝΙΚΩΝ ΠΡΟΒΛΗΜΑΤΩΝ')
		},
		od_score() {
			return this.getScore('ΟΡΓΑΝΩΤΙΚΕΣ ΔΕΞΙΟΤΗΤΕΣ')
		},
		ep_score() {
			return this.getScore('ΕΥΕΛΙΞΙΑ ΠΡΟΣΑΡΜΟΣΤΙΚΟΤΗΤΑ')
		},
		sad_score() {
			return this.getScore('ΣΩΜΑΤΙΚΗ ΑΝΤΟΧΗ ΚΑΙ ΔΥΝΑΜΗ')
		},
		ta_score() {
			return this.getScore('ΤΑΧΥΤΗΤΑ ΚΑΙ ΑΚΡΙΒΕΙΑ')
		},
		fd_score() {
			return this.getScore('ΦΑΝΤΑΣΙΑ ΔΗΜΙΟΥΡΓΙΚΟΤΗΤΑ')
		},
		tp_score() {
			return this.getScore('ΤΕΧΝΟΛΟΓΙΑ ΤΗΣ ΠΛΗΡΟΦΟΡΙΑΣ')
		}
	}
}

</script>

<style scoped>
.main {
	margin-top:30px;
}

.is-horizontal-center {
	justify-content: center;
}

#emoji-block {
	margin-top:2em;
}

.main div.container {
	padding-top: 30px;
}

.purple-theme {
	filter: brightness(0) saturate(100%) invert(54%) sepia(79%) saturate(5539%) hue-rotate(236deg) brightness(89%) contrast(87%);
}
</style>
