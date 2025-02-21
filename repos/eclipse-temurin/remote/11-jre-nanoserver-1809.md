## `eclipse-temurin:11-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:a05f2950db44f02e770e770a1d8e6d01f60c14a18797748df8eaebd2cd169ebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `eclipse-temurin:11-jre-nanoserver-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull eclipse-temurin@sha256:c39ef3f488dd0e117b4d0f748d2adaead58aa71c6954adc657496beaabeb5d3b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.8 MB (150755012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308fc37e08e57c0ccd423b78f877038df0ba1da028f99adae39be6fc3abeb35c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:17:51 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:17:54 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 13 Feb 2025 01:17:54 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 13 Feb 2025 01:17:55 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:17:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Feb 2025 01:17:58 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:18:02 GMT
COPY dir:e7319a06d2b9171c954fc18de0614fa7d0eb408950b795be61492806db04a6ea in C:\openjdk-11 
# Thu, 13 Feb 2025 01:18:06 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095d2f8fedfb5490450bbd42c650ea5d879829b73d6f5ab128cb6b99cf7a1b1b`  
		Last Modified: Thu, 13 Feb 2025 01:18:10 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c324be8909439bb20e59510dcc1cfd6828b947742dc3f8cb5b9b0f8d0e7dfec6`  
		Last Modified: Thu, 13 Feb 2025 01:18:10 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba4fba56537ab4cead3ed14efb6626b92d834b17f25657611498eec9cbb1be9`  
		Last Modified: Thu, 13 Feb 2025 01:18:10 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2843275d9d9882ba668243c2482f8db3d51e7b1dde603ab7350605419a97d70`  
		Last Modified: Thu, 13 Feb 2025 01:18:09 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfea8d0be4f0432ad954c2318dfd13da35c0dbd442686eae5cbbe5c63c761057`  
		Last Modified: Thu, 13 Feb 2025 01:18:09 GMT  
		Size: 80.3 KB (80344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5fd1c113e43733acb1b85aac9f5b64a03a287d2d535f5c2ea37f7b642377258`  
		Last Modified: Thu, 13 Feb 2025 01:18:09 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b05bc421a8d6f292f7a0ba0b7fcf939e3a57ef074aaabec401f79f43225008`  
		Last Modified: Thu, 13 Feb 2025 01:18:14 GMT  
		Size: 43.7 MB (43656310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f496ad1d58b8222a977e8b349349a563ed33dd74d28f6853355fa9f02fd84f3`  
		Last Modified: Thu, 13 Feb 2025 01:18:09 GMT  
		Size: 97.5 KB (97493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
