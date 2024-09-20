# GPTScore Prompt Template

## Factuality

template = """
Evaluate Factuality in the Generated Response

You will be given a source text and a generated response. Your task is to evaluate the factuality of the generated response by comparing it to the source text.

**Evaluation Criteria**:
- Factuality (1-5): Does the generated response accurately reflect the factual statements found in the source text? A score of 1 means that the response contains multiple inaccuracies or fabricated information, while a score of 5 means that the response is entirely accurate and preserves all factual details from the source text.

**Evaluation Steps**:
1. Carefully read the source text to identify key factual statements and details.
2. Review the generated response and compare it to the source text, focusing on the accuracy and integrity of the facts presented.
3. Assign a score for factuality on a scale of 1 to 5 based on the Evaluation Criteria.

**Important**: Ensure that all responses, including explanations and scores, are generated in Korean.

**Example**:
Source Text:
{source_text}

Generated Response:
{generated_response}
                        
Factuality Score (1-5):
"""

## Consistency
평가 설명 부분을 영어로 작성하면서도, 일관성(consistency)을 강조하도록 변경하였습니다. 평가자가 생성된 응답의 일관성을 분석하고, 출처 텍스트와의 차이나 충돌을 강조하도록 유도합니다.

template = """
Evaluate Consistency in the Generated Response

You will be given a source text and a generated response. Your task is to evaluate the consistency of the generated response by comparing it to the source text.

**Evaluation Criteria**:
- Consistency (1-5): Does the generated response consistently provide information that aligns with the source text? A score of 1 means that the response contains contradictory or conflicting information, while a score of 5 means that the response is fully consistent with no discrepancies.

**Evaluation Steps**:
1. Carefully read the source text to understand the key points and details.
2. Review the generated response and compare it to the source text, focusing on the consistency of the information provided.
3. Provide a detailed explanation of your evaluation, noting any inconsistencies or confirming the consistency of the response.
4. Assign a score for consistency on a scale of 1 to 5 based on the Evaluation Criteria.

**Important**: Ensure that all responses, including explanations and scores, are generated in Korean (한글로 작성하세요).

**Example**:
Source Text:
{source_text}

Generated Response:
{generated_response}

Evaluation Explanation:
- Provide an analysis of the consistency, highlighting specific aspects where the generated response aligns or diverges from the source text.

Consistency Score (1-5):
"""

## Relevance
평가자가 생성된 응답의 Relevance(적절성)을 분석할 수 있도록 하였습니다. 특히 생성된 응답이 출처 텍스트의 주요 주제나 요점을 얼마나 잘 반영하는지를 평가하도록 유도합니다.

template = """
Evaluate Relevance in the Generated Response

You will be given a source text and a generated response. Your task is to evaluate the relevance of the generated response by comparing it to the source text.

**Evaluation Criteria**:
- Relevance (1-5): How well does the generated response relate to the source text? A score of 1 means that the response is largely irrelevant or off-topic, while a score of 5 means that the response is highly relevant and directly addresses the key points of the source text.

**Evaluation Steps**:
1. Carefully read the source text to understand its main topics and key points.
2. Review the generated response and compare it to the source text, focusing on how well it addresses the main topics and key points.
3. Provide a detailed explanation of your evaluation, highlighting specific areas where the generated response is relevant or irrelevant to the source text.
4. Assign a score for relevance on a scale of 1 to 5 based on the Evaluation Criteria.

**Important**: Ensure that all responses, including explanations and scores, are generated in Korean (한글로 작성하세요).

**Example**:
Source Text:
{source_text}

Generated Response:
{generated_response}

Evaluation Explanation:
- Provide an analysis of the relevance, highlighting specific aspects where the generated response aligns or diverges from the main topics of the source text.

Evaluation Form (scores ONLY):
- Relevance Score (1-5):
"""

## Fluency
평가자가 생성된 응답의 Fluency(유창성)을 분석할 수 있도록 설계되었습니다. 생성된 응답이 얼마나 문법적으로 정확하고 읽기 쉬운지를 평가하도록 유도합니다.

template = """
Evaluate Fluency in the Generated Response

You will be given a source text and a generated response. Your task is to evaluate the fluency of the generated response by assessing its grammatical correctness and readability.

**Evaluation Criteria**:
- Fluency (1-5): How well is the generated response written in terms of grammar, syntax, and overall readability? A score of 1 means the response is poorly written, with numerous grammatical errors or awkward phrasing, while a score of 5 means the response is highly fluent, with excellent grammar and smooth readability.

**Evaluation Steps**:
1. Carefully read the source text to understand its style and tone.
2. Review the generated response, focusing on its grammatical correctness, sentence structure, and overall readability.
3. Provide a detailed explanation of your evaluation, noting any grammatical errors, awkward phrasing, or confirming the fluency of the response.
4. Assign a score for fluency on a scale of 1 to 5 based on the Evaluation Criteria.

**Important**: Ensure that all responses, including explanations and scores, are generated in Korean (한글로 작성하세요).

**Example**:
Source Text:
{source_text}

Generated Response:
{generated_response}

Evaluation Explanation:
- Provide an analysis of the fluency, highlighting specific aspects where the generated response is grammatically correct, easy to read, or where it may have issues with fluency.

Evaluation Form (scores ONLY):
- Fluency Score (1-5):
"""


## Coherence 
평가자가 생성된 응답의 Coherence(일관성, 논리적 흐름)를 분석할 수 있도록 하였습니다. 특히 생성된 응답이 얼마나 잘 구성되어 있는지, 논리적 흐름이 있는지를 평가하도록 유도합니다.
template = """
Evaluate Coherence in the Generated Response

You will be given a source text and a generated response. Your task is to evaluate the coherence of the generated response by comparing it to the source text.

**Evaluation Criteria**:
- Coherence (1-5): How well does the generated response make sense as a unified piece of text? A score of 1 means that the response is disjointed or lacks logical flow, while a score of 5 means that the response is well-structured and logically consistent throughout.

**Evaluation Steps**:
1. Carefully read the source text to understand its overall structure and key points.
2. Review the generated response and assess its logical flow, structure, and overall coherence.
3. Provide a detailed explanation of your evaluation, noting any logical inconsistencies or confirming the coherence of the response.
4. Assign a score for coherence on a scale of 1 to 5 based on the Evaluation Criteria.

**Important**: Ensure that all responses, including explanations and scores, are generated in Korean (한글로 작성하세요).

**Example**:
Source Text:
{source_text}

Generated Response:
{generated_response}

Evaluation Explanation:
- Provide an analysis of the coherence, highlighting specific aspects where the generated response aligns or diverges in its logical flow and structure compared to the source text.

Evaluation Form (scores ONLY):
- Coherence Score (1-5):
"""

## Accuracy 
평가자가 생성된 응답의 Accuracy(정확성)를 분석할 수 있도록 하였습니다. 특히 생성된 응답에 포함된 정보가 정확한지, 잘못된 정보가 있는지를 평가하도록 유도합니다.

template = """
Evaluate Accuracy in the Generated Response

You will be given a source text and a generated response. Your task is to evaluate the accuracy of the generated response by comparing it to the source text.

**Evaluation Criteria**:
- Accuracy (1-5): Are there any inaccuracies, omissions, or unfactual content in the generated response? A score of 1 means that the response contains significant inaccuracies or incorrect information, while a score of 5 means that the response is fully accurate and correctly reflects the source text.

**Evaluation Steps**:
1. Carefully read the source text to identify all the key facts and details.
2. Review the generated response and compare it to the source text, focusing on the accuracy of the information provided.
3. Provide a detailed explanation of your evaluation, highlighting any inaccuracies, omissions, or confirming the accuracy of the response.
4. Assign a score for accuracy on a scale of 1 to 5 based on the Evaluation Criteria.

**Important**: Ensure that all responses, including explanations and scores, are generated in Korean (한글로 작성하세요).

**Example**:
Source Text:
{source_text}

Generated Response:
{generated_response}

Evaluation Explanation:
- Provide an analysis of the accuracy, highlighting specific aspects where the generated response aligns with or diverges from the facts in the source text.

Evaluation Form (scores ONLY):
- Accuracy Score (1-5):
"""


## Multidimensional Quality
평가자가 생성된 응답의 Multidimensional Quality(다차원적 품질)를 분석할 수 있도록 하였습니다. 이는 응답의 사실성, 일관성, 관련성, 정확성 등 여러 측면에서의 성능을 종합적으로 평가하도록 유도합니다.

template = """
Evaluate Multidimensional Quality in the Generated Response

You will be given a source text and a generated response. Your task is to evaluate the overall quality of the generated response across multiple dimensions, including factuality, coherence, relevance, and accuracy.

**Evaluation Criteria**:
- Multidimensional Quality (1-5): How well does the generated response perform across all relevant quality dimensions (factuality, coherence, relevance, accuracy)? A score of 1 means the response performs poorly in most or all dimensions, while a score of 5 means the response performs excellently across all dimensions.

**Evaluation Steps**:
1. Carefully read the source text to understand the main content and quality dimensions.
2. Review the generated response, assessing its performance in terms of factuality, coherence, relevance, and accuracy.
3. Provide a detailed explanation of your evaluation, highlighting the strengths and weaknesses of the response across all quality dimensions.
4. Assign a score for overall multidimensional quality on a scale of 1 to 5 based on the Evaluation Criteria.

**Important**: Ensure that all responses, including explanations and scores, are generated in Korean (한글로 작성하세요).

**Example**:
Source Text:
{source_text}

Generated Response:
{generated_response}

Evaluation Explanation:
- Provide an analysis of the overall quality, considering the factuality, coherence, relevance, and accuracy of the generated response.

Evaluation Form (scores ONLY):
- Multidimensional Quality Score (1-5):
"""

## Semantic Appropriateness
평가자가 생성된 응답의 Semantic Appropriateness(의미적 적절성)를 분석할 수 있도록 설계되었습니다. 생성된 응답이 출처 텍스트의 의미와 맥락에 얼마나 적절하게 부합하는지를 평가하도록 유도합니다.

template = """
Evaluate Semantic Appropriateness in the Generated Response

You will be given a source text and a generated response. Your task is to evaluate the semantic appropriateness of the generated response by comparing it to the source text.

**Evaluation Criteria**:
- Semantic Appropriateness (1-5): How well does the generated response convey meaning that is appropriate and aligned with the context of the source text? A score of 1 means the response is semantically inappropriate or off-context, while a score of 5 means the response is fully appropriate and semantically consistent with the source text.

**Evaluation Steps**:
1. Carefully read the source text to understand its meaning and context.
2. Review the generated response and assess whether the meaning it conveys is appropriate and aligned with the source text.
3. Provide a detailed explanation of your evaluation, highlighting areas where the generated response is semantically appropriate or where it diverges from the intended meaning.
4. Assign a score for semantic appropriateness on a scale of 1 to 5 based on the Evaluation Criteria.

**Important**: Ensure that all responses, including explanations and scores, are generated in Korean (한글로 작성하세요).

**Example**:
Source Text:
{source_text}

Generated Response:
{generated_response}

Evaluation Explanation:
- Provide an analysis of the semantic appropriateness, highlighting specific aspects where the generated response aligns or diverges from the meaning and context of the source text.

Evaluation Form (scores ONLY):
- Semantic Appropriateness Score (1-5):
"""


## Understandability
평가자가 생성된 응답의 Understandability(이해 가능성)를 분석할 수 있도록 설계되었습니다. 생성된 응답이 얼마나 명확하고 쉽게 이해될 수 있는지를 평가하도록 유도합니다.

template = """
Evaluate Understandability in the Generated Response

You will be given a source text and a generated response. Your task is to evaluate the understandability of the generated response by considering how clear and easy it is to comprehend.

**Evaluation Criteria**:
- Understandability (1-5): How easy is it to understand the generated response? A score of 1 means that the response is confusing, unclear, or difficult to comprehend, while a score of 5 means that the response is very clear, straightforward, and easy to understand.

**Evaluation Steps**:
1. Carefully read the source text to understand its main points and context.
2. Review the generated response, focusing on how clearly the information is presented and whether it is easy to follow.
3. Provide a detailed explanation of your evaluation, noting any areas where the response is particularly clear or where it may be confusing.
4. Assign a score for understandability on a scale of 1 to 5 based on the Evaluation Criteria.

**Important**: Ensure that all responses, including explanations and scores, are generated in Korean (한글로 작성하세요).

**Example**:
Source Text:
{source_text}

Generated Response:
{generated_response}

Evaluation Explanation:
- Provide an analysis of the understandability, highlighting specific aspects where the generated response is clear or where it may be difficult to comprehend.

Evaluation Form (scores ONLY):
- Understandability Score (1-5):
"""
