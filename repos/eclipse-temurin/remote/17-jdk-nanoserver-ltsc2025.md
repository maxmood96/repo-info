## `eclipse-temurin:17-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:e71e7b04931cb6c44cf2f984eaf345fa8abfd199183f0593ee302aa7c45fdef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `eclipse-temurin:17-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull eclipse-temurin@sha256:bbcc398cd74bb2f7660268adf12d13b443f065a8fa6b90864a46093889a1fe0f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.6 MB (379588391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6b151668115ffd8a36c3233607e4a0f21b4c2f93b32af4cd184ccd96009fd3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 07 Jun 2025 15:19:59 GMT
RUN Apply image 10.0.26100.4349
# Tue, 10 Jun 2025 22:15:25 GMT
SHELL [cmd /s /c]
# Tue, 10 Jun 2025 22:15:27 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Tue, 10 Jun 2025 22:15:28 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 10 Jun 2025 22:15:29 GMT
USER ContainerAdministrator
# Tue, 10 Jun 2025 22:15:33 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Jun 2025 22:15:34 GMT
USER ContainerUser
# Tue, 10 Jun 2025 22:15:42 GMT
COPY dir:642284f27aa03ba1e21a689edd99e2d493ba3e3290e848ff1bdf623fc783a5e1 in C:\openjdk-17 
# Tue, 10 Jun 2025 22:15:50 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 10 Jun 2025 22:15:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:709fa8bff22087ae5c45c65a3b0777eb6ee12afd1b773aece2a322e84b66b1d1`  
		Last Modified: Tue, 10 Jun 2025 22:41:49 GMT  
		Size: 192.1 MB (192082516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa9fa8512a839655b63a4c0add504fac44c541d870b875c58030985b1a2eed5`  
		Last Modified: Tue, 10 Jun 2025 22:16:37 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:737027a13e49234ac3198aaccd620d6a70e2d2f1b0a0e283ae9bfd8b6c8028c2`  
		Last Modified: Tue, 10 Jun 2025 22:16:37 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:272ceb00ede31590eb09023e3693da69deed8b9a40b6468ccb70aace61362987`  
		Last Modified: Tue, 10 Jun 2025 22:16:37 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a3266df16d54824b24f8393a132c3b28c7053fe8bc530b76d148db10923cd0`  
		Last Modified: Tue, 10 Jun 2025 22:16:37 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a25e53b1796974b296fc05480b0d06afc96191c6134a5d6f0814626f530f098`  
		Last Modified: Tue, 10 Jun 2025 22:16:37 GMT  
		Size: 75.7 KB (75697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cca45d85d3d03cd00512a60413f5022d5295f04e36a17756690cb1d558501f`  
		Last Modified: Wed, 11 Jun 2025 00:13:59 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a27b60f18d9b8d4bee4fd13447dddf7dc2297c15a716b87d6af8ea947dcaea7`  
		Last Modified: Wed, 11 Jun 2025 00:14:13 GMT  
		Size: 187.3 MB (187310170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da9ba2873718343dc8ecd965c7a1121ecd464b8c044a030d83356a8b22792a9`  
		Last Modified: Wed, 11 Jun 2025 00:13:59 GMT  
		Size: 113.7 KB (113653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39577d3ca1ea6dcad9f066c82e688e65fe77b86e395a84cb62ec4d9e0565fda`  
		Last Modified: Wed, 11 Jun 2025 00:13:59 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
