# useForm

Ejemplo

    **En App.js**
```
    import { ViewportProvider } from './hooks/useViewport';

    export default function App() {
    return (
        <ViewportProvider>
            <MyComponent />
        </ViewportProvider>
    );
    }
```
    **En My Component**
```
    import { useViewport } from '../../hooks/useViewport';

    const MyComponent = () => {
        const { width, height } = useViewport();
        const breakpoint = 620;

        return width < breakpoint ? <MobileComponent /> : <DesktopComponent />;
    };
```
