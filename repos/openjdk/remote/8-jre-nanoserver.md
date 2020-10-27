## `openjdk:8-jre-nanoserver`

```console
$ docker pull openjdk@sha256:4e64b6825d43c35273360004495957a6996d47ffc79334a0b968435ac61fc3c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `openjdk:8-jre-nanoserver` - windows version 10.0.17763.1518; amd64

```console
$ docker pull openjdk@sha256:fc6ecd05d27d128813f2f820af772312acdb94599ddb1dd2d9e33160c95388eb
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139540776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f5882884a11febf8a945dac76b00b08eae1b96e104012791327b1c9030ea937`
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
# Mon, 26 Oct 2020 23:20:04 GMT
ENV JAVA_VERSION=8u272
# Mon, 26 Oct 2020 23:23:34 GMT
COPY dir:cbcfc3652aed057bcd6387f24201b1963f79bbe4e98f6b8927ff7925a8b991a5 in C:\openjdk-8 
# Mon, 26 Oct 2020 23:23:50 GMT
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
	-	`sha256:a91b5ea81f7e0c344a5e60dfa92af76925db5903d41399cee309a7499b67e1ae`  
		Last Modified: Mon, 26 Oct 2020 23:31:04 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c1cb83877e559bc7d27a18328e88f65870bd8d6edfd243820ed08aae744d9e0`  
		Last Modified: Mon, 26 Oct 2020 23:32:19 GMT  
		Size: 38.2 MB (38191536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1c4a7f7de62bc7dce3a6b56f207bb42a00c67de6c0e75fadacc3b0e58ac22d`  
		Last Modified: Mon, 26 Oct 2020 23:32:13 GMT  
		Size: 75.4 KB (75428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
