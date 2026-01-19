import 'package:flutter/material.dart';

void main(List<String> args) {
  runApp(const Apple());
}

class Apple extends StatelessWidget {
  const Apple({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      theme: ThemeData(
        scaffoldBackgroundColor: Color(0xFFA7DAD1),
        fontFamily: 'Roboto',
      ),
      debugShowCheckedModeBanner: false,
      home: const HomePage(),
    );
  }
}

class HomePage extends StatefulWidget {
  const HomePage({super.key});

  @override
  State<HomePage> createState() => _HomePageState();
}

class _HomePageState extends State<HomePage> {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: Stack(
        children: [
          _topBackground(),
          Align(
            alignment: AlignmentGeometry.bottomCenter,
            child: _loginCard(context),
          ),
        ],
      ),
    );
  }
}

Widget _topBackground() {
  return Container(
    height: 300,
    padding: const EdgeInsets.all(20),
    color: Color(0xFF0B6A6A),
    child: Column(
      crossAxisAlignment: CrossAxisAlignment.start,
      children: [
        SizedBox(height: 40),
        const Text(
          "Hello !",
          style: TextStyle(
            fontSize: 35,
            color: Colors.white,
            fontWeight: FontWeight.bold,
          ),
        ),
        const SizedBox(height: 6),
        const Text(
          "Welcome to Planland",
          style: TextStyle(color: Colors.white70),
        ),
      ],
    ),
  );
}

Widget _loginCard(BuildContext context) {
  final TextEditingController _usernamecontroller = TextEditingController();
  final TextEditingController _passwordcontroller = TextEditingController();
  return Container(
    height: MediaQuery.of(context).size.height * 0.65,
    padding: EdgeInsets.all(24),
    decoration: BoxDecoration(
      color: Color(0xFFF2F6F5),
      borderRadius: BorderRadius.vertical(top: Radius.circular(30)),
    ),
    child: Column(
      crossAxisAlignment: CrossAxisAlignment.start,
      children: [
        const Text(
          "Login",
          style: TextStyle(
            fontSize: 18,
            color: Colors.red,
            fontWeight: FontWeight.bold,
          ),
        ),
        const SizedBox(height: 5),
        TextField(
          controller: _usernamecontroller,
          decoration: InputDecoration(
            labelText: "Username",
            suffixIcon: Icon(
              Icons.person,
              size: 30,
              color: Colors.red,
              fontWeight: FontWeight.bold,
            ),
            border: OutlineInputBorder(
              borderRadius: BorderRadius.circular(30.0),
            ),
          ),
        ),
        const SizedBox(height: 10),
        TextField(
          controller: _passwordcontroller,
          decoration: InputDecoration(
            labelText: "Password",
            suffixIcon: Icon(
              Icons.lock,
              size: 30,
              color: Colors.red,
              fontWeight: FontWeight.bold,
            ),
            border: OutlineInputBorder(
              borderRadius: BorderRadius.circular(30.0),
            ),
          ),
          obscureText: true,
        ),
        Align(
          alignment: AlignmentGeometry.centerRight,
          child: const Text(
            "Forgot Password",
            style: TextStyle(
              fontSize: 12,
              fontWeight: FontWeight.bold,
              color: Colors.teal,
            ),
          ),
        ),
        const SizedBox(height: 20),
        ElevatedButton(
          style: ElevatedButton.styleFrom(
            backgroundColor: Color(0xFF0B6A6A),
            shape: RoundedRectangleBorder(
              borderRadius: BorderRadius.circular(25.0),
            ),
          ),
          onPressed: () {},
          child: Text("Login"),
        ),
        const SizedBox(height: 20),
        _divider(),
        const SizedBox(height: 20),
        _socialButton(),
        const Spacer(),

        Center(
          child: GestureDetector(
            onTap: () {
              Navigator.push(
                context,
                MaterialPageRoute(builder: (context) => const SignupScreen()),
              );
            },
            child: const Text(
              "Don't have account! Sign Up!",
              style: TextStyle(color: Colors.teal),
            ),
          ),
        ),
      ],
    ),
  );
}

class SignupScreen extends StatelessWidget {
  const SignupScreen({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: SafeArea(
        child: Column(
          children: [
            Align(
              alignment: AlignmentGeometry.centerLeft,
              child: IconButton(
                onPressed: () {
                  Navigator.pop(context);
                },
                icon: Icon(Icons.arrow_back, color: Colors.white),
              ),
            ),
            Expanded(
              child: Container(
                decoration: BoxDecoration(
                  color: Color(0xFFF2F6F5),
                  borderRadius: BorderRadius.circular(30),
                ),
                padding: EdgeInsets.all(24),
              ),
            ),
            Column(
              crossAxisAlignment: CrossAxisAlignment.start,
              children: [
                const Text(
                  "Sign Up",
                  style: TextStyle(fontSize: 24, color: Colors.red),
                ),
              ],
            ),
            const SizedBox(height: 20),
            TextField(
              decoration: InputDecoration(
                labelText: "Email",
                suffixIcon: Icon(Icons.person),
                hintText: "Email",
              ),
            ),
            const SizedBox(height: 10),
            TextField(
              decoration: InputDecoration(
                suffixIcon: Icon(Icons.password),
                labelText: "Password",
                hintText: "Password",
              ),
            ),
            const SizedBox(height: 10),
            TextField(
              decoration: InputDecoration(
                suffixIcon: Icon(Icons.phone),
                labelText: "Comfirm password",
                hintText: "Confirm password",
              ),
            ),
          ],
        ),
      ),
    );
  }
}

Widget _divider() {
  return Row(
    children: const [
      Expanded(child: const Divider()),
      Padding(
        padding: EdgeInsets.symmetric(vertical: 8),
        child: Text("or login with"),
      ),
      Expanded(child: const Divider()),
    ],
  );
}

Widget _socialButton() {
  return Row(
    mainAxisAlignment: MainAxisAlignment.center,
    children: const [
      CircleAvatar(radius: 50, child: Icon(Icons.facebook)),
      CircleAvatar(radius: 50, child: Icon(Icons.electric_bolt_sharp)),
      CircleAvatar(radius: 50, child: Icon(Icons.call_end)),
    ],
  );
}
