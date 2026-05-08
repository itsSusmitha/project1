# Harry Potter: Wizard Flight

A fully-featured magical browser game where you play as a young wizard from Hogwarts, flying on your broomstick through enchanted skies. Collect golden snitches, cast powerful spells, dodge dangerous dementors, and discover the unique abilities of your magical companion!

## 🎮 Features

### Immersive Gameplay
- **Fullscreen Canvas-Based Rendering** - Smooth 60FPS animations using requestAnimationFrame
- **Realistic Physics** - Movement inertia, floating animations, parallax cloud effects
- **Particle Effects** - Magical sparkles, energy waves, and visual feedback for all actions
- **Responsive Design** - Works perfectly on desktop, tablet, and mobile devices

### House System with Unique Abilities
Choose from 4 Hogwarts houses, each with special perks:

#### 🔴 Gryffindor
- **Bonus**: +2 extra points per snitch (17 instead of 15)
- **Companion**: Fire Phoenix
- **Ability**: Periodically shoots fire at enemies, dealing 1 hit per shot

#### 🟢 Slytherin
- **Bonus**: 25% faster movement speed for enhanced mobility
- **Companion**: Shadow Snake
- **Ability**: Poisons nearby enemies, slowing them by 50% for 4 seconds

#### 🔵 Ravenclaw
- **Bonus**: +10% score multiplier on all snitches
- **Companion**: Mystic Owl
- **Ability**: Reveals all spell orbs on screen with magical particles

#### 🟡 Hufflepuff
- **Bonus**: Start with 4 lives instead of 3
- **Companion**: Guardian Badger
- **Ability**: Generates a protective shield every 10 seconds that blocks dementor damage

### Magical Companion System
Your house companion follows you throughout the game with unique abilities:

- **Fire Phoenix** - Shoots flaming projectiles at enemies
  - Seeks nearest enemy within 400px
  - Activates every 3 seconds
  - Deals direct damage on hit

- **Shadow Snake** - Poisons nearby enemies
  - Affects all enemies within 250px range
  - Slows poisoned enemies by 50%
  - Activates every 4 seconds

- **Mystic Owl** - Reveals and enhances rewards
  - Highlights all spell orbs with sparkling effects
  - Grants +10% score bonus
  - Activates every 5 seconds

- **Guardian Badger** - Creates protective barriers
  - Generates a pulsing shield around the player
  - Lasts 5 seconds, blocks dementor hits
  - Activates every 10 seconds

### 5-Level Progressive Difficulty System

| Level | Name | Enemies | Speed | Spawn Rate | Special |
|-------|------|---------|-------|-----------|---------|
| 1 | Training Grounds | Normal | 1x | 1x | Introduction |
| 2 | Quidditch Pitch | Faster | 1.3x | 1.2x | Speed Boost |
| 3 | Forbidden Forest | Very Fast | 1.6x | 1.5x | Green Tint Atmosphere |
| 4 | Dark Storm | Extreme | 2x | 2x | Purple Tint Atmosphere |
| 5 | Final Battle | Boss Battle | Boss AI | Reduced | Giant Dark Lord Boss |

### Magical Collectibles

#### Golden Snitch
- Worth 15 points (17 for Gryffindor)
- Animated golden wings that flutter
- Leaves sparkle trails as it moves
- Target: 150 points to reach Level 5

#### Spell Orbs
Collect to temporarily gain powerful abilities:

1. **Expecto Patronum** (Blue)
   - Destroys all enemies on screen
   - Creates expanding wave rings
   - Grants 5-second invincibility to player
   - Spell Duration: 8 seconds (12 seconds for Ravenclaw)

2. **Lumos** (Gold)
   - Slows all enemies to 30% movement speed
   - Illuminates the screen with golden glow
   - Perfect for tactical positioning
   - Spell Duration: 8 seconds (12 seconds for Ravenclaw)

3. **Expelliarmus** (Orange)
   - Launches a force blast in all directions
   - Pushes all enemies away from player
   - Creates shockwave particle effects
   - Spell Duration: 8 seconds (12 seconds for Ravenclaw)

4. **Stupefy** (Pink)
   - Freezes all enemies in place
   - Enemies appear ghostly while frozen
   - Can be chained for continuous freezing
   - Spell Duration: 8 seconds (12 seconds for Ravenclaw)

### Enemy Types

#### Dementors
- **Appearance**: Tattered cloaks with glowing red eyes and smoke effects
- **Behavior**: Chase the player from right to left
- **Speed**: Increases with each level
- **Strategy**: Dodge or use spells to destroy them
- **Damage**: 1 life point per collision (with 2-second invincibility)

#### Dark Lord (Boss Battle)
- **Health**: 5 hits to defeat (using Expelliarmus or Stupefy)
- **Attacks**: Shoots green spells at the player
- **Screen Effects**: Shakes when attacking or taking damage
- **Victory**: Shows celebration particles and final score

## 🎮 How to Play

### Start Game
1. **Enter Your Wizard Name** - Maximum 20 characters
2. **Select Your House** - Choose from Gryffindor, Slytherin, Ravenclaw, or Hufflepuff
3. **Meet Your Companion** - Your magical companion appears based on your house
4. **Choose Character** - Select a character from your house to play as

### Controls

#### Desktop
- **Arrow Keys** - Move up/down/left/right
- **WASD** - Alternative movement controls

#### Mobile/Touch
- **On-Screen D-Pad** - Tap directional buttons to move
- **Responsive Touch Controls** - Optimized for all screen sizes

### Game Mechanics

- **Collect Golden Snitches** - +15 points (varies by house)
- **Grab Spell Orbs** - Activate powerful temporary spells
- **Avoid Dementors** - Each hit costs 1 life
- **Use Spells** - Select active spell via UI to use against enemies
- **Listen to Companion** - Your companion automatically uses its ability
- **Reach 150 Points** - Unlock Level 5 boss battle
- **Survive as Long as Possible** - Compete for high scores

### Strategy Tips

- **Gryffindor**: Use high bonus points to reach boss quickly
- **Slytherin**: Fast movement helps dodge many enemies
- **Ravenclaw**: Score multiplier builds up over time; focus on collecting
- **Hufflepuff**: Extra life and shield provide defensive advantages
- **Spell Management**: Use Lumos to slow enemies for easier dodging
- **Companion Synergy**: Let your companion do damage while you focus on collecting items
- **Movement**: Use inertia to your advantage for smooth, predictable movement

## 🛠 Technical Details

### Technology Stack
- **Framework**: React 19 with TypeScript
- **Rendering**: HTML5 Canvas API
- **Animation**: requestAnimationFrame (60 FPS)
- **Styling**: Tailwind CSS + Custom Shadows
- **Build**: Next.js 16 with Turbopack
- **Package Manager**: pnpm

### Browser Compatibility
- Chrome/Edge: Full support
- Firefox: Full support
- Safari: Full support
- Mobile Browsers: Full support with touch controls

### Performance
- Optimized for 60 FPS on desktop and mobile
- Efficient particle system with automatic cleanup
- Canvas rendering with shadow caching
- Smooth animations using CSS transforms

### Code Architecture

```
app/page.tsx
├── Types & Interfaces
│   ├── GameState
│   ├── Player
│   ├── Snitch
│   ├── SpellOrb
│   ├── Dementor
│   ├── Boss
│   └── Companion
├── Constants & Configs
│   ├── SPELLS
│   ├── COMPANION_CONFIGS
│   ├── HOUSE_COLORS
│   └── CHARACTER_CONFIGS
├── Game Rendering
│   ├── drawBackground
│   ├── drawPlayer
│   ├── drawSnitches
│   ├── drawSpellOrbs
│   ├── drawDementors
│   ├── drawBoss
│   ├── drawCompanion
│   └── drawUI
├── Game Logic
│   ├── Collision Detection
│   ├── Physics & Animation
│   ├── Spell Activation
│   ├── Companion Abilities
│   ├── Level Progression
│   └── Game State Management
└── UI Components
    ├── Start Screen
    ├── House Selection
    ├── Character Selection
    ├── Game Canvas
    ├── Game Over Screen
    └── Mobile Controls
```

## 📦 Installation & Setup

### Prerequisites
- Node.js 16+ and pnpm
- Modern web browser (Chrome, Firefox, Safari, Edge)

### Quick Start

1. **Clone the Repository**
```bash
git clone https://github.com/yourusername/harry-potter-wizard-flight.git
cd harry-potter-wizard-flight
```

2. **Install Dependencies**
```bash
pnpm install
```

3. **Run Development Server**
```bash
pnpm dev
```

4. **Open in Browser**
```
http://localhost:3000
```

5. **Build for Production**
```bash
pnpm build
pnpm start
```

### Deploy to Vercel

1. Push to GitHub
2. Import project to Vercel
3. Vercel auto-detects Next.js configuration
4. Deploy automatically on push

```bash
vercel deploy
```

## 🎨 Visual Features

### Animations & Effects
- **Smooth Floating** - Wizard, companions, and collectibles bob smoothly
- **Magical Auras** - Glowing effects around player and items
- **Particle Systems** - 15+ particle types for different effects
- **Screen Shake** - Boss attacks create impact feedback
- **Fade Transitions** - Smooth screen transitions between game states
- **Star Field** - Twinkling stars in the background
- **Cloud Parallax** - Multi-layer clouds for depth

### Color Scheme
- **Background**: Deep navy (#050510) with mystical atmosphere
- **Hogwarts Castle**: Dark architecture with golden lights
- **UI Elements**: Gold accents (#FFD700) for magical feel
- **House Colors**: Unique themed colors per house
- **Spell Orbs**: Distinct colors for each spell type
- **Glow Effects**: Subtle magical glow with shadows

## 📊 Game Statistics

### Default Stats
- **Starting Lives**: 3 (4 for Hufflepuff)
- **Snitch Points**: 15 (17 for Gryffindor, 16.5 avg for Ravenclaw)
- **Boss Health**: 5 hits
- **Spell Duration**: 8 seconds (12 for Ravenclaw)
- **Max Players**: Unlimited concurrent sessions
- **Data Storage**: Client-side only (browser storage)

## 🐛 Known Issues & Limitations

- Game state resets on page refresh (no persistence)
- Mobile controls work best on landscape orientation
- Some older browsers may have reduced animation smoothness

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs via GitHub Issues
- Suggest new features
- Submit pull requests with improvements

## 📄 License

This project is open source and available under the MIT License.

## 🎓 Educational Value

This game demonstrates:
- Canvas API and drawing primitives
- Game loop architecture with requestAnimationFrame
- Collision detection algorithms
- Physics simulation (movement, inertia, gravity)
- Particle system implementation
- State management in React
- TypeScript type safety
- Responsive design patterns
- Performance optimization techniques

## 🔮 Future Enhancements

Potential features for future versions:
- High score leaderboard with local storage
- Additional house companions with unique animations
- More spell types and power-ups
- Multiple boss battles
- Difficulty modifiers
- Sound effects and background music
- Achievements and badges system
- Multiplayer competitive mode
- Customizable game difficulty settings

## 📞 Support

For questions or issues, please:
1. Check existing GitHub Issues
2. Create a new Issue with detailed description
3. Include screenshots if applicable
4. Describe steps to reproduce bugs

## 🎮 Game Credits

- **Game Design & Development**: Built with React and Canvas API
- **Inspiration**: Harry Potter universe and magical themes
- **Assets**: Procedurally generated via Canvas drawing
- **Sounds**: (Future enhancement)
- **Music**: (Future enhancement)

---

**Enjoy your magical adventure in Harry Potter: Wizard Flight!** ⚡🧙‍♂️✨
