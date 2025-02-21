## `eclipse-temurin:8u442-b06-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:8a26b72b4993060cc60a318578435750ec1ef49267e29df703b2bc16a2727f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `eclipse-temurin:8u442-b06-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull eclipse-temurin@sha256:1600f08a5b565b8633b3398eb76e1ca76183d7afe2d382fbeb52c7a5f2aa1c6b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.4 MB (161408789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c63602f6d9b9aacac72c6f9a9a3d05dc8b88358b5ac78f1cf3ac1710b049d5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 20:45:43 GMT
RUN Apply image 10.0.20348.3207
# Thu, 13 Feb 2025 01:19:16 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:19:16 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 13 Feb 2025 01:19:17 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 13 Feb 2025 01:19:18 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:19:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Feb 2025 01:19:21 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:19:24 GMT
COPY dir:5687adced9ba5f2555526fe07fa3e848c7771941703db13fa4b29a0f81d58070 in C:\openjdk-8 
# Thu, 13 Feb 2025 01:19:28 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:938e4585b186fc3df3c1959d47ba7a634fea121cec7545db7923ceb191d99a33`  
		Last Modified: Tue, 11 Feb 2025 22:43:09 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ba70dbf3f40191b010fa33b1bd34f9d6f8d089219d77ba35d7c0c47ce22839`  
		Last Modified: Thu, 13 Feb 2025 01:19:32 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b0b4702ab0d37e437e1615b2294a4393d6d6edf8dcdc0908ea10d8c6f6fa92`  
		Last Modified: Thu, 13 Feb 2025 01:19:32 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e24a506ff8d7f646f1156acc8f33f0cb05ec18662f3dfd7f0b51b14e626470`  
		Last Modified: Thu, 13 Feb 2025 01:19:32 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c53fef263b73fbcbd35b639ac0e880af29a31e2558f9672035be8afdba1cca1`  
		Last Modified: Thu, 13 Feb 2025 01:19:31 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bfbade1fe44f7a88f34940ddf88b4b65f02ef84eb91e821c2ed2f8ed7f5b4c8`  
		Last Modified: Thu, 13 Feb 2025 01:19:31 GMT  
		Size: 77.8 KB (77766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5477b84876c85dedddf3eb09190837248be49feaa99bfc6422369535bf787a`  
		Last Modified: Thu, 13 Feb 2025 01:19:31 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba44beb4d6ef065bf8a185d11f5adc511ee3b5032ec4b92cdb39e5a5f68a796`  
		Last Modified: Thu, 13 Feb 2025 01:19:34 GMT  
		Size: 40.6 MB (40552285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0226aac1f12359a8767e8933a901f9f2fa5b5f51135035c18973ed860803d7fc`  
		Last Modified: Thu, 13 Feb 2025 01:19:31 GMT  
		Size: 107.0 KB (106980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
