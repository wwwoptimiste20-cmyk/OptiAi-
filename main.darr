import 'package:flutter/material.dart';

void main() {
  runApp(const OptiAIApp());
}

class OptiAIApp extends StatelessWidget {
  const OptiAIApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      title: 'OptiAI 2.0',
      theme: ThemeData(
        brightness: Brightness.dark,
        scaffoldBackgroundColor: const Color(0xFF030712), // Fond ultra sombre identique
        colorScheme: const ColorScheme.dark(
          primary: Color(0xFF1E40AF), // Bleu profond OptiAI
          secondary: Color(0xFF3B82F6), // Bleu néon éclatant
          surface: Color(0xFF0F172A), // Couleur des cartes du menu
        ),
        useMaterial3: true,
      ),
      home: const WelcomeScreen(),
    );
  }
}

// --- ÉCRAN 1 : BIENVENUE ET PRÉSENTATION ---
class WelcomeScreen extends StatelessWidget {
  const WelcomeScreen({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: SafeArea(
        child: Padding(
          padding: const EdgeInsets.symmetric(horizontal: 24.0),
          child: Column(
            mainAxisAlignment: MainAxisAlignment.center,
            children: [
              const Spacer(),
              // Logo Cercle Néon OptiAI
              Container(
                width: 140,
                height: 140,
                decoration: BoxDecoration(
                  shape: BoxShape.circle,
                  gradient: const RadialGradient(
                    colors: [Color(0xFF3B82F6), Color(0xFF1E40AF), Colors.transparent],
                  ),
                  border: Border.all(color: const Color(0xFF3B82F6), width: 3),
                  boxShadow: [
                    BoxShadow(color: const Color(0xFF3B82F6).withOpacity(0.5), blurRadius: 20),
                  ],
                ),
                child: const Center(
                  child: Icon(Icons.blur_on_rounded, size: 70, color: Colors.white),
                ),
              ),
              const SizedBox(height: 24),
              const Text(
                'OptiAI 2.0',
                style: TextStyle(fontSize: 36, fontWeight: FontWeight.bold, letterSpacing: 1.5, color: Colors.white),
              ),
              const Text(
                'Powered by OptiTechnologie',
                style: TextStyle(fontSize: 14, color: Colors.blueAccent, fontWeight: FontWeight.w500),
              ),
              const SizedBox(height: 40),
              const Text(
                "L'intelligence qui accompagne votre futur.",
                textAlign: TextAlign.center,
                style: TextStyle(fontSize: 16, color: Colors.grey, height: 1.5),
              ),
              const Spacer(),
              // Bouton Commencer
              SizedBox(
                width: double.infinity,
                height: 56,
                child: ElevatedButton(
                  style: ElevatedButton.styleFrom(
                    backgroundColor: const Color(0xFF1E40AF),
                    shape: RoundedRectangleBorder(borderRadius: BorderRadius.circular(16)),
                    elevation: 5,
                  ),
                  onPressed: () {
                    Navigator.push(context, MaterialPageRoute(builder: (context) => const MainNavigationScreen()));
                  },
                  child: const Text('Commencer', style: TextStyle(fontSize: 18, color: Colors.white, fontWeight: FontWeight.bold)),
                ),
              ),
              const SizedBox(height: 24),
            ],
          ),
        ),
      ),
    );
  }
}

// --- GESTIONNAIRE DE LA NAVIGATION PRINCIPALE ---
class MainNavigationScreen extends StatefulWidget {
  const MainNavigationScreen({super.key});

  @override
  State<MainNavigationScreen> createState() => _MainNavigationScreenState();
}

class _MainNavigationScreenState extends State<MainNavigationScreen> {
  int _currentIndex = 0;

  final List<Widget> _pages = [
    const HomeScreen(),
    const HistoriquePage(),
    const PlaceholderWidget(title: 'Favoris'),
    const ParametresPage(),
  ];

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: _pages[_currentIndex],
      bottomNavigationBar: BottomNavigationBar(
        currentIndex: _currentIndex,
        onTap: (index) => setState(() => _currentIndex = index),
        selectedItemColor: const Color(0xFF3B82F6),
        unselectedItemColor: Colors.grey,
        showUnselectedLabels: true,
        backgroundColor: const Color(0xFF0F172A),
        type: BottomNavigationBarType.fixed,
        items: const [
          BottomNavigationBarItem(icon: Icon(Icons.home_filled), label: 'Accueil'),
          BottomNavigationBarItem(icon: Icon(Icons.history_rounded), label: 'Historique'),
          BottomNavigationBarItem(icon: Icon(Icons.star_border_rounded), label: 'Favoris'),
          BottomNavigationBarItem(icon: Icon(Icons.person_outline_rounded), label: 'Profil'),
        ],
      ),
    );
  }
}

// --- ÉCRAN 2 : ACCUEIL PRINCIPAL AVEC LA PHOTO DE PROFIL ROBOT ---
class HomeScreen extends StatelessWidget {
  const HomeScreen({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        leading: const Icon(Icons.menu_rounded, color: Colors.white),
        title: const Text('OptiAI 2.0', style: TextStyle(color: Colors.white, fontWeight: FontWeight.bold)),
        backgroundColor: Colors.transparent,
        elevation: 0,
      ),
      body: Padding(
        padding: const EdgeInsets.all(20.0),
        child: Column(
          crossAxisAlignment: CrossAxisAlignment.start,
          children: [
            const Text('Bonjour', style: TextStyle(fontSize: 28, fontWeight: FontWeight.bold, color: Colors.white)),
            const SizedBox(height: 4),
            const Text('Comment puis-je vous aider aujourd\'hui ?', style: TextStyle(fontSize: 16, color: Colors.grey)),
            const SizedBox(height: 30),
            
            // AVATAR DE ROBOT BLEU DE L'IMAGE
            Center(
              child: Container(
                width: 160,
                height: 160,
                decoration: BoxDecoration(
                  shape: BoxShape.circle,
                  color: const Color(0xFF0F172A),
                  border: Border.all(color: const Color(0xFF3B82F6).withOpacity(0.6), width: 4),
                  boxShadow: [
                    BoxShadow(color: const Color(0xFF3B82F6).withOpacity(0.3), blurRadius: 25),
                  ],
                ),
                child: ClipOval(
                  child: Stack(
                    alignment: Alignment.center,
                    children: [
                      Container(
                        decoration: const BoxDecoration(
                          gradient: LinearGradient(
                            colors: [Color(0xFF1E3A8A), Color(0xFF020617)],
                            begin: Alignment.topCenter,
                            end: Alignment.bottomCenter,
                          ),
                        ),
                      ),
                      Column(
                        mainAxisAlignment: MainAxisAlignment.center,
                        children: [
                          Container(
                            width: 85,
                            height: 65,
                            decoration: BoxDecoration(
                              color: const Color(0xFF1E293B),
                              borderRadius: BorderRadius.circular(24),
                              border: Border.all(color: const Color(0xFF3B82F6), width: 2),
                            ),
                            child: Row(
                              mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                              children: [
                                _buildRobotEye(),
                                _buildRobotEye(),
                              ],
                            ),
                          ),
                          const SizedBox(height: 8),
                          Container(width: 25, height: 10, color: const Color(0xFF3B82F6)),
                          Container(
                            width: 70,
                            height: 20,
                            decoration: BoxDecoration(
                              color: const Color(0xFF1E293B),
                              borderRadius: BorderRadius.circular(10),
                            ),
                          ),
                        ],
                      ),
                    ],
                  ),
                ),
              ),
            ),
            const SizedBox(height: 35),
            
            // GRILLE DES FONCTIONNALITÉS
            Expanded(
              child: GridView.count(
                crossAxisCount: 2,
                crossAxisSpacing: 16,
                mainAxisSpacing: 16,
                childAspectRatio: 1.5,
                children: [
                  _buildMenuCard(context, Icons.chat_bubble_rounded, 'Chat', 'Discuter avec l\'IA', const ChatPage()),
                  _buildMenuCard(context, Icons.mic_rounded, 'Voix', 'Parler avec OptiAI', const VoixPage()),
                  _buildMenuCard(context, Icons.remove_red_eye_rounded, 'Vision', 'Analyser des images', const VisionPage()),
                  _buildMenuCard(context, Icons.description_rounded, 'Documents', 'Analyser des fichiers', const DocumentPage()),
                ],
              ),
            ),
          ],
        ),
      ),
    );
  }

  static Widget _buildRobotEye() {
    return Container(
      width: 20,
      height: 20,
      decoration: const BoxDecoration(shape: BoxShape.circle, color: Color(0xFF60A5FA)),
      child: Center(
        child: Container(
          width: 8,
          height: 8,
          
