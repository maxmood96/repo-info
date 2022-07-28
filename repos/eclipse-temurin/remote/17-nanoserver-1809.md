## `eclipse-temurin:17-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:def2fac0b1b035c7160948dad1720dd7dbc970f22c6c5719123366724592a64f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `eclipse-temurin:17-nanoserver-1809` - windows version 10.0.17763.3165; amd64

```console
$ docker pull eclipse-temurin@sha256:2e24561ae6f748ace319a9d4a0ec9610527cf82ec0c997dee6e579d92f839c90
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.2 MB (292220996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa36e48ae8dddf4031672117faf6a4f748c54bc647a82501f6332172956d2b1a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 06 Jul 2022 22:15:10 GMT
RUN Apply image 10.0.17763.3165
# Wed, 13 Jul 2022 14:50:41 GMT
SHELL [cmd /s /c]
# Thu, 28 Jul 2022 16:31:34 GMT
ENV JAVA_VERSION=jdk-17.0.4+8
# Thu, 28 Jul 2022 16:31:35 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 28 Jul 2022 16:31:35 GMT
USER ContainerAdministrator
# Thu, 28 Jul 2022 16:31:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 28 Jul 2022 16:31:46 GMT
USER ContainerUser
# Thu, 28 Jul 2022 16:31:59 GMT
COPY dir:be8ac85d984fd6d07ec942e6824366b313a501643dad7e29e6805d4aab47b44c in C:\openjdk-17 
# Thu, 28 Jul 2022 16:32:16 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 16:32:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5d24e1a2f5c566b0afb1e46fc24e5cec821c8ebf44220276a95a2b91f44a2f2a`  
		Size: 103.2 MB (103155009 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3b09c07c6aeead64423fdefc240fe2e1b6330c96732fd2705113030da84416be`  
		Last Modified: Mon, 18 Jul 2022 21:22:33 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2895487da2db86c62dbe5e78ed3eb9e82b82dcefd45f0920c1ebddce351b5e8d`  
		Last Modified: Thu, 28 Jul 2022 16:47:35 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb602783895d59eb3c367f6c49e797b6f531b4cc7bf2c8597a6302667302f3`  
		Last Modified: Thu, 28 Jul 2022 16:47:35 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0923366291c2355a7c25e03826245ce90a9c13dbc2c90c7b7502d2ca0707a1d`  
		Last Modified: Thu, 28 Jul 2022 16:47:35 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4f433194296f27434a06ca64d7359f939b637250531b3cbd3b12f33918b4c3`  
		Last Modified: Thu, 28 Jul 2022 16:47:33 GMT  
		Size: 73.4 KB (73365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601a9a7e1b55f3a24e32cb3e026b678483367ad999bb97c68db71f983aa96d69`  
		Last Modified: Thu, 28 Jul 2022 16:47:33 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9d5c531bf43951a01bc359455a13ab909c330822643e1440ed3c38a930a422`  
		Last Modified: Thu, 28 Jul 2022 16:47:53 GMT  
		Size: 185.3 MB (185342113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c752ea4024d0440e3b9983dbfef3dcce5c95e1e35efe798b766c88973cb2488e`  
		Last Modified: Thu, 28 Jul 2022 16:47:33 GMT  
		Size: 3.6 MB (3643617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c768edba6b966cb72b613845d96ab468d162a69269e7cf627c068367fc318b`  
		Last Modified: Thu, 28 Jul 2022 16:47:32 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
