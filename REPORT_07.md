# 第7回 Webエンジニアリング演習 レポート
## 学籍番号
4724210
## 2画面の見出しと本文
app.innerHTML = `
    <h1>詳細</h1>
    <p>詳細です。</p>
`;
app.innerHTML = `
    <h1>比較</h1>
    <p>比較です。</p>
`; 
## クリック後のURLとNetworkの確認
詳細を押すとcsr/#detail　に　比較を押すとcsr/##compareに変わった
## 画面を切り替える処理の要点
window.addEventListener("hashchange", () => {
    const page = location.hash;

    if (page === "#detail"){
        app.innerHTML = `
          <h1>詳細</h1>
          <p>詳細です。</p>
          <nav>
            <a href="#compare">比較</a>
            <a href="#detail">詳細</a>
          </nav>
        `;

    }else if(page === "#compare"){
        app.innerHTML = `
          <h1>比較</h1>
          <p>比較です。</p>
          <nav>
            <a href="#compare">比較</a>
            <a href="#detail">詳細</a>
          </nav>
       `; 
    }else{
      app.innerHTML = `
          <h1>比較</h1>
          <p>比較です。</p>
          <nav>
            <a href="#compare">比較</a>
            <a href="#detail">詳細</a>
          </nav>
       `; 
    }
});