# Healthcare Triage Chatbot - AI-Powered Medical Assistant for India

An intelligent conversational healthcare assistant designed for India that processes patient-provided natural language input to assess health conditions, classify risk levels, and provide appropriate guidance while maintaining strict safety and compliance standards.

## 🎯 Problem Statement

Patients often describe health issues in unstructured language, leading to:
- Delayed diagnosis of serious conditions
- Unnecessary hospital visits for minor ailments
- Lack of intelligent systems that can safely assess severity and guide users to appropriate care

## 🚀 Solution Overview

The Healthcare Triage Chatbot is a **safety-first AI system** that:
- Understands patient symptoms expressed in natural language (text/voice)
- Extracts medical information using advanced NLP
- Uses hybrid reasoning (rule-based + ML) for risk assessment
- Classifies conditions into LOW, MODERATE, or SEVERE risk levels
- Provides appropriate care recommendations and provider matching

## 🏥 Core Features

### 1. Natural Language Processing
- Text and voice input support
- Multi-language support for Indian languages
- Symptom, duration, and severity extraction
- Medical history parsing

### 2. Safety-First Risk Detection
- Rule-based emergency red-flag detection
- Critical symptom combination analysis
- **Emergency rules always override ML predictions**
- Immediate escalation for life-threatening conditions

### 3. Hybrid Risk Classification
- Three-tier system: LOW, MODERATE, SEVERE
- Rule-based medical guidelines
- Machine learning condition prediction
- Conflict resolution favoring higher risk

### 4. Risk-Based Recommendations

**LOW Risk:**
- Self-care guidance
- Over-the-counter medication suggestions
- Monitoring and follow-up advice

**MODERATE Risk:**
- Targeted assessment questions
- Diagnostic test suggestions
- Specialist/department routing

**SEVERE Risk:**
- Immediate medical attention
- Emergency provider recommendations
- Location-based hospital suggestions

### 5. Healthcare Provider Matching
- Location proximity
- Provider experience and specialization
- Affordability and availability
- Patient reviews and ratings

## 🛡️ Safety & Compliance

✅ **Never claims to provide medical diagnosis**  
✅ **Never prescribes prescription medications**  
✅ **Emergency red-flag rules override ML predictions**  
✅ **All outputs are explainable and transparent**  
✅ **Healthcare data privacy compliance**  
✅ **Mandatory disclaimers about AI limitations**

## 👥 Target Users

- General public (urban and rural India)
- First-time healthcare seekers
- Chronic disease patients
- Hospitals and clinics
- Doctors and specialists

## 🏗️ Architecture

The system follows a **microservices architecture** with safety-first design:

```
Patient Input → NLP Engine → Red Flag Detector → Risk Classifier → Recommendations → Provider Matching
                                    ↓
                            Emergency Override
                                    ↓
                            Immediate Escalation
```

### Key Components:
- **Input Processing Service** - Text/voice handling
- **NLP Engine** - Medical information extraction
- **Red Flag Detector** - Emergency condition detection
- **ML Risk Classifier** - Condition prediction
- **Recommendation Engine** - Care guidance generation
- **Provider Matching Service** - Healthcare provider recommendations

## 🛠️ Technology Stack

### Backend
- **Python** - Core implementation language
- **FastAPI** - REST API framework
- **Pydantic** - Data validation

### NLP & AI
- **spaCy** - Natural language processing
- **Medical NER Models** - Medical entity recognition
- **scikit-learn** - Machine learning models
- **Custom ML Models** - Medical condition prediction

### Testing
- **pytest** - Unit testing framework
- **Hypothesis** - Property-based testing
- **100+ iterations per property test**

### Data Storage
- **PostgreSQL** - Structured data
- **Redis** - Session management
- **Elasticsearch** - Medical knowledge base

### Infrastructure
- **Docker** - Containerization
- **Kubernetes** - Orchestration
- **Prometheus** - Monitoring
- **ELK Stack** - Logging

## 📁 Project Structure

```
healthcare-triage-chatbot/
├── .kiro/
│   └── specs/
│       └── healthcare-triage-chatbot/
│           ├── requirements.md      # Detailed requirements with acceptance criteria
│           ├── design.md           # System design and architecture
│           └── tasks.md            # Implementation task list
├── healthcare-triage-architecture.md  # Architecture diagrams (Mermaid)
├── generate_architecture_images.py    # Script to generate diagram images
└── README.md                          # This file
```

## 📋 Documentation

### Requirements Document
Comprehensive requirements following EARS patterns with:
- 10 major requirements
- 50+ acceptance criteria
- Safety and compliance constraints
- Multi-user support specifications

👉 **[View Requirements](.kiro/specs/healthcare-triage-chatbot/requirements.md)**

### Design Document
Detailed system design including:
- Microservices architecture
- Component interfaces and data models
- 18 correctness properties for testing
- Risk classification logic
- Explainability approach
- Scalability considerations

👉 **[View Design](.kiro/specs/healthcare-triage-chatbot/design.md)**

### Implementation Plan
Step-by-step task breakdown with:
- 15 major tasks with 30+ sub-tasks
- Property-based testing for all correctness properties
- Safety-first development sequence
- Checkpoint validations

👉 **[View Tasks](.kiro/specs/healthcare-triage-chatbot/tasks.md)**

### Architecture Diagrams
Visual representations of:
- High-level system architecture
- Detailed component architecture
- Data flow sequences
- Microservices deployment
- Safety-first decision flow
- Technology stack

👉 **[View Architecture Diagrams](healthcare-triage-architecture.md)**

## 🚦 Getting Started

### Prerequisites
- Python 3.9+
- Node.js (for Mermaid diagram generation)
- Docker (optional, for containerization)

### Generate Architecture Diagrams as Images

**Option 1: Online (Easiest)**
1. Visit https://mermaid.live/
2. Copy diagrams from `healthcare-triage-architecture.md`
3. Download as PNG/SVG

**Option 2: Command Line**
```bash
# Install mermaid-cli
npm install -g @mermaid-js/mermaid-cli

# Run the generator script
python generate_architecture_images.py
```

### Implementation

Follow the tasks in order from `tasks.md`:
1. Set up project structure and core interfaces
2. Implement input processing and validation
3. Build NLP engine for medical information extraction
4. Implement safety-first red flag detection
5. Create hybrid risk classification system
6. Build recommendation engine
7. Implement provider matching service
8. Add safety constraints and compliance features
9. Build explainability features
10. Implement multi-user support
11. Add error handling and reliability
12. Integration and system wiring
13. Create main application interface
14. Final validation and testing

## 🧪 Testing Strategy

### Property-Based Testing
- 18 correctness properties validated across all inputs
- Minimum 100 iterations per property test
- Safety invariants that must never be violated

### Unit Testing
- Specific medical scenarios and edge cases
- Component integration testing
- Error handling validation

### Key Properties Tested
- Natural language input processing
- Complete medical information extraction
- Emergency detection priority
- Emergency override safety
- Risk classification completeness
- Risk-appropriate recommendations
- Medical safety constraints
- Comprehensive explainability

## 🌍 Indian Context Adaptations

- **Multi-language Support** - Hindi, English, and regional languages
- **Cultural Considerations** - Urban and rural user adaptations
- **Local Healthcare Integration** - Indian hospital and clinic databases
- **Affordability Focus** - Cost-based provider filtering
- **Accessibility** - Voice input for low-literacy users

## 📊 Correctness Properties

The system validates 18 correctness properties including:

1. Natural Language Input Processing
2. Complete Medical Information Extraction
3. Emergency Detection Priority
4. Emergency Override Safety
5. Emergency Response Consistency
6. Risk Classification Completeness
7. Risk-Appropriate Recommendations
8. Comprehensive Provider Matching
9. Medical Safety Constraints
10. Medication Recommendation Safety
11. Mandatory Disclaimers
12. Comprehensive Explainability
13. User-Appropriate Communication
14. Chronic Condition Integration
15. Graceful Error Handling
16. Low Confidence Clarification
17. Higher Risk Prioritization
18. Multilingual Processing

## 🤝 Contributing

This is a hackathon project focused on architectural vision and product thinking for real-world impact in India's healthcare system.

## 📄 License

This project is designed as a conceptual architecture and specification for educational and hackathon purposes.

## 🎓 Acknowledgments

- Designed with safety-first principles for healthcare AI
- Follows EARS (Easy Approach to Requirements Syntax) patterns
- Implements property-based testing methodology
- Adheres to INCOSE requirements quality standards

## 📞 Contact

For questions about this architecture or implementation guidance, please refer to the detailed documentation in the `.kiro/specs/` directory.

---

**⚠️ Important Disclaimer:** This is a conceptual design for an AI healthcare triage system. Any real-world implementation must undergo rigorous medical validation, regulatory approval, and compliance with healthcare standards before deployment.

**🏥 Safety First:** Emergency detection always takes priority over AI predictions to ensure patient safety is never compromised.
