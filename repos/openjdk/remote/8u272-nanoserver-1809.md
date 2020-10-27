## `openjdk:8u272-nanoserver-1809`

```console
$ docker pull openjdk@sha256:402eb44d0ef38c0b09913c818992fe438f4a9123410ad9bf494af162171b2c9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `openjdk:8u272-nanoserver-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull openjdk@sha256:f2e69525066d7dde55572099daa6e937c3cca28ea71fab0a8416626ab05753c4
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.3 MB (202336791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7ac2f8b4d04779c8eb8f29c830ed62eb0b4896e4ba6cdbb0262723c874e0372`
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
# Mon, 26 Oct 2020 23:20:26 GMT
COPY dir:ba26a6340c532ef3b44bc920e785f61bc958fcf1ecefd576f1438bebffc3afee in C:\openjdk-8 
# Mon, 26 Oct 2020 23:20:45 GMT
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
	-	`sha256:a91b5ea81f7e0c344a5e60dfa92af76925db5903d41399cee309a7499b67e1ae`  
		Last Modified: Mon, 26 Oct 2020 23:31:04 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da66ccbd807de457b7dc35b3fef4e74d4037b11252cb82712d1f43483caee7f1`  
		Last Modified: Mon, 26 Oct 2020 23:31:17 GMT  
		Size: 101.0 MB (100972064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02181e88bd994c8b462a8dc0241a30157a1a143ece9ec41dc579a267b5cdd28c`  
		Last Modified: Mon, 26 Oct 2020 23:31:05 GMT  
		Size: 90.9 KB (90915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
