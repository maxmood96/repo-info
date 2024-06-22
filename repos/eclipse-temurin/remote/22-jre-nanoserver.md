## `eclipse-temurin:22-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:b31909bb9fa27982f26416101b65fb51b144de536e7070e1d1ef8658e2ebdea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2529; amd64
	-	windows version 10.0.17763.5936; amd64

### `eclipse-temurin:22-jre-nanoserver` - windows version 10.0.20348.2529; amd64

```console
$ docker pull eclipse-temurin@sha256:9c2639a8a27ea71c0afe4b6df4912ecff3ebc38b7a66b52e11afd54c4a3e045b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169144221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f3ec2d0fe6420ef7c9ce8b4be8a520283dbbfc05b11d94751477da79102ddbe`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 19 Jun 2024 19:27:30 GMT
RUN Apply image 10.0.20348.2529
# Sat, 22 Jun 2024 00:50:29 GMT
SHELL [cmd /s /c]
# Sat, 22 Jun 2024 00:55:51 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Sat, 22 Jun 2024 00:55:52 GMT
ENV JAVA_HOME=C:\openjdk-22
# Sat, 22 Jun 2024 00:55:52 GMT
USER ContainerAdministrator
# Sat, 22 Jun 2024 00:56:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 22 Jun 2024 00:56:04 GMT
USER ContainerUser
# Sat, 22 Jun 2024 00:57:02 GMT
COPY dir:b356dfbfb05ab2ab46133b6b7ad4e4cb6a7442df8599937d6806166f02780fa5 in C:\openjdk-22 
# Sat, 22 Jun 2024 00:57:16 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:a8c295c425a912de308ded279124ae45fec44d55a451843fe5877155417f453c`  
		Last Modified: Fri, 21 Jun 2024 02:24:34 GMT  
		Size: 120.5 MB (120499549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c04e6fe7f33e5ed7b73641c362d031eb0404b55967c9af2b8fa6f2269d9f92`  
		Last Modified: Sat, 22 Jun 2024 01:06:26 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1432edd48bbe96a06fbdb18d5da876e887b1b6b11037182c0def7ddbbde8ad`  
		Last Modified: Sat, 22 Jun 2024 01:09:30 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a64a4a225ae27f529207036c0e9b40ba5865840eccc2375e543183fe59e6ebf`  
		Last Modified: Sat, 22 Jun 2024 01:09:30 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94ca3e305ab3fdbf1ceea9ff500aa2b0e183ae5189767c53a4e12b500102d33`  
		Last Modified: Sat, 22 Jun 2024 01:09:30 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc652f13eef1ee37ff1e7edad0bf97fd5d90af7019d734b049fe4a1edebb13e1`  
		Last Modified: Sat, 22 Jun 2024 01:09:28 GMT  
		Size: 77.2 KB (77240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685ff38dad0dcba80a11ea60813f5f0452c3a8d5c9d56b24f8d97e486e617f49`  
		Last Modified: Sat, 22 Jun 2024 01:09:28 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f5ace3cbbefd4823fb09c401e22682c38c4ab50dea17ee385ea766e8a65afb`  
		Last Modified: Sat, 22 Jun 2024 01:10:07 GMT  
		Size: 48.5 MB (48488175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3600a449a7aff23243032cde01b67d40dc9290408cc42323107f7b511a9603`  
		Last Modified: Sat, 22 Jun 2024 01:09:58 GMT  
		Size: 73.4 KB (73442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22-jre-nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull eclipse-temurin@sha256:179987eed58dfa73bf4abbe889e710f6e950e8096bcf86ca064045ef758cd776
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.0 MB (206975566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec86a98cc3b9e8e774b6c327320d872ace8eedcd64bc662b2b0bd6b63092a57`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 17:41:08 GMT
SHELL [cmd /s /c]
# Wed, 12 Jun 2024 18:22:06 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Wed, 12 Jun 2024 18:22:06 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 12 Jun 2024 18:22:07 GMT
USER ContainerAdministrator
# Wed, 12 Jun 2024 18:22:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Jun 2024 18:22:16 GMT
USER ContainerUser
# Wed, 12 Jun 2024 18:27:26 GMT
COPY dir:b356dfbfb05ab2ab46133b6b7ad4e4cb6a7442df8599937d6806166f02780fa5 in C:\openjdk-22 
# Wed, 12 Jun 2024 18:27:37 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce076c01ab33a997d8fa4a6a49752f31455fef6df331991ad3b3736b3567321`  
		Last Modified: Wed, 12 Jun 2024 18:40:43 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5bb9e22f72bbccf429aadef40dc26c849c616be19af7360d07022b9c6e3555`  
		Last Modified: Wed, 12 Jun 2024 18:51:22 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5cae84b96e4a481431f172fff202189402b245b163ddd7feac8e000d2bf81b7`  
		Last Modified: Wed, 12 Jun 2024 18:51:22 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74170a35e66cab58f46036320f076bcec608c8b45f1f28ba32d5535e5ac73f8`  
		Last Modified: Wed, 12 Jun 2024 18:51:22 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3e9274ed02b839b87962b770ca3f42c9422727dd32d2030fefbbc512312cae`  
		Last Modified: Wed, 12 Jun 2024 18:51:20 GMT  
		Size: 67.6 KB (67579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a6f4595ad9de5446ea5c7999b3706deed6381732a01ecd3415d1eaf4e2c2cb`  
		Last Modified: Wed, 12 Jun 2024 18:51:20 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9b30a4146631222d9766d485c18cdfa8498a108ac0b4fbe09b1714b157bc93`  
		Last Modified: Wed, 12 Jun 2024 18:52:37 GMT  
		Size: 48.5 MB (48487949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bae7c76d24731d69e5d3f353acfdf7d9e5ecde0f618cfd3383ca4c82670db9f`  
		Last Modified: Wed, 12 Jun 2024 18:52:28 GMT  
		Size: 3.4 MB (3381012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
