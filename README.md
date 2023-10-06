# crlf-to-lf-test
A test repository to experiment with and verify Git's line-ending configurations, ensuring a transformation from CRLF to LF upon commits.

Line Ending Experiment
This repository serves as a playground to test and validate Git's line-ending configurations. The primary goal is to ensure that files with CRLF line endings on a local machine are correctly transformed to LF when committed to the repository.

Background
Line endings can be a subtle but potentially troublesome aspect of collaborative coding, especially when contributors use different operating systems. Windows, by default, uses CRLF (\r\n) as a line ending, while Unix-like systems (Linux, macOS) use LF (\n).

This discrepancy can lead to "noisy" commits, where line endings are unintentionally changed, making version control more challenging and diffs harder to read.

Git provides mechanisms to handle and configure line endings, ensuring consistent behavior across different systems.

Test Procedure
Local Configuration:

A file is created locally with CRLF line endings using a text editor.
This simulates the typical scenario on a Windows machine.
Commit & Push:

The file is then committed and pushed to this repository.
Verification:

Upon cloning this repository to a different location or inspecting it through platforms like GitHub, the line endings in the file should be LF, even if they were originally CRLF on the local machine.
Goal
By following this procedure, we can verify if the Git configuration for handling line endings is set up correctly. This ensures smoother collaboration across different platforms and maintains the integrity of our codebase.
