# Data Alchemist

A powerful AI-driven data transformation and resource allocation platform that transforms messy CSV and Excel files into clean, validated datasets with intelligent insights and automated processing.

## 🚀 Features

### Core Functionality
- **Smart File Upload**: Support for CSV and Excel files with AI-powered column mapping
- **Intelligent Data Parsing**: Automatic detection and mapping of data columns using AI
- **Advanced Validation**: Comprehensive data quality checks with 15+ validation rules
- **Real-time Error Detection**: Instant feedback on data quality issues
- **Interactive Data Grids**: Edit and validate data in real-time
- **Natural Language Search**: Query your data using plain English

### AI-Powered Features
- **AI Assistant**: Generate business rules from natural language instructions
- **Data Cleaning Suggestions**: AI-powered recommendations for fixing data issues
- **Validation Explanations**: Plain English explanations of data problems
- **Rule Optimization**: Analyze and optimize business rules for better performance

### Business Logic
- **Business Rules Engine**: Create and manage complex allocation rules
- **Prioritization Weights**: Configure allocation priorities using multiple methods
- **Resource Allocation**: Intelligent matching of tasks to workers based on skills and availability
- **Drag & Drop Ranking**: Visual prioritization interface
- **Pairwise Comparison**: AHP-based decision making

### Export & Integration
- **Multiple Export Formats**: CSV, Excel, and JSON export options
- **Bulk Export**: Export all data types simultaneously
- **Configuration Export**: Save business rules and prioritization settings

## 🛠️ Technology Stack

- **Frontend**: Next.js 13, React 18, TypeScript
- **UI Components**: Radix UI, Tailwind CSS
- **State Management**: Zustand
- **File Processing**: XLSX, PapaParse
- **AI Integration**: OpenAI GPT-4 API
- **Charts**: Recharts
- **Notifications**: Sonner

## 📋 Prerequisites

- Node.js 18+ 
- npm or yarn
- OpenAI API key (for AI features)

## 🚀 Getting Started

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd data-alchemist
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the development server**
   ```bash
   npm run dev
   ```

4. **Open your browser**
   Navigate to `http://localhost:3000`

## 📊 Data Format Requirements

### Clients Data
Required columns:
- `ClientID` - Unique identifier
- `ClientName` - Client name
- `PriorityLevel` - Priority (1-5)

Optional columns:
- `RequestedTaskIDs` - Comma-separated task IDs
- `GroupTag` - Client grouping
- `AttributesJSON` - Additional attributes in JSON format
- `Email`, `Phone`, `Address` - Contact information

### Workers Data
Required columns:
- `WorkerID` - Unique identifier
- `WorkerName` - Worker name
- `Skills` - Comma-separated skills list
- `AvailableSlots` - Available phase numbers
- `MaxLoadPerPhase` - Maximum tasks per phase

Optional columns:
- `WorkerGroup` - Worker grouping
- `QualificationLevel` - Skill level
- `Email` - Contact information

### Tasks Data
Required columns:
- `TaskID` - Unique identifier
- `TaskName` - Task name
- `Duration` - Number of phases required
- `MaxConcurrent` - Maximum parallel assignments

Optional columns:
- `Category` - Task category
- `RequiredSkills` - Comma-separated required skills
- `PreferredPhases` - Preferred execution phases
- `AttributesJSON` - Additional attributes

## 🤖 AI Features Setup

1. **Get OpenAI API Key**
   - Visit [OpenAI Platform](https://platform.openai.com/api-keys)
   - Create a new API key

2. **Configure AI Assistant**
   - Navigate to the AI Assistant page
   - Enter your OpenAI API key
   - Start using AI-powered features

## 🔧 Configuration

### Business Rules
Create rules for:
- **Co-location**: Tasks that must run together
- **Slot Restriction**: Time-based constraints
- **Load Limit**: Worker capacity limits
- **Phase Window**: Phase-specific timing
- **Custom**: Custom business logic

### Prioritization Weights
Configure allocation priorities:
- Priority Level (30%)
- Fulfillment (25%)
- Fairness (20%)
- Efficiency (15%)
- Skill Match (10%)

## 📁 Project Structure

```
data-alchemist/
├── app/                    # Next.js app directory
│   ├── ai-assistant/      # AI features page
│   ├── clients/           # Client management
│   ├── workers/           # Worker management
│   ├── tasks/             # Task management
│   ├── upload/            # File upload interface
│   ├── validations/       # Data validation results
│   ├── rules/             # Business rules management
│   ├── prioritization/    # Priority configuration
│   └── export/            # Data export options
├── components/            # Reusable UI components
│   ├── ui/               # Base UI components
│   ├── ai/               # AI-specific components
│   ├── data-grid/        # Data editing components
│   ├── layout/           # Layout components
│   └── upload/           # Upload components
├── lib/                  # Core business logic
│   ├── ai-service.ts     # AI integration
│   ├── file-parser.ts    # File processing
│   ├── validation.ts     # Data validation
│   ├── export.ts         # Export functionality
│   └── types.ts          # TypeScript definitions
└── public/               # Static assets
```

## 🚀 Deployment

### Build for Production
```bash
npm run build
```

### Static Export
The application is configured for static export and can be deployed to any static hosting service:

```bash
npm run build
```

The built files will be in the `out/` directory.

### Deployment Options
- **Vercel**: Automatic deployment from GitHub
- **Netlify**: Drag and drop the `out/` folder
- **GitHub Pages**: Upload the `out/` folder contents
- **Any static hosting**: Upload the `out/` folder

## 🔍 Usage Examples

### 1. Upload and Validate Data
1. Navigate to Upload Data
2. Drag and drop your CSV/Excel files
3. Review AI parsing suggestions
4. Check validation results
5. Fix any errors using the data grid

### 2. Create Business Rules
1. Go to Business Rules
2. Click "Create Rule"
3. Choose rule type (co-location, load-limit, etc.)
4. Configure conditions and actions
5. Activate the rule

### 3. Configure Prioritization
1. Visit Prioritization page
2. Adjust weights using sliders
3. Or use drag & drop ranking
4. Or complete pairwise comparisons
5. Save your configuration

### 4. Export Clean Data
1. Navigate to Export page
2. Choose format (CSV/Excel)
3. Select individual or bulk export
4. Download your clean data

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

For support and questions:
- Create an issue in the GitHub repository
- Check the documentation in the app
- Review the validation guide for data format requirements

## 🔮 Roadmap

- [ ] Advanced AI models integration
- [ ] Real-time collaboration features
- [ ] API endpoints for external integration
- [ ] Advanced analytics and reporting
- [ ] Multi-language support
- [ ] Database integration options
- [ ] Workflow automation
- [ ] Advanced visualization tools

---

**Data Alchemist** - Transform your data with the power of AI 🧪✨
