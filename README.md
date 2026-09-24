# LangGraph Recruitment Agent

A job-application screening workflow built with **LangGraph** and **Groq** (LLM).

## How it works
1. **Categorize experience**: the LLM labels the candidate Entry, Mid or Senior level.
2. **Assess skill set**: the LLM checks the application against a Python Developer role (Match / No Match).
3. **Conditional routing**:
   - Match → schedule HR interview
   - No match + Senior → escalate to recruiter
   - No match + Entry/Mid → reject

## Tech stack
Python, LangGraph, LangChain, Groq (`openai/gpt-oss-120b`)

## Run it
1. Open `recruitment_agent.ipynb` in Google Colab.
2. Add your Groq API key in Colab **Secrets** as `GROQ_API_KEY`.
3. Run all cells.

## Example results
| Application | Outcome |
|---|---|
| 10 yrs, Java | Escalate to recruiter |
| 1 yr, Java | Reject |
| Python experience | Schedule interview |
| 5 yrs, C++ | Reject |

## Credits
Based on a LangGraph tutorial video, adapted to use Groq.