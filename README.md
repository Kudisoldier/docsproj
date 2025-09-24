# Mydocs project  
  
Для инициализации и создания проекта я выполнил шаги:
- создал репозиторий на github
- склонировал его на локальную машину git clone git@github.com:Kudisoldier/docsproj.git
- установил uv командой brew install uv
- активировал окружение командой uv init
- установил mkdocs командой uv add --dev mkdocs
- создал проект mkdocs командой uv run mkdocs new mydocsproj
- далее в созданном проекте добавил свои файлы с документацией
- и настроил тему mkdocs на material, установив зависимость командой uv add --dev mkdocs-material
- создал ветку gh-pages и запушил ее на ремоут
- настроил github pages deploy from a branch gh-pages
- создал ci джобу для деплоя в ветку с помощью mkdocs gh-deploy по пушу в main
- готово, статический сайт развернут на https://kudisoldier.github.io/docsproj/
