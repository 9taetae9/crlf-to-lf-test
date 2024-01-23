# crlf-to-lf-test

crlf 에서 lf 로 변환하기
주요 목표: 로컬에서 CRLF로 끝나는 파일이 올바르게 LF로 커밋되는지 확인해보기

줄 바꿈기호인 CRLF(Carriage-Return Line Feed, \r\n)과 LF(Line Feed, \n)는 협업 코딩에서 문제가 될 수 있는 부분이다. Windows는 기본적으로 CRLF (\r\n)를 사용하며, Unix와 유사한 시스템 (Linux, macOS)은 LF (\n)를 사용하는데, 이러한 차이점이 의도하지 않은 줄 바꿈기호가 변경되면서 버전 제어가 더 어려워지게 만드는 커밋이 될 수 있다.

Git은 다양한 시스템 간의 일관된 동작을 보장하기 위해 줄 바꿈기호를 처리하고 구성하는 메커니즘을 제공한다.

테스트 절차

로컬 구성
텍스트 에디터를 사용하여 로컬에 CRLF로 끝나는 파일을 생성. (Windows 환경)

커밋 및 푸시
해당 파일을 레포지토리에 커밋하고 푸시한다.

검증
해당 레포지토리내의 파일을 github에서 다운 받고 cat -e filename 으로 확인시 , 파일의 줄 끝 형식은 CRLF가 아닌, LF여야 한다. 

<img width="80%" src="https://github.com/9taetae9/crlf-to-lf-test/assets/89383263/750fd413-f625-4829-a2e1-f9c7e9339df9"/>


A test repository to experiment with and verify Git's line-ending configurations, ensuring a transformation from CRLF to LF upon commits.

Line Ending Experiment
This repository is to test and validate Git's line-ending configurations. The primary goal is to ensure that files with CRLF line endings on a local machine are correctly transformed to LF when committed to the repository.

Background
Line endings can be a subtle but potentially troublesome aspect of collaborative coding, especially when contributors use different operating systems. Windows, by default, uses CRLF (\r\n) as a line ending, while Unix-like systems (Linux, macOS) use LF (\n).

This discrepancy can lead to "noisy" commits, where line endings are unintentionally changed, making version control more challenging and diffs harder to read.

Git provides mechanisms to handle and configure line endings, ensuring consistent behavior across different systems.

Test Procedure
Local Configuration
A file is created locally with CRLF line endings using a text editor.
This simulates the typical scenario on a Windows machine.

Commit & Push
The file is then committed and pushed to this repository.

Verification
Upon cloning this repository to a different location or inspecting it through platforms like GitHub, the line endings in the file should be LF, even if they were originally CRLF on the local machine.

By following this procedure, we can verify if the Git configuration for handling line endings is set up correctly. This ensures smoother collaboration across different platforms and maintains the integrity of our codebase.
