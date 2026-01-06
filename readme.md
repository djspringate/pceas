<h1>pceas - A Huc6280/PC Engine Assembler</h1>

<h2>Notes from djspringate:</h2>
<h3>06/01/2026</h3>
I've forked my own build for pceas: I'm looking to get it building on Win64 and Mac M1, likely using CMake to generate the appropriate Makefiles or projects. (Not sure yet.)<br>
I want to be able to write my own PC Engine assembler on my Windows laptop or Macbook.<br>

<h2>Notes from parent fork:</h2>
I recently needed to fix a nasty core dump that was happening when building my last demo under linux. Turns out pceas did not really enforce the 32-char max. symbol name length rule, so it went crazy when you had really long symbol names.<br>
I patched it so it issues a fatal error when a symbol name is too long, and also upped the limit to 64 chars.<br>

From what I'm seeing, a few different versions of pceas are floating around the internets: Tomaitheous' release seemed to be the most recent, so that's the one I patched.<br>

