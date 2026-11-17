# GitHub Pages 배포 순서

이 포트폴리오는 `dist/` 안의 정적 사이트 파일을 GitHub Pages로 배포하도록 설정되어 있습니다.

1. GitHub에서 새 저장소를 만듭니다. 예: `seojin-portfolio`
   - 개인 포트폴리오라면 Public 저장소를 선택하면 주소 접근과 공유가 간단합니다.
   - 저장소를 만들 때 README, .gitignore, License는 추가하지 않습니다.
2. 터미널에서 이 프로젝트 폴더로 이동하고 GitHub 저장소를 연결합니다.

   ```sh
   cd /path/to/portfolio-site
   git remote add origin https://github.com/YOUR_GITHUB_NAME/seojin-portfolio.git
   git add .github/workflows/pages.yml GITHUB_PAGES.md
   git commit -m "Configure GitHub Pages deployment"
   git push -u origin main
   ```

3. GitHub 저장소의 **Settings → Pages → Build and deployment → Source**에서 **GitHub Actions**를 선택합니다.
4. **Actions** 탭에서 `Deploy portfolio to GitHub Pages` 작업이 성공할 때까지 기다립니다.
5. 완료되면 **Settings → Pages**의 배포 주소를 엽니다. 주소는 보통 다음 형태입니다.

   ```text
   https://YOUR_GITHUB_NAME.github.io/seojin-portfolio/
   ```

이후 `main` 브랜치에 변경을 push할 때마다 사이트가 자동으로 다시 배포됩니다. 저장소 이름을 `YOUR_GITHUB_NAME.github.io`로 만들면 주소에서 저장소 이름 부분이 빠집니다.
