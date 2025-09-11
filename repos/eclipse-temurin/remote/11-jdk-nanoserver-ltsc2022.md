## `eclipse-temurin:11-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:72d91a716f3c6185835bf814066d7a7ded1ae25069096aedeefa786cfc4fe405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `eclipse-temurin:11-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull eclipse-temurin@sha256:7853d4de513d10596be5c54d1ec3b5725d49f3be0466b175b5ada600940334f6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.6 MB (317551506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38aa042c2e520fcef54d003fa621a002ce1d70f62d920ac297e3cfcb47376ca2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:18:16 GMT
SHELL [cmd /s /c]
# Wed, 10 Sep 2025 22:18:16 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Wed, 10 Sep 2025 22:18:17 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 10 Sep 2025 22:18:17 GMT
USER ContainerAdministrator
# Wed, 10 Sep 2025 22:18:19 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Sep 2025 22:18:20 GMT
USER ContainerUser
# Wed, 10 Sep 2025 22:18:28 GMT
COPY dir:210c213d7567f4ae9108259b6c16f9783779d8f224bc53a31a49e53f33738954 in C:\openjdk-11 
# Wed, 10 Sep 2025 22:18:32 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Sep 2025 22:18:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cbb86931614a5d803cf00ed301ed322ace890beae852523d46150a851ed2e7`  
		Last Modified: Wed, 10 Sep 2025 23:02:50 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29344e10407eb5d4775e1498d5edd345d593f5f232b49390a1922e88e2742761`  
		Last Modified: Wed, 10 Sep 2025 23:02:46 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90d51e4365b5cc403ac115ea9fc40a7ccadab8ce19998ca071969375b85dc65`  
		Last Modified: Wed, 10 Sep 2025 23:02:52 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6135ba5e2989a8d30d2b2e30b4c7db82b42fc4e86d57bf53c5cf43aba28a56`  
		Last Modified: Wed, 10 Sep 2025 23:02:48 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b9adb167a189508d7c6d513314f1660a4f821e307ebdd08bbfe3b47d2a66fa2`  
		Last Modified: Wed, 10 Sep 2025 23:02:46 GMT  
		Size: 87.8 KB (87822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663f544bd557c74954d0374ba99552d552d612d93155e60943c5f8a92dec0709`  
		Last Modified: Wed, 10 Sep 2025 23:02:51 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d87c45075c19a0a8cebb6a13ea13e1e6675db63f35fa4cd108884aff9369d4`  
		Last Modified: Wed, 10 Sep 2025 22:18:48 GMT  
		Size: 194.6 MB (194619307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f5997775bb14c7e60e862e5e10450dcc25a875bd26c69b6ad027cbc254f7fa`  
		Last Modified: Wed, 10 Sep 2025 23:02:51 GMT  
		Size: 118.1 KB (118075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b979983c138f62f7b0b7f9295a24d13840fc8d3a6b7e8a8e2cbb49ca2ed620b6`  
		Last Modified: Wed, 10 Sep 2025 23:02:48 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
