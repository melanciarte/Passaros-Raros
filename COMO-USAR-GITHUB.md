# 📘 Como Adicionar o Site no GitHub - Passo a Passo

## 🎯 Passo 1: Criar uma Conta no GitHub

1. Acesse [github.com](https://github.com)
2. Clique em "Sign up" (Cadastrar-se)
3. Siga as instruções para criar sua conta
4. Confirme seu email

## 📦 Passo 2: Criar um Novo Repositório

1. Após fazer login no GitHub, clique no botão "+" no canto superior direito
2. Selecione "New repository" (Novo repositório)
3. Preencha os dados:
   - **Repository name**: `passaros-raros` (ou outro nome de sua preferência)
   - **Description**: "Site sobre pássaros raros e ameaçados de extinção"
   - Marque como **Public** (Público)
   - **NÃO** marque "Initialize with README" (já temos um README)
4. Clique em "Create repository"

## 💻 Passo 3: Preparar os Arquivos

Antes de enviar ao GitHub, adicione suas imagens, vídeos e áudios:

### Imagens (pasta `imagens/`)
- arara-azul-lear.jpg
- kakapo.jpg
- condor-california.jpg
- mutum-nordeste.jpg
- colhereiro.jpg
- galeria-1.jpg, galeria-2.jpg, galeria-3.jpg, galeria-4.jpg, galeria-5.jpg, galeria-6.jpg
- thumb-video-1.jpg, thumb-video-2.jpg, thumb-video-3.jpg

### Áudios (pasta `audio/`)
- arara-azul.mp3
- kakapo.mp3
- mutum.mp3
- colhereiro.mp3

### Vídeos (pasta `videos/`)
- arara-azul.mp4
- kakapo.mp4
- documentario.mp4

## 🚀 Passo 4: Enviar para o GitHub

Execute os seguintes comandos no terminal:

```bash
# Inicializar o Git (se ainda não foi feito)
git init

# Adicionar todos os arquivos
git add .

# Criar o primeiro commit
git commit -m "Primeiro commit: Site de pássaros raros"

# Conectar com o repositório do GitHub (SUBSTITUA SEU-USUARIO pelo seu nome de usuário)
git remote add origin https://github.com/SEU-USUARIO/passaros-raros.git

# Renomear a branch para main
git branch -M main

# Enviar para o GitHub
git push -u origin main
```

**IMPORTANTE:** Na primeira vez que fizer `git push`, o GitHub pedirá suas credenciais:
- **Username**: Seu nome de usuário do GitHub
- **Password**: Use um **Personal Access Token** (não use sua senha normal)

### Como criar um Personal Access Token:
1. No GitHub, clique na sua foto de perfil
2. Settings → Developer settings → Personal access tokens → Tokens (classic)
3. Generate new token → Marque "repo" → Generate token
4. Copie o token e use como senha

## 🌐 Passo 5: Publicar o Site (GitHub Pages)

Para deixar seu site acessível na internet:

1. No seu repositório no GitHub, clique em **Settings**
2. No menu lateral, clique em **Pages**
3. Em **Source**, selecione:
   - Branch: `main`
   - Folder: `/ (root)`
4. Clique em **Save**
5. Aguarde alguns minutos

Seu site estará disponível em:
```
https://SEU-USUARIO.github.io/passaros-raros/
```

## 🔄 Como Atualizar o Site Depois

Quando você fizer alterações nos arquivos:

```bash
# Adicionar as mudanças
git add .

# Criar um commit com descrição do que foi alterado
git commit -m "Descrição das mudanças"

# Enviar para o GitHub
git push
```

## 📝 Dicas Importantes

1. **Tamanho dos arquivos**: O GitHub tem limite de 100MB por arquivo. Se seus vídeos forem muito grandes, considere hospedá-los no YouTube ou Vimeo.

2. **Nomes de arquivos**: Use sempre nomes sem espaços e sem caracteres especiais (acentos). Use hífen (-) para separar palavras.

3. **Formato dos arquivos**:
   - Imagens: JPG ou PNG
   - Áudios: MP3
   - Vídeos: MP4

4. **Estrutura das pastas**: Mantenha a organização:
   ```
   passaros-raros/
   ├── index.html
   ├── styles.css
   ├── README.md
   ├── imagens/
   ├── videos/
   └── audio/
   ```

## 🆘 Problemas Comuns

### "Permission denied"
- Certifique-se de estar usando o Personal Access Token correto

### "Repository not found"
- Verifique se o nome do repositório está correto no comando `git remote add origin`

### Site não carrega imagens
- Verifique se os nomes dos arquivos estão exatamente como esperado
- Verifique se as imagens estão na pasta correta (`imagens/`)

### Vídeos não aparecem
- Vídeos grandes podem não funcionar bem no GitHub Pages
- Considere usar links do YouTube ou Vimeo

## 🎉 Pronto!

Agora seu site está no GitHub e disponível para todos verem! Compartilhe o link com seus amigos e familiares.

---

**Precisa de ajuda?** Consulte a [documentação oficial do GitHub](https://docs.github.com)
