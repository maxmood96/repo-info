## `eclipse-temurin:24-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:4e2ac5f5438b31c2a674147e0ca815ac779a0f81eec8e3c03f738051119f5f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4652; amd64

### `eclipse-temurin:24-jre-nanoserver-ltsc2025` - windows version 10.0.26100.4652; amd64

```console
$ docker pull eclipse-temurin@sha256:0dd89795d0ab0d3f212045ab4dbf1bfd12fbef167e2e25fac17f3d4b28fe7153
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.0 MB (251044988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e339560d474bf072372162feaa16db0466eb9c18941c5c9d78083ef51d4cc331`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Jul 2025 18:13:07 GMT
RUN Apply image 10.0.26100.4652
# Wed, 09 Jul 2025 19:15:42 GMT
SHELL [cmd /s /c]
# Wed, 09 Jul 2025 19:15:43 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 09 Jul 2025 19:15:44 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 09 Jul 2025 19:15:46 GMT
USER ContainerAdministrator
# Wed, 09 Jul 2025 19:15:50 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Jul 2025 19:15:51 GMT
USER ContainerUser
# Wed, 09 Jul 2025 19:15:55 GMT
COPY dir:ad5bc1bf6efc16ac6d52d57c1c7046f6f9b2ef9ef08387497ec457eb9554ce7d in C:\openjdk-24 
# Wed, 09 Jul 2025 19:16:01 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:2fd4507679915420227c89c4f57165747b37deaa62748936e2af8c2f38de0b4e`  
		Last Modified: Wed, 09 Jul 2025 01:51:41 GMT  
		Size: 193.2 MB (193150329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af5002706dc9f2ddf09e1961318bb2450c387c25f1b41ac1295e65f567a1fff`  
		Last Modified: Wed, 09 Jul 2025 19:16:33 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202f7f838e482f171a0023e52af555800470c2db7b43f0e69dc1917c81462901`  
		Last Modified: Wed, 09 Jul 2025 19:16:35 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745c565f834ba8c4ddb5d8c85e5c4c2ccf30ea27fe853235334f98ef001c1cd9`  
		Last Modified: Wed, 09 Jul 2025 19:16:33 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d1bc255b2b73cf3cefa9f0fcdad2711acf918e7b4ebeb9a7ffb25a970ba223`  
		Last Modified: Wed, 09 Jul 2025 19:16:34 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3672e32bc9cb01f42deaf9400b5df729d9f3ea4580d9ce16b4d2e5d46e8153`  
		Last Modified: Wed, 09 Jul 2025 19:16:33 GMT  
		Size: 75.7 KB (75673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f00b4ca5f6af4a76ad6b5da724207329c87a2348947ddc5152683dd248a667`  
		Last Modified: Wed, 09 Jul 2025 19:16:33 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2716f8a3648820af3ee666bee0bde9e425b2f40b2f8f37507c3f97b680205c33`  
		Last Modified: Wed, 09 Jul 2025 19:16:38 GMT  
		Size: 57.7 MB (57709971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e686f086fb009dd04b5a889ac7a4257e6239212f7d89bcd925678c5f3aa10cf`  
		Last Modified: Wed, 09 Jul 2025 19:16:34 GMT  
		Size: 103.7 KB (103746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
