## `eclipse-temurin:25-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:285601696a321826b07f994678c9d30d7948ef4782ba2e4be232deaaae8ea523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `eclipse-temurin:25-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull eclipse-temurin@sha256:1607c95e61f476cacf7c87b713278ddde62721abc4ae532018edf2b28c62f3b6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.8 MB (260819002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3d96c84b699fc117bb575c85aa74539fa31732faf6f84878a15294ba59eec9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Sat, 08 Nov 2025 19:19:21 GMT
SHELL [cmd /s /c]
# Sat, 08 Nov 2025 19:19:22 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Sat, 08 Nov 2025 19:19:22 GMT
ENV JAVA_HOME=C:\openjdk-25
# Sat, 08 Nov 2025 19:19:23 GMT
USER ContainerAdministrator
# Sat, 08 Nov 2025 19:19:28 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 08 Nov 2025 19:19:28 GMT
USER ContainerUser
# Sat, 08 Nov 2025 19:19:54 GMT
COPY dir:889642903e29f32ff0f0b6da5f64cf6a40ecfa6d85d0926e4981ccbc885ac0c0 in C:\openjdk-25 
# Sat, 08 Nov 2025 19:19:58 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 08 Nov 2025 19:19:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8fcfa9b99eebc75a84c6511c7f2eafdc1efb8bf36c0e11e8f201e3c74228a1`  
		Last Modified: Sat, 08 Nov 2025 19:20:23 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e2a586b5ce3ab60bceddb7feeb354bd72cc3d0f747557469877c8ceeef3930`  
		Last Modified: Sat, 08 Nov 2025 19:20:23 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a51664d673a4eb59a615e60c29522d287380ac8d27b675d8e6bc83688b1032`  
		Last Modified: Sat, 08 Nov 2025 19:20:23 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b610d8d00411bb798a1c16e348cc88ce1eab2db9ff09c1e523ec498c7cc766d`  
		Last Modified: Sat, 08 Nov 2025 19:20:23 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2112b51a6ca48a93091da92b640b7ee5a1acad34173def1ee4192aa96971df4c`  
		Last Modified: Sat, 08 Nov 2025 19:20:23 GMT  
		Size: 69.7 KB (69676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a14f3225cb271eed5a2e33d38d06ef9994f1e0a8cc69d385a129bd3f172e8c36`  
		Last Modified: Sat, 08 Nov 2025 19:20:23 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52f8673f166de15864b6f76f8b7f5a30b58dfb28a8c7d11b1daa8419aec6e87`  
		Last Modified: Sat, 08 Nov 2025 22:21:07 GMT  
		Size: 138.0 MB (137951938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2246427734f43dd4b2d737117b2eea717b9a9c28a521a0c2dae8bc773983d6fc`  
		Last Modified: Sat, 08 Nov 2025 19:20:23 GMT  
		Size: 106.9 KB (106949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d6880c1ac529c0da77ebd866071b114b8704bece571c74fddbf5a9c29f0262`  
		Last Modified: Sat, 08 Nov 2025 19:20:23 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
