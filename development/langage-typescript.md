# TypeScript

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- l'intéret de TypeScript dans l'IDE  ✔️
- les types de bases  ✔️
- comment et pourquoi étendre une interface  ✔️
- les classes et les decorators  ✔️

## 💻 J'utilise

### Un exemple personnel commenté  ✔️

/**
	 * Ici Je type les arguments de ma fonction ainsi que les variables à l'intérieur,
	 * cela permet a TS de m'avertir si j'utilise un type non approprié ou différent de celui attendu
	 * **/

	addGrade: async (req: Request, res: Response) => {
		const {
			wilderId,
			skillId,
			grade,
		}: {wilderId: string; skillId: string; grade: number} = req.body;

		try {
			const wilder = await wilders.findOneByOrFail({id: wilderId});

			const skill = await skills.findOneByOrFail({id: skillId});

			await grades.save({
				grade: grade,
				wilderId: wilder.id,
				skillId: skill.id,
			});
			res.send(
				` wilder ${wilder?.name} has been given grade ${grade} in ${skill?.name}`
			);
		} catch (err) {
			console.log(err);
		}
	},
### Utilisation dans un projet  ✔️

[lien github](...)

Description :

### Utilisation en production si applicable ✔️

[lien du projet](...)

Description :

### Utilisation en environement professionnel ✔️

Description :

## 🌐 J'utilise des ressources

### Titre

- lien
- description

## 🚧 Je franchis les obstacles

### Point de blocage ✔️

Description:

Plan d'action : (à valider par le formateur)

- action 1 ❌ / ✔️
- action 2 ❌ / ✔️
- ...

Résolution :

## 📽️ J'en fais la démonstration

- J'ai ecrit un [tutoriel](...) ❌ 
- J'ai fait une [présentation](...) ❌ 
