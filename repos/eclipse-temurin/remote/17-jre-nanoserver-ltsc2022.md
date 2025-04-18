## `eclipse-temurin:17-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:cb7e0edff2b01a93c8b8b9a65188d4d898a0f6c55217b4456e687a96997a10ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull eclipse-temurin@sha256:901776ff3eee22e84a99396c3185c5d17c6da0b855c39879e7424c3e21ecb0d6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166447989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab8cda4212808dc61d882738d89f8dddc7f709381f1e2e276e85d20665e7e8b0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Fri, 18 Apr 2025 04:20:20 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:20:21 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Fri, 18 Apr 2025 04:20:21 GMT
ENV JAVA_HOME=C:\openjdk-17
# Fri, 18 Apr 2025 04:20:22 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:20:25 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:20:25 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:20:29 GMT
COPY dir:e48212bf4bd9a001a558a3ce6925b9b3b6903c8af46347cbb9e06ca86192ff86 in C:\openjdk-17 
# Fri, 18 Apr 2025 04:20:33 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Wed, 16 Apr 2025 23:30:29 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f77c10b6ff1d0f4a8394720b82bf899d2758989c2023061f602158c466b3f0`  
		Last Modified: Fri, 18 Apr 2025 04:20:36 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09dcf74eb88f0a64d9ba892d69cd49bc0184d06a618d7a4fd98a83514e22031d`  
		Last Modified: Fri, 18 Apr 2025 04:20:36 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c77392d3f1bca9fc76e94fdafb7c37ab0d0ce30d94d8bf8df4a47c27f6abb74`  
		Last Modified: Fri, 18 Apr 2025 04:20:36 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce40ff911588f7a163f3248824acb6c12b6fdf355261196976b635e05e62daeb`  
		Last Modified: Fri, 18 Apr 2025 04:20:35 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29149ae9a93d43cf0785f74403dd638c6422327f09a4f7e726f36b0d70e64ec`  
		Last Modified: Fri, 18 Apr 2025 04:20:35 GMT  
		Size: 78.7 KB (78737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7992e415fb0c9216d827867acc6d771281538c8fd8d2069c08faf04fab22db8`  
		Last Modified: Fri, 18 Apr 2025 04:20:35 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11009c31d4fedaac1824f01d53f910338b4ce02d23e15c4bf9a54e4c2b1335c`  
		Last Modified: Fri, 18 Apr 2025 04:20:40 GMT  
		Size: 43.7 MB (43727796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88d7f00ad79d2763e3324f9ce50c48332fa96200e21c7b5da37233c86e6d51d`  
		Last Modified: Fri, 18 Apr 2025 04:20:35 GMT  
		Size: 97.2 KB (97233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
