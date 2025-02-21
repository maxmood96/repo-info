## `eclipse-temurin:21-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:8c37b0cfab4897be1f409b7c7dcad8d582fbaefb79b4d66525b815373fc43c17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `eclipse-temurin:21-nanoserver-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull eclipse-temurin@sha256:54c0c06cd530206dabd5cd195b4a4b064ba3f37a747192821649a33e2e35f845
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322332044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c66a71c18e985a3ed38861e6f77a60bbe3d22ce2cc27dcb30dac6adbf68e20`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 20:45:43 GMT
RUN Apply image 10.0.20348.3207
# Thu, 13 Feb 2025 01:17:51 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:17:52 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 13 Feb 2025 01:17:53 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 13 Feb 2025 01:17:53 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:17:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Feb 2025 01:17:55 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:18:01 GMT
COPY dir:87fb2a3fe15bf051f07e33b0f4d627a83582ff5ee0a30a4b75036496ad24f723 in C:\openjdk-21 
# Thu, 13 Feb 2025 01:18:07 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 13 Feb 2025 01:18:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:938e4585b186fc3df3c1959d47ba7a634fea121cec7545db7923ceb191d99a33`  
		Last Modified: Tue, 11 Feb 2025 22:43:09 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25204a15728e70eb8e35e7cb44e768c524a477784378eaa531d68c359bb6f0c`  
		Last Modified: Thu, 13 Feb 2025 01:18:11 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcf13b226ea154427f770f93321e475d68a5ee671b6ed97454fd20b04231954`  
		Last Modified: Thu, 13 Feb 2025 01:18:11 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c6b32d586d1a0d0c73a07dd153dc33991ba68d037c2930febd1aefe99d9ab8`  
		Last Modified: Thu, 13 Feb 2025 01:18:11 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8463af7ed57afbc6c200fd0329e9ba017850c52acaa66c9de97f0062c317ab8c`  
		Last Modified: Thu, 13 Feb 2025 01:18:11 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19736f5dd304c1bfad747f23783e32e1b99df669dcae5b8775b3b2bf9d217e2`  
		Last Modified: Thu, 13 Feb 2025 01:18:10 GMT  
		Size: 77.1 KB (77096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4873c2bcfba1bdad7aaa9f70cf1c9029dadf283634968bd3551dd97977fd93cc`  
		Last Modified: Thu, 13 Feb 2025 01:18:10 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e29bdf28368d835c2bc330696b4b5b6f984efea2a4c9184a1f576239350b5d6`  
		Last Modified: Thu, 13 Feb 2025 01:18:21 GMT  
		Size: 201.5 MB (201475465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c6cbff5cd4f9d9a26755f3f287991233fe5ab5b0c6af103293949ba3789fb3`  
		Last Modified: Thu, 13 Feb 2025 01:18:10 GMT  
		Size: 106.7 KB (106684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a1b2e23cb8ab9c695984677e45dbf8783e492291f8a498724754f703116b9a`  
		Last Modified: Thu, 13 Feb 2025 01:18:10 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
