# flutter_2nd_app

### follwoing of Flutter Tutorial for Beginners

channel youtube of creator : https://www.youtube.com/channel/UCW5YeuERMmlnqo4oq8vwUpg

link playlist class : https://www.youtube.com/playlist?list=PL4cUxeGkcC9jLYyp2Aoh6hcWuxFDX6PBJ

thanks to the youtuber "The Net Ninja" ^^

# 15 Ninja ID Project

### the goal : create avatar characteristics
### preview: 
<img src="https://github.com/Geoffrey-Carpentier/flutter_2nd_app/blob/main/caps/chap15.JPG" height="600">

1) create a new flutter project with vs code
2) delete the "test" folder
3) delete all the code after the void main() line from "main.dart"
4) replace "my app" by MaterialApp and create an new StatelessWidget named "NinjaCard"to use in the home of the main()
~~~~
void main() {
  runApp(MaterialApp(
    home: NinjaCard()
  ));
}

class NinjaCard extends StatelessWidget {

  @override
  Widget build(BuildContext context) {
    return Container(
      
    );
  }
}
~~~~
5) replace the containe by a scaffold
~~~~
return Scaffold(
  appBar: AppBar(
    title: Text('Ninja ID Card'),
  ),
);
~~~~
5) create some widgets separed by sisedBOxs 
~~~~

~~~~
6) download an image and put it inside an "assets" folder 
7) add line on pubspec.yaml
~~~~
 assets:
     - assets/
~~~~
8) create a circleAvatar on the beginnng on the column with the image wrapped in a Center widget
~~~~
Center(
  child: CircleAvatar(
    backgroundImage: AssetImage('assets/chun-li.jpg'),
    radius: 40.0,
  ),
),
~~~~
9) just below the circleAvatar widget create a Divider to seperate the image and the rest of the other widgets
~~~~
Divider(
  height: 70.0,
  color: Colors.grey[800],
),
~~~~
