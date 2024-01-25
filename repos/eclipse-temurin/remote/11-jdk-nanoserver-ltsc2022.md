## `eclipse-temurin:11-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:1331d6921a6af3812b3f8d19962b35337ce0c2d4a90f3c1d09b8e4d3fe47cd75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `eclipse-temurin:11-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull eclipse-temurin@sha256:1837917d1220c57e3f965afe3bd7c25e2463e333d57298d5114157cbec543e22
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.9 MB (314903407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2948a0f1f39f23cd1cfa68e0f25c6e2783267d7c01ca4955052487e07d7e865`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 04 Jan 2024 03:13:36 GMT
RUN Apply image 10.0.20348.2227
# Wed, 10 Jan 2024 23:17:03 GMT
SHELL [cmd /s /c]
# Wed, 24 Jan 2024 21:54:51 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 21:54:52 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 24 Jan 2024 21:54:52 GMT
USER ContainerAdministrator
# Wed, 24 Jan 2024 21:55:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Jan 2024 21:55:03 GMT
USER ContainerUser
# Wed, 24 Jan 2024 21:55:19 GMT
COPY dir:06bb700052ae5de12c7654c6d453b954bdaac52e59d87856592b85cdd3ce67e9 in C:\openjdk-11 
# Wed, 24 Jan 2024 21:55:36 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 24 Jan 2024 21:55:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:11d5cdc5eaac7bace3ae1ecd3c0df2a27ef5005ab296c56b7f83e24bf25c236c`  
		Last Modified: Tue, 09 Jan 2024 20:57:18 GMT  
		Size: 120.8 MB (120769267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a5f2601f3a3b05b34c1f8683e3c9ea81ea63dbe1b04c37b85d09170f020fc0`  
		Last Modified: Thu, 11 Jan 2024 04:18:57 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b94e45fae708b0f7158f355b5c7b1b612328d98382452767f92e76f1fad98a`  
		Last Modified: Wed, 24 Jan 2024 22:12:04 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6220560fcf99c5da84f2fb116b11dae64b5c37ee20c84b15ae5f68b809d23dfb`  
		Last Modified: Wed, 24 Jan 2024 22:12:03 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9331775eb15d41534d010478da59f4a5c5d63ab3e32f6e754cfd5661522195f`  
		Last Modified: Wed, 24 Jan 2024 22:12:03 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7775b294baabf771e1a966e97bd6f83782cabdc3f4f7a95c5e14fea5a1e52d73`  
		Last Modified: Wed, 24 Jan 2024 22:12:02 GMT  
		Size: 82.8 KB (82823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c270d1788f3d09c93f2fd4b98b47bd9f9f707b93d8ad12f90bbd9d4a19e622`  
		Last Modified: Wed, 24 Jan 2024 22:12:01 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906e780962adcb7c6c30bd45f8f51a7279d73245df013ef5f5fcc052315a4a55`  
		Last Modified: Wed, 24 Jan 2024 22:12:19 GMT  
		Size: 194.0 MB (193982189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9914f32398015cbcb2cf7cbd64984672610565e6418dbc2451c2c9732831c59e`  
		Last Modified: Wed, 24 Jan 2024 22:12:02 GMT  
		Size: 62.1 KB (62147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671ff3023172836a2387395f7cefbadd6a939a075c172aefb0f0d57e2ea44ba4`  
		Last Modified: Wed, 24 Jan 2024 22:12:02 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
