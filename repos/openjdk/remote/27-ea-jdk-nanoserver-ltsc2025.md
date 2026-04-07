## `openjdk:27-ea-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:7b728499076fe3d281519f5c23b4dafd073eded0364e488db1562ec6d5755ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `openjdk:27-ea-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull openjdk@sha256:6284b729a40c159a1c208ad4a04a42c055d2d673dbffec24141c160a65267055
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.4 MB (424360829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a92dc0c96d93d3d8b9aedab3af94d2109408040a7b4855128f40ce65f4ff44e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Mar 2026 01:45:55 GMT
RUN Apply image 10.0.26100.32522
# Mon, 06 Apr 2026 18:50:32 GMT
SHELL [cmd /s /c]
# Mon, 06 Apr 2026 18:50:33 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 06 Apr 2026 18:50:34 GMT
USER ContainerAdministrator
# Mon, 06 Apr 2026 18:50:46 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 06 Apr 2026 18:50:46 GMT
USER ContainerUser
# Mon, 06 Apr 2026 18:50:47 GMT
ENV JAVA_VERSION=27-ea+16
# Mon, 06 Apr 2026 18:51:45 GMT
COPY dir:55270656ab5feced27f5cb37a9607ccdf4477020b36ca2637f5afcedca09c62e in C:\openjdk-27 
# Mon, 06 Apr 2026 18:51:55 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 06 Apr 2026 18:51:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:06fab7822816d5f43d6835d07ac8db280fdf81384187f36d8dc43bbb7064a76d`  
		Last Modified: Tue, 10 Mar 2026 20:41:46 GMT  
		Size: 199.4 MB (199409325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca15b088faeff2cfe9e130485d2d9a221329914b77166bf77c15655c70b6ea49`  
		Last Modified: Mon, 06 Apr 2026 18:52:01 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc5a0884d786d3d71224663f73ce21f216d5ffa7680f8ba4d100c7ee1dc0dc1`  
		Last Modified: Mon, 06 Apr 2026 18:52:01 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074429098f87aabcdb840549fe260156b369550404b68980daa739c6a1aaac46`  
		Last Modified: Mon, 06 Apr 2026 18:52:00 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f902af4d0e88abc6d52a74db6f02d627cb6a57f6463a5805a8ae47bb90ac8112`  
		Last Modified: Mon, 06 Apr 2026 18:52:00 GMT  
		Size: 84.8 KB (84764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161697602044aa6ab408c3554e78a5dd8eb2d454f54b8c3b78b395e2c501a013`  
		Last Modified: Mon, 06 Apr 2026 18:51:59 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a997eeb80e711c575653f5fa9c0c27c70fe110e7bf59318442e1c1e079192d`  
		Last Modified: Mon, 06 Apr 2026 18:51:59 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb0627295a0b6d2b263f47e20e96b3b4b92d88fcb0549c2fe4d4414bcb5d61c`  
		Last Modified: Mon, 06 Apr 2026 18:52:16 GMT  
		Size: 224.7 MB (224745852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e93da66049b756117951e76af42d482082222d1b0f54be6a1fe60a5a216fe7f`  
		Last Modified: Mon, 06 Apr 2026 18:51:59 GMT  
		Size: 114.5 KB (114467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da22da6547026c68f8eefd588f78f6259c2854b3f8f55826174813ed693d897`  
		Last Modified: Mon, 06 Apr 2026 18:51:59 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
