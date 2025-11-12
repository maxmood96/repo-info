## `eclipse-temurin:11-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:f941813319d3a2d3a4a9da559626d53d0339938c2e9d25ea86c6971b799ddd47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `eclipse-temurin:11-nanoserver` - windows version 10.0.26100.7171; amd64

```console
$ docker pull eclipse-temurin@sha256:1c2ace8b698310c5ce2930148e6da477dfc3307b6ed2177ca7f0a300ddbd0ce5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.8 MB (392794983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde68496688b2663294f269704e8b983f35686cd20d3c43035d1f52fbc1e03b0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 09 Nov 2025 10:04:50 GMT
RUN Apply image 10.0.26100.7171
# Tue, 11 Nov 2025 20:11:08 GMT
SHELL [cmd /s /c]
# Tue, 11 Nov 2025 20:11:09 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Tue, 11 Nov 2025 20:11:09 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 11 Nov 2025 20:11:09 GMT
USER ContainerAdministrator
# Tue, 11 Nov 2025 20:11:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 11 Nov 2025 20:11:13 GMT
USER ContainerUser
# Tue, 11 Nov 2025 20:11:30 GMT
COPY dir:207a50c3961430a3231a748eb9ce354eec00313f0753b2d5e8f279d3afd46cd8 in C:\openjdk-11 
# Tue, 11 Nov 2025 20:11:35 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 11 Nov 2025 20:11:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:87c91227213eb6e7c8cfe33b6bd0429350e524756878f37f3860b013f804bf59`  
		Last Modified: Tue, 11 Nov 2025 20:41:49 GMT  
		Size: 197.9 MB (197936447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6194cd77702c569004d9457e0c06be0662b8256bcd8f00c1d770f01827ff09e`  
		Last Modified: Tue, 11 Nov 2025 20:12:01 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67871f81b5ec40ac602e45a83ebe454e076338464f766992203bc1f53f4e1a35`  
		Last Modified: Tue, 11 Nov 2025 20:12:01 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c35afdfbbc4c4b0757cc4c62c9ebc693d58f784680717e31026a5c9067ae2db`  
		Last Modified: Tue, 11 Nov 2025 20:12:02 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e791920643a287ad1c39321fa982e9dec7b3587424d99d26b6554d861f686d`  
		Last Modified: Tue, 11 Nov 2025 20:12:02 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef790762d90ad66ecef8715e67bffff3b1d67033204833d8cf9b46d4f986fdf`  
		Last Modified: Tue, 11 Nov 2025 20:12:02 GMT  
		Size: 69.4 KB (69449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c973c6572d8c7d29ac1d3f9489cd0cf6a0d741c2e1f87cd84dba78f5666b318`  
		Last Modified: Tue, 11 Nov 2025 20:12:02 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16b0aa9daeedbef78d5ef96ba6d82ea4924d3dd24903e783786de787748ca5a`  
		Last Modified: Tue, 11 Nov 2025 22:13:01 GMT  
		Size: 194.7 MB (194670594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c90c2e6e877d122887029383a02ef8cdce9a5a92aec6c67aa97060be1007e1`  
		Last Modified: Tue, 11 Nov 2025 20:12:02 GMT  
		Size: 112.1 KB (112140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd1d483696e0605e62da83b7ce480d25f9ce7a73f43a76b6450d22eaeedd0061`  
		Last Modified: Tue, 11 Nov 2025 20:12:02 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-nanoserver` - windows version 10.0.20348.4405; amd64

```console
$ docker pull eclipse-temurin@sha256:e9c7713328396e6b94c40e9dbfa06802ad863dd72383d05ccbfcedf2d37f86e0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.2 MB (321218565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2cbca55aaad35a0fc76c111597d61781df9e9e045902d31f27c938e91a11b11`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 11 Nov 2025 20:11:06 GMT
SHELL [cmd /s /c]
# Tue, 11 Nov 2025 20:11:07 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Tue, 11 Nov 2025 20:11:07 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 11 Nov 2025 20:11:07 GMT
USER ContainerAdministrator
# Tue, 11 Nov 2025 20:11:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 11 Nov 2025 20:11:09 GMT
USER ContainerUser
# Tue, 11 Nov 2025 20:11:16 GMT
COPY dir:207a50c3961430a3231a748eb9ce354eec00313f0753b2d5e8f279d3afd46cd8 in C:\openjdk-11 
# Tue, 11 Nov 2025 20:11:21 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 11 Nov 2025 20:11:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97be436214312a6298d6bd952225e6bd6e31ec3de7e85f7960b99f405d5e9ff8`  
		Last Modified: Tue, 11 Nov 2025 20:11:46 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2cba1572ea09f1a5ec91c52c80ca86a4329ddb251c6f1fa0177c423c2fb824e`  
		Last Modified: Tue, 11 Nov 2025 20:11:46 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c427728add9669ee56c567aef50d673b57128e8be97db9f01c2e752f7b1822`  
		Last Modified: Tue, 11 Nov 2025 20:11:46 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06536cbc99cec4dc1adfba32f9011672f5e3e88fc0d18e47ed4616cabd9d3f7`  
		Last Modified: Tue, 11 Nov 2025 20:11:46 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996c77a0a9fc8d0b4e7eff97327c02a58bc14a9659dd79945116f586476430a5`  
		Last Modified: Tue, 11 Nov 2025 20:11:46 GMT  
		Size: 86.4 KB (86373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ed31a831be550aa176808e49bdaa111923d37fac52d2f7aa5e0884aeca7a6d`  
		Last Modified: Tue, 11 Nov 2025 20:11:46 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390e3592d980e3ea4f2ddb527a5be5442d465dce6b6121f76c7a502cbb0a28fc`  
		Last Modified: Tue, 11 Nov 2025 22:13:03 GMT  
		Size: 194.7 MB (194670240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b460cd67c65a9ed0b8b21f9966e413642b06ddfa37ad41d5de7c626844935d86`  
		Last Modified: Tue, 11 Nov 2025 20:11:46 GMT  
		Size: 106.5 KB (106516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13a235935b4e5d4838ea160575ada0691aa6ff4e29e9080e11d46f127498fd6`  
		Last Modified: Tue, 11 Nov 2025 20:11:46 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
