## `openjdk:24-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:0dce6f2879b138ec74beb45293d6e0722e31957f1471cc6efa9ed9b8ba6aa485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `openjdk:24-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull openjdk@sha256:3ac45f4492fb0646ad155708560578a6bb549924e47e69db908c183c9520e48d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.0 MB (415024990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3578199173b5b43d3150cb9e810929178a264aa3a8e4dd565aeabb88329c5d4c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Wed, 12 Mar 2025 20:16:27 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 20:16:27 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 12 Mar 2025 20:16:28 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 20:16:31 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 12 Mar 2025 20:16:32 GMT
USER ContainerUser
# Wed, 12 Mar 2025 20:16:33 GMT
ENV JAVA_VERSION=24
# Wed, 12 Mar 2025 20:16:40 GMT
COPY dir:cf5ecdf170ed29d5224593d2b3a510464d2e7297517065c397a2229de8b2a139 in C:\openjdk-24 
# Wed, 12 Mar 2025 20:16:47 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 12 Mar 2025 20:16:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cc6622170242b97dec857f04ec214c2eac82ba5cf9e0dc3bd06e085bdbfe86`  
		Last Modified: Wed, 12 Mar 2025 20:16:54 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbcadbb15be9f8a0826327ed9d3f56a5c8f0dccaeab2a8a7142288ad717a869`  
		Last Modified: Wed, 12 Mar 2025 20:16:54 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a240907a0a0e4138336cee02bdb24df221e01561ef76cf594c581c16c7929aca`  
		Last Modified: Wed, 12 Mar 2025 20:16:54 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e536b3da1cacb478c1023a8a9694b308b130b7e74c12db98b67adc336dea6e`  
		Last Modified: Wed, 12 Mar 2025 20:16:54 GMT  
		Size: 76.0 KB (76001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10449b92c264842fdfd8f0b3cf1f43bcd42be6a7acf016a2afd6e7c4f7ec263b`  
		Last Modified: Wed, 12 Mar 2025 20:16:52 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37f863d986ff7053004a96ef0d1fb0418f865377a19b2d6e1097c271045ffa6`  
		Last Modified: Wed, 12 Mar 2025 20:16:52 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da13f25d9b62b08dc3de933d68b6700a2bc44bf5a47bac1a1bd6fe2c8fe94455`  
		Last Modified: Wed, 12 Mar 2025 20:17:03 GMT  
		Size: 208.5 MB (208526023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367130c979c4c8cefff1131124589a33b26cc0b785e65d97a0d07a0bceb82030`  
		Last Modified: Wed, 12 Mar 2025 20:16:52 GMT  
		Size: 114.3 KB (114322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30428d0fa016312a7681999e9f8811fa4353d048b9e1e8f1fa6ad278da2ddfe`  
		Last Modified: Wed, 12 Mar 2025 20:16:52 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
