# Sell My Pet Food — PLTW AP CSA Unit 2 Project

AP Computer Science A project — an automated e-commerce sentiment analysis tool that scrapes Amazon product reviews and generates marketing copy.

## Features

- **Amazon Review Scraping**: Automated product search and review extraction via Selenium WebDriver
- **Sentiment Analysis**: TensorFlow Java API model for positive/negative review classification
- **Social Media Post Generation**: Automatically curates positive reviews into shareable social media posts
- **Advertisement Curation**: Separates positive and negative feedback for targeted marketing

## Tech Stack

- **Language**: Java 21
- **Build**: Maven (POM)
- **Web Automation**: Selenium Java 4.18.1 (SafariDriver)
- **ML Inference**: TensorFlow Java API (`org.tensorflow`)
- **Target**: Amazon.com review pages

## Project Structure

```
src/main/java/org/example/
├── Main.java              -- Entry point with scraping, analysis, and file output

socialmediaposts.txt       -- Generated positive review posts (output)
advertisement.txt          -- Curated positive advertisement copy (output)
pom.xml                    -- Maven build configuration
```

## Setup

```bash
# Build the project
mvn clean compile

# Run (requires Safari with remote automation enabled)
mvn exec:java -Dexec.mainClass="org.example.Main"
```

## Output

- `socialmediaposts.txt` — Positive reviews formatted as quotable social media content
- `advertisement.txt` — Aggregated positive feedback for marketing use

## Note

This project uses Safari's native WebDriver. For cross-browser support, replace `SafariDriver` with `ChromeDriver` or `FirefoxDriver` and update the POM accordingly.
