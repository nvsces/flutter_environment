# flutter_environment

export PATH="$PATH:$HOME/dev/flutter/bin"
vim ~/.zshrc
i
esc
:
wq!

# extensions:
Dart
Flutter
Material Icon Theme
Dart Data Class Genereator
Awesome Flutter Snippets

# snippets:
{
  //freezed bloc
     "Freezed BLoC": {
        "prefix": "fbloc",
        "body": [
          "import 'package:bloc/bloc.dart';",
          "import 'package:freezed_annotation/freezed_annotation.dart';",
          "",
          "part '${TM_FILENAME_BASE}.freezed.dart';",
          "",
          "@freezed",
          "class $NAME$Event with _$$NAME$Event {",
          " const $NAME$Event._();",
          "",
          " const factory $NAME$Event.create() = Create$NAME$Event;",
          "",
          " const factory $NAME$Event.read() = Read$NAME$Event;",
          "",  
          " const factory $NAME$Event.update() = Update$NAME$Event;",
          "",
          " const factory $NAME$Event.delete() = Delete$NAME$Event;",
          "}",
          "",
          "@freezed",
          "class $NAME$State with _$$NAME$State {",
          " const $NAME$State._();",
          "",  
          " const factory $NAME$State.initial() = Initial$NAME$State;",
          "",
          " const factory $NAME$State.loading() = Loading$NAME$State;",
          "",
          " const factory $NAME$State.loaded(List<dynamic> result) = Loaded$NAME$State;",
          "",
          " const factory $NAME$State.failure() = Failure$NAME$State;",
          "}",
          "",
          "class $NAME$Bloc extends Bloc<$NAME$Event, $NAME$State> {",
          " $NAME$Bloc() : super(const Initial$NAME$State()){",
          " on<Create$NAME$Event>(_create); ",
          " on<Read$NAME$Event>(_read); ", 
          " on<Update$NAME$Event>(_update); ", 
          " on<Delete$NAME$Event>(_delete);", 
          "}",    
          " Future<void> _create(Create$NAME$Event event, Emitter<$NAME$State> emit) async {",
          "  // ...",    
          " }",
          "",
          " Future<void> _read(Read$NAME$Event event, Emitter<$NAME$State> emit) async {",
          "  // ...",
          " }",
          "",
          " Future<void> _update(Update$NAME$Event event, Emitter<$NAME$State> emit) async {",
          "  // ...",
          " }",
          "",
          " Future<void> _delete(Delete$NAME$Event event, Emitter<$NAME$State> emit) async{",
          "  // ...",
          " }",
          "}",
         
        ],
        "description": "Template BLoC with Freezed"
      },


      "Freezed Class": {
        "prefix": "freezedClass",
        "body": [
          "import 'package:freezed_annotation/freezed_annotation.dart';",
          "part '${TM_FILENAME_BASE}.freezed.dart';",
          "part '${TM_FILENAME_BASE}.g.dart';",
          "",
          "",
          "@freezed",
          "class $NAME with _$$NAME {",
          "",
          "factory $NAME(String id)= _$NAME;",
          "",
          "factory $NAME.fromJson(Map<String, dynamic> json) =>",
          "_$${NAME}FromJson(json);",
          "}"
        ],
        "description": "Template class with Freezed & json serialization"
    },   
}
