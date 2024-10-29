# Discos

## Configuración de fstab

Este documento detalla cómo identificar discos en Unix y qué configuraciones realizar de manera manual en el archivo `fstab`.
> Nota: fstab es un archivo de configuración que especifica cómo montar dispositivos de almacenamiento en el sistema Unix.

### Cómo identificar un disco?

```bash
# Lista los bloques disponibles en el sistema.
lsblk
```

Se espera algo similar a:

```bash
    NAME   MAJ:MIN RM   SIZE RO TYPE MOUNTPOINTS
sda      8:0    0 465.8G  0 disk 
└─sda1   8:1    0 465.8G  0 part /mnt/disco_secundario
sdb      8:16   0 223.6G  0 disk 
├─sdb1   8:17   0   600M  0 part /boot/efi
├─sdb2   8:18   0     1G  0 part /boot
└─sdb3   8:19   0   222G  0 part /home
                                 /
zram0  252:0    0     8G  0 disk [SWAP]
```

### Cómo editar el archivo /etc/fstab?

```bash
# Editar archivo con permisos elevados usando nano
sudo nano /etc/fstab 
```

### Cuál es el formato a seguir?

> DEVICE | DIR | TYPE | OPTIONS | DUMP | FSCK

**DEVICE**: Identificacion del bloque, (p. ej., /dev/sda1, UUID=..., LABEL=...).

**DIR**: Es el directorio donde se montará el dispositivo.

**TYPE**: Tipo de sistema de archivo, (p. j., ext4, ntfs, nfs, vfat, swap, xfs, etc.).

**OPS**: Opciones de montaje.

**DUMP**: Es una opción para el comando dump que determina la frecuencia de respaldo: 0: No respaldar, 1: Respaldo completo, 2: Respaldo incremental.

**FSCK**: Es el orden en que se ejecuta la comprobación del sistema de archivos con fsck al iniciar el sistema: 0: No comprobar., 1: Comprobar primero (/), 2: Comprobar despues del sistema raiz.

### ¿Qué OPS tengo disponibles?

Algunas opciones comunes son:

**defaults**: Montaje con los permisos predeterminados.

**rw**: Montaje con permisos de lectura y escritura.

**ro**: Montaje con permisos de solo lectura.

**async**: Operaciones de entrada/salida asíncronas.

**sync**: Operaciones de entrada/salida síncronas.

**auto**: Montaje automático al iniciar el sistema.

**noauto**: No montar automáticamente al iniciar el sistema.

**exec**: Permitir la ejecución de archivos en el disco.

**noexec**: No permitir la ejecución de archivos en el disco.

**dev**: Permitir el acceso a dispositivos especiales en el disco.

**nodev**: No permitir el acceso a dispositivos especiales en el disco.

**uid**: Establecer el propietario del disco.

**gid**: Establecer el grupo propietario del disco.

**umask**: Establecer la máscara de permisos para el disco.

**x-gvfs-show**: Mostrar el disco en la interfaz gráfica (GVFS).

## Cómo configurar un disco por UUID

- Obetener UUID:

```bash
sudo bkid /dev/sd[xn]
```

Crear directorio donde se montara el disco:

```bash
mkdir /mnt/[disco_secundario]
```

Editar el archivo /etc/fstab:

```bash
sudo nano /etc/fstab
```

Cargar la nueva configuracion del archivo fstab

```bash
sudo mount -a
```

> Si necesitas ver el disco desde la interfaz, necesitas agregar la opción `x-gvfs-show` en el fstab, ya que Nautilus, por defecto, muestra únicamente lo que está en `/media`.
