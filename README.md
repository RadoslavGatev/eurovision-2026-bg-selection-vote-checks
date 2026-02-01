# Eurovision 2026 Bulgaria National Selection - Vote Discrepancy Analysis

This repository contains evidence documenting discrepancies between the official voting results announced on Bulgarian National Television (BNT) during the Eurovision 2026 national selection final and the actual data returned by the voting system's API.

## Background

On the night of January 31, 2026, BNT held the national selection final to choose Bulgaria's representative for Eurovision 2026. After the broadcast, viewers discovered that the voting results API endpoint (`https://voteapi31.eurovision2026.bg/results`) was still accessible and returning data that did not match the results announced on television.

## Evidence

### API Response Data

The file `results-payload.json` contains the JSON response from the official voting API, showing the actual vote counts and jury points for each contestant.

### Comparison with TV Broadcast

The `comparison.xlsx` spreadsheet and `comparison.png` image show a side-by-side comparison of the API data versus the results announced on television. Cells highlighted in red indicate discrepancies.

![Comparison of API data vs TV broadcast results](comparison.png)

### Visual Evidence

- `youtube-results.jpg` / `youtube-results-highlighted.png` - Screenshots from the [official BNT YouTube broadcast](https://youtu.be/Oan0V5gDBWw?t=12193) showing the announced results

![Screenshot from official BNT YouTube broadcast showing the announced results](youtube-results-highlighted.png)

### Network Traffic Capture

The file `voteapi31.eurovision2026.bg.har` is an HTTP Archive (HAR) file containing the full network request/response to the voting API endpoint, captured on February 1, 2026 at 09:13:42 UTC.

### Social Media Screenshots

The `screenshots-from-social/` directory contains screenshots from social media posts discussing the discrepancies.

## Technical Details

The voting API was hosted at `https://voteapi31.eurovision2026.bg/results` and returned JSON data with:
- Total vote count
- Per-contestant vote counts
- Jury points per contestant
- Voting status and timestamps

The API response was served via Cloudflare and configured with CORS headers allowing requests from `https://vote.eurovision2026.bg`.

## Purpose

This repository serves as a public record of the evidence for transparency and accountability purposes. The data suggests that the results announced on television may have been altered from the actual voting system data.

## Disclaimer

This repository is for informational and transparency purposes only. All data was obtained from publicly accessible sources.

## License

The evidence and documentation in this repository are provided for public interest and journalistic purposes.
