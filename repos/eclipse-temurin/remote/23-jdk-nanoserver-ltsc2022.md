## `eclipse-temurin:23-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:1a38ecda31fa3fd273a6c203ce5c3f9907f8c83f4eecae34f9e39bf907e0f5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `eclipse-temurin:23-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull eclipse-temurin@sha256:90945c743e3f412dfccca9493a906c64a399f336d49eab311b748ef5e7b03b2b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.9 MB (330898640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842af8a520181f5774f9f0cb3240fee4afc222769b6aafaca724b045eac2264f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Dec 2024 01:18:54 GMT
RUN Apply image 10.0.20348.2966
# Wed, 11 Dec 2024 21:48:45 GMT
SHELL [cmd /s /c]
# Wed, 11 Dec 2024 21:48:45 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 11 Dec 2024 21:48:46 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 11 Dec 2024 21:48:47 GMT
USER ContainerAdministrator
# Wed, 11 Dec 2024 21:48:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Dec 2024 21:48:50 GMT
USER ContainerUser
# Wed, 11 Dec 2024 21:48:57 GMT
COPY dir:997f391ddfc9feaa4d1b725e1babc077a76dd78201dd489cc8f03fe767c19cd0 in C:\openjdk-23 
# Wed, 11 Dec 2024 21:49:05 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 11 Dec 2024 21:49:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f9d5d5ca3244fc2c429a892cbe6066394790f649f32d59acfdf012e490896378`  
		Last Modified: Tue, 10 Dec 2024 18:34:17 GMT  
		Size: 120.6 MB (120601318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa825a06857fcef519974d69d43ae3afd8b2d171a8c32aeaadea6ff4ae3976e`  
		Last Modified: Wed, 11 Dec 2024 21:49:09 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1167278f39f1bc75236d63ac1e4e35d4e2e2f4f2306098aba8699710648167`  
		Last Modified: Wed, 11 Dec 2024 21:49:09 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1179472e8ed228c7beda33a65df90f247f1c605c72af03d7866f25dc7cc4a97d`  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b414b47d6818b890b2f721152465ccf54a12a65b046d967229055442448f8d3`  
		Last Modified: Wed, 11 Dec 2024 21:49:09 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484f1bb4cf46945556d4fb75b06d296bfd5ef301e3dee44c1b78b8a84e5417da`  
		Size: 77.7 KB (77734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406c4ef50a205f2e5f830de9c6ea7b2c994ed36822fda53a2b16350b2278d949`  
		Last Modified: Wed, 11 Dec 2024 21:49:08 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0b46b0800bb2ed437cfefc2114989a0990864e51bdbf5124045db88fcbf222`  
		Last Modified: Wed, 11 Dec 2024 21:49:19 GMT  
		Size: 210.1 MB (210105792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7784f3b68e73e5d4e5967eba596ee10ebec5050911be2a7b509e87a3f8ed0f`  
		Last Modified: Wed, 11 Dec 2024 21:49:08 GMT  
		Size: 107.4 KB (107421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dcf48f5699d6cdcc43836d5b5f484b516ae9baff7ff065e9d265cdbeb133601`  
		Last Modified: Wed, 11 Dec 2024 21:49:08 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
