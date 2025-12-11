# Night Highway Patrol (GLUT)

Setup steps for Windows + Code::Blocks to download, open, build, and run.

Assumption: GLUT (or FreeGLUT) is already installed on your system. You know the include, lib, and DLL paths.

1) Download the project from GitHub
- Open the GitHub repository page.
- Click Code → Download ZIP.
- Extract the ZIP to a folder, e.g. f:\25Fall\CG\Lab\Night_Highway_Patrol.

2) Open the project in Code::Blocks
- Start Code::Blocks.
- File → Open → select Night_Highway_Patrol.cbp.

3) Configure include and library paths (one-time)
- Project → Build options → Search directories:
  - Compiler: add your GLUT include path (e.g. C:\path\to\glut\include).
  - Linker: add your GLUT lib path (e.g. C:\path\to\glut\lib).

4) Link required libraries
- Project → Build options → Linker settings → add:
  - glut32 (or freeglut)
  - opengl32
  - glu32
  - winmm
  - gdi32

5) Ensure DLL availability
- Place the corresponding DLL (e.g. glut32.dll or freeglut.dll) next to the built executable in bin\Debug, or ensure its folder is on PATH.

6) Build and run
- Build → Build.
- Build → Run.

Notes
- Source uses #include <GL/glut.h>. If you installed FreeGLUT, #include <GL/freeglut.h> also works.
- If you see include errors, re-check step 3 and architecture consistency (x86 vs x64) with your compiler.
