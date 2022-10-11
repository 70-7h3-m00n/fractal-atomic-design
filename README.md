# Fractal Atomic Design

## Universal items

### Files example

```
|__ types.ts
|__ utils.ts
|__ constants.ts
```

### Directories example

```
|__ types
  |__ [typeName].ts
  |__ index.ts

|__ utils
  |__ [utilName].ts
  |__ index.ts

|__ constants
  |__ [constantName].ts
  |__ index.ts
```

## Atomic componnets

```
|__ components
  |__ atoms
    |__ [atomName].tsx
      or
    |__ [atomName]
      |__ component.tsx
      |__ style.models.scss
      |__ [universal items] (if needed)
      |__ index.ts
    |__ index.ts

  |__ molecules
    |__ [moleculeName].tsx
      or
    |__ [moleculeName]
      |__ component.tsx
      |__ style.models.scss
      |__ [universal items] (if needed)
      |__ index.ts
    |__ index.ts

  |__ organisms
    |__ [organismName].tsx
      or
    |__ [organismName]
      |__ component.tsx
      |__ style.models.scss
      |__ [universal items] (if needed)
      |__ index.ts
    |__ index.ts

  |__ index.ts
```

## General project structure

```
|__ modules
  |__ [moduleName]
    |__ widgets
      |__ [widgetName].tsx
        or
      |__ [widgetName]
        |__ widget.tsx
        |__ style.models.scss
        |__ [universal items] (if needed)
        |__ [atomic components] (if needed)
        |__ index.ts
        ...
      |__ index.ts

    |__ services
      |__ [servicesName]
        |__ api.ts
         or
        |__ api
          |__ [apiName].ts
          |__ index.ts

        |__ hooks.ts (if needed)
          or
        |__ hooks
          |__ [hookName].ts
          |__ index.ts

        |__ getServerSideProps.ts (if needed)
            or
        |__ getServerSideProps
          |__ [getServerSidePropName].ts
          |__ index.ts

        |__ getStaticProps (if needed)
          or
        |__ getStaticProps
          |__ [getStaticPropsName].ts
          |__ index.ts

        |__ contexts.ts (if needed)
          or
        |__ contexts
          |__ [contextName].ts
          |__ index.ts

        |__ index.js
         ...

    |__ [universal items]
    |__ [atomic components] (if needed)
    |__ index.js

|__ templates
  |__ [templateName].tsx
    or
  |__ [templateName]
    |__ template.tsx
    |__ style.models.scss
    |__ [universal items] (if needed)
    |__ [atomic component] (if needed)
        |__ index.ts

|__ pages
  |__ [pageName].ts
      or
      [parentPageName]
        |__ [pageName].ts

    ...
|__ [universal items] (if needed)
|__ [atomic components] (if needed)
|__ [and other]
```

## Import/export

`index.ts` - transport file that connects other files. `/pages/index.tsx` is an exception

### Example

```ts
export { TemplateCt } from "./components";
export { LoginWt, ConfirmWt } from "./widgets";
```

### Symantic postfixes

- `[componentName]Ct.tsx`

- `[wingetName]Wt.tsx`

- `[layoutName]Lt.tsx`

- `[serviceName]Sc.tsx`

- `[contextName]Cxt.tsx`

- `[propviderContextName]PrCxt.tsx`

- `[controllerName]Clr.tsx`

- `[controllerName]Sc.tsx`

- `[requestDTOName]RqDTO.tsx`

- `[bodyRequestDTOName]BodyRqDTO.tsx`

- `[paramsRequestDTOName]ParamsRqDTO.tsx`

- `[queryRequestDTOName]QueryRqDTO.tsx`

- `[responseDTOName]RsDTO.tsx`
