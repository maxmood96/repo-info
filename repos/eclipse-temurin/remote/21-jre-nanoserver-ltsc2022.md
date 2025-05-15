## `eclipse-temurin:21-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:a24956666f9a5583864b5cfd89929834f0c5cce50de076d401f83153e9f5ebf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `eclipse-temurin:21-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull eclipse-temurin@sha256:5c8db03deb4a5080a4856771b48534766749321d0a737f43fdd1acaa6380c2c6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171714608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33777a94d5c45553db440cd2b1183763dc46bd25cd9b28305c6e7749f26ddb76`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Wed, 14 May 2025 21:18:49 GMT
SHELL [cmd /s /c]
# Wed, 14 May 2025 21:18:50 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 14 May 2025 21:18:50 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 14 May 2025 21:18:51 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 21:18:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 May 2025 21:18:54 GMT
USER ContainerUser
# Wed, 14 May 2025 21:18:59 GMT
COPY dir:e77a568eefeac18db14cfb92f416dab13c56713fa78f747642b83f8e2eb5149f in C:\openjdk-21 
# Wed, 14 May 2025 21:19:03 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf6008a9caec82732ee3e932d7b0aa1ab78c3868d420a77510758af56e19096`  
		Last Modified: Wed, 14 May 2025 21:19:06 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e2da16e67f25b602769b631dd334a1847aca94190936ee5a95eec43a925394`  
		Last Modified: Wed, 14 May 2025 21:19:06 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787872a0ec19feffa5230f28b1fa7e580af84a3fba74b8104c38596f46cf57d0`  
		Last Modified: Wed, 14 May 2025 21:19:06 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a38ae7d40c876fd77e6ff70f76ea43f424a6ba2c3b5fbd50d34bc15a1cf98b`  
		Last Modified: Wed, 14 May 2025 21:19:05 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d05cf234add71ecdb020ddb399c6b81d8e7f730da520979a34916d3bccb9872`  
		Last Modified: Wed, 14 May 2025 21:19:05 GMT  
		Size: 77.5 KB (77480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:725ed4845e2d6699b33081218291ad717ecb8fab14dbc3aa22a600c9c11c6b3f`  
		Last Modified: Wed, 14 May 2025 21:19:05 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5db7aa4162830d5bd8211c8c4c47ddf39a95b215e3f4438067c273ae5521863`  
		Last Modified: Wed, 14 May 2025 21:19:11 GMT  
		Size: 48.9 MB (48945895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6125e32c01c5b3b91260d1744743cebc4c0df637c51602e91a558bed0e50a87`  
		Last Modified: Wed, 14 May 2025 21:19:05 GMT  
		Size: 109.4 KB (109400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
