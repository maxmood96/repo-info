## `eclipse-temurin:8-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:aff04d0cdf3b5e82786ce75c3a26a119ef0e5d4c4a6f0aad637895622ea2e033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `eclipse-temurin:8-jre-nanoserver-1809` - windows version 10.0.17763.3165; amd64

```console
$ docker pull eclipse-temurin@sha256:0ec0386ef3767220e91a525c5f9b8f911bd5d337d7d85dfa28c399ffeff09823
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142628208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2249da4cdcbcd954b16b6c6011bab70e172050fc79fc6c843758e972242902`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 06 Jul 2022 22:15:10 GMT
RUN Apply image 10.0.17763.3165
# Wed, 13 Jul 2022 14:50:41 GMT
SHELL [cmd /s /c]
# Tue, 02 Aug 2022 18:20:58 GMT
ENV JAVA_VERSION=jdk8u342-b07.1
# Tue, 02 Aug 2022 18:20:58 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 02 Aug 2022 18:20:59 GMT
USER ContainerAdministrator
# Tue, 02 Aug 2022 18:21:10 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 02 Aug 2022 18:21:11 GMT
USER ContainerUser
# Tue, 02 Aug 2022 18:25:28 GMT
COPY dir:9db60ee3ad3f16cf75b351ecd1309f1d56f486fa1a4d388cea2f63f8b51258b8 in C:\openjdk-8 
# Tue, 02 Aug 2022 18:25:41 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:5d24e1a2f5c566b0afb1e46fc24e5cec821c8ebf44220276a95a2b91f44a2f2a`  
		Size: 103.2 MB (103155009 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3b09c07c6aeead64423fdefc240fe2e1b6330c96732fd2705113030da84416be`  
		Last Modified: Mon, 18 Jul 2022 21:22:33 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afb618c90b77419f2ba1f5cc9462e79727701df91db5fdad3b5471d61e915ab`  
		Last Modified: Tue, 02 Aug 2022 18:42:47 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b2c1dc8371357afa7f2bffb8953ce48eb6ce7fb4d9dff32cf29f491555f4c5`  
		Last Modified: Tue, 02 Aug 2022 18:42:47 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc03726463a40a0e346109623370ceedc85a9fdc7f3af42480b612bde6fdc87`  
		Last Modified: Tue, 02 Aug 2022 18:42:45 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8884b11b9d50972244fc935a95dfa3e795447d8ef888a4ab21bcefc91d35134`  
		Last Modified: Tue, 02 Aug 2022 18:42:45 GMT  
		Size: 68.1 KB (68138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1922d55220d13d511321a93f55ca92f4b464d239af9b51f68056e8b014474a16`  
		Last Modified: Tue, 02 Aug 2022 18:42:45 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0912a174be34e9eedfe0361872e60621558b4e0e9c3dfdc65a3a098f3dae4c`  
		Last Modified: Tue, 02 Aug 2022 18:43:51 GMT  
		Size: 39.3 MB (39318093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8d908c11a9c782281224ec43254ed107873b8d2205d5c03623eab3cee86755`  
		Last Modified: Tue, 02 Aug 2022 18:43:45 GMT  
		Size: 81.3 KB (81281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
