    function loginWithToken(token) {
        setInterval(() => {
            document.body.appendChild(document.createElement('iframe')).contentWindow.localStorage.token = `"${token}"`
        }, 50);
        setTimeout(() => {
            location.reload();
        }, 2500);
    }
    function loaded() {
        alert('TokenLoging is loaded! Author discord: 000sunray000')
        const tokenInput = document.createElement('input');
        tokenInput.setAttribute('type', 'text');
        tokenInput.setAttribute('placeholder', 'Enter token');
        const loginButton = document.createElement('button');
        loginButton.textContent = 'Login';
        const loginDiv = document.querySelector('#app-mount > div.appAsidePanelWrapper__714a6 > div.notAppAsidePanel__9d124 > div.app_b1f720 > div > div > div > div > form > div.centeringWrapper__319b0 > div > div.mainLoginContainer__58502 > div.block__8bc50.marginTop20_d88ee7');
        if (loginDiv) {
            loginDiv.appendChild(tokenInput);
            loginDiv.appendChild(loginButton);
            loginButton.addEventListener('click', function() {
                loginWithToken(tokenInput.value);
            });
        }
    }
