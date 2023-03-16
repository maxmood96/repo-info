## `eclipse-temurin:17-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:d7038dad0ab19d4eb1e7c975da789789f66598d9246a059a405aa2c6404b752d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1607; amd64
	-	windows version 10.0.17763.4131; amd64

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.20348.1607; amd64

```console
$ docker pull eclipse-temurin@sha256:8b0c865b101e7d3d186e57661c242b506b775c612911d82110b76370c06c595a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.8 MB (307811017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f58a1f2ca42fff69f296b1be5faee029210e6d26f16c90a3e17adb2e25276c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 10 Mar 2023 06:31:34 GMT
RUN Apply image 10.0.20348.1607
# Thu, 16 Mar 2023 01:29:33 GMT
SHELL [cmd /s /c]
# Thu, 16 Mar 2023 01:33:25 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 01:33:26 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 16 Mar 2023 01:33:27 GMT
USER ContainerAdministrator
# Thu, 16 Mar 2023 01:33:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 16 Mar 2023 01:33:39 GMT
USER ContainerUser
# Thu, 16 Mar 2023 01:33:55 GMT
COPY dir:b9d1887161cde3cc24ae2101d8a284bfc20814b15fed427bc1c905c1248fb0bf in C:\openjdk-17 
# Thu, 16 Mar 2023 01:34:36 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 01:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7abf0a70d48bf65f3d985f5780d4bdaece36f1f4bb8be10d5a6aacce33dacc75`  
		Last Modified: Thu, 16 Mar 2023 01:54:24 GMT  
		Size: 122.2 MB (122171731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a611a20686e9374e3a55a49399506f83c041ae711ed47018c2267c341156dd97`  
		Last Modified: Thu, 16 Mar 2023 01:53:50 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9653c7841fe2911686bb05797100e5d3aac112a6c5a31fd109fdf273c3c7d81`  
		Last Modified: Thu, 16 Mar 2023 01:55:45 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d961af1d066326c8e1186fbc6876a3d4dbe91d3d6872218505bec61dd725a21f`  
		Last Modified: Thu, 16 Mar 2023 01:55:45 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69ba0af288067e9cca1f23c1de2ead5658b53ed2546ea3de73c6f4e1b897504`  
		Last Modified: Thu, 16 Mar 2023 01:55:45 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1548f7ad98467d9f81b01049dc8293c2e89075b47855b6bbd4ec968122d401d`  
		Last Modified: Thu, 16 Mar 2023 01:55:43 GMT  
		Size: 80.0 KB (80016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24269970d76158337295eb022f62b2023eea8965be236222ea57b4f5ccbc6159`  
		Last Modified: Thu, 16 Mar 2023 01:55:43 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d466b70892a902e66a98a465c889f98691e262c776119b05363bd767add03f`  
		Last Modified: Thu, 16 Mar 2023 01:56:04 GMT  
		Size: 185.5 MB (185456425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf93481ed42c92b3232cb483e92ffb080186c7df5c9a5dd16e7be0f45048b5e8`  
		Last Modified: Thu, 16 Mar 2023 01:55:43 GMT  
		Size: 95.9 KB (95853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:386de6621e693368b294048039e6bb8935f07150c98cf844c4afb1f03a782af4`  
		Last Modified: Thu, 16 Mar 2023 01:55:43 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.17763.4131; amd64

```console
$ docker pull eclipse-temurin@sha256:bd1d7127a5d7eb8a5618ee034eb0489ea6513c05243414bee175fd09d8501736
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295914060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5103f308f4c041d356234f85a0477e81d12b8b0ce7de0705944cc693015f07ab`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 11 Mar 2023 10:09:02 GMT
RUN Apply image 10.0.17763.4131
# Thu, 16 Mar 2023 00:45:50 GMT
SHELL [cmd /s /c]
# Thu, 16 Mar 2023 01:10:40 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 01:10:41 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 16 Mar 2023 01:10:42 GMT
USER ContainerAdministrator
# Thu, 16 Mar 2023 01:10:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 16 Mar 2023 01:10:54 GMT
USER ContainerUser
# Thu, 16 Mar 2023 01:11:10 GMT
COPY dir:b9d1887161cde3cc24ae2101d8a284bfc20814b15fed427bc1c905c1248fb0bf in C:\openjdk-17 
# Thu, 16 Mar 2023 01:11:35 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 01:11:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:95eb2f0f3287f5ec687287cc244924aafc74c7ada3121d43f54223487f3f2d8d`  
		Last Modified: Thu, 16 Mar 2023 01:43:14 GMT  
		Size: 106.7 MB (106684240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5837fe68a36caddf38b0aaa99f4ef20ca36d8dfe2825fa6ffbcf0d38b9d59a`  
		Last Modified: Thu, 16 Mar 2023 01:42:43 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cef6b623b0498bbc748423c89b5ead7b9c77269a3ff759cdbeb3067625df172`  
		Last Modified: Thu, 16 Mar 2023 01:49:08 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4c24f4b371e2c05b725b983ca3515f3a9e357c1be997893795a766ef67f631`  
		Last Modified: Thu, 16 Mar 2023 01:49:07 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d088c9439a9a0516cb592c4a77f5cc4e3a76015e3ea92d78de5a491305b667`  
		Last Modified: Thu, 16 Mar 2023 01:49:07 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1acbd9403c07bd275e88a3a4f87c12423f8e635b4be1bb490e565397fe2d64de`  
		Last Modified: Thu, 16 Mar 2023 01:49:05 GMT  
		Size: 71.6 KB (71593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a3b89d22970421cb0ce96cf04bef4d162f237ff90934963e4f6d0df4049d78`  
		Last Modified: Thu, 16 Mar 2023 01:49:05 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c8ed9747970f920a489c1cdefa1b13bf0294822b9f4134dd63c478c8b9840a4`  
		Last Modified: Thu, 16 Mar 2023 01:49:28 GMT  
		Size: 185.5 MB (185475121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042c22019df4ea8a01606c23f3a5e75799cb8abc12fe28acd04a57bc2f73164c`  
		Last Modified: Thu, 16 Mar 2023 01:49:06 GMT  
		Size: 3.7 MB (3676088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675b9067d38d9eda39daa5aad4f06a9eac7e036824d09d7b9b5acd430b6d1d5d`  
		Last Modified: Thu, 16 Mar 2023 01:49:05 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
