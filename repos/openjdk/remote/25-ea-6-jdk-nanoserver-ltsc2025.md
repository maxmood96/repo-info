## `openjdk:25-ea-6-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:cc4b8b127f54947e29c0d47c561e28da06c35741ddee258c07a1dde5dc415456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `openjdk:25-ea-6-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:17dd0a32b83a724262f4373311dbc24c225b569470d6a45a2b9615f25bb5ffc8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.6 MB (406611738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c7de41f0bf9502a0397385e2c0145ba54b55d0acc53b9b16b92eef7e628391b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Wed, 22 Jan 2025 21:16:04 GMT
SHELL [cmd /s /c]
# Wed, 22 Jan 2025 21:16:05 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 22 Jan 2025 21:16:06 GMT
USER ContainerAdministrator
# Wed, 22 Jan 2025 21:16:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 22 Jan 2025 21:16:09 GMT
USER ContainerUser
# Wed, 22 Jan 2025 21:16:11 GMT
ENV JAVA_VERSION=25-ea+6
# Wed, 22 Jan 2025 21:16:17 GMT
COPY dir:f68a0a203262648eaad23f672eb21e06d231a686a9fcf56b24be2d2d46cfaae7 in C:\openjdk-25 
# Wed, 22 Jan 2025 21:16:24 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 22 Jan 2025 21:16:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303973f8fcab885da13334982934b6ca4e0619160524ec79d3bc8891b10231ce`  
		Last Modified: Wed, 22 Jan 2025 21:16:29 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f2fd8d1250b64b74238d0dc821ac217b4de5683a2c4076843ec5e0df78f90c`  
		Last Modified: Wed, 22 Jan 2025 21:16:29 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da07ddead9c467542de8075e9cbbcd5ecba2234e8456ef4dc9fddfada7a7beff`  
		Last Modified: Wed, 22 Jan 2025 21:16:29 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05faaa59235673c6e768cd2ffa206410feca9ba3b41f694c9a62d87afe1fa9b9`  
		Last Modified: Wed, 22 Jan 2025 21:16:29 GMT  
		Size: 76.6 KB (76553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3f233bc91a2b83dfb467aa5f80b25ebc9ec2942435c5eec9748ddd1f25632d`  
		Last Modified: Wed, 22 Jan 2025 21:16:28 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b3802163a4526513a38e0b2c97f6a1c1f926bcc167f53d403725e5549b321e`  
		Last Modified: Wed, 22 Jan 2025 21:16:28 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d634cb95715dd8088e7a9b02fafd93bdf705424857c9e6c95980333c5bcdd705`  
		Last Modified: Wed, 22 Jan 2025 21:16:39 GMT  
		Size: 207.4 MB (207370344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f52ed464df0ce5940d1395eebe83f9456eda847b692db035b399697b6ef8867`  
		Last Modified: Wed, 22 Jan 2025 21:16:28 GMT  
		Size: 104.1 KB (104127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112461794b1d0eae54bfad158d2bc7f7471e897e5be8dee305485f066c3df075`  
		Last Modified: Wed, 22 Jan 2025 21:16:28 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
