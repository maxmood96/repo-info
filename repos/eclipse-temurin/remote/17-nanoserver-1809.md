## `eclipse-temurin:17-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:f699cba86ccc6f3c872cb0c5fba1009f7a144738071087af63854b1feba80b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:17-nanoserver-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull eclipse-temurin@sha256:a5929185df5bc4250fd4e2ebf5f8fea14c7173de39ca205b865e64c942b886a3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.2 MB (345221025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2fb51964213869282bac8c846d2ce10655dea1e2373ec9e64091a408503d3f7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 16:38:43 GMT
SHELL [cmd /s /c]
# Tue, 23 Jul 2024 00:19:40 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Tue, 23 Jul 2024 00:19:41 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 23 Jul 2024 00:19:41 GMT
USER ContainerAdministrator
# Tue, 23 Jul 2024 00:19:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 23 Jul 2024 00:19:53 GMT
USER ContainerUser
# Tue, 23 Jul 2024 00:20:03 GMT
COPY dir:11f935f87b5561ba9de5a02e585d9b073f4114e9ab1765209f28e6005e01c91d in C:\openjdk-17 
# Tue, 23 Jul 2024 00:20:13 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 23 Jul 2024 00:20:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00a79547db1bc3ab4a5550f2ec9ba165e302f4a4984af3c1bfbbbe1726a3bf6`  
		Last Modified: Wed, 10 Jul 2024 17:28:00 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad586d68932eb4f5593d11718113bf29e815de2477942809ad435388afa4841e`  
		Last Modified: Tue, 23 Jul 2024 00:38:14 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe8249ad28f733c50edafc6a986eefeffd8a33247bcfdc8b66c207d6823afc3`  
		Last Modified: Tue, 23 Jul 2024 00:38:14 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc730398c9de27b889030709a242bd7da7ef3371588881e0a0aa2d50d5f0bda`  
		Last Modified: Tue, 23 Jul 2024 00:38:14 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9283bfea5738fe545d54136ad4cf589daa7ca9cd6b046c743d2801f60fc59ca0`  
		Last Modified: Tue, 23 Jul 2024 00:38:12 GMT  
		Size: 68.2 KB (68236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88c890511e21b6c2cf0a188d2b5d2b9d80684c0aacedc7a62399b5535209af6`  
		Last Modified: Tue, 23 Jul 2024 00:38:12 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e1520a5026f17ce6652c304f385dc2f4aaf675e5733d913f0a81206590bb7c`  
		Last Modified: Tue, 23 Jul 2024 00:38:26 GMT  
		Size: 186.5 MB (186459089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b15f488d26e6c465c143c2d2a06ba1d9728e282f57bb026f28fc42b77e1de32`  
		Last Modified: Tue, 23 Jul 2024 00:38:13 GMT  
		Size: 3.6 MB (3605442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafb0eb923190eaf35fa72ee47de26dd7880d0dbb88e7511d4cab497ef731fbf`  
		Last Modified: Tue, 23 Jul 2024 00:38:12 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
