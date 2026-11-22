# humano

Una skill para Claude que reescribe tus textos de negocio en español (correos, mensajes de WhatsApp, descripciones
de servicios, posts) para que suenen escritos por una persona y no por una IA, **sin cambiar ningún dato**.

¿Usas ChatGPT, Gemini u otra IA? Copia el prompt de [`prompt.md`](prompt.md): hace lo mismo.

## Antes y después

> **Antes (ChatGPT):** Sabemos que entre el trabajo, el estudio y los compromisos de la semana, encontrar un espacio
> para ir al odontólogo puede ser difícil. Por eso, queremos darte más opciones para cuidar tu sonrisa.
>
> **Después (/humano):** Desde el 1 de diciembre también abrimos los sábados, de 8 a.m. a 1 p.m.

Probada con textos escritos por ChatGPT (detector ZeroGPT, gratis):

| Texto | Antes | Con /humano |
|---|---|---|
| Correo para clientes de un consultorio | 70 % IA | 0 % |
| Descripción de un servicio | 30 % IA | 0 % |

Y en todos, los mismos datos: fechas, horarios, precios y condiciones.

## Cómo instalarla

**En claude.ai o la app de Claude:** descarga [`humano.zip`](https://github.com/tigermendez/humano/releases/latest),
ve a Configuración → Capacidades → Skills y súbelo. Después escribe `/humano` en cualquier chat y pega tu texto.

**En Claude Code:**

```bash
git clone https://github.com/tigermendez/humano ~/.claude/skills/humano-repo && ln -s ~/.claude/skills/humano-repo/humano ~/.claude/skills/humano
```

## Qué hace

- Quita lo que suena a IA en español: "Sabemos que…", "Nos complace anunciar…", "No es solo X, es Y", "llevar al
  siguiente nivel", todo de a tres, exclamaciones y rayas por todas partes, asuntos de folleto.
- Deja igual las fechas, horarios, precios, nombres, enlaces y condiciones. No inventa nada.
- Respeta el tú o el usted del original, y el largo puede bajar pero no subir.

Un detector de IA no es una prueba de nada: lo que importa es que tu cliente lea algo que suena a ti.

## Créditos

Hecha por [Tiger Mendez](https://tigermendez.com). Basada en [blader/humanizer](https://github.com/blader/humanizer)
(MIT), que a su vez se basa en la guía de Wikipedia
["Signs of AI writing"](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing). Licencia MIT.

---

**English:** A Claude skill that rewrites Spanish business text (emails, WhatsApp messages, service descriptions) so
it reads like a person wrote it, without changing any facts. Based on blader/humanizer (MIT).
