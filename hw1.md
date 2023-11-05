[作業一影片demo](https://youtube.com/shorts/kplNMpfWTeA?feature=share)
```swift

  import SwiftUI
  struct ContentView: View {
      var body: some View {
          ScrollView {
              VStack(alignment: .leading) {
                  
                  Image("MyPicture")
                      .resizable()
                      .scaledToFit()
                      .clipShape(Circle())
                      .shadow(radius: 7)
                      .overlay {
                          Circle().stroke(.white, lineWidth: 4)
                      }
                      .padding()
                  HStack {
                      
                      Text("楊皓翔")
                          .font(.title)
                      Text("Sam Yang").font(.title)
                  }
                  
                  HStack {
                      Text("元智大學 資訊工程學系")
                      Image(systemName: "moon.fill")
                          .foregroundColor(.black)
                      Spacer()
                      Text("sid : 1091456")
                  }
                  .font(.subheadline)
                  .foregroundColor(.secondary)
                  Divider()
                  
                  Text("About Me")
                      .font(.title2)
                  Text("我是一名資工的學生。我的生活充滿了程式碼、演算法、和技術的迷人世界，但在某個點上，這些似乎失去了光彩。在學業之外，當我有時間放鬆時，我發現自己陷入了無聊的漩渦。\n無聊是一種有趣的感覺。它不是痛苦，也不是悲傷，但它有著一種使人難以捉摸的重量。這種感覺激發了我的好奇心，推動我開始探索生活的真正意義。我開始問自己：「為什麼我會感到無聊？」「生活中真正重要的是什麼？」\n這些問題引領我走上一段反思和探索的旅程。我開始深入思考生活的本質，超越了表面的日常忙碌和工作。我探索哲學、心靈成長、藝術、甚至尋找各種可能的方式來貢獻於社會。在這個探索過程中，我發現生活的意義並不是固定不變的。對我而言，它是一種動態的狀態，一種能隨著時間而變化的體驗。它在於學習、成長和尋找那些觸動心靈的事物。而這些事物可能與我所經歷的、我所學習的、以及我所創造的有關。因此，無論是在程式碼的世界中還是在日常生活中，我開始尋找著那些能為我的生活增添色彩的事物。這些可能是新的程式語言、寫作、探索大自然，或者幫助他人。它們讓我感到充實，讓我對生活的可能性充滿了期待。或許，追尋生命的意義並不在於解決無聊，而是在於接納它、並把它作為一種啟發，去追求更有意義和豐富的生活。")
              
              }
              .padding()
          }
        }
  }
```

