## `eclipse-temurin:8-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:9a550ba4bd79b465be27e1f94f5098dc03fdfbcace4f4dd7d7b827b6a63c46a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2527; amd64

### `eclipse-temurin:8-nanoserver-ltsc2022` - windows version 10.0.20348.2527; amd64

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
