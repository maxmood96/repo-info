## `eclipse-temurin:8-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:a25c7490bd064d413e19bea0bdfc6760532959fd83f88ae181b77811853619e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `eclipse-temurin:8-jre-nanoserver-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull eclipse-temurin@sha256:5cc8b802db3e8372898c67a1b10354645ce25806c1a5ecfaafd54f119d7d0f36
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144600483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d0523e3eca216daf05f7969864017be5e74ece072af85635f46ffcdcebc872c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 29 Aug 2023 16:42:02 GMT
RUN Apply image 10.0.17763.4851
# Wed, 13 Sep 2023 02:29:44 GMT
SHELL [cmd /s /c]
# Wed, 13 Sep 2023 02:29:45 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Wed, 13 Sep 2023 02:29:45 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 13 Sep 2023 02:29:46 GMT
USER ContainerAdministrator
# Wed, 13 Sep 2023 02:29:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Sep 2023 02:29:57 GMT
USER ContainerUser
# Wed, 13 Sep 2023 02:34:49 GMT
COPY dir:f24575d0fd9e2979f5a8010c202ec6d963a3eb3cd788517e3ab1d758c8e6ad81 in C:\openjdk-8 
# Wed, 13 Sep 2023 02:35:02 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:17ba6b878467260559b72cb6f7e79c829eae67862a09efe87f6dc324f49fc086`  
		Last Modified: Tue, 12 Sep 2023 18:31:40 GMT  
		Size: 104.5 MB (104492504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a5bcbc9b0f0398bf8f14c235b24ba85d9acacf855518119cd1ce338a235a15`  
		Last Modified: Wed, 13 Sep 2023 03:36:33 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c2888b3f642e1b1385bfbf9deb93337f9ce2cc85d2b9d4bd36a6521d748567`  
		Last Modified: Wed, 13 Sep 2023 03:36:32 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac76b5fd5d37abc0b888fbadaca1529600eda8aa3cc72071592093ef8449318`  
		Last Modified: Wed, 13 Sep 2023 03:36:32 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c67d9ddb3e1826ea731a3f80884c665c21a5148abff12818787a5e47caae56f`  
		Last Modified: Wed, 13 Sep 2023 03:36:30 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e2efbb2925f0780ee2abcaff75dc2aa71939a7210d065703fbf6705008b8ac`  
		Last Modified: Wed, 13 Sep 2023 03:36:30 GMT  
		Size: 76.5 KB (76484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15e73b36640cedf631491a32e1f42dfab668944efd20ea45ecd333720639f4a`  
		Last Modified: Wed, 13 Sep 2023 03:36:30 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5c786c9ba6bb610c58930086a574117c0e47cdca19964bedd2d13208fd099a`  
		Last Modified: Wed, 13 Sep 2023 03:37:42 GMT  
		Size: 40.0 MB (39978995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76c7080e63932b6f7b521f13416780c2e7b4adb22c92174ff50034a437da43e`  
		Last Modified: Wed, 13 Sep 2023 03:37:36 GMT  
		Size: 46.7 KB (46694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
