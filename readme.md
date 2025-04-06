
# “Show Me How”: Benefits and Challenges of Agent-Augmented Counterfactual Explanations for Non-Expert Users

**ABSTRACT**
```
Counterfactual explanations offer actionable insights by illustrating how changes to inputs can lead to different outcomes. However, these explanations often suffer from ambiguity and impracticality, limiting their utility for non-expert users with limited AI knowledge. Augmenting counterfactual explanations with Large Language Models (LLMs) has been proposed as a solution, but little research has examined their benefits and challenges for non-experts. To address this gap, we developed a healthcare-focused system that leverages conversational AI agents to enhance counterfactual explanations, offering clear, actionable recommendations to help patients at high risk of cardiovascular disease (CVD) reduce their risk. Evaluated through a mixed-methods study with 34 participants, our findings highlight the effectiveness of agent-augmented counterfactuals in improving actionable recommendations. Results further indicate that users with prior experience using conversational AI demonstrated greater effectiveness in utilising these explanations compared to novices. Furthermore, this paper introduces a set of generic guidelines for creating augmented counterfactual explanations, incorporating safeguards to mitigate common LLM pitfalls, such as hallucinations, and ensuring the explanations are both actionable and contextually relevant for non-expert users.
```

**Please cite our work using the following bibtext**
```
@inproceedings{bhattacharya2025show,
  author    = {Aditya Bhattacharya and Tim Vanherwegen and Katrien Verbert},
  title     = {``Show Me How'': Benefits and Challenges of Agent-Augmented Counterfactual Explanations for Non-Expert Users},
  booktitle = {Proceedings of the 33rd ACM Conference on User Modeling, Adaptation and Personalization (UMAP '25)},
  year      = {2025},
  location  = {New York City, NY, USA},
  publisher = {ACM},
  pages     = {11 pages},
  doi       = {10.1145/3699682.3728321},
  url       = {https://doi.org/10.1145/3699682.3728321}
}
```
or
**using the ACM Reference Format**
```
Aditya Bhattacharya, Tim Vanherwegen, and Katrien Verbert. 2025. “Show Me How”: Benefits and Challenges of Agent-Augmented Counterfactual Explanations for Non-Expert Users. In 33rd ACM Conference on User Model-
ing, Adaptation and Personalization (UMAP ’25), June 16–19, 2025, New York City, NY, USA. ACM, New York, NY, USA, 11 pages. https://doi.org/10.1145/3699682.3728321 
```

** Originally cloned from: https://github.com/Vanherwegentim/HeartDiseaseRisk.git **

*Streamlit has had an update which could improve the speed of this application. Future work could start by improving this*

This is the code for the thesis on the influence of conversational agents on non-expert users in the healthcare sector. To get started do the following steps:

1. ```
   git clone https://github.com/Vanherwegentim/HeartDiseaseRisk.git
   ```

2. ```
   pip install -r requirements.txt
   ```

3. ```
   streamlit run app.py
   ```

4. Access the application at  http://localhost:8501

The analytics are currently enabled and can be accessed at http://localhost:8501/?analytics=on. Scroll all the way down to view these. The code to connect these analytics to a cloud firestore database is currently commented by can be reconfigured to suit your needs.

An OpenAI api-key is needed to run the conversational agent. To add this to your application, you need to create a .streamlit folder. In that folder you need to create a secrets.toml file where you will put your api-key. This should look something like this:

```
OPENAI_API_KEY="sk-therestofyourkey"
PROD="False"
```

You would also need to the firestore credentials here if you wanted the analytics in the database.

The hosted version of this app can be found here https://heartdiseaseriskassessment.streamlit.app.

