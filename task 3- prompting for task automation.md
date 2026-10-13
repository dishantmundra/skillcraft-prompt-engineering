SkillCraft Technology Internship

Task 03: Prompting for Task Automation

Domain: Prompt Engineering

1. Objective

To design a consistent prompt that transforms unstructured student notes into structured JSON, making information easier to organize and process automatically.

2. Automation Task

Convert student assignment details into a standard JSON format.

3. Reusable Prompt

You are a data-processing assistant. Convert the input text into valid JSON using the following schema:

{
"student_name": "",
"subject": "",
"assignment": "",
"deadline": "",
"priority": ""
}

Rules:

1. Extract only information explicitly provided in the input.
2. If a field is missing, use an empty string.
3. Set priority to "High", "Medium", or "Low" only when the input supports that classification.
4. Return valid JSON only, without explanations or Markdown formatting.
5. Use the same keys and structure for every input.

4. Input-Output Example 1

Input:

Rahul has to submit his Data Structures assignment by 20 October 2026. It is urgent.

Output:

{
"student_name": "Rahul",
"subject": "Data Structures",
"assignment": "Data Structures assignment",
"deadline": "20 October 2026",
"priority": "High"
}

5. Input-Output Example 2

Input:

Priya needs to complete her Python lab report by 25 October 2026. It is not urgent.

Output:

{
"student_name": "Priya",
"subject": "Python",
"assignment": "Python lab report",
"deadline": "25 October 2026",
"priority": "Low"
}

6. Input-Output Example 3

Input:

Aman has a mathematics project to submit. The deadline has not been announced.

Output:

{
"student_name": "Aman",
"subject": "Mathematics",
"assignment": "Mathematics project",
"deadline": "",
"priority": ""
}

7. Reflection on Prompt Iteration and Debugging

During prompt design, the output may initially contain explanations, inconsistent field names, or missing values. To improve reliability, I added explicit rules for JSON-only output, fixed field names, and handling missing information.

These refinements make the prompt more consistent across different inputs. The examples demonstrate how the same prompt structure can handle multiple student records.

8. Conclusion

This task demonstrates how prompt engineering can semi-automate repetitive data-processing work. A clear schema, explicit instructions, and multiple input-output examples improve consistency and reduce formatting errors.

Note: This is a prompt-based demonstration. Production automation should also validate the JSON and handle unexpected inputs.
