# ExpBeta

App SaaS de gestão de condomínios (Flutter + Supabase)

---

## Pré-requisitos

- Flutter 3.19.6 (travado via .flutter-version)
- Dart 3.3.x
- Conta no Supabase (dois projetos: staging e produção)
- Android Studio, VS Code ou outro editor com plugin Flutter

---

## Setup do Projeto

1. **Clone o repositório:**
   ```sh
   git clone <repo_url>
   cd expbeta
   ```
2. **Garanta que está usando o Flutter 3.19.6:**
   ```sh
   flutter --version
   # Ou use fvm se preferir
   ```
3. **Instale as dependências:**
   ```sh
   flutter pub get
   ```
4. **Configure os ambientes:**
   - Edite `.env.staging` e `.env.prod` com as URLs e chaves do Supabase.

---

## Estrutura de Pastas
```
lib/
  core/                # Temas, helpers, configs globais
  data/                # Models, datasources, repositórios
  domain/              # Entidades, casos de uso, interfaces
  presentation/
    screens/           # Telas e módulos
    widgets/           # Componentes reutilizáveis
    providers/         # Providers Riverpod
  main.dart            # Entry point

test/                  # Testes unitários e de widget
.env.staging           # Configuração Supabase (staging)
.env.prod              # Configuração Supabase (produção)
.flutter-version        # Versão travada do Flutter
pubspec.yaml           # Dependências
README.md              # Documentação
```

---

## Principais Dependências
- supabase_flutter
- flutter_riverpod
- google_sign_in
- intl
- fl_chart
- speech_to_text
- url_launcher
- responsive_framework

---

## Como rodar o projeto

### Web
```sh
flutter run -d chrome
```

### Android/iOS
- Conecte um dispositivo ou inicie um emulador
- Execute:
```sh
flutter run
```

---

## Ambiente e Segurança
- Dois ambientes: staging e produção (use .env.staging e .env.prod)
- Dados isolados por tenant_id (multi-tenant SaaS)
- RLS (Row Level Security) ativo no Supabase

---

## Próximos passos
- Implementação dos módulos conforme roadmap
- Commits frequentes e tags por fase (v0.1-login, v0.2-onboarding, ...)
- Documentação e comentários em todo o código

---

## Contato e Suporte
Para dúvidas, sugestões ou suporte, abra uma issue no repositório ou entre em contato com o time ExpBeta.


## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.
