Welcome to [Domains Project](http://domainsproject.org)!
==========

[![Domain count](https://img.shields.io/badge/domains-164%20million-brightgreen)](https://github.com/tb0hdan/domains/blob/master/STATS.md)
[![GitHub stars](https://img.shields.io/github/stars/tb0hdan/domains?style=social)](https://github.com/tb0hdan/domains/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/tb0hdan/domains?style=social)](https://github.com/tb0hdan/domains/network/members)
![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/tb0hdan/domains)
![GitHub repo size](https://img.shields.io/github/repo-size/tb0hdan/domains)
[![GitHub issues](https://img.shields.io/github/issues/tb0hdan/domains)](https://github.com/tb0hdan/domains/issues)
[![GitHub license](https://img.shields.io/github/license/tb0hdan/domains)](https://github.com/tb0hdan/domains/blob/master/LICENSE)
[![GitHub commit activity](https://img.shields.io/github/commit-activity/w/tb0hdan/domains)](https://github.com/tb0hdan/domains/commits/master)

# Sorted list of internet domains

This dataset was created as an experiment with hopes of being useful.

[Dataset statistics](STATS.md)

## Milestones:

### Domains

- [x] 10 Million
- [x] 20 Million
- [x] 30 Million
- [x] 50 Million
- [x] 70 Million
- [x] 100 Million
- [x] 150 Million
- [ ] 300 Million

### (Wasted) Internet traffic:

- [x] 500TB
- [ ] 1PB


Random facts:

- More than 1TB of Internet traffic is just 3 Mbytes of compressed data
- 1 million domains is just 5 Mbytes compressed
- More than 500TB of Internet traffic is necessary to get 76 million domains (6.6TB / 1 million).
- Only 621 Mbytes of disk space is required to store 164 million domains in compressed form
- 1Gbit fully saturated link is good for about 2 million new domains every day
- 8c/16t and 64 Gbytes of RAM machine is good for about 2 million new domains every day
- 2 [ISC Bind9](https://www.isc.org/bind/) instances (>400 Mbytes RSS each) are required to get 2 million new domains every day
- After reaching 9 million domains I've switched to archived storage.
  Please use freely available [XZ](https://tukaani.org/xz/) to unpack files.
- After reaching 30 million domains I've moved domain directories to `/data`
  so repository doesn't have it's README at the very bottom.

# Using dataset
Raw (unpacked and unfiltered) data may be available at [http://dataset.domainsproject.org](http://dataset.domainsproject.org), though
it is recommended to use Github repo.

This repository empoys [Git LFS](https://git-lfs.github.com/) technology, therefore user
has to use both `git lfs` and `xz` to retrieve data. Cloning procedure is as follows:

```bash
git clone https://github.com/tb0hdan/domains.git
cd domains
./unpack.sh
```

## Data format
After unpacking, domain lists are just text files (~3.2Gb at 164mil) with one domain per line.
Sample for `data/afghanistan/domain2multi-af.txt`:

```
1tv.af
1tvnews.af
3rdeye.af
8am.af
aan.af
acaa.gov.af
acb.af
acbr.gov.af
acci.org.af
ach.af
acku.edu.af
acsf.af
adras.af
aeiti.af
```



# Search engines and crawlers


## Crawlers

### Domains Project bot


Typical user agent for Domains Project bot looks like this:

```
Mozilla/5.0 (compatible; Domains Project/1.0.7; +http://domainsproject.org)
```

Some older versions have set to Github repo:

```
Mozilla/5.0 (compatible; Domains Project/1.0.4; +https://github.com/tb0hdan/domains)
```

All data in this dataset is gathered using [Scrapy](https://scrapy.org) and [Colly](http://go-colly.org/) frameworks.

Crawler code for this project is available at: [Domains Crawler](https://github.com/tb0hdan/domains-crawler)

Starting with version `1.0.7` [Domains Crawler](https://github.com/tb0hdan/domains-crawler) has `robots.txt` support
and rate limiting. Please open issue if you experience any problems. Don't forget to include your domain.


## Others


### Yacy

[Yacy](https://Yacy.net) is a great opensource search engine. Here's my post
on Yacy forum: https://searchlab.eu/t/domain-list-for-easier-search-bootstrapping/231


# Additional sources

[List of .FR domains from AfNIC.fr](http://opendata.afnic.fr/en/products-and-services/services/opendata-en.html)

[Majestic Million](https://blog.majestic.com/development/majestic-million-csv-daily/)

[Internetstiftelsen Zone Data](https://zonedata.iis.se/)

[DNS Census 2013](https://dnscensus2013.neocities.org/)

# Research

This dataset can be used for research. There are papers that cover different topics.
I'm just going to leave links to them here for reference.

## Re-registration and general statistics

[Analysis of the Internet Domain Names Re-registration Market](https://www.researchgate.net/publication/220307877_Analysis_of_the_Internet_Domain_Names_Re-registration_Market)

## Lexical analysis of malicious domains.

[Detection of malicious domains through lexical analysis](https://www.c-mric.com/wp-content/uploads/2018/06/Egon_Cybersecurity2018.pdf)

[Malicious Domain Names Detection Algorithm Based on Lexical Analysis and Feature Quantification](https://www.researchgate.net/publication/335742562_Malicious_Domain_Names_Detection_Algorithm_Based_on_Lexical_Analysis_and_Feature_Quantification)

[Detecting Malicious URLs Using Lexical Analysis](https://www.researchgate.net/publication/308365207_Detecting_Malicious_URLs_Using_Lexical_Analysis)
