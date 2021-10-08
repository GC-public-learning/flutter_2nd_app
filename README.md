# flutter_2nd_app

### follwoing of Flutter Tutorial for Beginners

channel youtube of creator : https://www.youtube.com/channel/UCW5YeuERMmlnqo4oq8vwUpg

link playlist class : https://www.youtube.com/playlist?list=PL4cUxeGkcC9jLYyp2Aoh6hcWuxFDX6PBJ

thanks to the youtuber "The Net Ninja" ^^

# 15 Ninja ID Project

### the goal : create an avatar characteristics

preview :
<img src="caps/chap15.jpg" width="400">

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
return Scaffold(
  backgroundColor: Colors.grey[900],
  appBar: AppBar(
    title: Text('Ninja ID Card'),
    centerTitle: true,
    backgroundColor: Colors.grey[850],
    elevation: 0.0,
  ),
  body: Padding(
    padding: EdgeInsets.fromLTRB(30.0, 40.0, 30.0, 0.0),
    child: Column(
      crossAxisAlignment: CrossAxisAlignment.start,
      children: <Widget>[
        Text(
          'NAME',
          style : TextStyle(
            color: Colors.grey,
            letterSpacing: 2.0
          )),
          SizedBox(height: 10.0,),
          Text(
          'Chun-Li',
          style : TextStyle(
            color: Colors.amberAccent[200],
            letterSpacing: 2.0,
            fontSize: 20.0,
            fontWeight: FontWeight.bold,

          )),
          SizedBox(height: 30.0,),
          Text(
          'CURRENT NINJA LEVEL',
          style : TextStyle(
            color: Colors.grey,
            letterSpacing: 2.0
          )),
          SizedBox(height: 10.0,),
          Text(
          '8',
          style : TextStyle(
            color: Colors.amberAccent[200],
            letterSpacing: 2.0,
            fontSize: 20.0,
            fontWeight: FontWeight.bold,
          )),
          SizedBox(height: 30.0,),
          Row(
            children: <Widget>[
              Icon(
                Icons.email,
                color: Colors.grey[400]
              ),
              SizedBox(width: 10.0,),
              Text(
                'chunli@flutter.net',
                style: TextStyle(
                  color: Colors.grey[400],
                  fontSize: 18.0,
                  letterSpacing: 1.0,
                )
              ),
            ],
          ),    
      ],
    )
    )
);
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
