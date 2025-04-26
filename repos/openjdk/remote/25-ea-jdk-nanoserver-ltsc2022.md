## `openjdk:25-ea-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:1677b7d67b1a3853f66a798be29f59246e5e57cb67c11a546895ee38b6f27498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `openjdk:25-ea-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull openjdk@sha256:7590750fe75adad48d7e868b8685b0cee72c3f76928234540af7d64ba69bc6eb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330406836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:372efeb6ac181b2662ca3d4e1b6edaab30a3931af7521cbb5e7992c5bea710fd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Fri, 25 Apr 2025 22:17:38 GMT
SHELL [cmd /s /c]
# Fri, 25 Apr 2025 22:17:39 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 25 Apr 2025 22:17:40 GMT
USER ContainerAdministrator
# Fri, 25 Apr 2025 22:18:03 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 25 Apr 2025 22:18:04 GMT
USER ContainerUser
# Fri, 25 Apr 2025 22:18:05 GMT
ENV JAVA_VERSION=25-ea+20
# Fri, 25 Apr 2025 22:18:13 GMT
COPY dir:68bac63248f06b5a3c6e48fd170d3fc54c730eec81f70554d15d79ed34fe2288 in C:\openjdk-25 
# Fri, 25 Apr 2025 22:18:22 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 25 Apr 2025 22:18:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Wed, 16 Apr 2025 23:30:29 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e05e297e8ed2009fcd69b67d982c8b8f4c4385ee29e281cfa10cb04543cfd9`  
		Last Modified: Fri, 25 Apr 2025 22:18:27 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7aec49f736c308cbe381bf2fc6415cff88e17dc2e607551ac7171c76614c767`  
		Last Modified: Fri, 25 Apr 2025 22:18:27 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c7a0816d3c5ab9daaae4419402bd9a202720d4c502d2248834edf750daea77`  
		Last Modified: Fri, 25 Apr 2025 22:18:27 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8281d9aa4cb23b895af0113dbba423e846c2a4bccd4ffbab5a8d460435d5331f`  
		Last Modified: Fri, 25 Apr 2025 22:18:27 GMT  
		Size: 72.3 KB (72314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1ab1b8f67e8389d42b606f3702188f27d096f22a912097d17893d30c76ea30`  
		Last Modified: Fri, 25 Apr 2025 22:18:26 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f15b31a8db2208fb66f1f08ac72c12e6d2dbb74e75564adf2f526babb0940b`  
		Last Modified: Fri, 25 Apr 2025 22:18:26 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63324c1474e13803e8f64d0a0779f446efe8b73824293391aff1108b8354c96`  
		Last Modified: Fri, 25 Apr 2025 22:18:37 GMT  
		Size: 207.7 MB (207700807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61dc5cdf3ac63db31398210e9abd7d12eb8799de63e584b619328b724fa3c9e6`  
		Last Modified: Fri, 25 Apr 2025 22:18:26 GMT  
		Size: 88.5 KB (88452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b056dbe8f46591a25b812821e0f61eddf0aeb401bbaa85ecb8dce98e74e42a49`  
		Last Modified: Fri, 25 Apr 2025 22:18:26 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
