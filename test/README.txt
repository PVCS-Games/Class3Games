PVCS REUSABLE INTERACTIVE WORKBOOK
==================================

FILES
  index.html      Reusable quiz engine (keep unchanged for new lessons).
  quiz-data.json  Content for the current lesson (edit this for new quizzes).

QUICK START
  1. Upload index.html and quiz-data.json TOGETHER into the same folder on
     your PVCS Games GitHub Pages repository.
  2. Open the GitHub Pages URL for that folder's index.html.
  3. For the next lesson, make a copy of the folder, change ONLY quiz-data.json,
     then publish the new folder. Do not overwrite old quiz folders if you want
     old quizzes to remain available.
  4. Test Practice Mode, Test Mode, teacher-review answers, and a Google Form
     test submission before sharing with students.

IMPORTANT: This version loads quiz-data.json using fetch. Double-clicking
index.html on your computer may be blocked by browser file:// security.
Use GitHub Pages or a local web server to test. JSON must be valid (no comments,
no trailing commas); VS Code is a useful editor.

CONTENT FIELDS
  meta.quizName          Sent to the shared Google Form (change per chapter).
  meta.title             Header title.
  meta.subtitle          Subtitle in the header.
  pages.page1.data       Word banks and fill-the-blank questions.
  pages.page1.charPinyin Pinyin pronunciation lookup.
  pages.page2.questions  Circle-the-answer questions, options and answers.
  pages.page2.py         Pinyin lookup.
  pages.pagelesson       Dialogue speaker, emoji, Chinese, English, Pinyin.
  pages.page3.shorts     Open answers for TEACHER REVIEW.
  pages.page3.tfs        True/false questions and answer keys.
  pages.page4.sections   Listening-test questions.
  pages.page4.audioUrl   Optional audio file URL, e.g. "lesson-audio.mp3".
  pages.page5.left/right Matching pairs; keys = correct right-side index
                        for each left-side item (index starts at zero).
  pages.page6.writing    Character-writing items for TEACHER REVIEW.
  pages.page6.words      Vocabulary choices for dialogue blanks.
  pages.page6.lines      Dialogue sections and word-blank positions.
  pages.page6.keys       Correct choice indices for dialogue blanks.
  pages.page7.passages   Chinese passage paragraphs and English translations.
  pages.page7.questions  Comprehension true/false questions and answer keys.
  pages.page7.PY         Pinyin lookup.

IMPORTANT CONTENT RULES
  * Keep JSON property names exactly as written; change VALUES only.
  * Preserve array/object shapes for each exercise type.
  * Multiple-choice answer values are zero-based in some sections.
  * Update answer keys whenever you change options or reorder matching pairs.
  * Update the appropriate Pinyin dictionary for new Chinese characters.
  * Page 3 short answers and Page 6 writing remain teacher-reviewed.
  * All page results and individual answers continue to submit only in Test Mode.

AUDIO
  The original Chapter 2 listening recording remains embedded in index.html,
  so the sample works as before. For a different lesson's recording, place an
  MP3 in the same folder and set pages.page4.audioUrl to the filename. This
  makes an OPTIONAL third media file for lessons with different recorded audio.
  Other speech buttons continue using speech synthesis.

GOOGLE FORMS
  The Google Form action, form entry IDs, answer details, summary formatting,
  and Test Mode submission restriction remain in index.html. The quiz name
  comes from meta.quizName in quiz-data.json. Background form submissions
  cannot be conclusively acknowledged by Google Forms in the browser, so
  check your response spreadsheet after a test submission.

For another quiz, upload these two files plus new lesson source material in a
new chat and say: 'Change ONLY quiz-data.json for this chapter, preserving
index.html exactly. Keep the same seven page types and Google Form fields.'
