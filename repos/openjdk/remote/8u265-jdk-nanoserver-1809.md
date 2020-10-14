## `openjdk:8u265-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:510313cf149509506a474160f27f71ea868b66a4d0eecadb71910f87add0c569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `openjdk:8u265-jdk-nanoserver-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull openjdk@sha256:0aefe13d2def05f972f0cf442a5e9511234be6633707e9eb845e9028ac4c6dd2
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.5 MB (201470080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b14e5b86688858a88ee66281a96480aefedeee3135cd3e955c88d59794876155`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 30 Sep 2020 11:25:56 GMT
RUN Apply image 1809-amd64
# Wed, 14 Oct 2020 17:46:04 GMT
SHELL [cmd /s /c]
# Wed, 14 Oct 2020 18:19:47 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 14 Oct 2020 18:19:48 GMT
USER ContainerAdministrator
# Wed, 14 Oct 2020 18:19:59 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 14 Oct 2020 18:20:00 GMT
USER ContainerUser
# Wed, 14 Oct 2020 18:20:00 GMT
ENV JAVA_VERSION=8u265
# Wed, 14 Oct 2020 18:20:29 GMT
COPY dir:3c2880b061bc00940ee162754a64e55567e0dbb10e65b749277b54fa005ce8de in C:\openjdk-8 
# Wed, 14 Oct 2020 18:20:47 GMT
RUN echo Verifying install ... 	&& echo   javac -version && javac -version 	&& echo   java -version && java -version
```

-	Layers:
	-	`sha256:aab6118ce69c93410df7fa15842a6e3b3c7ff20b639c779b5d5f78e7653eaa07`  
		Size: 101.2 MB (101205155 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:40f59dc77cd194db29e444ce30cc9a91a3d555f7d4d7329fb6f46c13e559dc2f`  
		Last Modified: Wed, 14 Oct 2020 18:31:55 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f822d9b5f4a27e75717d840213bf01aa457181f76080288360e2cad1b45a3a51`  
		Last Modified: Wed, 14 Oct 2020 18:52:10 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc2109693b56565a97d180b522fad17ec423e033c7f1a3db51ee9d180e66258`  
		Last Modified: Wed, 14 Oct 2020 18:52:10 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37efdccecd7ae96c22c31406b30fad32db36533af566b8b8b39aea4b5fad57b6`  
		Last Modified: Wed, 14 Oct 2020 18:52:07 GMT  
		Size: 64.2 KB (64239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6622c960b719718f8db57a370f97ff41eef0b48712d53f38d0bd887de528ec0f`  
		Last Modified: Wed, 14 Oct 2020 18:52:08 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7cc7087c61a510339361b6faa4dfea1b9710a1b0019fcca3c3551fb1779544`  
		Last Modified: Wed, 14 Oct 2020 18:52:07 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f4350791209fa3d02905915a731726942d299f99c13bdfe2e38dc1dc0c16e9`  
		Last Modified: Wed, 14 Oct 2020 18:53:56 GMT  
		Size: 100.1 MB (100110739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b999399da01491a08528ad477bf2ae2a8a2fc5473f4da317903e6faad6791f`  
		Last Modified: Wed, 14 Oct 2020 18:52:07 GMT  
		Size: 85.5 KB (85525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
