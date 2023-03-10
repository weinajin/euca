# EUCA dataset description

Associated Paper: 
**[EUCA: the End-User-Centered Explainable AI Framework](http://arxiv.org/abs/2102.02437)**

Authors:
Weina Jin, Jianyu Fan, Diane Gromala, Philippe Pasquier, Ghassan Hamarneh

----------------

EUCA dataset is for modelling personalized or interactive explainable AI. It contains 309 data points of 32 end-users' preferences on 12 forms of explanation (including feature-, example-, and rule-based explanations). The data were collected from a user study on 32 layperson participants in the Greater Vancouver city area in 2019-2020. In the user study, the participants (P01-P32) were presented with AI-assisted critical tasks on house price prediction, health status prediction, purchasing a self-driving car, and studying for a biological exam [1]. Within each task and for its given explanation goal [2], the participants selected and rank the explanation forms [3] that they saw the most suitable. 

1. [ExplanationFormRanking.csv](https://github.com/weinajin/euca/blob/master/EUCA_dataset_quantitative_and_qualitative_data/EUCA_quantitative_dataset/ExplanationFormRanking.csv)

   **Column description**:

   - **Index** - Participants' number
   - **Case** - task-explanation goal combination
   - **accept to use AI? trust it?** - Participants response to whether they will use AI given the task and explanation goal
   - **require explanation?** - Participants response to the question whether they request an explanation for the AI
   - **1st, 2nd, 3rd, ...** - explanation form card selection and ranking 
     cards fulfill requirement? - After the card selection, participants were asked whether the selected card combination fulfill their explainability requirement.

2. [demography.csv](https://github.com/weinajin/euca/blob/master/EUCA_dataset_quantitative_and_qualitative_data/EUCA_quantitative_dataset/demography.csv)

   It contains the participants demographics, including their age, gender, educational background, and their knowledge and attitudes toward AI.

[EUCA dataset zip file for download](https://github.com/weinajin/euca/blob/master/EUCA_dataset_quantitative_and_qualitative_data.zip)

----------------

### [1] Critical tasks

There are four tasks. Task label and their corresponding task titles are:
house - Selling your house 
car - Buying an autonomous driving vehicle
health - Personal health decision
bird - Learning bird species

Please refer to [EUCA quantatative data analysis report](https://github.com/weinajin/euca/blob/master/paper/SupplementaryMaterialS2_UserStudy.pdf) for the storyboard of the tasks and explanation goals presented in the user study.

### [2]  [Explanation goal](goal.md)

End-users may have different goals/purposes to check an explanation from AI. The EUCA dataset includes the following 11 explanation goals, with its [label] in the dataset, full name and description

1. [trust] **[Calibrate trust](goal.md#trust)**: trust is a key to
   establish human-AI decision-making partnership. Since users can
   easily distrust or overtrust AI, it is important to calibrate the
   trust to reflect the capabilities of AI systems.
2. [safe] **[Ensure safety](goal.md#safe)**: users need to ensure
   safety of the decision consequences.

3. [bias] - **[Detect bias](goal.md#bias)**: users need to ensure the
   decision is impartial and unbiased.

4. [unexpect] **[Resolve disagreement with AI](goal.md#unexpected)**: the AI
   prediction is *unexpected* and there are
   disagreements between users and AI. 

 5. [expected] - **[Expected](goal.md#expected)**: the AI's prediction is
    *expected* and aligns with users'
    expectations.

6. [differentiate] **[Differentiate similar instances](goal.md#differentiate)**: due to
   the consequences of wrong decisions, users sometimes need to discern
   similar instances or outcomes. For example, a doctor differentiates
   whether the diagnosis is a benign or malignant tumor.

7. [learning] **[Learn](goal.md#learn)**: users need to gain knowledge,
   improve their problem-solving skills, and discover new knowledge

8. [control] **[Improve](goal.md#improve)**: users seek causal factors to
   control and improve the predicted outcome.

9. [communicate] **[Communicate with stakeholders](goal.md#communicate)**: many
   critical decision-making processes involve multiple stakeholders,
   and users need to discuss the decision with them.

10. [report] **[Generate reports](goal.md#report)**: users need to utilize
    the explanations to perform particular tasks such as report
    production. For example, a radiologist generates a medical report on
    a patient's X-ray image.

11. [multi] **[Trade-off multiple objectives](goal.md#multi)**: AI may be
    optimized on an incomplete objective while the users seek to fulfill
    multiple objectives in real-world applications. For example, a
    doctor needs to ensure a treatment plan is effective as well as has
    acceptable patient adherence. Ethical and legal requirements may
    also be included as objectives.

### [3] [explanation form](explanation_form.md)

The following 12 explanation forms are end-user-friendly, i.e.: no technical knowledge is required for the end-user to interpret the explanation.


* [Feature-Based Explanation](explanation_form.md/#feature)
    * Feature Attribution - fa	
      * Note: for tasks that has image as input data, the feature attribution is denoted by the following two cards:
      * ir:  important regions (a.k.a. heat map or saliency map)
      * irc: important regions with their feature contribution percentage
    * Feature Shape - fs
    * Feature Interaction - fi

* [Example-Based Explanation](explanation_form.md/#example)
    * Similar Example - se
    * Typical Example - te
    * Counterfactual Example - ce
      * Note: for contractual example, there were two visual variations used in the user study:
      * cet:  counterfactual example with transition from one example to the counterfactual one
      * ceh:  counterfactual example with the contrastive feature highlighted

* [Rule-Based Explanation](explanation_form.md/#rule)
    * Rule - rt
    * Decision Tree - dt
    * Decision Flow - df

* [Contextual Information](explanation_form.md/#suppl)
    * Input
    * Output
    * Performance
    * Dataset - prior  (output prediction with prior distribution of each class in the training set)

Note: occasionally there is a wild card, which means the participant draw the card by themselves. It is indicated as 'wc'.

For visual examples of each explanation form card, please refer to the [Explanatory_form_labels.pdf](https://github.com/weinajin/euca/blob/master/EUCA_dataset_quantitative_and_qualitative_data/EUCA_quantitative_dataset/EUCA_explanation_form_labels.pdf) document.

[Link to the details on users' requirements on different explanation forms](explanation_form.md)

## Code and report for EUCA data quantatitve analysis

* [EUCA data analysis code](https://github.com/weinajin/euca/tree/master/EUCA_dataset_quantitative_and_qualitative_data/quantitative_data_analysis_code)
* [EUCA quantatative data analysis report](https://github.com/weinajin/euca/blob/master/paper/SupplementaryMaterialS2_UserStudy.pdf)

## EUCA data citation

```
@article{jin2021euca,
   title={EUCA: the End-User-Centered Explainable AI Framework},
      author={Weina Jin and Jianyu Fan and Diane Gromala and Philippe Pasquier and Ghassan Hamarneh},
      year={2021},
      eprint={2102.02437},
      archivePrefix={arXiv},
      primaryClass={cs.HC}
}
```

