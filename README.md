# BidUp

Aplicativo de leilões online feito em Flutter. A ideia é permitir que qualquer pessoa anuncie um item, defina um lance inicial e um prazo, e acompanhe os lances em tempo real até o encerramento.

O projeto está no começo. Por enquanto o repositório contém apenas a estrutura base gerada pelo Flutter; as funcionalidades descritas abaixo são o que está planejado, não o que já existe.

## Funcionalidades planejadas

**Para quem vende**

- Cadastro de itens com fotos, descrição, categoria e estado de conservação
- Definição de lance inicial, incremento mínimo e preço de reserva opcional
- Escolha da data e hora de encerramento do leilão
- Painel com os leilões ativos, encerrados e o histórico de lances de cada um

**Para quem compra**

- Busca e filtros por categoria, faixa de preço e tempo restante
- Lances com atualização em tempo real
- Lista de favoritos para acompanhar leilões de interesse
- Notificação quando alguém cobre o seu lance ou quando um leilão está perto de acabar

**Geral**

- Conta de usuário com login por e-mail
- Perfil com avaliações entre compradores e vendedores
- Contagem regressiva visível em cada anúncio
- Extensão automática do prazo quando há lance nos últimos minutos, para evitar o "lance de último segundo"

## Stack

- [Flutter](https://flutter.dev) com Dart SDK `^3.10.8`
- Material Design
- `flutter_lints` para análise estática

Backend, autenticação e persistência ainda não foram definidos.

## Plataformas

O projeto já tem as pastas de Android, iOS, Web, macOS, Linux e Windows. O foco inicial é Android e iOS.

## Como rodar

Pré-requisitos: Flutter instalado e configurado (`flutter doctor` sem erros para a plataforma que você vai usar).

```bash
git clone <url-do-repositorio>
cd BidUp
flutter pub get
flutter run
```

Para escolher o dispositivo:

```bash
flutter devices
flutter run -d <id-do-dispositivo>
```

## Testes e análise

```bash
flutter test
flutter analyze
```

## Build

```bash
flutter build apk      # Android
flutter build ios      # iOS (requer macOS e Xcode)
flutter build web      # Web
```

## Estrutura

```
lib/        código do app
test/       testes
android/    projeto nativo Android
ios/        projeto nativo iOS
web/        arquivos da versão web
macos/, linux/, windows/   projetos desktop
```

## Próximos passos

1. Definir o backend e o modelo de dados (usuários, itens, leilões, lances)
2. Montar as telas de listagem, detalhe do leilão e cadastro de item
3. Implementar autenticação
4. Implementar lances em tempo real
5. Notificações push
