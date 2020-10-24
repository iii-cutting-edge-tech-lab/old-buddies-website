## 如何建立 Hugo 環境

Our hugo theme [Hugo Scroll](https://themes.gohugo.io/hugo-scroll/)

```bash
git clone https://github.com/iii-cutting-edge-tech-lab/old-buddies-website.git

cd old-buddies-website

## update theme submodule
git submodule update --init --recursive
```

### 地端測試網頁 

```bash
hugo server -D
```

### 發布文章

請參考 GitHub flow 由 Roya 寫的[教學文章](https://awdr74100.github.io/2020-05-11-git-githubflow/)，大致的流程如下：

1. fork 我們共用的 old-buddies-website 專案
2. 創建一個新的 branch，並且這個 branch 名稱要跟你修改的目的有關，像是 `feature/add-main-page` or `fix/date-issue`
3. 寫一些新的 code、修改設定檔、寫新的文章或更改新的 theme 都好，最後 `git commit -m "你這次做了什麼"`
4. 之後把你新的 branch push 到你剛剛 fork 好的專案上，並且發起 PR（Pull Request），並且自己看一下 `Files changed` 是不是你自己預期的改動，並且 assign 給專案負責人
5. 專案負責人會 code review 你這次的改動給予回饋，有可能需要叫你再做修改，直到專案負責人覺得可以才會 Approve & Merge
6. 當 Merge 之後會 trigger [GitHub Actions](https://github.com/features/actions) 把專案內容 build & deploy 到 [old-buddies-website](https://iii-cutting-edge-tech-lab.github.io/) 的宣傳網站
