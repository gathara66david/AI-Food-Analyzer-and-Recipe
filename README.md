# AI-Powered Food Image Analysis & Recipe System 🍳📸

[![Python 3.10+](https://img.shields.io/badge/python-3.10%2B-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

An intelligent system that analyzes food images and recommends recipes using Gemini AI models and ChromaDB.

![Demo Visualization](https://via.placeholder.com/800x400.png?text=Food+Analysis+%26+Recipe+Recommendation+Demo)

## Features ✨

- **Multi-Stage Food Analysis**
  - Basic ingredient detection
  - Enhanced meal suggestions with confidence scores
  - Knowledge-enhanced recipe generation
- **Dynamic Recipe Management**
  - Vector database storage (ChromaDB)
  - Semantic recipe retrieval
  - AI-generated recipe synthesis
- **Robust Visualization**
  - Interactive ingredient charts
  - Beautiful HTML recipe cards
  - Analysis comparison tables
- **Production-Ready**
  - Comprehensive error handling
  - Metadata validation
  - Performance tracking

## Installation 💻

```bash
git clone https://github.com/yourusername/food-ai-system.git
cd food-ai-system

# Install dependencies
pip install -r requirements.txt
```

**Requirements:**
- Python 3.10+
- Google API key (for Gemini)
- ChromaDB 1.0+

## Usage 🚀

1. **Configure API Keys**
```python
from kaggle_secrets import UserSecretsClient
user_secrets = UserSecretsClient()
genai.configure(api_key=user_secrets.get_secret("GOOGLE_API_KEY"))
```

2. **Run Analysis Pipeline**
```python
from core import analyze_food_image

# Analyze sample images
analyze_food_image("/path/to/food_image.jpg")
```

3. **Expected Output**
```
🔍 Analyzing food_image.jpg
✅ Analysis completed in 8.2s

📊 Detected Ingredients:
- Chicken breast (cooked)
- Rice (steamed)
- Broccoli (fresh)

🍴 Top Recommendations:
1. Chicken Stir-Fry Bowl (0.92 confidence)
2. Meal Prep Protein Box (0.85 confidence)
```

## Database Structure 🗃️

```python
{
  "id": "unique_recipe_id",
  "metadata": {
    "meal_type": "dinner",
    "difficulty": "medium",
    "cuisine": "asian",
    "prep_time": 25,
    "tags": "protein,quick,healthy"
  },
  "document": "Recipe text with ingredients and steps"
}
```

## API Reference 📚

| Function | Description |
|----------|-------------|
| `basic_vision_analysis()` | Extract ingredients from image |
| `enhanced_analysis()` | Get meal suggestions + nutrition estimates |
| `knowledge_enhanced_analysis()` | Full recipe generation pipeline |
| `display_recipe_card()` | Render HTML recipe visualization |

## Contributing 🤝

I welcome contributions! Please follow these guidelines:
1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License 📄

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments 🙏

- Google Gemini AI Team
- ChromaDB Developers
- Kaggle Community

--
