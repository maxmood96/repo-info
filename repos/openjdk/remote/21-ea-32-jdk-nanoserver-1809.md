## `openjdk:21-ea-32-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:ae55eb79a855ccd421fa96f467a03df68dab54b4847db194dc5194ff09ded2ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `openjdk:21-ea-32-jdk-nanoserver-1809` - windows version 10.0.17763.4645; amd64

```console
$ docker pull openjdk@sha256:484aecb2459cc7f973d0b836dc9d2235f3d3e59347560cd7988ff5a37ad8dcec
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.3 MB (306343003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e14b3cdf84f487fa83de3a87bc7e2907f4cb9544ba5a6a4b23c10a4fd8126fb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jul 2023 07:42:59 GMT
RUN Apply image 10.0.17763.4645
# Thu, 13 Jul 2023 21:36:32 GMT
SHELL [cmd /s /c]
# Fri, 14 Jul 2023 00:19:53 GMT
ENV JAVA_HOME=C:\openjdk-21
# Fri, 14 Jul 2023 00:19:53 GMT
USER ContainerAdministrator
# Fri, 14 Jul 2023 00:20:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 14 Jul 2023 00:20:02 GMT
USER ContainerUser
# Thu, 20 Jul 2023 20:40:57 GMT
ENV JAVA_VERSION=21-ea+32
# Thu, 20 Jul 2023 20:41:11 GMT
COPY dir:f71c4b7717208adb78386436674e3f3303b0e9f5d07c3b7cfde68c6b3b03c0b1 in C:\openjdk-21 
# Thu, 20 Jul 2023 20:41:25 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 20 Jul 2023 20:41:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5c5b06ba65934bcf850a1a54ecf4b3da34d3e6d6c8e90dbc897719c3ea377c8a`  
		Last Modified: Tue, 11 Jul 2023 17:31:37 GMT  
		Size: 104.4 MB (104408241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13c473988daf5951866dd9b290bd6417227c1d7df6e811cfe11438d033a1eba`  
		Last Modified: Thu, 13 Jul 2023 22:19:06 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289ea5fc8a7f31b38120d64f4fc304a5e09ac629f99bc9b5e92a4349bcf143bf`  
		Last Modified: Fri, 14 Jul 2023 00:25:00 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66b7bdcadf86bdda397cf414ae45f974a40e697d5002156e00e7cd59e946cbc`  
		Last Modified: Fri, 14 Jul 2023 00:25:00 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d929e2c9bf4cff0381fd000609dc5a373e8d51ceaca78fe43f609176c7d62d78`  
		Last Modified: Fri, 14 Jul 2023 00:25:00 GMT  
		Size: 67.7 KB (67668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ab158d7279412c8630521a444777102ad52479439f793e296ac44ef396e701`  
		Last Modified: Fri, 14 Jul 2023 00:24:58 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7788845ad382e0b646610bdf35db28a18566e8352c573d495fb7fe3f26dd54e`  
		Last Modified: Thu, 20 Jul 2023 20:45:49 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d4915d0cdb62298153c06587cad27ece8a07085420c0d000c8fec9f78c60ab`  
		Last Modified: Thu, 20 Jul 2023 20:46:09 GMT  
		Size: 198.0 MB (198036432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cda996b3791e08c3cdbdcca3c4debd2a6cb872715b1d7ab3fe9ffdfa4d73085`  
		Last Modified: Thu, 20 Jul 2023 20:45:50 GMT  
		Size: 3.8 MB (3823723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb954500fb63c8a3d6638f821c9a90d667bd1b0bdba0e6580d7094748c218fd`  
		Last Modified: Thu, 20 Jul 2023 20:45:49 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
