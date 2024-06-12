## `eclipse-temurin:21-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:f28dea963288c5b274aae10c12c42e8e5ef464faf9f120a09b592b55dd1f2788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2527; amd64

### `eclipse-temurin:21-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.2527; amd64

```console
$ docker pull eclipse-temurin@sha256:5c63fcd3a02a68cc3b10bebadeeb570951acd84d3170c925bf04565cfb2e44ac
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.8 MB (321785133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84d043f6eebd76a28f3cbb287e4704f4ac482d37be1c4b7309892df99933bb79`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jun 2024 08:41:16 GMT
RUN Apply image 10.0.20348.2527
# Wed, 12 Jun 2024 18:27:44 GMT
SHELL [cmd /s /c]
# Wed, 12 Jun 2024 18:31:40 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Wed, 12 Jun 2024 18:31:41 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 12 Jun 2024 18:31:41 GMT
USER ContainerAdministrator
# Wed, 12 Jun 2024 18:31:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Jun 2024 18:31:52 GMT
USER ContainerUser
# Wed, 12 Jun 2024 18:32:08 GMT
COPY dir:23b4ead9c2036754f644b00182bded9da6af0a8e5b9adaf18f46a103fb435a07 in C:\openjdk-21 
# Wed, 12 Jun 2024 18:32:24 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Jun 2024 18:32:24 GMT
CMD ["jshell"]
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
	-	`sha256:3b40561204a4f3536062546d63933827486bc6620ff394e717285903f8d70960`  
		Last Modified: Wed, 12 Jun 2024 18:55:06 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae6e4cf930b7e987ea283c92fdf5be3d6c0c47f3aefbc75d3467e4e14093aac`  
		Last Modified: Wed, 12 Jun 2024 18:55:06 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0056ea243e3d4e283afee4558cb371e1ccddc3935caf8eda0362c1e8013964`  
		Last Modified: Wed, 12 Jun 2024 18:55:06 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59d5dca2a50ac3c094e0de2a94989b6b0d0f5183c4c6ea3d746f0664c9f0700`  
		Last Modified: Wed, 12 Jun 2024 18:55:04 GMT  
		Size: 82.2 KB (82237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7add38f094379695566e26a62a6c6596a2d22ffed119f1696c7b65e5f61d6933`  
		Last Modified: Wed, 12 Jun 2024 18:55:04 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990e47ddc0cd0a9862f7b62431a27b9c38eb972823d52952164dadee0a6ac80f`  
		Last Modified: Wed, 12 Jun 2024 18:55:22 GMT  
		Size: 201.1 MB (201148275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce208e5f819472c3fc98c62464fb954dce866bbe2a6894197fe24522af1f7be`  
		Last Modified: Wed, 12 Jun 2024 18:55:04 GMT  
		Size: 58.7 KB (58707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbb6ccd8ddfe27746b160283cbfc49b0aa40751de5c9d4620998ec01b88a945`  
		Last Modified: Wed, 12 Jun 2024 18:55:04 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
