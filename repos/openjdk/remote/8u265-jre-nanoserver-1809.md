## `openjdk:8u265-jre-nanoserver-1809`

```console
$ docker pull openjdk@sha256:ddfa0290c609fca5e192c9347538336cee12a113d0eab518e20fe43a8c380e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `openjdk:8u265-jre-nanoserver-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull openjdk@sha256:deacaf34f4e260c7afe7acb10d6bcac8303da69c0edb334c6f56f4ab24a44eaf
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138775906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d71b4b95ee96b597c5fcfbab58aff25d38302ec89506750d11b83c8c388b0ec`
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
# Wed, 14 Oct 2020 18:23:53 GMT
COPY dir:f9cdcac6b6965117d0bbadf86b5d0b55237954c067839a8e6ad0130705a48c8f in C:\openjdk-8 
# Wed, 14 Oct 2020 18:24:10 GMT
RUN echo Verifying install ... 	&& echo   java -version && java -version
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
	-	`sha256:de1b07dcf4691e49d03284701120395ec77a648017bc55e0c9f722ee51c38abd`  
		Last Modified: Wed, 14 Oct 2020 18:55:03 GMT  
		Size: 37.4 MB (37425957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f6e87aeefadb23cf7c124e0f0dd825af320dd753b56e0503c9da1397176c41`  
		Last Modified: Wed, 14 Oct 2020 18:54:57 GMT  
		Size: 76.1 KB (76133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
