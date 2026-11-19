# discussions-in-russian--practice-tool
# An AI-Assisted Nontechnical User-Friendly Russian Language Discussion Training Tool based on YouTube audios

An educational experiment designed to help students develop their comprehension, interpretation, expression, and analytical skills through discussions of literature, psychology, and related topics.

## The project combines:
- YouTube lectures and podcasts in Russian and English
- Speech transcription
- English-to-Russian translation
- Main-idea extraction and comprehension questions
- Three AI discussion partners
- Retrieval-Augmented Generation (RAG)

Open notebook in Google Colab: https://colab.research.google.com/drive/1m46ixOoGrV0SqF4ylpPXWmz3viAdHYkK
For project output examples open the links below or go to PROJECT_OUTPUT_EXAMPLES.md file.

## What It Does
1. Handles audio from YouTube: downloads, trims and saves audio from a specified lecture or podcast for further processing. Materials on literature and psychology can be used for discussions with AI partners; materials on other subjects can be processed for transcription, translation, and main-idea extraction.
2. Transcribes the selected audio segment. (See output example: https://docs.google.com/document/d/1kNhJ9duc1xhB6b-BlJE3j0b0UZjBKtDcN1SXcrncS8A/edit?usp=drivesdk )
3. Extracts main ideas: Identifies and explains the main ideas, generating two questions for each idea to encourage further exploration. (See output example: https://docs.google.com/document/d/1WHRmFTaTbBJfJpO0W-gddCSLk_kNH01VgGesLIFaxaM/edit?usp=drivesdk )
4. Translates English transcripts into Russian. (See output example: https://docs.google.com/document/d/1PfN5lK1n85Uh-9y5OPi4XeQ0-n4pMg318Mqwus7qisI/edit?usp=drivesdk )
5.  Creates a searchable Russian-language knowledge base (основа для обсуждения) from available Russian transcripts and translations for in-depth discussions with an AI partner of the user's choice.
6. Provides three AI discussion partners, each with a distinct specialty:
Литературовед (Literary Critic) — literature and literary analysis.
Психолог (Psychologist) — psychology-related topics.
Собеседник-оригинал (Unconventional Thinker) — original perspectives and unconventional ideas.
The partners respond in Russian by identifying three main aspects of the student's question, explaining their implications, and offering an idea or suggestion for further exploration of each aspect. When discussing material from the knowledge base, students should ask questions in Russian. (See chat output example: https://docs.google.com/document/d/1ihoHnkYjHspB1g96JSjCVF3ckrBRxkRt_jTYZQpGRdU/edit?usp=drivesdk ) For open-ended discussions within the AI partners' areas of expertise, questions can be asked in either Russian or English. (See chat output example: https://docs.google.com/document/d/1sajcMVOHzJe5JjBhHd-r99Ixpj4NW66nedJwzKpxhTI/edit?usp=drivesdk )   To switch from discussing knowledge-base material to an open-ended discussion in a fresh context with the same AI partner, start a new chat.
7. Offers four interchangeable conversational personalities for the AI discussion partners:
Понимающий старый друг (Understanding Old Friend)
Жизнерадостный наставник дзен (Playful Zen Teacher)
Викторианский джентльмен (Victorian Gentleman)
Стоик-аналитик (Stoic Analyst)
8. Maintains shared conversational memory across all AI partners within a chat, including recent conversational context and longer-term summarized information. (See an example of chat output with printed conversation summaries: https://docs.google.com/document/d/1SE1AL5cAvol8chrHU-vwhjlMRr10qpdfahJ0cXS0Pu8/edit?usp=drivesdk  )
9. Automates file naming. Users only need to choose a topic name (смысловое наименование) when saving the initial audio for further processing. This name becomes the filename base for the resulting transcripts, translations, and knowledge bases.
10. Handles storage cleanup with user-friendly prompts. Users can review and confirm actions involving essential files, while unnecessary and temporary files are cleaned up automatically after processing. (See example of main cleanup output: https://docs.google.com/document/d/1ZV6LSLUcxUnsAWvenAsF96MTKbLkNxPErq1ZVMqK15g/edit?usp=drivesdk  )

## Running the Project
The project is designed to run in Google Colab and uses OpenAI's gpt-4o-mini model. It aims to be accessible to non-technical users.
Each processing step provides detailed instructions in plain language, with user-friendly options to cancel or exit when appropriate. (See interaction messages in examples linked above)

## Requirements
You will need:
- A Google account to access Google Colab and Google Drive.
- A Google Drive folder for storing processed material. Specify the folder path in the relevant FOLDER PATH(S) configuration cells in the notebook. For example:
/content/drive/My Drive/YouTube_stuff
- OpenAI API access. The notebook supports two configuration options (see the corresponding notebook cells):
    "DIRECT ACCESS" — provide your OpenAI API key through Google Colab Secrets;
    "ACCESS VIA PROXY" — provide your proxy API key through Google Colab Secrets and configure the proxy's base URL in the corresponding notebook cell.
API keys should be stored securely in Google Colab Secrets, not written directly into the notebook. Each user must obtain their own OpenAI API key or proxy credentials and arrange billing with the relevant service provider.
- An intermediate level of Russian or higher. The AI discussion partners respond only in Russian; in discussions of material from the knowledge base (основа обсуждения) questions should be asked only in Russian; and user-facing instructions are also in Russian.

## Google Colab Compatibility
The project was tested in Google Colab at publication time, and its complete workflow ran successfully despite a dependency conflict reported by pip during installation:
'google-colab 1.0.0 requires requests==2.32.4,
but you have requests 2.34.2 which is incompatible'.
This warning indicates a version mismatch between the installed requests package and the exact version required by the preinstalled google-colab package.
Google Colab's preinstalled packages and dependencies may change over time, so compatibility issues may need to be addressed in the future.
