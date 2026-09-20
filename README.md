# EarningsCall

**Earnings call transcripts, audio, slide decks, and earnings calendar for 9,000+ public companies. One API.**

EarningsCall provides developers, quants, and researchers with programmatic access to structured earnings call data, with many transcripts available within 15 minutes of each call ending.

---

## What We Offer

### API
REST API and official Python and JavaScript SDKs for accessing:
- Earnings call transcripts with speaker-level data
- Q&A and prepared remarks segmented separately
- Raw MP3/WAV audio files
- Investor slide decks
- Earnings event calendar
- Real-time webhook notifications

Covers 9,000+ publicly traded companies across NYSE, NASDAQ, and global exchanges with 5 years of historical data.

### Mobile App
Real-time access to earnings call data on iOS and Android. Stay updated on earnings calls while on the go.

---

## Quick Start

```bash
pip install --upgrade earningscall
```

```python
from earningscall import get_company
from datetime import date
from earningscall import get_calendar

company = get_company("aapl")
transcript = company.get_transcript(year=2026, quarter=2)

# Access speaker-level data
for speaker in transcript.speakers:
    print(f"{speaker.speaker_info.name} ({speaker.speaker_info.title})")
    print(speaker.text[:200])

# Download audio file
company.download_audio_file(year=2026, quarter=2, file_name="AAPL-Q2-2026.mp3")

# Download slide deck
company.download_slide_deck(year=2026, quarter=2, file_name="AAPL-Q2-2026-Slides.pdf")

# Get earnings calendar
calendar = get_calendar(date(2026, 9, 20))
for event in calendar:
    print(f"{event.company_name} - Q{event.quarter} {event.year} on: {event.conference_date.astimezone().isoformat()}")
```

For full documentation and examples, visit the [API Documentation](https://earningscall.biz/api-guide) page. To learn more about transcript data and coverage, see the [Earnings Call Transcripts API](https://earningscall.biz/earnings-transcripts-api) page.

---

## Key Features

- **Speaker-level transcripts:** every word mapped to the speaker who said it
- **Q&A segmentation:** prepared remarks and analyst Q&A separated automatically
- **Audio files:** MP3/WAV download for every covered earnings call
- **Slide decks:** investor presentation slides alongside transcripts
- **Earnings calendar:** upcoming earnings event data via API
- **Real-time notifications:** webhook alerts when new transcripts are available
- **Python and JavaScript SDKs:** official clients for fast integration

---

## Pricing

Plans start at $60/month. No annual lock-in. 7-day money-back guarantee.

[View Pricing](https://earningscall.biz/api-pricing)

---

## Use Cases

**Backtesting**
Quants and algorithmic traders use earnings call transcripts as a signal source, testing how management tone, guidance language, and Q&A sentiment correlate with post-earnings price movement.

**Trading Applications**
Fintech builders embed EarningsCall data into trading platforms and analytics tools, giving their users access to structured transcript data and audio alongside market data.

**Dashboards**
Teams build internal dashboards that pull transcripts and earnings calendar data to monitor portfolio companies, track executive commentary, and flag guidance changes automatically.

**Internal Research**
Investment firms and analysts use EarningsCall to speed up equity research, pulling transcripts programmatically instead of reading PDFs or watching recordings manually.

**Sentiment and NLP**
Data scientists build sentiment models, topic classifiers, and named entity extraction pipelines on top of speaker-level transcript data from thousands of companies.

**AI Agents**
Developers building financial AI agents and copilots connect EarningsCall to their LLM pipelines to answer questions about what management said on any earnings call.

**Academic Research**
Universities and research institutions use EarningsCall to build financial NLP datasets, reproduce published studies, and run new research on management communication and market behavior.

---

## Who Uses EarningsCall

- **Developers:** building financial data apps and NLP pipelines
- **Quants and researchers:** event-driven strategies and sentiment analysis
- **Institutional investors:** tracking management tone and guidance
- **Academic researchers:** financial NLP datasets and studies
- **Finance professionals:** faster equity research

---

## Resources

- [Earnings Call Transcripts API](https://earningscall.biz/earnings-transcripts-api)
- [API Documentation](https://earningscall.biz/api-guide)
- [Python SDK](https://github.com/EarningsCall/earningscall-python)
- [JavaScript SDK](https://github.com/EarningsCall/earningscall-js)
- [Website](https://earningscall.biz)
- [iOS App](https://apps.apple.com/us/app/earnings-call/id1626859464)
- [Android App](https://play.google.com/store/apps/details?id=biz.earningscall.app)

---

## Mission

To give developers and analysts reliable, structured access to earnings call data, without scraping, parsing, or waiting.

---

© EarningsCall LLC 2026
