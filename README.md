# 🚀 Flutter Developer | Mobile App Enthusiast

[![Flutter](https://img.shields.io/badge/Flutter-02569B?logo=flutter&logoColor=white)](https://flutter.dev)
[![Dart](https://img.shields.io/badge/Dart-0175C2?logo=dart&logoColor=white)](https://dart.dev)
[![GitHub Followers](https://img.shields.io/github/followers/ngtrongha?label=Follow&style=social)](https://github.com/ngtrongha)

<div align="center">
  <img src="https://media.giphy.com/media/3o7TKMt1VV26qJQ5AA/giphy.gif" width="200">
</div>

## 📱 Projects Highlight
| Project | Description | Tech Stack | Source Code |
|---------|-------------|------------|-------------|
| **E-Commerce App** | A full-featured shopping app with Firebase backend. | Flutter, Firebase, Bloc | [GitHub Repo](https://github.com/ngtrongha/ecommerce-app) |
| **Weather App** | Real-time weather updates using OpenWeather API. | Flutter, REST API, Provider | [GitHub Repo](https://github.com/ngtrongha/weather-app) |

## 📊 GitHub Stats
[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=ngtrongha&layout=compact&theme=radical&hide=html,css)](https://github.com/anuraghazra/github-readme-stats)
[![GitHub Streak](https://streak-stats.demolab.com?user=ngtrongha&date_format=j%20M%5B%20Y%5D&exclude_days=Mon)](https://git.io/streak-stats)

## 🛠️ Flutter Tech Stack
- **State Management**: Bloc, Provider, Riverpod  
- **Database**: Firebase, Hive, SQLite  
- **Architecture**: Clean Architecture, MVVM  
- **Tools**: VS Code, Android Studio, Figma  

## 🌟 Featured Flutter Snippet
```dart
// Flutter: Custom Animated Button
class AnimatedButton extends StatefulWidget {
  @override
  _AnimatedButtonState createState() => _AnimatedButtonState();
}

class _AnimatedButtonState extends State<AnimatedButton> with SingleTickerProviderStateMixin {
  late AnimationController _controller;

  @override
  void initState() {
    super.initState();
    _controller = AnimationController(
      vsync: this,
      duration: Duration(milliseconds: 200),
    );
  }

  @override
  Widget build(BuildContext context) {
    return GestureDetector(
      onTapDown: (_) => _controller.forward(),
      onTapUp: (_) => _controller.reverse(),
      child: ScaleTransition(
        scale: Tween(begin: 1.0, end: 0.9).animate(_controller),
        child: Container(
          padding: EdgeInsets.symmetric(horizontal: 24, vertical: 12),
          decoration: BoxDecoration(
            color: Colors.blue,
            borderRadius: BorderRadius.circular(8),
          ),
          child: Text('Press Me', style: TextStyle(color: Colors.white)),
        ),
      ),
    );
  }
}
