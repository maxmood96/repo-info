## `openjdk:22-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:a365ac96d77ef55a59b41463a4992a4f0878a79629d6500c2066ff701b0c7921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `openjdk:22-jdk-nanoserver-1809` - windows version 10.0.17763.4737; amd64

```console
$ docker pull openjdk@sha256:eb3bf0bf80789307c7c6eb58c16eae66609ce302bce3f3e7c44acc30fa6b0d97
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.3 MB (307299357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd3350e551b1811c4bd239ea15c37d33fc3162210e4f938127fcad3275932f28`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 02 Aug 2023 08:33:47 GMT
RUN Apply image 10.0.17763.4737
# Wed, 09 Aug 2023 23:39:50 GMT
SHELL [cmd /s /c]
# Thu, 10 Aug 2023 02:42:08 GMT
ENV JAVA_HOME=C:\openjdk-22
# Thu, 10 Aug 2023 02:42:09 GMT
USER ContainerAdministrator
# Thu, 10 Aug 2023 02:42:19 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 10 Aug 2023 02:42:20 GMT
USER ContainerUser
# Tue, 29 Aug 2023 00:19:33 GMT
ENV JAVA_VERSION=22-ea+12
# Tue, 29 Aug 2023 00:19:48 GMT
COPY dir:41cbabb7c141be97f1c5bfbed2d29f4d4f704e0407b6bf871a0221f52cd9b028 in C:\openjdk-22 
# Tue, 29 Aug 2023 00:20:06 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 29 Aug 2023 00:20:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:86fab75eb466cadf89d853682179b3b57eba9fe28c78041dd52bced81e18a627`  
		Last Modified: Tue, 08 Aug 2023 17:55:54 GMT  
		Size: 104.5 MB (104459386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7e08c5247c8c7d832882da17ac85015e9dd4d4dfc9e4114fc14746eb2abded`  
		Last Modified: Thu, 10 Aug 2023 00:21:01 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a07a6ee55409326d8105cc13d850b1705bbe4498575cf2e27bc34e78a1b5063`  
		Last Modified: Thu, 10 Aug 2023 02:50:16 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f896f4ed09b9390bcd098f89bb4624ae91e82cf7a9c4588ecdeeaa28378701`  
		Last Modified: Thu, 10 Aug 2023 02:50:15 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa6961892f2fba93ceeaf5806dc38793f041309ff787a61ccbd94e178ffd4af`  
		Last Modified: Thu, 10 Aug 2023 02:50:16 GMT  
		Size: 71.1 KB (71084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d01d10dd6ecb83bb10dfbaee0c9743aa78c0fb19d3da95691428a5cb7c9e078`  
		Last Modified: Thu, 10 Aug 2023 02:50:13 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1a0ddcf13130ffd9b6ec9c400ecaaa02fa8adf3bbdda137597827585f021b2`  
		Last Modified: Tue, 29 Aug 2023 00:22:47 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45a46ce945213b0e40ab95473395350f81e45673e847a50f57860d55a2856fa`  
		Last Modified: Tue, 29 Aug 2023 00:23:07 GMT  
		Size: 198.9 MB (198919778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b525f73133e357def7438f8a172b3db865eb4c0a55f9b894624442d65c9b1a7`  
		Last Modified: Tue, 29 Aug 2023 00:22:48 GMT  
		Size: 3.8 MB (3842203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93599220aa7bafa5bf3b3af9057f88e1fb23b68d6fe290af162f9a934a7f302`  
		Last Modified: Tue, 29 Aug 2023 00:22:47 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
