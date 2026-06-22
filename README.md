# Automated Role-Based Airtable Routing

An automated talent screening pipeline that categorizes incoming job applications (AI Engineer, Graphic Designer, Data Scientist) and logs them into Airtable. It then leverages a Google Gemini AI agent to assess the submission and automatically updates the candidate's record with a final rating.

## 🎯 Features

- **Automatic Application Categorization** - Intelligently routes job applications to appropriate role categories
- **Airtable Integration** - Seamlessly logs candidate information into structured Airtable bases
- **AI-Powered Assessment** - Uses Google Gemini AI to evaluate candidate submissions
- **Automated Rating System** - Generates and stores candidate ratings automatically
- **Role-Based Workflow** - Specialized handling for:
  - AI Engineer positions
  - Graphic Designer positions
  - Data Scientist positions

## 📋 Prerequisites

Before you begin, ensure you have the following:

- Python 3.8 or higher
- [Airtable API Key](https://support.airtable.com/hc/en-us/articles/219046677-API-overview)
- [Google Gemini API Key](https://ai.google.dev/)
- Required Python packages (see Installation section)

## 🚀 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/maryam-javaid/Automated-Role-Based-Airtable-Routing.git
   cd Automated-Role-Based-Airtable-Routing
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure environment variables**
   
   Create a `.env` file in the root directory:
   ```env
   AIRTABLE_API_KEY=your_airtable_api_key
   AIRTABLE_BASE_ID=your_airtable_base_id
   GEMINI_API_KEY=your_google_gemini_api_key
   ```

## 🔧 Configuration

### Airtable Setup

1. Create an Airtable base with a table for candidates
2. Ensure your table includes the following fields:
   - Name
   - Email
   - Role Category
   - Submission/Resume
   - AI Rating
   - Assessment Results

### Google Gemini Setup

1. Enable the Google Generative AI API in your Google Cloud Console
2. Create an API key for your application
3. Store it in your `.env` file

## 📖 Usage

### Running the Application

```bash
python main.py
```

### Application Workflow

1. **Submission Intake** - Receives job application submissions
2. **Role Classification** - Automatically categorizes applications by role type
3. **Airtable Logging** - Records candidate information in the appropriate Airtable base
4. **AI Assessment** - Google Gemini evaluates the candidate's qualifications
5. **Rating Update** - Automatically updates the candidate's record with the AI-generated rating

## 📁 Project Structure

```
Automated-Role-Based-Airtable-Routing/
├── main.py              # Entry point for the application
├── requirements.txt     # Python dependencies
├── .env.example         # Example environment variables
├── README.md            # This file
└── [additional files]   # Supporting modules and utilities
```

## 🔌 API Integrations

### Airtable
- **Purpose**: Store and manage candidate records
- **Documentation**: [Airtable API Docs](https://airtable.com/developers/web/api/introduction)

### Google Gemini
- **Purpose**: AI-powered candidate assessment and evaluation
- **Documentation**: [Google Gemini API Docs](https://ai.google.dev/)

## 🛠️ Troubleshooting

### Common Issues

**API Key Errors**
- Verify your `.env` file is correctly configured
- Ensure API keys have the necessary permissions
- Check that keys are not accidentally committed to version control

**Airtable Connection Issues**
- Confirm Base ID and API Key are correct
- Verify table field names match configuration
- Check network connectivity

**Gemini Assessment Failures**
- Ensure Gemini API quota has not been exceeded
- Verify submission format is compatible with AI processing

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request or open an Issue for bugs and feature requests.

## 📝 License

This project is open source and available under the MIT License. See LICENSE file for more details.

## 📧 Contact

For questions or support, please reach out to maryamjavaidbcs164@gmail.com or open an issue on GitHub.

## 🙏 Acknowledgments

- [Airtable](https://airtable.com/) for the database and automation platform
- [Google AI](https://ai.google.dev/) for the Gemini AI capabilities
- All contributors and users who help improve this project

---

**Last Updated**:June 22, 2026
