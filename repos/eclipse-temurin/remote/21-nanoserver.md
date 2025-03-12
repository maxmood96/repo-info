## `eclipse-temurin:21-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:cccfb9cff831541496261dd11a43573ecbcd0993f5236c226d7dccd9ec24aae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `eclipse-temurin:21-nanoserver` - windows version 10.0.26100.3476; amd64

```console
$ docker pull eclipse-temurin@sha256:321fe8bac6a248f696720911e261b412a7c508a6b277c76e573c43524b0835b1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.0 MB (407975345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c9d662ec49c8b9b9c599063f59a898ca4ac9b933459477c5f3b5f60a4b9333`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Wed, 12 Mar 2025 19:17:32 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:17:33 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Wed, 12 Mar 2025 19:17:34 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 12 Mar 2025 19:17:36 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:17:40 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:17:41 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:17:49 GMT
COPY dir:87fb2a3fe15bf051f07e33b0f4d627a83582ff5ee0a30a4b75036496ad24f723 in C:\openjdk-21 
# Wed, 12 Mar 2025 19:17:59 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Mar 2025 19:18:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63cb0af4790fd9fa24f5a04f3b0c3cd3f4b2365b302f31a48ce57e81f623275`  
		Last Modified: Wed, 12 Mar 2025 19:18:05 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693902bde0060fa4e856b13505fdc66736429a988ca0133e7a45f6d45d15164f`  
		Last Modified: Wed, 12 Mar 2025 19:18:05 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaf65f6164e37e76f6edb5dfaba3ed74718f53e1585cb5a3e899e52ed363650`  
		Last Modified: Wed, 12 Mar 2025 19:18:05 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91871d109e03dcb9aec98f079453eff0dc3ea8adbc8f87e9da78db67cd7b5e41`  
		Last Modified: Wed, 12 Mar 2025 19:18:05 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febda657a6b33f600c7c5b78cba0b9339b2878b4a5d5b871c6a63534bfbf6c5e`  
		Last Modified: Wed, 12 Mar 2025 19:18:04 GMT  
		Size: 75.9 KB (75853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d570c19ede791dd5632a1c0f943e2cd22ac6bcda22dd470653ac07305e6490c1`  
		Last Modified: Wed, 12 Mar 2025 19:18:04 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9303ed57525f1c8bcb012e7c43f5321e22d578127c2fe3523ad88f59ecedee4d`  
		Last Modified: Wed, 12 Mar 2025 19:18:15 GMT  
		Size: 201.5 MB (201476025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f90c4330fb08bb68d2a844902ebfca7539af8c3bd0a500c23bfafe575077d8`  
		Last Modified: Wed, 12 Mar 2025 19:18:04 GMT  
		Size: 114.9 KB (114923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:500c28e1a89af560c55ba040a34d2a79c6d6dfef83f2348d78715c480d5a5d0c`  
		Last Modified: Wed, 12 Mar 2025 19:18:04 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-nanoserver` - windows version 10.0.20348.3328; amd64

```console
$ docker pull eclipse-temurin@sha256:c1cb12141daafbca65ed33d17d8528e90083b28d363232ae76079f4f3628b4a4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322361273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36aa88539e50413b5f50398d81cea6490c2eb6680cc2ff88d5c46dbd2133ae99`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Wed, 12 Mar 2025 19:21:15 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:21:16 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Wed, 12 Mar 2025 19:21:17 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 12 Mar 2025 19:21:18 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:21:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:21:21 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:21:29 GMT
COPY dir:87fb2a3fe15bf051f07e33b0f4d627a83582ff5ee0a30a4b75036496ad24f723 in C:\openjdk-21 
# Wed, 12 Mar 2025 19:21:34 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Mar 2025 19:21:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8cfb411f0d924614195c4591d3fbd5748c8568f99c75da90b13cd30d50f912`  
		Last Modified: Wed, 12 Mar 2025 19:21:38 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3843ef4f4640ee229b83a9df130defb616770d9db95c21f18d0753fb9e36abd6`  
		Last Modified: Wed, 12 Mar 2025 19:21:38 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7482bfdfc51a0d083a0e2528aa419005e17c3157532a6daa8c945c9da2eff418`  
		Last Modified: Wed, 12 Mar 2025 19:21:37 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3d74c986f892c1a2bca8cf2bf7d6bba8874e0280a0a9022ac85784425191c6`  
		Last Modified: Wed, 12 Mar 2025 19:21:38 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af68a7d718c79b53e5857f28b22419a5b934331e8543f04bbdf697d7ba868b4`  
		Last Modified: Wed, 12 Mar 2025 19:21:37 GMT  
		Size: 76.6 KB (76635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d51f6b18bbb59aa6234630061fc587429740422a209741efe462069c6ac33e`  
		Last Modified: Wed, 12 Mar 2025 19:21:36 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27942e712f377ddbf70184d1180cd29cf7ad819df5c0871c9e80518f079a2f05`  
		Last Modified: Wed, 12 Mar 2025 19:21:48 GMT  
		Size: 201.5 MB (201475584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5ef297db8830846f2aed41cca0d2b0af2a10a32834aba6f835979234699f18`  
		Last Modified: Wed, 12 Mar 2025 19:21:37 GMT  
		Size: 107.3 KB (107294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbbc8bc8cc517b4c160529d580403b3fd75357e43047f60d8e25e26f97f8f88`  
		Last Modified: Wed, 12 Mar 2025 19:21:37 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-nanoserver` - windows version 10.0.17763.7009; amd64

```console
$ docker pull eclipse-temurin@sha256:d31df68726e3b9f2eceeb2c60653302185ae6e425438e2242cb9082750c6ae20
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.3 MB (312284750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f19af27b2d2e7be69a741890c921d087c5f4ebb0f2ac8d99a3190e248943e1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Wed, 12 Mar 2025 19:20:15 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:20:16 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Wed, 12 Mar 2025 19:20:16 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 12 Mar 2025 19:20:17 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:20:19 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:20:20 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:20:27 GMT
COPY dir:87fb2a3fe15bf051f07e33b0f4d627a83582ff5ee0a30a4b75036496ad24f723 in C:\openjdk-21 
# Wed, 12 Mar 2025 19:20:32 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Mar 2025 19:20:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633f59717174c850348fe3b434bc068593733d2346e5c6fbbe529aee63882d4d`  
		Last Modified: Wed, 12 Mar 2025 19:20:40 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16104bba48dd3f262a1756ee0c39c520ec395044b6c17eec513018085d1a3a77`  
		Last Modified: Wed, 12 Mar 2025 19:20:40 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0482c5222d87fc37204d3c7ff8353d32d2e8295ef2d4c6841f228e54d033778`  
		Last Modified: Wed, 12 Mar 2025 19:20:40 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c03d2e2b3139f16c922e7661e82c9e2f8755efca961aa43df372a963a9ff885`  
		Last Modified: Wed, 12 Mar 2025 19:20:40 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e8b1b7ee6a41bca3c51e594346839c0e5b2b0d820d6e236a634c24b970d106`  
		Last Modified: Wed, 12 Mar 2025 19:20:38 GMT  
		Size: 70.5 KB (70460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533408626693c507c6339b2dee63b9025758cd2fca34256fa9535685385d257f`  
		Last Modified: Wed, 12 Mar 2025 19:20:38 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd289ee9eaf2cc98b0eea2f219c35ecc10acae4b99dc80831c609261348e213`  
		Last Modified: Wed, 12 Mar 2025 19:20:49 GMT  
		Size: 201.5 MB (201476126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ba3d812be4f32aad0f951e94e51a61bdf668d408b70f403bc5396c492e9593`  
		Last Modified: Wed, 12 Mar 2025 19:20:38 GMT  
		Size: 3.8 MB (3823839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c196135ca02bfcbd9d80724698d5bc2bfd0a48bd46a089118d2cf8564a4cdc`  
		Last Modified: Wed, 12 Mar 2025 19:20:38 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
