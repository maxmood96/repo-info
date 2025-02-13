## `eclipse-temurin:8-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:d602ea58698c4ff6fd23f46c102e52a0c34f7010350cf6d6366058cd7e88816c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `eclipse-temurin:8-jre-nanoserver-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull eclipse-temurin@sha256:76268eeef1d01ea11e5880e5afa34614aa6591e4330fa246f527413b1fc4f974
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147666937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e2646b77ae9801e2f08c74b879e1a27acce9efdbfb43c6648a891e691cc76d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:16:09 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:16:10 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 13 Feb 2025 01:16:11 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 13 Feb 2025 01:16:11 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:16:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Feb 2025 01:16:14 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:16:16 GMT
COPY dir:5687adced9ba5f2555526fe07fa3e848c7771941703db13fa4b29a0f81d58070 in C:\openjdk-8 
# Thu, 13 Feb 2025 01:16:19 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Wed, 12 Feb 2025 21:38:54 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6f21906c13536ac52a4e444ca1564bd9b24c89aea9d9365bf250496965acd4`  
		Last Modified: Thu, 13 Feb 2025 04:17:42 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26dd6cea81edf388c4c196f574c03fcbd30a08b54b4c164ce759f8e2ddb0654`  
		Last Modified: Thu, 13 Feb 2025 04:17:42 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209b95b49fb9a13664ca64d75cdd44c463e9385c3f0eec096c626bca01b000f5`  
		Last Modified: Thu, 13 Feb 2025 04:17:42 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb9247e29e3c3c135077ea418c67149ec791baa28c630ba77bd79265c641641`  
		Last Modified: Thu, 13 Feb 2025 04:17:42 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03b34f98a0d7bcc6dc472b522b7742e742198b3311b4eed06b461c9e5a73cee`  
		Last Modified: Thu, 13 Feb 2025 04:17:42 GMT  
		Size: 83.6 KB (83631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8704f2e956529882a556a4e33e026bdccb7f78437550e99522f11ce470b8c7b2`  
		Last Modified: Thu, 13 Feb 2025 04:17:43 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5c06d39ba5b395f5e6ed3cac9ddd3c22f7c539bf0b825678e86d1574638223`  
		Last Modified: Thu, 13 Feb 2025 04:17:45 GMT  
		Size: 40.6 MB (40552128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53dd063e1841b5a0fdbd64a02fea99c82dedee9de8d246e7faf66916d5fbdade`  
		Last Modified: Thu, 13 Feb 2025 04:17:43 GMT  
		Size: 110.5 KB (110517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
