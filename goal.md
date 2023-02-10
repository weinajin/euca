### **End-Users' Explanation Goals** {#purpose}

Even for the same user and task, end-users' needs for explanation, i.e.:
the trigger point or motivation to check the explanation of an AI
system, may vary from time to time based on different contexts or usage
scenarios.  We summarized ten potential [***explanation goals***](#)
from prior works [^prior] as follows:

1.   **[Calibrate trust](#trust)**: trust is a key to
    establish human-AI decision-making partnership. Since users can
    easily distrust or overtrust AI, it is important to calibrate the
    trust to reflect the capabilities of AI systems [^Turner] [^Zhang2020].

2.   **[Ensure safety](#safe)**: users need to ensure
    safety of the decision consequences.

3.   **[Detect bias](#bias)**: users need to ensure the
    decision is impartial and unbiased.

4.   **[Resolve disagreement with AI](#unexpected)**: the AI
    prediction is *unexpected* and there are
    disagreements between users and AI. 
    
 5. **[Expected](#expected)**: the AI's prediction is
    *expected* and aligns with users'
    expectations.

6.   **[Differentiate similar instances](#differentiate)**: due to
    the consequences of wrong decisions, users sometimes need to discern
    similar instances or outcomes. For example, a doctor differentiates
    whether the diagnosis is a benign or malignant tumor.

7.   **[Learn](#learn)**: users need to gain knowledge,
    improve their problem-solving skills, and discover new knowledge

8.   **[Improve](#improve)**: users seek causal factors to
    control and improve the predicted outcome.

9.   **[Communicate with stakeholders](#communicate)**: many
    critical decision-making processes involve multiple stakeholders,
    and users need to discuss the decision with them.

10.   **[Generate reports](#report)**: users need to utilize
    the explanations to perform particular tasks such as report
    production. For example, a radiologist generates a medical report on
    a patient's X-ray image.

11.   **[Trade-off multiple objectives](#multi)**: AI may be
    optimized on an incomplete objective while the users seek to fulfill
    multiple objectives in real-world applications. For example, a
    doctor needs to ensure a treatment plan is effective as well as has
    acceptable patient adherence. Ethical and legal requirements may
    also be included as objectives.

The following are fine-grained details from our user study findings on
end-users' requirements in different explanation goal scenarios. 

---
# <a name="trust"></a> 1. **Calibrate trust**

The process of calibrating trust involves multiple factors and their
complicated interactions. We summarize the following key emerged themes
participants requested to calibrate their trust toward AI.

1.  **Performance** Trust towards AI is fundamental to incorporate AI's
    opinion into the critical decision-making process, and
    many explanation goals below are built on trust.

    Since end-users usually do not have complete computational and
    domain knowledge to judge AI's decision process, model performance
    becomes an important surrogate to establish trust.
    
    > *"Even if AI tells me how it reaches its decision, I cannot judge
    whether it's correct since it is a medical analysis and requires
    professional medical knowledge. I just know the accuracy and that'll
    be fine."* 

    Prior work identified two types of performance: stated and observed
    performance [^Yin2019], and they were both mentioned in the
    interview. *Stated performance* or accuracy is performance metrics
    tested on previous hold-out test data, and it was mentioned by most
    participants as a requirement to build model trust.

    >  *"I understand maybe AI is learning from past examples, and it may
    be finding patterns in the data that might not be easy to explain.
    So I'm less concerned about how it's getting there. I think I do
    have a trust that is doing it right, as long as there's something
    you can test after how accurate it's been. "* 

    Compared to assessing the performance metrics, some participants
    tended to test AI by themselves and get hands-on *observed
    performance* to be convinced. This requires users to have a referred
    ground truth from their own judgment or reliable external sources.

    > *"(My own test driving experience) is way more useful than watching
    a (test driving) video, because you shouldn't trust everything. The
    video might be just made to wait for you to buy the car. So talking
    from a customer perspective, I would like to try it myself, because
    I also sell things. So I would always like to try it myself instead
    of watching a video."* 

2.  **Feature** The important features that AI was based on are the next
    frequently mentioned information.

    > *"I would like to know the list of criteria that the AI chose the
    price based on, and which one weighs more."* 

3.  **The ability to discriminate similar instances** This information
    was requested by several participants to demonstrate AI's
    capability.

    > *"([Decision tree](explanation_form.md#dt)) It's showing me that it's
    picking from a few similar ones, not just like a random ray of blue,
    purple, green birds. It's not random, it's a calculated response.
    More of that would help me trust AI."* 

    > *"[Typical example](explanation_form.md#te) seems to be pretty good
    at picking up on differences. [Similar
    example](explanation_form.md#) I can see that it's got a good
    variety of similar birds. So I found these ones make me trust it
    more.* 

4.  **Dataset** The dataset size that AI was trained on is another
    surrogate mentioned by some participants to enhance trust.

    > *"To me what artificial intelligence does is just collecting a lot
    of data, and tries to make sense for behavioral patterns. So I would
    actually trust it, because I think it's just based on data, it is a
    more accurate measurement of what market rate is for house prices."*
    

    >  *"If I know that the AI comes from a large database, it seems like
    the database is actually the experience that AI has. So the larger
    it (dataset) gets, the more experienced AI would be, so I can trust
    it more."* 

5.  **External information** This is another surrogate mentioned by
    participants to judge if AI is trustworthy. The external information
    could include:

    1.  Peer reviews, endorsement, and company credit.

        >  *"Since I'm not really a tech person, so I'm not sure how I look
        at it in a technical way. So that's why I just really depend on
        the company's reputation, and also how people feel about the
        website."* 

    2.  Authority approval and liability.

        > *"I trust more if the government themselves kind of stands
        behind it, getting some sort of government approval helps it a
        little bit more. So if there's some health authority like Health
        Canada or FDA support gives it more legitimacy."*

        > *"For me personally, I would prefer if an actual person is there
        in the end, at least in the beginning stage. So if somebody is
        there to just say, 'hi, I'm so and so', and then AI takes
        control. Then we still know that there is somebody who's liable
        in the end for whatever happens.''* 

### Preferred explanation forms 

In our user study, the top three most selected forms for the need to calibrate
trust were [performance](explanation_form.md#performance)
(20/40), [output](explanation_form.md#output) (20/40), and [feature
attribute](explanation_form.md#fa) (17/40). 



# <a name="safe"></a>2. **Ensure safety**

To ensure safety and reliability of the AI system in critical tasks (the
autonomous driving vehicle task in our study), participants frequently
mentioned **checking AI's performances in test cases**, expecting the
testing to **cover a variety of scenarios** to show the robustness of
safety. Although it is impossible to enumerate a complete list of
potential failure cases in testing, extreme cases or potential accidents
were the main concerns and focuses of end-users.

> *"Potential crashes or just like someone speeding or a pedestrian
jumping out of nowhere."* 

> *"There is likely to be someone running around, so it needs to show me
the extreme cases. \...I need to see something like FMEA, failure modes
and effects analysis, just to be like, 'okay this is how it works.'
because I know nothing is foolproof. There are always to be something,
but to what extent."* 

Similar to the need to [calibrate trust](#trust), alongside
the above *stated performance*, a few participants required *observed
performance* to emotionally accept AI as an emerging technology.

> *"definitely I would want to be in one car. I think information is not
helpful, it's not an intellectual factual thing, it's emotionally not
acceptable. It (AI) is new and I have to learn to trust it."* 

### Preferred explanation forms 

Regarding the specified information to present in the performance
testing, participants would like to check the objects detected by AI
([feature attribute](explanation_form.md#fa), 9/13):

> *"It shows how it detects the important objects and how it makes
decision"* 

> *"See if (the [feature attributes](explanation_form.md#fa)) align with my
own judgment of feature importance."*

[Performance](explanation_form.md#performance) (6/13) were also favourable to
check the metrics summary of performance. A specified
[performance](explanation_form.md#performance) analysis in different test
scenarios may also help as a safety alert by revealing the weakness of
the system.

> *"Let's say I'm driving on a rainy day, then I know that I should be a
lot more careful than when I'm with the car in a normal condition."*


[Similar example](explanation_form.md#se) (7/13) were preferred since it
showed *"what's the condition or what kind of decision the car gonna
make"*, although participants did not focus on its similarity
nature, but rather assumed it can showcase a variety of cases including
the extreme cases. Several participants chose [decision
tree](explanation_form.md#dt) (6/13) because it *"gave me an overview of
how the car makes decision"*.

# <a name="bias"></a> 3. Detect bias

Participants were concerned about population bias [^Mehrabi2019], or
distribution shift where AI models are applied to a different population
other than the training dataset. Such concern is more prominent when a
prediction is based on users' own personal data, and when users are in
minority subgroups. Participants wanted to compare and see **if their
own subgroup is included in the training data**.

> *"I know I'm in a class, they talked about how a lot of studies haven't
been done specifically on women, even though they (diabetes) affect men
and women differently. That is probably something I would want to know
about, like if it gave me this result and then it had a little note that
explained the research was done more on that demographic, so it may be
more true for that demographic, but they're just trying to, what's the
word, extrapolate to this group where I sit."* 

Unlike the common bias and fairness problem in AI where the protected
features should not affect the prediction, in our Health task on
diabetes prediction, the protected features (age, gender, ethnicity) do
lead to a difference in diabetes outcome (referred as explainable
discrimination in [^Mehrabi2019]). Participants who were aware of this
point **required AI to account for such differences among subgroups**.

> *"I know some ethnic groups just by genetic makeup could be more
predisposed to diabetes. In order for it (AI) to arrive at this
decision, I would think that it has maybe like a sample size of
different people with different ethnicities to try to figure out. I
would think there'll be years and years of research has already been
done of the different groups, different ages that would then be factored
in by AI. If I can see it (AI) is using that information, I'll be a lot
more comfortable to actually using the AI's recommendation."* 

In cases where the AI task is not related to personal information (in
our study the self-driving car task), participants required AI to be
able to detect objects and perform equally in all potential biased
conditions.

> *"Now we are operating in night time, or different weather, but they
(the self-driving cars) still have to be able to see the signs and
identify the objects."* 

### Preferred explanation forms 

A fine-grained [performance](explanation_form.md#performance) (12/24) analysis
based on protected-feature-defined subgroups [^Mehrabi2019] can help
users to identify potential biases.

> *"I would want to see the certainty and what the prediction error can
potentially be for my demographic versus other groups. If it (the
prediction error) is quite low, then I would probably worry less about
that."* 

Participants chose [similar](explanation_form.md#se) + [typical
example](explanation_form.md#te) (12/24, means out of the 24
card-selection responses on [Bias](#bias), 12 selected
either [similar](explanation_form.md#se) or [typical
example](explanation_form.md#te)) to help inspect the data and model, and
to compare with other similar instances to confirm their subgroup is
included in the model.

> *"You would want to know what the data that it's being drawn from, is it
similar to you?"* 

[Feature attribute](explanation_form.md#fa) (12/24) was also chosen since
participants wanted to check if AI could still detection important
features in minority conditions.

> *"I want to see how well AI is performing at night to see what it
detected."* 

# <a name="unexpected"></a> 4. Unexpected: When Users Disagree with AI

When AI's predictions
did not align with participants' own expectations, most participants
would *"question AI"* and *"the contradiction may let me
confuse"*. Some may lose trust with AI thus would not go further
to check its explanations, if they were confident about their own
judgment. Some would check *"a trusted second opinion"*, or
refer to human experts.

But for the majority of participants, **explanations were needed *"to
know why"*** and to resolve conflicts.

> *"I'm feeling conflicted because it's giving me two different
information, my own personal belief and AI. So in order to convince me
that AI does know what it's talking about, you need to go through the
mental validation step [pointing to the ranked explanatory cards]. So
by the time I go through this (explanatory cards) and I come out of it,
I am extremely convinced."* 

Explanations help to identify AI's flaws and reject AI, or to check the
detailed differences and to be convinced and correct user's own
judgment, although *"it might be harder to persuade me"*.
Specifically, participants *"try to understand what makes a difference
(between AI and my prediction)"*, which is similar to the need to
[differentiate](#differentiate). To show why the predictions are different,
many participants **required a list of key features**.

> *"Because AI cannot think like a human, so the reason that I ask for the
criteria list is trying to think how similar to me is AI's thinking. So
maybe AI is thinking better, or is seeing a wider range, so it's
checking things that I've never thought about."* 

In case AI made errors, seeing what AI is based on can facilitate user's
"debugging'' process. Although end-users cannot debug the algorithmic
part, they may be able to debug the input to see if AI *"have the
complete information"* as users have. Furthermore, if some key
input information is lacking in AI's decision, the system needs to allow
users to provide feedback by inputting more information, or
> *"correct the error"* for AI.

### Preferred explanation forms

[Feature attribute](explanation_form.md#fa): 28/61

[similar example](explanation_form.md#se): 25/61

[decision tree](explanation_form.md#dt): 23/61

[performance](explanation_form.md#performance): 20/61

# <a name="expected"></a> 5. Expected: When Users Agree with AI

In contrast, when the prediction matched participants' expectations,
participants *"will trust the AI more"* , and the motivation to
check explanations was *"not as strong as the previous one
([unexpected](#) purpose)"*. Some participants
stopped at the prediction, willing to accept the "black-box'' AI and may
 *"not even waste my time (checking explanations)"*.

A few participants still wanted to check further explanations for the
following motivations:

1.  To **boost user's confident**.

    > *"Even in this (expected) scenario, it would be nice to have some
    bullet points, like the reasons behind it the estimation being
    accurate, because if someone says that you're charging me way too
    much, I can have point by point reasons explaining to you why this
    house worth this price, it actually kind of as a confidence boost to
    think you are not overcharging or undercharging."* 

2.  To [**improve the outcome**](#improve).

    > *"If diabetes already runs in my family, (and AI predicts my risk of
    diabetes is 80%), it would probably make me more confident about the
    software. So I might want to ask for more information about which
    aspects of my health records were the most important for making this
    decision? Coz then maybe that can help me with my future activities
    and changing things in the future."* 

### Preferred explanation forms 

[Feature attribute](explanation_form.md#fa): 13/34

[similar example](explanation_form.md#se): 12/34

[typical example](explanation_form.md#te): 10/34

# <a name="differentiate"></a> 6. Differentiate similar instances

To facilitate end-users' need to differentiate similar instances, AI is
required to first have the ability to discern similar instances.

> *"Depends on how good it is\...So I think you would have to improve how
AI picks up the birds, like maybe these are the same color birds, but
maybe they have slightly different characteristics. So if AI can pick
that up, then I think it would be better."* 

In case of doubtful prediction, participants expected AI to indicate how
certain it is to the prediction.

> *"I would expect AI if it doesn't know, it would give choices. So it
would say 100% or 99% that's an indigo bunting, and 89% it thinks it's a
finch."* 

Based on that, AI needs to be able to *"**pinpoint unique features**
that made them really different from each other"*. In addition,
the interface may also need to support users' own comparison.

> *"AI can tell you what the differences are. I guess it could be some
list of the beak is longer for this and that. But I think visually
bringing the differences up side by side, and then I can directly
compare what the differences are."* 

### Preferred explanation forms 

[Rule](explanation_form.md#rl) (12/14) and [counterfactual
example](explanation_form.md#ce) (10/14) were the most preferable forms.
Participants chose [rule](explanation_form.md#rl) since *"you could write
that you differentiated the bird's tail were long or short, or beak thin
or thick"*. The [counterfactual examples](explanation_form.md#ce)
> *"identify where specifically to look"*, and *"describe the change,
the progress"* .

# <a name="learn"></a> 7. Learn

Using AI for user's personal learning, improving problem solving skills,
and knowledge discovery,  *"depends on how reliable it (AI) really is"*. And participants expected AI to *"receive human feedback to
correct its error and improve itself"*.

To facilitate learning and knowledge discovery, *"just looking at
(input) pictures and (output) names isn't enough"*, and
participants **expected a wide range of explanations** depending on the
particular learning goal, such as *"more details to systematically
learn, go over that same bird, \...a mind map to build a category of
birds by one feature"* ,*"the specific characteristic about this
bird, and how can I differentiate this bird from other birds"*.
Other learning features mentioned by participants include: referring to
external *"respectable source"*, supporting personalized learning
for unfamiliar terms, and *"collecting information about how well
I'm doing on it, like if I guess wrong, does it record that? to see if
I'm progressing"*.

### Preferred explanation forms 

Rule-based explanations ([rule](explanation_form.md#rl): 12/14, [decision
flow chart](explanation_form.md#dt): 10/14, [decision
tree](explanation_form.md#dt): 8/14) were more favourable for the need to
learn, since they showed *"a learning process. It has like how you could
recognize a bird. So help me to learn some new knowledge"*. Same
as in [Report](#report), participants would prefer to see
> *"the graphics and text combined"*: *"It combines text and
pictures, and they are relevant to each other. It's kind of a
multi-modal learning"*.

# <a name="improve"></a> 8. Improve the predicted outcome

Participants intuitively seek explanations to improve the predicted
outcome, when predictions are related to personal data (in our study,
the House and Health tasks). However, they **tended to unwarrantedly
assume the explanations were causal** (causal illusion [^Matute2015],
i.e., believe there is a causal connection between the breakdown factors
and the outcome), even though the cause-effect relationship has not been
confirmed, and AI largely relies on correlation for
prediction [^Pearl2000]. Only a few participants required more solid
evidence to support the explanations on improving the predicted outcome,
especially when the action was related to critical consequences
(personal health outcomes).

> *"I presume the recommendation (on improvement actions from AI) is also
has been backed up by Health Canada, because I think I would tend to
follow the recommendations if I know there's definitely medical support
behind it."* 

> *"I would definitely want to know like what can I do to mitigate those
risk factors or to address those things so that I can decrease the risk.
I would really like to know if it had an explanation of how reliable
each source was. Coz I know some studies, they might seem like a
correlation, but it doesn't mean it's a direct cause. So I would really
love it if it could potentially explain how powerful those studies are
suggesting."*

Regarding the specific requirements on the explanations for improvement,
participants were looking for **controllable features** and ignoring the
features that cannot be changed.

> *"I can not change my age, but I'm able to reduce my weight"*

Knowing the controllable features has a positive psychological effect to
give users a sense of control, and vice versa.

> *"If I'm afraid of getting diabetes, and assume that I'm going to
sentence, it feels like there's nothing I can do about it. But when I
see this one ([feature attribute](explanation_form.md#fa)), I think, 'oh
geez, maybe there are other factors here that I can do something about.'
So this may make me more positive about doing something about my
condition."* 

> *"I know it ([feature interaction](explanation_form.md#fi)) is comparing
my house area and my number of rooms with other houses. I can understand
'okay if I increase my room number, the price will be increased that
much.' But the problem is I cannot change any of them (the house
features). It just gives me the feeling of disappointment."*

To counterpoise the unchangeable features, users may intuitively apply
counterfactual reasoning to compare different feature adjustment
settings.

> *"If I make any change in my house appliance and renew, then I can still
reach the same price as if my house was bigger"* 

### Preferred explanation forms
[Counterfactual
example](explanation_form.md#ce) (18/26) and [feature
shape](explanation_form.md#fs) (13/26) were the top two selected forms.
While [counterfactual example](explanation_form.md#ce) provides
how to achieve the target outcome change by adjusting the input features
(counterfactual reasoning), [feature shape](explanation_form.md#fs) and [feature
interaction](explanation_form.md#fi) allow users to adjust features and
see how that leads to outcome change.


# <a name="communicate"></a>9. Communicate with stakeholders

To communicate with other stakeholders, some participants chose to
communicate verbally about their opinions without mentioning AI. Others
preferred to present stakeholders with more evidence by bringing AI's
additional information explicitly to the discussion. For the latter
case, the **other stakeholders need to establish basic understanding and
trust towards AI** before discussing AI's explanations.

> *"I'd sit down and get my family together and explain about the
artificial intelligence thing."* 

> *"I would try to get some evidence from it (AI) that I could take to the
doctor to get them to buy into it."* 

To do so, most participants chose to present AI's performance
information to build trust.

> *"As long as the backstage is accurate and then I can just provide
accuracy to my wife and she'll be able to get that. Trustworthy is the
most fundamental."* 

Different audiences and explanation goals of communication may require
distinct explanations, as described by one participant:

> *"I'm pretty sure my husband or my mother has a different way to decide
or they want to know different things."*

In addition, in the Health task, we asked participants to communicate
with family members or doctors about their diabetes predictions. Since
the requested explanation covered a wide range of contents, we did not
identify any distinct differences in the communicating contents between
the two audiences.

A formal summary or report from AI may facilitate the communication with
other stakeholders, as requested by many participants.

> *"A written report from AI that I would be able to reference to, in
order to talk to my family about that. It would feel a little bit more
official rather than just, 'oh, this is what somebody said', there's no
real evidence, whereas this sort of creates that paper trail.''* 

### Preferred explanation forms
While [output](explanation_form.md#output)
(21/46) and [performance](explanation_form.md#performance) (17/46) provide AI's
result and help to [build trust](#trust), [feature
attribute](explanation_form.md#fa) (27/46) and [decision
tree](explanation_form.md#dt) (17/46) show the breakdown factors and
internal logic behind the prediction.

# <a name="report"></a> 10. Generate reports

The content of reports may largely depend on the specific purpose and
readers of the report. In our study, participants frequently mentioned
the report should include *"key identifying features"*,  *"list of
distinguishing characteristics or what makes it unique"* , or *"**a summary of factors** that were part of the input led to
the diabetic prediction"*. Users also mentioned including
supporting information to back up the decisions, such as the training
dataset size of the predicted class, and the decision certainty level
.

### Preferred explanation forms
[Rule](explanation_form.md#rl)(12/14),
[decision flow chart](explanation_form.md#dt)(7/14), and [feature
attribute](explanation_form.md#fa)(5/14) are the most frequently selected
explanation forms.

Rule descriptions can conveniently generate text reports.

> *"I have to write the explanation"* 

> *"You can not only by looking at the images and get some explanation.
You need some more specific description."* 

In addition, adding image to the text *"would be complementary"*
to each other, and the format of image + text were more favourable by
many participants.

> *"[Rule](explanation_form.md#) is just describing and writing. It
doesn't really show you a visual on how to compare them."* 

> *"[Feature attribute](explanation_form.md#fa) and [decision flow
chart](explanation_form.md#dt) (presented in image format on bird
recognition task) highlights what [rule](explanation_form.md#rl) is
saying, this knowledge complements your statement."* 

# <a name="multi"></a> 11. Trade-off multiple objectives

Usually it is the human user rather than AI to trade-off among multiple
objectives in AI-assisted decision-making tasks. Thus when multiple
objectives get conflicted (in our study, they are scenarios when car
drives autonomously and passenger gets a car sick; and AI predicts
diabetes and uses it to determine insurance premium), AI was required to
allow users to take over or to receive users' inputs.

> *"It's the most important thing I would want to do is to allow me to
stop, or asking to slow down if I'm feeling sick."*

Explanations are required if the multiple objectives conflict and need
to trade-off. And users could use such explanations to defend for or
against certain objectives.

> *"I think it's like a defensive thing, like if I'm expecting that
they're going to cause an increase in my payments or whatever they're
going to deny me (health insurance) coverage, I would be trying to find
out what it's based on for the opposite reason maybe to discredit it."*

---
**References**

[^prior]: [Gregor1999](https://doi.org/10.2307/249487); [Doshi-Velez2017](http://arxiv.org/abs/1702.08608); [Nunes2017](https://doi.org/10.1007/s11257-017-9195-0); [Ribera2019](http://ceur-ws.org/Vol-2327/IUI19WS-ExSS2019-12.pdf)

[^Turner]: [Calibrating Trust in AI-Assisted Decision Making. (2020)](https://www.ischool.berkeley.edu/sites/default/files/sproject_attachments/humanai_capstonereport-final.pdf)

[^Zhang2020]: [Effect of confidence and explanation on accuracy and trust calibration in AI-assisted decision making](https://doi.org/10.1145/3351095.3372852) 

[^Yin2019]: [Understanding the Effect of Accuracy on Trust in Machine Learning Models](https://doi.org/10.1145/3290605.3300509)


[^Mehrabi2019]:  [A Survey on Bias and Fairness in Machine Learning](http://arxiv.org/abs/1908.09635)

[^Matute2015]: [Illusions of causality: how they bias our everyday thinking and how they could be reduced](https://doi.org/10.3389/fpsyg.2015.00888)

[^Pearl2000]: [Causality: Models, Reasoning, and Inference](http://bayes.cs.ucla.edu/BOOK-2K/)
