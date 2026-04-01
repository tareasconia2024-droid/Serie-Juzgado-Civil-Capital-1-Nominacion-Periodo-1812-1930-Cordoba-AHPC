# AHPC · Juzgado Civil Capital 1° Nominación — App Web

Aplicación Flask para consultar el índice onomástico de partes de expedientes
del Juzgado Civil Capital 1° Nominación del AHPC (1883–1925).

## Instalación

```bash
pip install -r requirements.txt
python app.py
```

Abrí en el navegador: http://localhost:5005

## Estructura

```
civil1_app/
├── app.py                  # Servidor Flask
├── ahpc_civil1.db          # Base de datos SQLite (17.852 registros)
├── requirements.txt
└── templates/
    ├── base.html           # Layout y estilos
    ├── index.html          # Página de inicio
    ├── buscar.html         # Buscador con autocomplete
    ├── detalle.html        # Ficha de un expediente
    ├── por_causa.html      # Todos los expedientes de una causa
    └── estadisticas.html   # Gráficos y estadísticas
```

## Funcionalidades

- **Buscador** con filtros por partes (apellido/nombre), causa, período, legajo, expediente y texto libre (FTS)
- **Autocomplete** para partes y causas
- **Detalle** de expediente con otros del mismo legajo/año y otros del mismo apellido
- **Por causa** con todos los expedientes de ese tipo de juicio
- **Estadísticas** con gráficos CSS por década y top 30 causas (sin dependencias externas)
- **Exportar PDF** de cualquier búsqueda (máx. 500 registros)

## Datos

- **Fondo**: Poder Judicial de la Provincia de Córdoba
- **Subfondo**: Juzgados Civiles
- **Serie**: Juzgado Civil Capital 1° Nominación
- **Período**: 1883–1925
- **Total**: 17.852 expedientes
