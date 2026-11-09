# 第7回 Webエンジニアリング演習 レポート
## 学籍番号
4724225
## 2画面の見出しと本文
window.addEventListener("hashchange", () => {
    const page = location.hash;
    console.log(page);
    console.log(location.hash)

    if (page === "#detail"){
        app.innerHTML = `
            <h1>課題用画面 詳細</h1>
            <p>この文章を書き換えた。</p>
            <nav>
                <a href="#compare">比較</a>
                <a href="#detail">詳細</a>
            </nav>
        `;
    } else if (page === "#compare") {
        app.innerHTML = `
            <h1>課題用画面　比較</h1>
            <p>この文章を書き換えた。</p>
            <nav>
                <a href="#compare">比較</a>
                <a href="#detail">詳細</a>
            </nav>
        `;
    }
});
## クリック後のURLとNetworkの確認
https://humble-spork-wrqr977gw6w42qp9-3000.app.github.dev/csr/#compare
https://humble-spork-wrqr977gw6w42qp9-3000.app.github.dev/csr/#detail
## 画面を切り替える処理の要点
csr/	200	document	Other	2.3 kB	635 ms