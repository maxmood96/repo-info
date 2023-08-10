## `eclipse-temurin:20-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:d82b5b69745105b4a2fa45210694030939368493777bd92fa529869b2a293567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `eclipse-temurin:20-nanoserver-1809` - windows version 10.0.17763.4737; amd64

```console
$ docker pull eclipse-temurin@sha256:be60b529af41fa56590a8558d41687fd3ee220e274dc05bee08642790612786e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303780239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3390b5f677eaca292e3abc24164b420c4d711eef6b8f8c9930742e27f00de793`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 02 Aug 2023 08:33:47 GMT
RUN Apply image 10.0.17763.4737
# Wed, 09 Aug 2023 23:39:50 GMT
SHELL [cmd /s /c]
# Thu, 10 Aug 2023 00:06:51 GMT
ENV JAVA_VERSION=jdk-20.0.2+9
# Thu, 10 Aug 2023 00:06:51 GMT
ENV JAVA_HOME=C:\openjdk-20
# Thu, 10 Aug 2023 00:06:52 GMT
USER ContainerAdministrator
# Thu, 10 Aug 2023 00:07:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 10 Aug 2023 00:07:03 GMT
USER ContainerUser
# Thu, 10 Aug 2023 00:07:17 GMT
COPY dir:4ed074865171ba014f3c2f68f57ad2bb21a4dd6e4cf7ff9654ee6c4c6e5176c0 in C:\openjdk-20 
# Thu, 10 Aug 2023 00:07:29 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 10 Aug 2023 00:07:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:86fab75eb466cadf89d853682179b3b57eba9fe28c78041dd52bced81e18a627`  
		Last Modified: Tue, 08 Aug 2023 17:55:54 GMT  
		Size: 104.5 MB (104459386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7e08c5247c8c7d832882da17ac85015e9dd4d4dfc9e4114fc14746eb2abded`  
		Last Modified: Thu, 10 Aug 2023 00:21:01 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9575234e65f0976570bdba51047c45b788c182e59a4a86efb4e30d4521c51d`  
		Last Modified: Thu, 10 Aug 2023 00:29:16 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96fa2722f8ce44a51817418af6adfc29ee0522f15f87ba911f83eae6afd62db`  
		Last Modified: Thu, 10 Aug 2023 00:29:15 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e8e732dea3e0c5045455018aca97c4e3956b4d16523e55434ddd09ced37551`  
		Last Modified: Thu, 10 Aug 2023 00:29:15 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b616fa9db00ddfffdc8a08b4b5b953c148cf5fac4aebf6fad6e93a366d2687`  
		Last Modified: Thu, 10 Aug 2023 00:29:14 GMT  
		Size: 68.4 KB (68432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1e05a9538fe6c1208075edbb290cd34f9912ad871f9bf68547fda8513874dd`  
		Last Modified: Thu, 10 Aug 2023 00:29:14 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44638f71a1a6d90f3eacdb32369c8ad9c5ebde7a46d6e950171b6fcfa7b49ad2`  
		Last Modified: Thu, 10 Aug 2023 00:29:32 GMT  
		Size: 195.5 MB (195464445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33046371120fbfbd709a1e3d26af280cf78ec1a838cab30cc8b5db18b8385f7c`  
		Last Modified: Thu, 10 Aug 2023 00:29:15 GMT  
		Size: 3.8 MB (3781023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c85f50cd5fd154bfe93caa4fe6437935c394cd68c8d55d49ad36842f29c25b6`  
		Last Modified: Thu, 10 Aug 2023 00:29:13 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
