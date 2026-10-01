# Component Libraries

Component libraries in the templ ecosystem provide ready-to-use UI elements.

## templUI

![templUI Banner](/img/ecosystem/templui.png)

### About

templUI is the premier UI component library built specifically for templ. It combines the type-safety of Go with the interactivity of Alpine.js and the styling power of Tailwind CSS to create beautiful, responsive web applications.

### Features

- **30+ Ready-made Components**: Buttons, cards, modals, charts, and more
- **Enterprise-Ready**: Built for production with security in mind
- **CSP Compliant**: Works seamlessly with Content Security Policy
- **Type-Safe**: Full Go type system integration and checking
- **Customizable**: Easily adapt to match your brand identity

### Example

```go
import "github.com/axzilla/templui/components"

templ ExamplePage() {
  @components.Button(components.ButtonProps{
    Text: "Click me",
    IconRight: icons.ArrowRight(icons.IconProps{Size: "16"}),
  })
}
```

### Links

- [Documentation](https://templui.io)
- [GitHub](https://github.com/axzilla/templui)
- [Quick Start Template](https://github.com/axzilla/templui-quickstart)

## templ-components

![templ-components Banner](/img/ecosystem/templ-components.png)

### About

templ-components is a server-rendered UI component library built on templ, HTMX, and Tailwind CSS v4. It ships typed Go props, dark mode, CSP nonce support, and ARIA accessibility out of the box, with no client-side JavaScript framework — JavaScript only enhances the server-rendered HTML.

### Features

- **120+ typed components**: Cards, tables, forms, overlays, charts, and a dedicated HTMX package for loading, error, and out-of-band swap helpers
- **Dual-transport wiring**: One typed action spec renders either HTMX attributes or Datastar expressions
- **Dark mode and accessibility**: Every component ships tested dark-mode variants, ARIA roles, and keyboard navigation
- **No framework lock-in**: Pure Go with templ and Tailwind v4 class strings; no Node.js runtime
- **CSP-safe by construction**: Every inline script carries a nonce

### Example

```go
import (
  "github.com/larsartmann/templ-components/display"
  "github.com/larsartmann/templ-components/layout"
)

templ ExamplePage() {
  @layout.Base(layout.DefaultPageProps()) {
    @display.StatCard(display.StatCardProps{
      Label:  "Active users",
      Value:  "1280",
      Change: "+12%",
      Trend:  display.TrendUp,
    })
  }
}
```

### Links

- [Documentation](https://templcomponents.lars.software)
- [GitHub](https://github.com/larsartmann/templ-components)
- [API Reference](https://pkg.go.dev/github.com/larsartmann/templ-components)
