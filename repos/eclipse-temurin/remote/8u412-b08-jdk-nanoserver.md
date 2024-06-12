## `eclipse-temurin:8u412-b08-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:ed138cb2dfa0d7593a3a350fe97ca74985606d9dbdc107a969f48ab06e3da363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2527; amd64
	-	windows version 10.0.17763.5936; amd64

### `eclipse-temurin:8u412-b08-jdk-nanoserver` - windows version 10.0.20348.2527; amd64

```console
$ docker pull eclipse-temurin@sha256:cbee22c4c09ae5c02c2bee5a2478cce7d5c7ac02ebe547dc81a6d622531a36f5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.3 MB (222343315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e313730b6e814bb52cce5b333755179214ac87bd61e13c17ec27beae4f59bb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jun 2024 08:41:16 GMT
RUN Apply image 10.0.20348.2527
# Wed, 12 Jun 2024 18:27:44 GMT
SHELL [cmd /s /c]
# Wed, 12 Jun 2024 18:27:45 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Wed, 12 Jun 2024 18:27:45 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 12 Jun 2024 18:27:46 GMT
USER ContainerAdministrator
# Wed, 12 Jun 2024 18:27:59 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Jun 2024 18:28:00 GMT
USER ContainerUser
# Wed, 12 Jun 2024 18:28:10 GMT
COPY dir:5498972beafb1de3e4749bc87b064f8ce9cec472aae9e7d0f4643a99f48638da in C:\openjdk-8 
# Wed, 12 Jun 2024 18:28:25 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:f9825bcd6f9509654677a23b5fa1d32b32e1e32ff51914ebfaa76d5e79c22b50`  
		Last Modified: Wed, 12 Jun 2024 02:27:19 GMT  
		Size: 120.5 MB (120488969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ae17666c85b2b00f8e5aa24951a59f0b01a1eb41704faa32e1282e0f0ef217`  
		Last Modified: Wed, 12 Jun 2024 18:52:48 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9810bd1ece92cc8c6b01d420e14565e774bed05f414b93e3cd71a54f70dda26`  
		Last Modified: Wed, 12 Jun 2024 18:52:48 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421c68de0fd45f05a2752b0c83793739cd30c57b5ae5491c3141160c219ac360`  
		Last Modified: Wed, 12 Jun 2024 18:52:47 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1858de9f088ee1b7e4f02b6a9fa76de8ed7f8afecd0eda55247112ff4223401`  
		Last Modified: Wed, 12 Jun 2024 18:52:45 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce46f48606178dcedec80045637615eab0fdd951fea4a6bd49c5083e076a856b`  
		Last Modified: Wed, 12 Jun 2024 18:52:45 GMT  
		Size: 77.6 KB (77610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7353e8c7cb28d9c7bb89e81aeb4007a9fe70557ad72c8a17e96ac1e74f611086`  
		Last Modified: Wed, 12 Jun 2024 18:52:45 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71bb5b3662d88962b2d3df35ed4f9232f0aa9e92cf7f3e4b3ca2d3f6d0e98caf`  
		Last Modified: Wed, 12 Jun 2024 18:52:57 GMT  
		Size: 101.7 MB (101709541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9512501e62d1aabc1a5fb818b524dc9afe759bc47b49653fdda9881367b00ae4`  
		Last Modified: Wed, 12 Jun 2024 18:52:46 GMT  
		Size: 61.5 KB (61482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u412-b08-jdk-nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull eclipse-temurin@sha256:213cfc48d6c1162f70bdfbe486c5d53db1de3e412277faafea859d572c6a8890
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.9 MB (256902909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c9a3cf4adedbf6bf61e269180206524d9f0f1c33f58e9d0c84f244a32c2cff`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 17:41:08 GMT
SHELL [cmd /s /c]
# Wed, 12 Jun 2024 17:41:08 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Wed, 12 Jun 2024 17:41:09 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 12 Jun 2024 17:41:09 GMT
USER ContainerAdministrator
# Wed, 12 Jun 2024 17:41:24 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Jun 2024 17:41:24 GMT
USER ContainerUser
# Wed, 12 Jun 2024 17:41:36 GMT
COPY dir:5498972beafb1de3e4749bc87b064f8ce9cec472aae9e7d0f4643a99f48638da in C:\openjdk-8 
# Wed, 12 Jun 2024 17:41:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce076c01ab33a997d8fa4a6a49752f31455fef6df331991ad3b3736b3567321`  
		Last Modified: Wed, 12 Jun 2024 18:40:43 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e103b0c4319eeff05be4b5cc015670eb122f3727896333159e7321bc10634963`  
		Last Modified: Wed, 12 Jun 2024 18:40:43 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8d6954eb39f9fd2f578ce496e72392db95feeba4f554191404ad7b6b709d5e`  
		Last Modified: Wed, 12 Jun 2024 18:40:42 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ff02bf0ad42d650e4abb942ee2fbdfb7ed0cf9a7ceae338aaa48c0a6dfc9cd`  
		Last Modified: Wed, 12 Jun 2024 18:40:41 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a84c83bc80d6b9b72ded2a37d4cfd8436c1a3bb6a6dae21c64eacf138db34d5`  
		Last Modified: Wed, 12 Jun 2024 18:40:41 GMT  
		Size: 76.0 KB (75997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f107f1e4d09247900bdf27d9c22c33a029f55e34fef8538899888171bba9a887`  
		Last Modified: Wed, 12 Jun 2024 18:40:41 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d22cfc6909b097347eb6f46d08a1092a9f0df3d2b12292b0e7e681c94b1772`  
		Last Modified: Wed, 12 Jun 2024 18:40:53 GMT  
		Size: 101.7 MB (101699154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c448abd661b393e23cff7543bcd83a1aed436ca6ff1c8e841237a2fddddd89e3`  
		Last Modified: Wed, 12 Jun 2024 18:40:41 GMT  
		Size: 88.8 KB (88759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
