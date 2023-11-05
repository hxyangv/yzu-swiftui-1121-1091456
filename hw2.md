[作業二影片demo](https://youtube.com/shorts/t7nmopvNAX4?feature=share)
```swift

import SwiftUI

struct ContentView: View {
    @State private var leftSelection: String = ""
    @State private var rightSelection: String = ""
    @State private var gameResult: String = ""
    
    var body: some View {
        VStack {
            Text("Rock-Paper-Scissors Game")
            
            HStack {
                Button(action: {
                    leftSelection = getEmojiSelection()
                    playGame()
                }) {
                    Text(leftSelection.isEmpty ? "Left" : leftSelection)
                        .font(.system(size: 50))
                }
                .padding()
                
                Button(action: {
                    rightSelection = getEmojiSelection()
                    playGame()
                }) {
                    Text(rightSelection.isEmpty ? "Right" : rightSelection)
                        .font(.system(size: 50))
                }
                .padding()
            }
            
            if !gameResult.isEmpty {
                Text(gameResult)
                    .padding()
                
                Button(action: {
                    restartGame()
                }) {
                    Text("Restart")
                }
            }
        }
    }
    
    func getEmojiSelection() -> String {
        let emojis = ["✊", "✋", "✌️"]
        let randomIndex = Int.random(in: 0...2)
        return emojis[randomIndex]
    }
    
    func playGame() {
        if !leftSelection.isEmpty && !rightSelection.isEmpty {
            if leftSelection == rightSelection {
                gameResult = "It's a tie!"
            } else if (leftSelection == "✊" && rightSelection == "✌️") ||
                        (leftSelection == "✋" && rightSelection == "✊") ||
                        (leftSelection == "✌️" && rightSelection == "✋") {
                gameResult = "Left wins!"
            } else {
                gameResult = "Right wins!"
            }
        }
    }
    
    func restartGame() {
        leftSelection = ""
        rightSelection = ""
        gameResult = ""
    }
}

struct ContentView_Previews: PreviewProvider {
    static var previews: some View {
        ContentView()
    }
}
```
