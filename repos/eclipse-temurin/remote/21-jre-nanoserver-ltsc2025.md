## `eclipse-temurin:21-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:ffbb8c9be350de30e4054ceaad1a6d63dedfb600ed1c4d506884254f883412cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `eclipse-temurin:21-jre-nanoserver-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull eclipse-temurin@sha256:4a642a32ec686596dd10fd493ee64d0c87860369437ecc32bd600092316b84a0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241205881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6c2e9f542d53dafba6d93f1de3be3abbe8071d15116deaab0a0ab83a8f78c7f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 07 Jun 2025 15:19:59 GMT
RUN Apply image 10.0.26100.4349
# Tue, 10 Jun 2025 22:14:28 GMT
SHELL [cmd /s /c]
# Tue, 10 Jun 2025 22:14:29 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Tue, 10 Jun 2025 22:14:30 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 10 Jun 2025 22:14:31 GMT
USER ContainerAdministrator
# Tue, 10 Jun 2025 22:14:33 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Jun 2025 22:14:34 GMT
USER ContainerUser
# Tue, 10 Jun 2025 22:14:38 GMT
COPY dir:e77a568eefeac18db14cfb92f416dab13c56713fa78f747642b83f8e2eb5149f in C:\openjdk-21 
# Tue, 10 Jun 2025 22:14:43 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:709fa8bff22087ae5c45c65a3b0777eb6ee12afd1b773aece2a322e84b66b1d1`  
		Last Modified: Tue, 10 Jun 2025 22:41:49 GMT  
		Size: 192.1 MB (192082516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05047007e1707d07554a764224f98b8dd9b05d2df5ff78159108db7e191b8f8c`  
		Last Modified: Tue, 10 Jun 2025 22:15:26 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a38df05f482862ab94e4a7af4cdb1a709dec83335fb73d0bc1ba8d6a1fab76be`  
		Last Modified: Tue, 10 Jun 2025 22:15:26 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03eebb15af5ec6e7ef7b434d523b5e3a9bef3cdd3e33396fe8df4e2518667811`  
		Last Modified: Tue, 10 Jun 2025 22:15:26 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60a6420ed456f4c4789a6be1929918d9278c2ebc3638d6ff6727e1ff54dda49`  
		Last Modified: Tue, 10 Jun 2025 22:15:27 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0549dcff77c567e1d100231157f90c9c5de8ce036673a06ee2e2d5a49b7af5`  
		Last Modified: Tue, 10 Jun 2025 22:15:27 GMT  
		Size: 77.4 KB (77354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5490bd6fb856708d6289c87c526d8afe271b53f8e60a9882121478f1d5adcdea`  
		Last Modified: Tue, 10 Jun 2025 22:15:27 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc3213f27941b4697eeb88c0db08f0872cef2d517012b68a68df5018e967840`  
		Last Modified: Tue, 10 Jun 2025 22:15:30 GMT  
		Size: 48.9 MB (48946990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e32eaae8e331fbedcc52d42e5316e9e2cd70d582b6485e7b8c173abd473eab`  
		Last Modified: Tue, 10 Jun 2025 22:15:28 GMT  
		Size: 93.8 KB (93752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
