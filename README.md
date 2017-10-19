# python_chatbot

1. (20 marks) Opens a text file whose path is given on the command
line, counts and prints the number of times each word occurs. Words
must be converted to lower case only and you must remove all non-
alphabetic characters. Hyphenated words should be split into two (or
more). Each line of your program's output must have one word and
its corresponding frequency in the format \word:frequency". Output
must be sorted by descending frequency. Your code must be written in
<i>q1_word_count.py</i>.

2. (30 marks) Perform the same operation as Q1, but count word pairs.
Output is a word-pair followed by the number of times it was found,
in the format \word1-word2:frequency". The lines must be sorted by
descending frequency. Your code must be written in <i>q2_pair_count.py</i>.

3. (50 marks) Write a chat-bot program, <i>q3_chat_bot.py</i> that generates
responses using a simple data-driven language model. The program
must parse word pairs from one or more text file whose paths are given
as command line arguments. The user interaction is terminal based
(stdin, stdout) and must follow the same format as Q2 and Q3 from
Assignment 3. That is Send: and Receive: are written, followed by a
one-line message. We will not use any chat handle here. Each time a
user enters a query message (one single line of text ended by new-line),
your program must immediately generate a response message where:
<ul>
<li>The first word in the response (R1) starts with a capital letter.</li>
<li>If the user's last word (QN) occurs in the text, R1 must be chosen
so that QN-R1 has been seen in the text at least once. If QN was
not seen in the text, R1 is allowed to be any word from the text.</li>
<li>Every word pair in the response (RI-RJ) must have been seen at
least once in the text.</li>
<li>The response can end in three ways. (1) On a stop-pair. These
are pairs that ended a sentence in the text at least once. Every
time a stop pair is output, the response must end. (2) If a word
RI is chosen for which no pair RI-RJ exists, then RI must be the
last word in the response. This only happens when RI ends a text
and has never been seen otherwise. (3) If twenty words have been
correctly generated without the first two conditions being met,
then word twenty will end the response.</li>
<li>The last word in the response must be followed by a period.</li>
</ul>
