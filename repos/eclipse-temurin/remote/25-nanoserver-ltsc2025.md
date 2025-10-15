## `eclipse-temurin:25-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:cd2066d4066b0286dc6d161d0019aeb370e1a6da3237234664e3691bd3bedfc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6899; amd64

### `eclipse-temurin:25-nanoserver-ltsc2025` - windows version 10.0.26100.6899; amd64

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
