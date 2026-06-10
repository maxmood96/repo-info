## `eclipse-temurin:21-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:1f30d9ecbfc00694fa33d052d428c7d055671a3846e3cc0cfe058047eb3a2a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `eclipse-temurin:21-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull eclipse-temurin@sha256:acb80eb44161e5097fc5ed28d3e488a73e84e6855a522147d1c4d53b8bec1917
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.7 MB (398723999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94bc3f038a7e0de366e482946c5f044ec467437c5ef0efbed95663b3a25e3004`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 07:06:15 GMT
RUN Apply image 10.0.26100.32995
# Tue, 09 Jun 2026 23:20:59 GMT
SHELL [cmd /s /c]
# Tue, 09 Jun 2026 23:21:00 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 09 Jun 2026 23:21:02 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 09 Jun 2026 23:21:03 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2026 23:21:10 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Jun 2026 23:21:11 GMT
USER ContainerUser
# Tue, 09 Jun 2026 23:21:57 GMT
COPY dir:be4fce80d476aa164b4bdafca77eddb646da4c27d929101014e2067a583f974e in C:\openjdk-21 
# Tue, 09 Jun 2026 23:22:04 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 09 Jun 2026 23:22:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:64f5cd94d3bcd0fae94830b1fad0f8b3dc33677f8d7dc15c5219b56fe2a6584e`  
		Last Modified: Tue, 09 Jun 2026 22:11:30 GMT  
		Size: 196.7 MB (196668131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ab5707c2d79eb4001f8d5b866a44a91d6de92292c479800687533de823d0cb`  
		Last Modified: Tue, 09 Jun 2026 23:22:13 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e676c754ef8b64f17ccbe5758f29f76c425d6e4f7dadd34eecd5908aae0c82`  
		Last Modified: Tue, 09 Jun 2026 23:22:13 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025b7136c126c8488b825568afd816f0bb91b74047d678845d0c4d2f142938f6`  
		Last Modified: Tue, 09 Jun 2026 23:22:13 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2571dc95838a8487f9bb91ec470eeca8346992b95ef109c463d18593658e90`  
		Last Modified: Tue, 09 Jun 2026 23:22:13 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97bbd10670ff8d30173a49e05d29a54c2d95a23dc4e9a4369a9d017d3ffe753a`  
		Last Modified: Tue, 09 Jun 2026 23:22:11 GMT  
		Size: 71.1 KB (71133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cc1f60942bcb4a0f143fb7ada2fa9448b3ce4c66afcd2840c472a7bdc2ed90`  
		Last Modified: Tue, 09 Jun 2026 23:22:11 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9df3f3337d915f42a955a2b080dd114457fa7697759ebf967868a35d86c3625`  
		Last Modified: Tue, 09 Jun 2026 23:22:24 GMT  
		Size: 201.9 MB (201875356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2744a1b3f06a34367be71e96353675eb76988c8af32cb64b533ae6aa6e2b17`  
		Last Modified: Tue, 09 Jun 2026 23:22:12 GMT  
		Size: 103.1 KB (103112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1433e5f1271e8407f29898f0af871af7ea3bedcd732925b33e9494d056017985`  
		Last Modified: Tue, 09 Jun 2026 23:22:11 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
