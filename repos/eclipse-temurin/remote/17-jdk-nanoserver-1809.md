## `eclipse-temurin:17-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:9e94ab30ff808f55a959a15e3dea8fa7ae4bfbef4a136089d9b4aa4495b9c2c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:17-jdk-nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:cd29f73dbee165e30b7e9e6ebbad5a0ff51c25abe2680f25dd0cb8cd6fdde949
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.2 MB (345179696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bebaaca967ab98aad83e0408d064057c6a100b3efef7bc335cbfd3101aabb44f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Sat, 19 Oct 2024 02:06:58 GMT
SHELL [cmd /s /c]
# Sat, 19 Oct 2024 02:07:00 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Sat, 19 Oct 2024 02:07:00 GMT
ENV JAVA_HOME=C:\openjdk-17
# Sat, 19 Oct 2024 02:07:01 GMT
USER ContainerAdministrator
# Sat, 19 Oct 2024 02:07:18 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 19 Oct 2024 02:07:18 GMT
USER ContainerUser
# Sat, 19 Oct 2024 02:07:27 GMT
COPY dir:90bd01c2ed4c0253f6ac9cf5667f45dc63e1de5f60f2ba53c8784cd5f813ea62 in C:\openjdk-17 
# Sat, 19 Oct 2024 02:07:33 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 19 Oct 2024 02:07:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90971c3df7cb103164f2727922f06634de3891bdab1c3ba93621d19ec49e7598`  
		Last Modified: Sat, 19 Oct 2024 02:07:39 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6cd9cf8fe7af23a4161a031ffc4269573cc4712e614d66afac8f067104c47b0`  
		Last Modified: Sat, 19 Oct 2024 02:07:39 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d2166adcff3743bbce23f7d73e75425a61cfe07113afdea31d86d12ea77e87`  
		Last Modified: Sat, 19 Oct 2024 02:07:38 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f02d991df733b51e987f78533c121a2a8df2c364491774c53d1d003a33a8987`  
		Last Modified: Sat, 19 Oct 2024 02:07:38 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b812a2320135d63372fa9bae21e870c05fba1273ba4934c0f066a5ee47343c5`  
		Last Modified: Sat, 19 Oct 2024 02:07:37 GMT  
		Size: 66.5 KB (66522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4df676b6a51cfa3d9e7fe94e19d439a6b810002c8257c281ba592e4bf53dd56`  
		Last Modified: Sat, 19 Oct 2024 02:07:37 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f68e1b5b25891dab18c8f096065fe03681ff647242de03cfcecd1375874ade`  
		Last Modified: Sat, 19 Oct 2024 02:07:48 GMT  
		Size: 186.4 MB (186420503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8070a0b0cec93368019032dd562ceff781696fe2529cd6cdcab092baeaa9a74`  
		Last Modified: Sat, 19 Oct 2024 02:07:38 GMT  
		Size: 3.6 MB (3592747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b58438a5b92fa5e0b65a83f53eee84aaff1ca668ffeac53283c0d5c8d8afd17c`  
		Last Modified: Sat, 19 Oct 2024 02:07:37 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
