# 📋 Documentação dos 100 Casos de Teste

Cada teste simula um email forward para o workflow de arquivamento automático.

---

## 🎯 Casos Básicos (TC001-TC010)

| ID | Descrição |
|----|-----------|
| **TC001** | Forward PT com ID projeto explícito (123) e entidade Vodafone na assinatura |
| **TC002** | Forward sem ID projeto, entidade Galp no corpo |
| **TC003** | Forward PT com ID 456, múltiplos anexos PDF, entidade PwC |
| **TC004** | Forward "Enc:" (prefixo alternativo), entidade na assinatura |
| **TC005** | Forward EN com invoice #789, entidade Microsoft |
| **TC006** | Forward sem assinatura clara - deve ser "Desconhecido" |
| **TC007** | Múltiplos prefixos (FW: RE: Fwd:), ID 001 |
| **TC008** | ⚠️ Auto-reply "Out of Office" - deve ser FILTRADO |
| **TC009** | ⚠️ Auto-reply "Automatic reply" - deve ser FILTRADO |
| **TC010** | Email ENVIADO (martim é o From original) - sentido ENV |

---

## 📤 Sentido ENV (TC010-TC011)

| ID | Descrição |
|----|-----------|
| **TC010** | Sentido ENV - utilizador enviou email para cliente |
| **TC011** | Sentido ENV - relatório enviado para Altice |

---

## 🌍 Caracteres Especiais (TC012)

| ID | Descrição |
|----|-----------|
| **TC012** | Caracteres especiais €ñç, email espanhol |

---

## 🔢 IDs de Projeto (TC013-TC015, TC057-TC058)

| ID | Descrição |
|----|-----------|
| **TC013** | ID 999 - número máximo de 3 dígitos |
| **TC014** | ID 1 - deve ser normalizado para 001 |
| **TC015** | ID "ABC" - inválido, deve usar 000 |
| **TC057** | ID 12345 - excede 3 dígitos, deve usar 000 |
| **TC058** | "500 unidades" no corpo - NÃO é ID de projeto |

---

## 📭 Conteúdo Vazio/Mínimo (TC016-TC017)

| ID | Descrição |
|----|-----------|
| **TC016** | Email com corpo vazio |
| **TC017** | Email sem assunto |

---

## 📎 Anexos (TC018-TC021, TC059-TC060)

| ID | Descrição |
|----|-----------|
| **TC018** | Múltiplos anexos PDF (4 ficheiros) |
| **TC019** | Anexos de imagem (JPG, PNG) |
| **TC020** | Anexo Excel (.xlsx) |
| **TC021** | Anexo Word (.docx) |
| **TC059** | Anexo grande (simulado 50MB) |
| **TC060** | Nome de anexo com caracteres especiais |

---

## 🖥️ HTML/Formatação (TC022, TC078-TC082)

| ID | Descrição |
|----|-----------|
| **TC022** | HTML complexo com estilos inline |
| **TC078** | Tabela HTML no corpo |
| **TC079** | Lista com bullets (•) |
| **TC080** | Citação longa com > prefixos |
| **TC081** | Disclaimer corporativo longo |
| **TC082** | Imagem inline base64 |

---

## 🏢 Extração de Entidade (TC023-TC035)

| ID | Descrição |
|----|-----------|
| **TC023** | Entidade apenas no domínio do email (@deloitte.pt) |
| **TC024** | Entidade com "Lda" no nome |
| **TC025** | Entidade com "SA" no nome |
| **TC026** | Sigla conhecida - CTT |
| **TC027** | Sigla - SIBS |
| **TC028** | Banco comercial - Millennium BCP |
| **TC029** | Seguradora - Fidelidade |
| **TC030** | Texto muito longo, entidade no final |
| **TC031** | Corpo só com números |
| **TC032** | Entidade explícita: "Somos da IKEA" |
| **TC033** | Email de particular - usar nome pessoal |
| **TC034** | Gmail pessoal - extrair nome |
| **TC035** | Assinatura enterprise completa |

---

## 🔄 Forwards Especiais (TC036-TC040)

| ID | Descrição |
|----|-----------|
| **TC036** | Forward aninhado (forward de forward) |
| **TC037** | Thread de emails com citações |
| **TC038** | "Enviado do meu iPhone" |
| **TC039** | "Enviado pelo Gmail Mobile" |
| **TC040** | Assinatura Outlook clássica |

---

## 🔍 IDs com Formatos Alternativos (TC062-TC064)

| ID | Descrição |
|----|-----------|
| **TC062** | ID com hashtag: "Projeto #234" |
| **TC063** | ID com prefixo: "Proj-345" |
| **TC064** | Código PO: "PO-567" |

---

## 🌐 Idiomas (TC047-TC050)

| ID | Descrição |
|----|-----------|
| **TC047** | Email em inglês |
| **TC048** | Email em francês |
| **TC049** | Email em espanhol |
| **TC050** | Email misto PT/EN |

---

## 🚀 Startups/Unicórnios (TC065-TC067)

| ID | Descrição |
|----|-----------|
| **TC065** | Startup PT - Talkdesk |
| **TC066** | Unicórnio - Farfetch |
| **TC067** | Fintech - Revolut |

---

## 🏛️ Entidades Públicas (TC068-TC077)

| ID | Descrição |
|----|-----------|
| **TC068** | Governo de Portugal |
| **TC069** | Câmara Municipal de Lisboa |
| **TC070** | Autoridade Tributária |
| **TC071** | Segurança Social |
| **TC072** | Universidade de Lisboa |
| **TC073** | Hospital/Centro Hospitalar |
| **TC074** | ONG - Amnistia Internacional |
| **TC075** | Sindicato - CGTP |
| **TC076** | Associação empresarial - CIP |
| **TC077** | Consulado/Embaixada |

---

## 🔤 Casos de Formatação (TC054-TC056, TC085-TC090)

| ID | Descrição |
|----|-----------|
| **TC054** | Tudo em CAPS LOCK |
| **TC055** | Tudo em minúsculas |
| **TC056** | MiXeD CaSe |
| **TC085** | Corpo só com espaços |
| **TC086** | Caracteres japoneses |
| **TC087** | Caracteres árabes |
| **TC088** | Caracteres chineses |
| **TC089** | Newlines excessivas |
| **TC090** | Tabs e espaços misturados |

---

## 📧 Clientes Email Diferentes (TC091-TC092)

| ID | Descrição |
|----|-----------|
| **TC091** | Forward Apple Mail ("Begin forwarded message") |
| **TC092** | Forward Yahoo Mail |

---

## 📬 Headers Especiais (TC093-TC098)

| ID | Descrição |
|----|-----------|
| **TC093** | Entidade apenas no campo To |
| **TC094** | Email para "undisclosed-recipients" |
| **TC095** | CC múltiplo |
| **TC096** | BCC visível por forward |
| **TC097** | Reply-To diferente do From |
| **TC098** | Referência a anexo inline (cid:) |

---

## 🏆 Casos Completos (TC099-TC100)

| ID | Descrição |
|----|-----------|
| **TC099** | Projeto 42, 3 anexos diferentes, assinatura completa Accenture |
| **TC100** | **TESTE FINAL** - Todos elementos: ID 777, múltiplos anexos, CC, assinatura enterprise completa, disclaimer, OutSystems |

---

## 📊 Estatísticas

| Categoria | Quantidade |
|-----------|------------|
| Casos com ID projeto | 15 |
| Casos ENV (enviado) | 2 |
| Casos REC (recebido) | 96 |
| Casos filtrados | 2 |
| Casos com anexos | 25 |
| Casos edge-case | 30+ |
| **Total** | **100** |
