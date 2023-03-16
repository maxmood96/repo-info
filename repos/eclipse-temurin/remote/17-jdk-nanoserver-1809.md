## `eclipse-temurin:17-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:337c8ed4e15d9231fffe6db6077057bd544b5f8998ce97d16b40d825f8036f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4131; amd64

### `eclipse-temurin:17-jdk-nanoserver-1809` - windows version 10.0.17763.4131; amd64

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
