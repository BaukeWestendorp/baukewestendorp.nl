<script lang="ts">
	import hetDagboekImage from '$lib/img/projects/het_dagboek.jpg';
	import impossibleRoboticsImage from '$lib/img/projects/impossible_robotics.jpg';
</script>

<svelte:head>
	<title>Projecten | Bauke Westendorp</title>
	<meta
		name="description"
		content="Bauke Westendorp werkt mee aan meerdere projecten zoals
        Allround Portraits, Radiant, Linkage en Impossible Robotics."
	/>
</svelte:head>

<article>
	<h1>Projecten</h1>

	<section>
		<div class="header">
			<h2>Het Dagboek</h2>
		</div>
		<img src={hetDagboekImage} alt="Het Dagboek" />
		<p>
			Ter ere van de 80e herdenking van de Slag om Arnhem heeft Stichting Verscholen Verhalen een
			meeslepende filmtheatervoorstelling ontwikkeld genaamd “Het Dagboek”.
		</p>
		<p>
			Voor dit project heb ik op de draaidagen van de filmscènes portretfoto's van alle acteurs én
			behind the scenes foto's gemaakt.
		</p>
		<p>
			Meer informatie:
			<a href="https://www.filmtheatervoorstelling.nl">www.filmtheatervoorstelling.nl</a>
		</p>
	</section>

	<section>
		<div class="header">
			<h2>Allround Portraits</h2>
		</div>
		<p>
			Bij <a href="https://allroundportraits.nl">Allround Portraits</a>
			combineren we onze liefde voor fotografie met op maat gemaakte pakketten. We staan dagelijks klaar
			om de mooiste momenten vast te leggen. Ben jij op zoek naar nieuwe portretfoto's, pasfoto's of
			leuke plaatjes met je partner, hond of familie. Dan ben je bij ons aan het juiste adres.
		</p>
	</section>

	<section>
		<div class="header">
			<h2>Radiant</h2>
		</div>
		<p>
			<a href="https://github.com/BaukeWestendorp/radiant">Radiant</a> is software voor het designen
			van lichtshows. Het is bedoeld om te experimenteren met nieuwe manieren van effecten genereren
			en het procedureel genereren van shows.
		</p>
	</section>

	<section>
		<div class="header">
			<h2>Linkage</h2>
		</div>
		<p>
			<a href="https://github.com/Impossible-Robotics-5412/linkage">Linkage</a> is een experimenteel
			Robot Control System ontworpen om het programmeren van een robot simpel, overzichtelijk en
			toegankelijk te maken voor iedereen. Linkage is bedacht om de overpriced hardware voor
			<a href="https://www.firstinspires.org/robotics/frc">FRC</a> competities te vervangen voor off-season
			evenementen zodat de dure hardware ieder jaar kan worden hergebruikt voor een nieuwe robot.
		</p>
	</section>

	<section>
		<div class="header">
			<h2>Impossible Robotics</h2>
		</div>
		<img src={impossibleRoboticsImage} alt="Impossible Robotics" />
		<p>
			<a href="https://impossiblerobotics.nl">Impossible Robotics</a> is een
			<a href="https://www.firstinspires.org/robotics/frc">FRC</a>,
			<a href="https://first.global">FGC</a> en
			<a href="https://www.firstinspires.org/robotics/ftc">FTC</a>
			robotica team waar ik begin 2019 me bij heb aangesloten als student. Inmiddels ben ik mentor en
			leer ik met plezier jongeren een robot bouwen, programmeren en de teamspirit er in te houden.
		</p>
	</section>
</article>

<style>
	article {
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	section {
		max-width: 42rem;
		margin-bottom: 2rem;
		display: flex;
		flex-direction: column;
		gap: 0.5rem;
	}

	section img {
		width: 100%;
	}

	section:last-child {
		margin-bottom: 0;
	}

	.header {
		display: flex;
		justify-content: space-between;
		align-items: center;

		border-bottom: 1px solid var(--c-accent-secondary);
	}
</style>
