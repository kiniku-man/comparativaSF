# Tabla Comparativa de Sistemas de Archivos

| Característica | FAT32 | NTFS | exFAT | ext3 | ext4 | Btrfs | XFS |
|----------------|-------|------|-------|------|------|-------|-----|
| **Desarrollador** | Microsoft | Microsoft | Microsoft | Stephen Tweedie | Theodore Ts'o | Oracle | SGI |
| **Año de lanzamiento** | 1996 | 1993 | 2006 | 2001 | 2008 | 2009 | 1994 |
| **Sistemas operativos** | Multiplataforma | Windows, Linux, macOS (solo lectura) | Multiplataforma | Linux | Linux | Linux | Linux, Unix |
| **Tamaño máximo de archivo** | 4 GB | 16 EB | 16 EB | 2 TB | 16 TB | 16 EB | 8 EB |
| **Tamaño máximo de volumen** | 2 TB | 16 EB | 64 ZB | 32 TB | 1 EB | 16 EB | 8 EB |
| **Tamaño máximo de nombre** | 255 chars | 255 chars | 255 chars | 255 bytes | 255 bytes | 255 chars | 255 chars |
| **Caracteres permitidos** | Unicode (UTF-16) | Unicode (UTF-16) | Unicode (UTF-16) | Cualquiera excepto / y null | Cualquiera excepto / y null | Cualquiera excepto / y null | Cualquiera excepto / y null |
| **Journaling** | No | Sí | No | Sí | Sí | Sí | Sí |
| **Compresión** | No | Sí | No | No | No | Sí | No |
| **Cifrado** | No | EFS | No | No | No | Sí | No |
| **Snapshots** | No | VSS (Volume Shadow Copy) | No | No | No | Sí | Sí |
| **Deduplicación** | No | No | No | No | No | Sí | No |
| **Copy-on-Write** | No | No | No | No | No | Sí | No |
| **Checksums** | No | No | No | No | No | Sí (datos y metadatos) | Sí (metadatos) |
| **Subvolúmenes** | No | No | No | No | No | Sí | No |
| **Fragmentación** | Alta | Media | Media | Baja | Baja | Muy baja | Muy baja |
| **Rendimiento con archivos pequeños** | Regular | Bueno | Bueno | Bueno | Bueno | Excelente | Excelente |
| **Rendimiento con archivos grandes** | Pobre | Excelente | Excelente | Bueno | Excelente | Excelente | Excelente |
| **Tolerancia a fallos** | Baja | Alta (auto-reparación) | Media | Media (con journaling) | Alta (con journaling) | Muy alta (auto-reparación) | Alta |
| **Uso recomendado** | Dispositivos USB, cámaras, compatibilidad multiplataforma | Discos del sistema Windows, discos internos | Discos USB grandes, tarjetas SD | Sistemas Linux antiguos | Sistemas Linux generales | Sistemas con alta disponibilidad, servidores | Servidores de alto rendimiento, grandes archivos |
| **Ventajas principales** | Compatibilidad universal, simple | Seguridad, estabilidad, características avanzadas | Sin límites FAT32, buena compatibilidad | Estable, probado en el tiempo | Mejoras sobre ext3, buen equilibrio | Características avanzadas, flexibilidad | Alto rendimiento, escalabilidad |
| **Desventajas principales** | Límite 4GB por archivo, sin journaling | Complejidad, limitada compatibilidad multiplataforma | No journaling, menos compatible que FAT32 | Límites de tamaño, menos eficiente que ext4 | Menos características que sistemas modernos | Complejidad, en desarrollo | Menos flexible que Btrfs |

## Resumen de Usos Prácticos:

- **FAT32**: Ideal para unidades USB pequeñas, cámaras digitales y máxima compatibilidad entre dispositivos
- **NTFS**: Perfecto para discos del sistema Windows y almacenamiento interno
- **exFAT**: Mejor opción para unidades USB grandes y tarjetas SD modernas
- **ext4**: Excelente opción general para sistemas Linux
- **Btrfs**: Ideal para servidores que necesitan snapshots, deduplicación y alta integridad de datos
- **XFS**: Óptimo para servidores de alto rendimiento que manejan archivos muy grandes

¿Necesitas más detalles sobre algún sistema de archivos en particular?
