# Peregrine Deployment Strategist Take-Home Exercise

## Setup

1. Install Python dependencies:
    ```bash
    pip3 install -r requirements.txt
    ```

2. Run the Jupyter notebook located at `analysis.ipynb` to follow along with the analysis and visualizations described in the assignment overview below.


## Assignment Overview

At Peregrine, we help analysts and investigators solve crimes. One subset of complex crimes is money laundering. The goal of [money laundering](https://en.wikipedia.org/wiki/Money_laundering) is to conceal the origins of illegally obtained money by passing it around in a complex series of transfers or transactions. In effect, the illegally obtained money is “washed” through a network of innocuous-looking transactions so that it comes out the other side “clean”.   In California, [money](https://www.justice.gov/usao-cdca/pr/two-california-men-found-guilty-federal-crimes-participating-massive-international) [laundering](https://www.justice.gov/usao-sd/pr/california-woman-sentenced-235-months-involvement-meth-and-money-laundering-conspiracy) [cases](https://apnews.com/article/campaigns-california-los-angeles-money-laundering-7e01fe02d007373359546bd1f72a90c0) are [common](https://www.usnews.com/news/best-states/california/articles/2021-11-05/la-area-casino-settles-money-laundering-case-for-500-000). Sometimes, these cases involve [drug cartels](https://www.ice.gov/news/releases/large-scale-law-enforcement-effort-targets-downtown-los-angeles-businesses-linked) looking to wash their ill-gotten gains.

Imagine that you are an intelligence analyst for the California Bureau of Investigation working on a case involving a Mexican drug cartel. A few months back, you identified a suspicious business called "The Flower Shop" thanks to an anonymous tip. 

You contacted the California Office of the Attorney General and received a dataset of all money transfers made by The Flower Shop in the past year. The AML (Anti-Money Laundering) data is attached. You are looking for a pattern of money laundering between individuals. You’ll need to present your Director a short list of suspects and the analysis developed to identify them.

## Deliverables

### Part 1

1. As a warmup, spend some time exploring the dataset. What patterns do you see in the data? Consider factors such as transaction size, transaction frequency, commonly used send and pay agents, send and pay locations, and so on. Visuals and explanations of your findings are encouraged throughout.

2. List out some hypotheses as to what indicates a suspicious transaction. Feel free to use external sources, such as [FINCEN](https://www.fincen.gov/resources/law-enforcement/case-examples) to guide you. **Make sure to explain why your hypotheses might indicate suspicious behavior.**
    
    For example, a short time between the wiring and receiving of a transaction may be suspicious because the quick reception of a transfer means that the receiver was informed that the transaction would be coming through (these transactions are being wired and received in person).

### Part 2

1. **Test the hypothesis**. What interesting or suspicious patterns can you find? Share any supporting analysis and visualizastions. In your analysis, be sure to test:

    - Transaction amount/size
    - Transaction frequency
    - Short time between wiring and receiving
    - Any other hypothesis you found compelling

2. Develop a **write-up** that clearly states the "answer," your rationale, and any supporting analysis. Keep in mind that your Director is a detail-oriented & analytical individual, who appreciates data visualizations.

We ask that you explore the dataset in any analysis tool of your choice (Excel, Python, R, etc., are all fine). Your deliverable from this exercise is a writeup (longform text, markdown, slides – whatever you’re most comfortable with) that responds to the questions outlined in the prompt. We also ask that you share your code or other artifacts that help illustrate your thinking. 

### Columns

- **Sender ID1 Info** - whether a sender indicated his or her ID (binary). In a real anti-money laundering (AML) analysis, this would be an ID number (e.g. a driver's license).
- **Payee ID1 Info** - whether a payee (receiver) indicated his or her ID (binary). In a real anti-money laundering (AML) analysis, this would be an ID number (e.g. a driver's license).
- **Sender Name** - the name of the sender
- **Payee Name** -  the name of the payee (receiver)
- **Send Agent Name** - the physical location or business address where the sender wires money. Frequently, AML cases are initiated because of suspicious transactions being made out of specific stores (or send agents)
- **Send Operator Name -**  the sender's wire transfer operator (such as Western Union)
- **Pay Agent Name -** the physical location or business address where the receiver (payee) receives the money
- **Pay Operator Name** - the receiver's wire transfer operator (again, such as Western Union)
