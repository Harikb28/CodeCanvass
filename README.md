# CodeCanvass
el.setAttribute("class","message my-message");
            el.innerHTML = `
            <div>
            <div class="name">You</div>
                <div class="text">${message.text}</div>
            
            </div>
            `;
            
            messageContainer.appendChild(el);
        }else if(type == "other"){
            let el = document.createElement("div");
            el.setAttribute("class","message other-message");
            el.innerHTML = `
            <div>
            <div class="name">${message.username}</div>
                <div class="text">${message.text}</div>
            
            </div>
            `;
           }else if(type == "update"){
            let el = document.createElement("div");
            el.setAttribute("class","update");
            el.innerText = message;
            messageContainer.appendChild(el);

        }
        //scroll chat to end
        messageContainer.scrollTop = messageContainer.scrollHeight - messageContainer.clientHeight;
     }
})();
