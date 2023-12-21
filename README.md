# gLTF Tools + Calva Problem Reproduction Project

Something with the gLTF Tools and the Calva extensions for VS Code do not chime. This is a minimal Clojure project exposing the problem.

## Prerequisites

* Java
* the Clojure CLI
* VS Code
  * gLTF Tools Extension
  * Calva Extension
* This project opened in VS Code

## To reproduce

1. Issue the command **Calva: Start a Project REPL and Connect (aka Jack-in)**
2. Open the file [src/pez/hello.clj](src/pez/hello.clj)
3. Issue the command: **Calva: Evaluate Top Level Form** (`alt/option+enter`)
   * **Expected result**: `nil` is printed to the Calva Output Window (`output.calva-repl`)
   * Repeat the command a few times for more of the same
4. Open [Box.gltf](Box.gltf)
   * **Expected result**: `nil` is printed to the Calva Output Window
   * **Actual result**: `; RangeError: Maximum call stack size exceeded` is printed to the Calva Output Window
   * The Calva REPL is now defunct until you reload the VS Code window