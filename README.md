# crlf-to-lf-test

테스트 리포지토리는 Git의 줄 끝 설정을 실험하고 확인하기 위한 것입니다. 이를 통해 커밋 시 CRLF에서 LF로 변환되는지를 확인합니다.

crlf 에서 lf 로 변환하기
주요 목표: 로컬에서 CRLF로 끝나는 파일이 올바르게 LF로 커밋되는지 확인해보기

배경
줄 바꿈기호인 CRLF(Carriage-Return Line Feed, \r\n)과 LF(Line Feed, \n)는 협업 코딩에서 문제가 될 수 있는 부분입니다. Windows는 기본적으로 CRLF (\r\n)를 사용하며, Unix와 유사한 시스템 (Linux, macOS)은 LF (\n)를 사용합니다. 

이러한 차이점은 의도하지 않은 줄 바꿈기호가 변경되면서 버전 제어가 더 어려워지고 더 어렵게 읽히게 만드는 커밋이 될 수 있습니다.

Git은 다양한 시스템 간의 일관된 동작을 보장하기 위해 줄 바꿈기호를 처리하고 구성하는 메커니즘을 제공합니다.

테스트 절차
로컬 구성:
텍스트 에디터를 사용하여 로컬에 CRLF로 끝나는 파일을 생성합니다. (Windows 환경임을 가정)

커밋 및 푸시:
이 파일을 레포지토리에 커밋하고 푸시합니다.

검증:
이 레포지토리를 다른 위치로 clone하거나 GitHub과 같은 플랫폼에서 검사할 때, 파일의 줄 끝 형식은 CRLF가 아닌, LF여야 합니다. 

목표
Git의 줄 끝 처리 형식이 올바르게 설정되어 있는지 확인함을 통해 다양한 플랫폼 간의 더 부드러운 협업을 보장하고 코드베이스의 무결성을 유지할 수 있습니다.

A test repository to experiment with and verify Git's line-ending configurations, ensuring a transformation from CRLF to LF upon commits.

Line Ending Experiment
This repository is to test and validate Git's line-ending configurations. The primary goal is to ensure that files with CRLF line endings on a local machine are correctly transformed to LF when committed to the repository.

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
