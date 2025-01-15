## `eclipse-temurin:11-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:14e4550001ff67e0b7afe2300aa9ec862d91dfa7da2b621fb4c561bf0547c341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:5d2dea090a00f83e93c7346b3bf83d109adb707e1905d5a277a8a8d3f98c551d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165151845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f98d7bbcb87ad43a12da17630790571b939a2ba3fbb70ac01d91db37884d23c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Wed, 15 Jan 2025 18:03:44 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2025 18:03:46 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 15 Jan 2025 18:03:46 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 15 Jan 2025 18:03:47 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 18:03:50 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jan 2025 18:03:50 GMT
USER ContainerUser
# Wed, 15 Jan 2025 18:03:54 GMT
COPY dir:a15dacd11bbcaacf83a6b6e1490d6483ae4af68a125407fd4cb6bb7a70e4639c in C:\openjdk-11 
# Wed, 15 Jan 2025 18:03:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702ecb7213207878c5547fe11fb7ad15757faacd0a2967ab313bcdd7169a790d`  
		Last Modified: Wed, 15 Jan 2025 18:04:02 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbd0f63af70e369b7a5e3a1dc3d08b656b9508e96ef172109e99ad17b3c451b`  
		Last Modified: Wed, 15 Jan 2025 18:04:02 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0962b5c37f9951de726b2bd0937e270750dbd6f564ee27cb0c93105353e18c3c`  
		Last Modified: Wed, 15 Jan 2025 18:04:02 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05e01dc0fafeb96633a06c3cadb436accc4f9932301868d705643711bd37b34`  
		Last Modified: Wed, 15 Jan 2025 18:04:01 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01173cd0bca87a951bb197ed13cc31982b8b229c03c1c05026ef708f9289df7`  
		Last Modified: Wed, 15 Jan 2025 18:04:01 GMT  
		Size: 78.1 KB (78114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b3a06d06b94a931c1f42584c9c82f6ac654a4ff399900b45e9637b5bbd449b`  
		Last Modified: Wed, 15 Jan 2025 18:04:01 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a501623ba4e7fc0caae094c1c569d3e7edfb92be4903b7d447f9e0b01d318d0`  
		Last Modified: Wed, 15 Jan 2025 18:04:05 GMT  
		Size: 44.3 MB (44309073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5baf9ef006eb772adf314563a8eb84aa6d174e9133d99c04660c89cdd64772d8`  
		Last Modified: Wed, 15 Jan 2025 18:04:01 GMT  
		Size: 98.0 KB (97951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
