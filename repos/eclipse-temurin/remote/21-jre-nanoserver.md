## `eclipse-temurin:21-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:1637ac5ed208fb7bb69f3dcff172b1b404ca526b11bdf4a02e82c962f8a7fe43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:65c1205182decf0dfef2f27db8a7953d2c71fccb69cbed8eb573fa288ed7d5de
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170425335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833ec730982102c7eea4049f617ef7524bd016e737b28aa26da5fad22272fe0c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Wed, 15 Jan 2025 18:01:48 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2025 18:01:48 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 15 Jan 2025 18:01:49 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 15 Jan 2025 18:01:50 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 18:01:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jan 2025 18:01:52 GMT
USER ContainerUser
# Wed, 15 Jan 2025 18:01:56 GMT
COPY dir:d301f311784d572cc6cc0a5ee90712dcade9d3f8b4a48a0f2df4274582f5072e in C:\openjdk-21 
# Wed, 15 Jan 2025 18:02:00 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a01e615305dd2d16888a74c4ed26ec69cae6b71242786f21768b77969d2a36`  
		Last Modified: Wed, 15 Jan 2025 18:02:05 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed3a5175961301d6051424913862ddc65557d0d6266b81dded813e01473a95f4`  
		Last Modified: Wed, 15 Jan 2025 18:02:05 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019fb5e9231428e85262335d8edf23b79fc066a47913a629ccee8fc13cfedf18`  
		Last Modified: Wed, 15 Jan 2025 18:02:05 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5ad51951169cd60a0fa27fb8bedc2ab0bb1fd2279fa97e16a9946fc86c1f8e`  
		Last Modified: Wed, 15 Jan 2025 18:02:03 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cce615580c4e000b1500fa84ec3970da988e13c6d9e8a84a87f35ca9d74f7fc`  
		Last Modified: Wed, 15 Jan 2025 18:02:03 GMT  
		Size: 75.5 KB (75510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5499412ef408b4d9578999ccab9e545326194c2d5ab819619f721c2d07c4d5e5`  
		Last Modified: Wed, 15 Jan 2025 18:02:03 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88783bb9c41c68b14f89574168d7b159b2071f802b2140a3b67c317a46b5c9b3`  
		Last Modified: Wed, 15 Jan 2025 18:02:09 GMT  
		Size: 49.6 MB (49586266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6f435b804482f07e9557010ec96fe004ae65d4bf9060f1a30045a21dbbda69`  
		Last Modified: Wed, 15 Jan 2025 18:02:03 GMT  
		Size: 96.8 KB (96823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:45378b02251842ae36cb5ba4e75163085bdc2124b1c5fb9efc7699414b809fc0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208319598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2054e90a28e996395634f51229b1300ba9b6ccc65603f2106ecca3113982b30`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 15 Jan 2025 18:02:19 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2025 18:02:21 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 15 Jan 2025 18:02:23 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 15 Jan 2025 18:02:24 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 18:02:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jan 2025 18:02:32 GMT
USER ContainerUser
# Wed, 15 Jan 2025 18:02:38 GMT
COPY dir:d301f311784d572cc6cc0a5ee90712dcade9d3f8b4a48a0f2df4274582f5072e in C:\openjdk-21 
# Wed, 15 Jan 2025 18:02:45 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0518f764b368beeb0ed8d1056aa8db1e4b1fe4f690798804807eb350a5f5d3da`  
		Last Modified: Wed, 15 Jan 2025 18:02:48 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5e283466aa6f32907338c83f064c1e50b563769c2df10f260c62cca851892e`  
		Last Modified: Wed, 15 Jan 2025 18:02:48 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788c8a5c347b2e3d83c5cf603efa2e4b05e7245e1e6de59df22968583b3fe7f6`  
		Last Modified: Wed, 15 Jan 2025 18:02:48 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2fab20c26fb09d362d85b32417f24a64fd92e407cd070768d41d19d9ae6cce`  
		Last Modified: Wed, 15 Jan 2025 18:02:47 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a1ef81838dfda8b6fc71df98c6c9a4e1d47d4c5d1e1e7b427deb6e085a8e17`  
		Last Modified: Wed, 15 Jan 2025 18:02:47 GMT  
		Size: 83.9 KB (83935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67db9790bf56abe4b0f4f1c1156a9515be166463443df69799c80024870da70f`  
		Last Modified: Wed, 15 Jan 2025 18:02:47 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da00196971ed0eda5f42c9d6b27eb64943fe418571546db44e8b4d5efa601349`  
		Last Modified: Wed, 15 Jan 2025 18:02:52 GMT  
		Size: 49.6 MB (49585735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3199da1cc4f3437f0abb53bf947e99dcf04e34be63a3acae6717fdad3354725f`  
		Last Modified: Wed, 15 Jan 2025 18:02:47 GMT  
		Size: 3.4 MB (3377191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
