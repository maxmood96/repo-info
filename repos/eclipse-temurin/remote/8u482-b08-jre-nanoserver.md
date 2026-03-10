## `eclipse-temurin:8u482-b08-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:ec486f6f32c4c693926c20a59ad656baa887d4978b57ad706f215d9ecf5af301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `eclipse-temurin:8u482-b08-jre-nanoserver` - windows version 10.0.26100.32522; amd64

```console
$ docker pull eclipse-temurin@sha256:526dbfe3aad112801d474a01cc0a179637163bcf31e7541ed4cef21ca142d092
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.5 MB (239541783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c30b8c7d9e78fce4a4ff89aa5bd0b59a1ad223922669c1d4dd3a31ed94292a0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Mar 2026 01:45:55 GMT
RUN Apply image 10.0.26100.32522
# Tue, 10 Mar 2026 22:42:57 GMT
SHELL [cmd /s /c]
# Tue, 10 Mar 2026 22:42:58 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 10 Mar 2026 22:42:59 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 10 Mar 2026 22:42:59 GMT
USER ContainerAdministrator
# Tue, 10 Mar 2026 22:43:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Mar 2026 22:43:04 GMT
USER ContainerUser
# Tue, 10 Mar 2026 22:43:10 GMT
COPY dir:e192ec1627bb02acae941746a6647cea6857b84f7daa4f746913822a0bac9dcc in C:\openjdk-8 
# Tue, 10 Mar 2026 22:43:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:06fab7822816d5f43d6835d07ac8db280fdf81384187f36d8dc43bbb7064a76d`  
		Last Modified: Tue, 10 Mar 2026 20:41:46 GMT  
		Size: 199.4 MB (199409325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982f6bcd510ac3d867816ccc93a3285f373275b9c91df694985b091ce189a66b`  
		Last Modified: Tue, 10 Mar 2026 22:43:18 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c51e5c79ba90603b1e4ac729bf2671990420bb737fa00a23f57052d2ae6760c`  
		Last Modified: Tue, 10 Mar 2026 22:43:18 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03ba2bcc6a24e51b7a322d198dea744e3287ae16fb825b5750733f8cff71da2`  
		Last Modified: Tue, 10 Mar 2026 22:43:18 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dead7438daf7ba3d9aa881827833db71731d1ac4ac15a1b6294bc703f7ff49b2`  
		Last Modified: Tue, 10 Mar 2026 22:43:16 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e384b79d32873328a227206543c4298bf9103ce8e7cf17405b284d8e753438`  
		Last Modified: Tue, 10 Mar 2026 22:43:16 GMT  
		Size: 77.6 KB (77567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34871689e9a61b776e28e85a52426fe72779df3b6206f9ca3163b8ab9a05e44e`  
		Last Modified: Tue, 10 Mar 2026 22:43:16 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0045ee81f835dd6b86f094c7e7afd6bb1961f6e425827933ffe6e288e01dd75`  
		Last Modified: Tue, 10 Mar 2026 22:43:20 GMT  
		Size: 40.0 MB (39969860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f87aa06f05f77f514de81001d709035999fab1286f33b21f4c6a70ea673ea8a`  
		Last Modified: Tue, 10 Mar 2026 22:43:16 GMT  
		Size: 79.7 KB (79683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u482-b08-jre-nanoserver` - windows version 10.0.20348.4893; amd64

```console
$ docker pull eclipse-temurin@sha256:28a45b77845361ea7f13d0df7218e2e93334a64a94dc2677cf989d734806fff1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166792069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e8160ddd2a4deb7d4c4b5eeea7add6ba45c551893ee7be101efb796084035f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 10 Mar 2026 22:36:11 GMT
SHELL [cmd /s /c]
# Tue, 10 Mar 2026 22:36:11 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 10 Mar 2026 22:36:11 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 10 Mar 2026 22:36:12 GMT
USER ContainerAdministrator
# Tue, 10 Mar 2026 22:36:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Mar 2026 22:36:15 GMT
USER ContainerUser
# Tue, 10 Mar 2026 22:36:19 GMT
COPY dir:e192ec1627bb02acae941746a6647cea6857b84f7daa4f746913822a0bac9dcc in C:\openjdk-8 
# Tue, 10 Mar 2026 22:36:21 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62fed3face2429e33d46c7bd16d631ccc57a3988e4f3168d9273ff5de0c9322`  
		Last Modified: Tue, 10 Mar 2026 22:36:27 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4fd65e0469201dadc3edff28384911d4def88318dc23e644b851042be30fc2`  
		Last Modified: Tue, 10 Mar 2026 22:36:27 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e059762a06d6a119ce1b465d7cea3042db7179af40d204a90b42006a393a984`  
		Last Modified: Tue, 10 Mar 2026 22:36:27 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b17203df2ee9bca3f6ee15fd7c51aa59633ab570871c467e65eb5becdace1d`  
		Last Modified: Tue, 10 Mar 2026 22:36:25 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b16b0ff42435282c5afa5b997f0637a4ffe68483ec9318c927fc3a891398b40`  
		Last Modified: Tue, 10 Mar 2026 22:36:25 GMT  
		Size: 75.6 KB (75613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcda8f8c9a37b57802a80ebc4d06357e5f00ef131a42a2c097f7934901125d6e`  
		Last Modified: Tue, 10 Mar 2026 22:36:25 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932da3ec230955558fdf6c187ef216cffc580f4931b955e22c4ccc3d962d4a48`  
		Last Modified: Tue, 10 Mar 2026 22:36:30 GMT  
		Size: 40.0 MB (39969724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6ca16d499e0bb29fc86ca2518b24b70146c5b0fc0a50748be7507f9a11da49`  
		Last Modified: Tue, 10 Mar 2026 22:36:26 GMT  
		Size: 90.9 KB (90920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
