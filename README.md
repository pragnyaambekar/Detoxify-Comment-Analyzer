# Detoxify-Comment-Analyzer
A Python tool for analyzing toxic content in comment datasets using the Detoxify ML model. Detects multiple categories of toxicity (obscenity, threats, insults, identity attacks) and generates comprehensive reports on content toxicity distribution. Perfect for content moderation, online community health analysis, and toxic communication research.

**Overview**
This project provides a comprehensive solution for analyzing comment toxicity in CSV datasets. It uses the Detoxify library (which leverages transformer-based models) to detect various forms of toxic content such as obscenity, threats, insults, and identity-based attacks.
The tool processes CSV files containing comment data, analyzes each comment for different categories of toxicity, and generates detailed reports on the distribution of toxic content.

**Features**
Multi-category Toxicity Analysis: Detects and categorizes multiple types of toxic content
Progress Monitoring: Real-time processing feedback with speed metrics and time estimation
Comprehensive Result Classification: Identifies primary toxicity type for each comment
Distribution Reporting: Generates statistical breakdowns of toxicity in your dataset
Customizable Thresholds: Adjustable sensitivity for toxicity classification

**Installation**
bashCopy# Clone the repository
git clone https://github.com/yourusername/detoxify-comment-analyzer.git
cd detoxify-comment-analyzer

# Install required packages
pip install -r requirements.txt
**Requirements**
Python 3.7+
pandas
detoxify
time (standard library)

**Usage**
Basic Usage

pythonCopyfrom detoxify_analyzer import analyze_toxicity, get_toxicity_distribution

# Analyze a CSV file containing comments
results = analyze_toxicity("your_comments.csv", save_results=True)

# Get distribution of toxicity types
toxicity_distribution = get_toxicity_distribution(results)

**Input Format**
The tool expects a CSV file with at least a comment_text column containing the comments to analyze.

**Parameters**
csv_file_path: Path to the CSV file containing comments
save_results: Whether to save results to a new CSV file (default: True)
sample_size: Number of comments to analyze (default: None, analyzes all)

**Output**
The tool generates:
A new CSV file with toxicity scores and classifications
A statistical summary of toxicity distribution

**How It Works**

**Data Loading:** Reads the CSV file containing comments
**Model Initialization:** Loads the Detoxify ML model
**Text Processing:** Analyzes each comment for toxicity scores
**Classification:** Determines primary toxicity type based on scores
**Results Compilation:** Aggregates results and generates statistics

**Functions**

**analyze_toxicity(csv_file_path, save_results=True, sample_size=None)**
Processes a CSV file containing comments and analyzes their toxicity.

**get_primary_toxicity(row)**
Determines the main type of toxicity for each comment.

**get_toxicity_distribution(df)**
Summarizes the distribution of toxicity types in your dataset.

**Applications**
Content Moderation: Identify toxic comments in user-generated content
Community Health Analysis: Assess the health of online communities
Research: Study patterns of toxic communication in different contexts
Content Filtering: Develop systems to filter out harmful content
