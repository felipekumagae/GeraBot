
# 🤖 GeraBot

Automação de envio de avisos para grupos do WhatsApp utilizando Python e Selenium.

---

## 📚 **Descrição**

O GeraBot realiza o envio automático de mensagens no WhatsApp Web, lendo arquivos `.txt` organizados por semana e dia da semana.  
A automação foi desenvolvida para manter avisos de aulas atualizados, enviando:

- 📅 Avisos diários de manhã (aulas do dia)  
- 📅 Avisos à noite (aulas do dia seguinte), com exceção de sexta-feira  
- 📅 Aviso de domingo para segunda-feira  

---

## 🚀 **Funcionalidades**

- Envio de mensagens via WhatsApp Web usando Selenium  
- Persistência de sessão (não precisa escanear o QR Code toda vez)  
- Organização de mensagens por semana (A ou B) e dias úteis  
- Logs de envio para acompanhamento  
- Totalmente automatizado via agendamento de tarefas  

---

## 📦 **Estrutura de Pastas**

```
GeraBot/
├── avisos/                # Arquivos .txt com as mensagens
├── chromedriver/          # ChromeDriver para Selenium
├── session_data/          # Dados de sessão do WhatsApp Web (não versionado)
├── src/                   # Código-fonte (main.py)
├── .gitignore
├── README.md
└── requirements.txt
```

---

## ⚙️ **Como Usar**

1. Clone o repositório:
```bash
git clone https://github.com/felipekumagae/GeraBot.git
```

2. Instale as dependências:
```bash
pip install -r requirements.txt
```

3. Baixe o [ChromeDriver](https://chromedriver.chromium.org/downloads) correspondente à sua versão do Chrome e sistema operacional, e coloque na pasta `chromedriver/`.

4. Configure o nome do grupo no arquivo `src/main.py`:
```python
GROUP_NAME = "Nome Exato do Grupo no WhatsApp"
```

5. Execute o script:
```bash
python3 src/main.py
```

---

## 📅 **Agendamentos Automáticos**

| Período   | Horário  | Ação                |
|------------|----------|---------------------|
| Manhã      | 07:00    | Enviar aviso do dia |
| Noite      | 17:00    | Enviar aviso do dia seguinte (exceto sexta) |
| Domingo    | 17:00    | Enviar aviso de segunda-feira |

---

## 🛡️ **Atenção**
- A pasta `session_data/` contém informações de sessão do WhatsApp Web e **não deve ser versionada**.
- Para garantir isso, o `.gitignore` já foi configurado.

---

## 👨‍💻 **Autor**
- Felipe Kumagae  
- [LinkedIn](https://www.linkedin.com/in/felipekumagae) | [GitHub](https://github.com/felipekumagae)
