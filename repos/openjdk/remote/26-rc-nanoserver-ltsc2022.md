## `openjdk:26-rc-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:e40c47392169363590a125a49eb225a9b78fa3e8aef709fe0083019508c40114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `openjdk:26-rc-nanoserver-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull openjdk@sha256:d1c794df0993baf25f56b2af4a4ed8d8dd870cbb6437db89a4ad987cd2f8f3b4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.8 MB (350791120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a908652b9ea31947f0a9db5b5da1c26d6d93dab6b55abdf2f3daebcd88d30b0f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 10 Mar 2026 22:36:18 GMT
SHELL [cmd /s /c]
# Tue, 10 Mar 2026 22:40:11 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 10 Mar 2026 22:40:11 GMT
USER ContainerAdministrator
# Tue, 10 Mar 2026 22:40:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 10 Mar 2026 22:40:13 GMT
USER ContainerUser
# Tue, 10 Mar 2026 22:40:14 GMT
ENV JAVA_VERSION=26
# Tue, 10 Mar 2026 22:40:23 GMT
COPY dir:48d9a1614aae77abafeeb59360dca42b580c313456033330908c8e794bbb7778 in C:\openjdk-26 
# Tue, 10 Mar 2026 22:40:28 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 10 Mar 2026 22:40:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba2425154dbe4f9c92a7daa50ee78f1d65a2f56409da6f247f3870c5a1f698a`  
		Last Modified: Tue, 10 Mar 2026 22:36:37 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb82b6bc5a9f90952aac65c3cb71ba080613cc4a16a8388c783cd9f3ebb193b`  
		Last Modified: Tue, 10 Mar 2026 22:40:34 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2f330fcf134f213b9995ae1fedd12c50293ebfaf7eb746e93dcd86bdf84521`  
		Last Modified: Tue, 10 Mar 2026 22:40:33 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2b3ac0a842aba78ce85591fa7bf73969fd8cd7816507d8a4fa03720bbb5a06`  
		Last Modified: Tue, 10 Mar 2026 22:40:33 GMT  
		Size: 76.6 KB (76570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e081012b9980a99fae51fabebcbc40a8ad24d56765e26af362f9243ab9a2a5bd`  
		Last Modified: Tue, 10 Mar 2026 22:40:32 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d469dc3944df392e5e1ebf1661dde9c2b32c7c1aa13193652f1c5e889989b4`  
		Last Modified: Tue, 10 Mar 2026 22:40:32 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece040cee1133bd1fa98e8add636620831529308448f281ee69b5491a8b1610c`  
		Last Modified: Tue, 10 Mar 2026 22:40:48 GMT  
		Size: 224.0 MB (223950547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f1035e3dd36028d312b78cd344fd9f6ca69745dadc2340c3bd54dcf702d692`  
		Last Modified: Tue, 10 Mar 2026 22:40:32 GMT  
		Size: 107.0 KB (107044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6bcd72ec7de00fed32731e88b906c3af715de3b5a49761e88ac6c2d6b40fbe6`  
		Last Modified: Tue, 10 Mar 2026 22:40:32 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
