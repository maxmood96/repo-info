## `eclipse-temurin:11-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:61e34c7705e1b1a38051a08d17385609c48499f796d88508b771c8e679230c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `eclipse-temurin:11-nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull eclipse-temurin@sha256:88d825fbc30e3f709fc4f633a1ca5fe91447f0ee4de6cbabe371fbe5bb6d6244
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.5 MB (317513070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf23410ad29fcce654e7c1ffc68e2a7c8df8c91fbe05c73bf1eddee23b0bb399`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Fri, 24 Oct 2025 19:21:09 GMT
SHELL [cmd /s /c]
# Fri, 24 Oct 2025 19:21:10 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Fri, 24 Oct 2025 19:21:11 GMT
ENV JAVA_HOME=C:\openjdk-11
# Fri, 24 Oct 2025 19:21:11 GMT
USER ContainerAdministrator
# Fri, 24 Oct 2025 19:21:17 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 24 Oct 2025 19:21:18 GMT
USER ContainerUser
# Fri, 24 Oct 2025 19:21:49 GMT
COPY dir:210c213d7567f4ae9108259b6c16f9783779d8f224bc53a31a49e53f33738954 in C:\openjdk-11 
# Fri, 24 Oct 2025 19:21:56 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 24 Oct 2025 19:21:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7729b23a010af9686f9afc668de371e8700b1d0dbcd0402878856359e69f441f`  
		Last Modified: Fri, 24 Oct 2025 19:22:45 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc77e61398d840efc9bfd2d78066ece0ad3662485fcb22df236a0ac149e34b3`  
		Last Modified: Fri, 24 Oct 2025 19:22:45 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0801cc9616c1e90f78ed09b425c1205438477431785cca24a5277de25c8a6b`  
		Last Modified: Fri, 24 Oct 2025 19:22:45 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0443a5ea1b039c07a016d67763755a9f4e00946acce361cbd7286e2e2a3a9d6b`  
		Last Modified: Fri, 24 Oct 2025 19:22:46 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7afe6e94e51b4f617c81345fda9b6b173cfe6980ad01035213b091e7ea4314fe`  
		Last Modified: Fri, 24 Oct 2025 19:22:45 GMT  
		Size: 71.7 KB (71660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ceca7f31cf6b202c7ce669afe4affa253f3c829e932ab609bb4b58cf39d0b0`  
		Last Modified: Fri, 24 Oct 2025 19:22:46 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6150cd721091c471e09f34ed43209809d5b900e9e3f98b5cf1c43a45617867f8`  
		Last Modified: Fri, 24 Oct 2025 21:12:52 GMT  
		Size: 194.6 MB (194619773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a50c1e1e5f2786ce8ce16ae12ee762f7187b2c50ea3794bd77880a6f81eeea9a`  
		Last Modified: Fri, 24 Oct 2025 19:22:45 GMT  
		Size: 131.2 KB (131193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab68c90a38606bb6085889be27f8ce91a2e47b51f846d9626736f68f23f439da`  
		Last Modified: Fri, 24 Oct 2025 19:22:45 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
