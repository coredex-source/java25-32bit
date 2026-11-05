# Backports

Base is upstream jdk-25+5 (last 25 build with the x86_32 port). Stuff pulled in from later 25 builds so Minecraft runs:

- JDK-8350118 (jdk-25+13), only the 32-bit bit of it: FFM pointer handles were broken on 32-bit so LWJGL couldn't call anything
- JDK-8355992 (jdk-25+23): `Math.powExact` and friends, 26.3 needs it
- JDK-8354724 (jdk-25+26): `Reader.readAllAsString`, every 26.x uses it

Skipped JDK-8344168 (jdk-25+9), LWJGL just falls back without it.

Changed code is marked with `Backported from jdk-25+N (JDK-...)`.
