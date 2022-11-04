**Created:** Friday 04, November 2022, at 16:44.
**Status:** #note 
**Tags:**  [[Módulos en Angular]]

# Componentes en Angular

Los componentes son básicamente las propias clases, solo que están "decoradas" como el atributo `@Component`.
Teniendo un componente, podemos aplicarle ciertas propiedades, por ejemplo:
- **`template`(s) and `selector`(s):** la propiedad `selector` nos permite implementar HTML reemplazando lo que se encuentre en el HTML file (en el momento en que cargue Angular) por el contenido HTML de la plantilla `template` (esta template se puede aplicar interna o externamente, por medio de una referencia utilizando `templateUrl`).
``` ts
@Component({
	selector: 'my-selector',
	template: `
		<h1>Hello World</h1>
		<p>Hey {{user}}! Notice that we have to put this beetwen '``' to make it multiline!</p>
	`
})
export class DemoComponent{
	user:string = "Nassim";
}
```
La salida será la siguiente:
``` markdown
# Hello World
Hey Nassim! Notice that we have to put this beetwen '``' to make it multiline!
```

## Interpolation

### 1-Way Data Binding:
Como podemos notar, encapsulando nuestro string *user* en `{{}}`, atamos su valor de salida como entrada. Esto es llamado **1-Way Data Binding**, y se puede realizar de forma inversa utilizando `[]`. A continuación vemos un ejemplo:
```ts
@Component({
	selector: 'my-selector',
	template: '<button [disabled]="dataNotChanged">Save</button>'
})
export class DemoComponent {
	dataNotChanged = true;
}
```
Aquí, podemos observar que inicialmente el botón estará desactivado ya que refiere a *dataNotChanged* que es verdadero. Luego, si reasignamos `false` a *dataNotChanged*, veremos que el botón ya no estará desactivado.
```ad-cite
"1-Way Data Binding can reflect the model to the view, but not both ways" 
```


### 2-Way Data Binding:

---
## References:
- <iframe title="Angular + Typescript = Powerful Web Apps" src="https://www.youtube.com/embed/0akfix87OdE?feature=oembed" height="113" width="200" allowfullscreen="" allow="fullscreen" style="aspect-ratio: 16 / 9; width: 100%; height: 100%;"></iframe>