## `eclipse-temurin:25-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:5df827aab7b9085cd8e35936add39cb35f56a19cda3c780e153a2ae4d617e9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6899; amd64
	-	windows version 10.0.20348.4294; amd64

### `eclipse-temurin:25-jdk-nanoserver` - windows version 10.0.26100.6899; amd64

```console
$ docker pull eclipse-temurin@sha256:cc7633c80503d8753f936567fd233e2bd14c244d17d9b1f26db7cba253a5176b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.1 MB (332125551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb142840c4a89a8b2b65c632482535538aa857fc9138587b23df59e1be890436`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 11 Oct 2025 15:58:41 GMT
RUN Apply image 10.0.26100.6899
# Tue, 14 Oct 2025 21:13:44 GMT
SHELL [cmd /s /c]
# Tue, 14 Oct 2025 21:13:45 GMT
ENV JAVA_VERSION=jdk-25+36
# Tue, 14 Oct 2025 21:13:46 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 14 Oct 2025 21:13:46 GMT
USER ContainerAdministrator
# Tue, 14 Oct 2025 21:13:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Oct 2025 21:13:52 GMT
USER ContainerUser
# Tue, 14 Oct 2025 21:14:08 GMT
COPY dir:3b404a1cbcdf7278c6a85a2778d3f0c01bd0f1229e8c8ae0734ae7bd6fe589bb in C:\openjdk-25 
# Tue, 14 Oct 2025 21:14:13 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 14 Oct 2025 21:14:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:463edd10ad50b00cf92c69fc3eaa85e1fa40aad1b7938fa232899405bd80f001`  
		Last Modified: Tue, 14 Oct 2025 22:41:48 GMT  
		Size: 194.0 MB (194026741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b68ab870fe169bb7406c5e952672af773d7d592fd29fe201c012eabe5ab9d3`  
		Last Modified: Tue, 14 Oct 2025 21:15:09 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7cb24f5e3bd6e59e9207e2f01f3ce29b1a675a7f1ce345bc3c80cbbd471ab6d`  
		Last Modified: Tue, 14 Oct 2025 21:15:09 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b828c159f8e54d69ccf94484c7146cf67c2def3642e4c3bc593f00d7f88606`  
		Last Modified: Tue, 14 Oct 2025 21:15:09 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cc2773a769885f0c978ecd8725c6bad9607e955a93a356d04b485b2788abe5`  
		Last Modified: Tue, 14 Oct 2025 21:15:09 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d38c4fa98c3860e26be95ef726b1eda0d2f9a040124821645773ce0f5bf28331`  
		Last Modified: Tue, 14 Oct 2025 21:15:09 GMT  
		Size: 71.2 KB (71174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:488e960af1d85bf48cb62a6a6a53298a3e8da1772ffaa157a036a2cb26a19205`  
		Last Modified: Tue, 14 Oct 2025 21:15:09 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ea1975eca93e5892c07a7d4d7a4e6dd886df68700016d62692d5b8268855dc`  
		Last Modified: Wed, 15 Oct 2025 00:18:17 GMT  
		Size: 137.9 MB (137936474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:defb08a1f5f161715fdd1dc9223021a6e8e0a9079b4b4ab4dd34a8ceed1b7073`  
		Last Modified: Tue, 14 Oct 2025 21:15:09 GMT  
		Size: 84.8 KB (84820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caecbceef66656c621de2bd37c6042cd1b07302f339cad1338ca00da0c7b866d`  
		Last Modified: Tue, 14 Oct 2025 21:15:09 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:25-jdk-nanoserver` - windows version 10.0.20348.4294; amd64

```console
$ docker pull eclipse-temurin@sha256:20814c62f2f6e4af01c06e9244f42e01190b5cd2b10a194c6d5f66decf32d6c2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.8 MB (260817624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef21b9f944fa0b43b8e34ee1ad025f7c698c891f6fd150e6ad1919b1d379a3a4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Oct 2025 07:34:08 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 21:12:37 GMT
SHELL [cmd /s /c]
# Tue, 14 Oct 2025 21:13:18 GMT
ENV JAVA_VERSION=jdk-25+36
# Tue, 14 Oct 2025 21:13:18 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 14 Oct 2025 21:13:18 GMT
USER ContainerAdministrator
# Tue, 14 Oct 2025 21:13:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Oct 2025 21:13:21 GMT
USER ContainerUser
# Tue, 14 Oct 2025 21:13:30 GMT
COPY dir:3b404a1cbcdf7278c6a85a2778d3f0c01bd0f1229e8c8ae0734ae7bd6fe589bb in C:\openjdk-25 
# Tue, 14 Oct 2025 21:13:34 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 14 Oct 2025 21:13:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f68a3bbf3ee20b515c5b8b801e5627a9dac3782ef264e37060c34ed80e5d8874`  
		Last Modified: Tue, 14 Oct 2025 20:41:53 GMT  
		Size: 122.7 MB (122688886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cc1e407ae6e924b90e92be01a4a3da1bfc030b400da250e7591cd9ecad51cd`  
		Last Modified: Tue, 14 Oct 2025 21:13:12 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bebd96b3d485446fd8697e1c524c5e094949b156da24819abb35a6e604ae15`  
		Last Modified: Tue, 14 Oct 2025 21:14:09 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc0520df3614ae4cd1091f3ff2d4f3ebe4a367e368cffd08e85581ee67e4bc4`  
		Last Modified: Tue, 14 Oct 2025 21:14:09 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4950ea488542fd4433e503b4a61b0c9827f9e8723b38a335efff56589160f09`  
		Last Modified: Tue, 14 Oct 2025 21:14:09 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411e47c415cb052c34538b023982d09a475f4369eabce17491f0c63d1be4bba7`  
		Last Modified: Tue, 14 Oct 2025 21:14:09 GMT  
		Size: 78.6 KB (78645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca2179e5ac5d869966a275cd4f114f584534e990889b01b6c73202f781c6cf6`  
		Last Modified: Tue, 14 Oct 2025 21:14:09 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3369868dc67dd7d7425b21c302f4fc34ef0206ea31fdd2f390630a7760a0b94d`  
		Last Modified: Wed, 15 Oct 2025 00:18:19 GMT  
		Size: 137.9 MB (137936688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79ae854d7770f50dc2c1e7b29a419ff211b7f514f61e95ba10e16140a5f99f6`  
		Last Modified: Tue, 14 Oct 2025 21:14:09 GMT  
		Size: 107.1 KB (107051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bdfebd913ec93d61413d84a45e1bb9edc37bbafa742dad49574effdc694c75c`  
		Last Modified: Tue, 14 Oct 2025 21:14:09 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
