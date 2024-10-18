# ServidorLib

**ServidorLib** es una biblioteca de clases en C# que permite abrir un servidor HTTP local para manejar solicitudes de manera sencilla y eficiente. Esta biblioteca es ideal para desarrolladores que necesitan un servidor ligero para pruebas o desarrollo local.

Autor Jose Vinaches.

## Características

- Permite iniciar un servidor HTTP en un puerto específico.
- Maneja solicitudes GET y POST.
- Respuestas personalizables.
- Fácil de integrar en otros proyectos.

## Tecnologías Utilizadas

- C#
- .NET Framework / .NET Core
- Visual Studio

## Instalación

1. Clona el repositorio:
    ```bash
    git clone https://github.com/tu_usuario/ServidorLib.git
    ```
   
2. Navega a la carpeta del proyecto:
    ```bash
    cd ServidorLib
    ```

3. (Opcional) Restaura paquetes de NuGet:
    ```bash
    dotnet restore
    ```

## Uso

Para usar **ServidorLib**, primero debes agregar la referencia a la DLL en tu proyecto. Una vez hecho esto, puedes utilizar la clase `HttpServer` de la siguiente manera:

```csharp
using ServidorLib;

class Program
{
    static void Main(string[] args)
    {
        HttpServer server = new HttpServer(8080); // Crea una instancia del servidor en el puerto 8080
        server.Start(); // Inicia el servidor

        Console.WriteLine("Servidor en ejecución. Presiona cualquier tecla para detenerlo...");
        Console.ReadKey(); // Espera a que el usuario presione una tecla

        server.Stop(); // Detiene el servidor
    }
}
