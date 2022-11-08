## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:ceb9df1967434eec1ab6066568ea423bec0ec92123e28982e3928d97ec1aba6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1249; amd64
	-	windows version 10.0.17763.3650; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.20348.1249; amd64

```console
$ docker pull eclipse-temurin@sha256:c882c634904abd3c3ecd4f338157b0bae2e095bac077ac35499d1cccf70e6687
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165199692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597e9de8df7b2edd8696ff141857ea6f9ac0887cf5b1c71a116c7e6745f4a545`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Nov 2022 07:21:30 GMT
RUN Apply image 10.0.20348.1249
# Tue, 08 Nov 2022 19:27:23 GMT
SHELL [cmd /s /c]
# Tue, 08 Nov 2022 19:29:25 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Tue, 08 Nov 2022 19:29:26 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 08 Nov 2022 19:29:27 GMT
USER ContainerAdministrator
# Tue, 08 Nov 2022 19:29:40 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 08 Nov 2022 19:29:40 GMT
USER ContainerUser
# Tue, 08 Nov 2022 19:31:03 GMT
COPY dir:f12bd30467bc1b7f61ca05a6124e6eb838888f3685c56f372d6fed2165b193b1 in C:\openjdk-11 
# Tue, 08 Nov 2022 19:31:32 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:72e5d750fe8c1a32d4a26ef3b4a4e1f6124ac079b142f12724af2abfcba1c8b3`  
		Last Modified: Tue, 08 Nov 2022 19:57:58 GMT  
		Size: 122.1 MB (122092167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd83067a7e6c6d9dab3ac0265a21919de95a0bf4e737e647fbf3e43c9874b0`  
		Last Modified: Tue, 08 Nov 2022 19:57:27 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf64ef5841c3055c97da30afe94e91f36d8258ef461b52540da9903c4e3bc9a`  
		Last Modified: Tue, 08 Nov 2022 19:58:33 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c375a4f91fe23421131785b0b42e01c977a392cf2b3e31402bf0d22f9485b2`  
		Last Modified: Tue, 08 Nov 2022 19:58:33 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37f60d8c806f3324c10a3f609dd590835d2f256a88a14d5555cbee6050df6e4`  
		Last Modified: Tue, 08 Nov 2022 19:58:32 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea17a3ec8151119077e9676e7507f58607330aade351454cc2b611ce183fdc90`  
		Last Modified: Tue, 08 Nov 2022 19:58:30 GMT  
		Size: 85.1 KB (85094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d30911c1c2bad5db46115e443e5a3fb3242f0d01dae68a8b470990aee8b83c`  
		Last Modified: Tue, 08 Nov 2022 19:58:30 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0175b41e5a484bde62357172b9b18b47976e8d786f500ff8ea680e53b894ae44`  
		Last Modified: Tue, 08 Nov 2022 19:59:15 GMT  
		Size: 43.0 MB (42954870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a1389b4f6c4a9ab430911e5a3811bb5682f47c9fb4dfe386a16e2cc6ce0aae`  
		Last Modified: Tue, 08 Nov 2022 19:59:06 GMT  
		Size: 61.9 KB (61895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.17763.3650; amd64

```console
$ docker pull eclipse-temurin@sha256:e2fed6be654fb897a9bdfea759f60828b6d3a301cf9fd3b88affe2b4bd8bcb5f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149837385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e71141f093d882c898b8d293801842c5b79179efb2c9937b1aa72bb04caa1f9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Nov 2022 18:06:28 GMT
RUN Apply image 10.0.17763.3650
# Tue, 08 Nov 2022 18:36:25 GMT
SHELL [cmd /s /c]
# Tue, 08 Nov 2022 18:51:15 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Tue, 08 Nov 2022 18:51:16 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 08 Nov 2022 18:51:17 GMT
USER ContainerAdministrator
# Tue, 08 Nov 2022 18:51:33 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 08 Nov 2022 18:51:34 GMT
USER ContainerUser
# Tue, 08 Nov 2022 18:57:34 GMT
COPY dir:f12bd30467bc1b7f61ca05a6124e6eb838888f3685c56f372d6fed2165b193b1 in C:\openjdk-11 
# Tue, 08 Nov 2022 18:57:53 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:35ab4104a4d9df6a0d1eac84cc8fbc13511ef6c8aef5ced04fdf63e7e20803a3`  
		Last Modified: Tue, 08 Nov 2022 19:45:20 GMT  
		Size: 106.7 MB (106723592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e8f4bb4b79b67857c1e4ac5c66026fd5ff5badbde5a8b59b11251b02699586`  
		Last Modified: Tue, 08 Nov 2022 19:44:52 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e31d7a079d8015c583b6bf92d9578552be10348f6e39dfdfc7fcd3f0709288d`  
		Last Modified: Tue, 08 Nov 2022 19:48:08 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7057989690fc8ef5f9b0a864b96a374e3085973d23e6a890d4cd9dceb8868c9`  
		Last Modified: Tue, 08 Nov 2022 19:48:08 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36298ec2e53419f44640e53a23afb93709de306ebf9acb2ce5abc232a12a76e`  
		Last Modified: Tue, 08 Nov 2022 19:48:07 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c19e765a35428811d9125073672b2bd1d30252c50e959f9e177eff49496977`  
		Last Modified: Tue, 08 Nov 2022 19:48:05 GMT  
		Size: 71.2 KB (71191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22f76bb3259773dd98831017ffddef9fc9764e384de52bfc050fa7bfc098bad`  
		Last Modified: Tue, 08 Nov 2022 19:48:05 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdfbe2e5920538a3a92c03f8a8abf09887485a0e9563b3d86c1ee908634514f`  
		Last Modified: Tue, 08 Nov 2022 19:49:34 GMT  
		Size: 43.0 MB (42961323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088c6af0c59f83a60545cd04b00b279bf44963a7a9562c1b27881d283ce7fed1`  
		Last Modified: Tue, 08 Nov 2022 19:49:26 GMT  
		Size: 75.7 KB (75701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
