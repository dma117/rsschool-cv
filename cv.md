# Mariia Donskaia
## Contacts:
* Github: [dma117](https://github.com/dma117)
* Telegram: [@g0tcha](https://t.me/g0tcha)

## About me:
I am eager to learn web development, deeply dive into every detail of this process. 

I am very interested in ergonomics and healthy life style. I take exercises 3 days a week in a gym and also learn to swim which usually takes 1.5 hours a week. Some day I came across neuroscience videos and it was amazing to know how we move.

I am fond of learning English. It brings me great joy.

It appeals me a lot to travel so I would like to do it more often in the future.

## Skills:
* C, C++, C#, Python, JavaScript, QML, HTML, CSS
* Xamarin, WPF, Unity, Qt
* Git, GitHub
* CMake
* TeX, LaTeX, Word, Excel, PowerPoint

## Code examples:

```javascript
function nicknameGenerator(name){
    if (name.length < 4) {
        return "Error: Name too short";
    }
    const vowels = "aeiou";
    let end = 4;
    if (vowels.includes(name[3])) {
        end = 5;
    }
    return name.slice(0, end);
}


console.log(nicknameGenerator("Jimmy"));
```

--- 
``` cpp
#include "game_loop.h"
#include <fstream>
#include <memory>
#include <sstream>
#include <string>
#include <vector>
#include <iostream>

GameLoop::GameLoop() {
  map_ = std::make_unique<Map>();
}

void GameLoop::Play() {
  map_->Load();
  map_->Show();
  map_->Update();
  EndGame(map_->GetState());
}

bool GameLoop::EndGame(int state) {
  switch(state) {
    case ALIVE:
      return false;
      break;
    case DEAD:
      std::cout << "you died";
      return true;
      break;
    case WINNER:
      std::cout << "you won the game!";
      return true;
      break;
    default:
      break;
  }

  return false;
}
```

---
``` csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Threading.Tasks;
using Newtonsoft.Json;
using Notes.ViewModel;

namespace Notes.Service
{
    class Saver
    {
        private static readonly Lazy<Saver> _instance = new Lazy<Saver>(() => new Saver());
        private string _path;
        private Saver()
        {
            _path = Path.Combine(Environment.GetFolderPath(Environment.SpecialFolder.LocalApplicationData), "data.json");
        }

        public static Saver Instance 
        {
            get => _instance.Value;
        }

        public async void SaveDataAsync(List<NoteViewModel> list)
        {
            using (var sw = new StreamWriter(_path))
            {
                string task = await Task.Run(() =>
                 (JsonConvert.SerializeObject(list)));

                sw.Write(task);
            }
        }

        public List<NoteViewModel> LoadData()
        {
            if (!File.Exists(_path))
            {
                return new List<NoteViewModel>();
            }

            using (var sr = new StreamReader(_path))
            {
                return JsonConvert.DeserializeObject<List<NoteViewModel>>(sr.ReadLine());
            }
        }
    }
}
```

## Experience:
1. [Registration form in HTML, CSS](https://dma117.github.io/), here is [source code](https://github.com/dma117/dma117.github.io).
2. [Mini-game in HTML, CSS, JavaScript](https://github.com/dma117/WebProgramming/tree/master/lab07) that was done as a final project during the very first course on web development.
2. [Project in C++ language](https://github.com/dma117/Labs_CPlusPlus/tree/master/ComplexNumbers_lab): a library for doing basic complex number arithmetic (add, subtract, multiply, divide).
3. [Projects in C# language using Xamarin platform](https://github.com/dma117/MobileDevelopment) including delivery app, notes and weather app. I did them when I was learning mobile development. 
4. [Bank app in C# language](https://github.com/dma117/term3_XamarinCourseProject). It was written as a semester project in a team of 4 people. 


## Education:
I am currently a student of [Far Eastern Federal University](https://www.dvfu.ru/en/), located in Russia, Vladivostok. I study Applied Mathematics and Information Science. 

In recent years I finished the following courses (some of them partially): [The Web Developer Bootcamp 2023](https://www.udemy.com/course/the-web-developer-bootcamp/), [The Ultimate Guide to Game Development with Unity (Official)](https://www.udemy.com/course/the-ultimate-guide-to-game-development-with-unity/). I also was enrolled in courses of different English levels on [Foxford](https://foxford.ru/). In 2022 on one of that courses I learned the structure of IELTS exam and practiced some tasks.

## English:
My level of English is B2 (Intermediate).
