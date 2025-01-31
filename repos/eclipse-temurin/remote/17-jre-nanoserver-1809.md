## `eclipse-temurin:17-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:83d508cf439010cdefe5ff6bdf5936abc739824c9ef6cb60d69cd31a80252de3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:17-jre-nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:2cbe46127d053fd504593a30154e5110c80c95a5064419a3688ebc7972422b36
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.0 MB (202043425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9088a193a0a995ee13e348d77c30725110c0b376853900001eabc1792697334d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Fri, 31 Jan 2025 02:11:46 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 02:11:48 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Fri, 31 Jan 2025 02:11:48 GMT
ENV JAVA_HOME=C:\openjdk-17
# Fri, 31 Jan 2025 02:11:49 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 02:12:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 02:12:08 GMT
USER ContainerUser
# Fri, 31 Jan 2025 02:12:17 GMT
COPY dir:e48212bf4bd9a001a558a3ce6925b9b3b6903c8af46347cbb9e06ca86192ff86 in C:\openjdk-17 
# Fri, 31 Jan 2025 02:12:23 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1d44072914e85d8aef8f480a6d089701677bcee11e6b8fd2aeffb001ef2eb2`  
		Last Modified: Fri, 31 Jan 2025 02:12:27 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e48fddc7733467c55c4aa368d87b972da7dca7709eeb179fccbd0414a1214f`  
		Last Modified: Fri, 31 Jan 2025 02:12:27 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51ef85cb87f1af29efe103a1470072cdb9cd31df84b1e8255da13102f2fe0ae`  
		Last Modified: Fri, 31 Jan 2025 02:12:27 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37973e712afd7b836700ddb4aee17bad305fcca7203eddeb3e33b5ec2227596`  
		Last Modified: Fri, 31 Jan 2025 02:12:26 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cacf67623da9b5d61a83b0125c59620d3ff80b9bf567f8cfb8baaafa7daead73`  
		Last Modified: Fri, 31 Jan 2025 02:12:26 GMT  
		Size: 65.6 KB (65554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e072ea265e19dc3e48e09724e792d30a06f4018d6ead3123891a22999eed20b`  
		Last Modified: Fri, 31 Jan 2025 02:12:26 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975c56306282a001cc1ca8f7f33d9eeafbd74f478a873057e9e7120782e055da`  
		Last Modified: Fri, 31 Jan 2025 02:12:31 GMT  
		Size: 43.7 MB (43728867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f20533afa69afeb1dd968c596928086f2cdcd12f86ffd6995ff798fdbdd82a9`  
		Last Modified: Fri, 31 Jan 2025 02:12:26 GMT  
		Size: 3.0 MB (2976091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
