## `eclipse-temurin:21-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:ff6f386a38362ee9c66e2ba5ffe11b3935248c8bc54f23eea0ea9ed9c5fd19e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `eclipse-temurin:21-jdk-nanoserver-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull eclipse-temurin@sha256:0e6acbb324e80d6e6c4ffb469ff579e0cc0d0d68a4b5d170b45a3432ed96e9ee
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.4 MB (309393720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03be500870dea4c16b6de8b84ad629fe3f655a16fd14a0522e409778386927c4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Nov 2023 17:21:05 GMT
RUN Apply image 10.0.17763.5122
# Thu, 16 Nov 2023 01:41:12 GMT
SHELL [cmd /s /c]
# Thu, 16 Nov 2023 02:11:58 GMT
ENV JAVA_VERSION=jdk-21.0.1+12
# Thu, 16 Nov 2023 02:11:59 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 16 Nov 2023 02:12:00 GMT
USER ContainerAdministrator
# Thu, 16 Nov 2023 02:12:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 16 Nov 2023 02:12:10 GMT
USER ContainerUser
# Thu, 16 Nov 2023 02:12:25 GMT
COPY dir:fd62014fea6b5cd8b6f3d34ff8f9c5e95aa0ce969b7fd9201e979e77a3abe050 in C:\openjdk-21 
# Thu, 16 Nov 2023 02:12:39 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 16 Nov 2023 02:12:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:24e10ec0ecb89022cf68752b9f9196dcf2f423f9589b14401693fb2a1b3de37f`  
		Last Modified: Tue, 14 Nov 2023 22:06:25 GMT  
		Size: 104.5 MB (104497517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e5c133738aab79d4c21c47e77cb838e2d00166f5e3e2632177622f67488259`  
		Last Modified: Thu, 16 Nov 2023 02:28:08 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1f93705bc66be9e7bd16a63fb2083eaa966ce68e0a041581f4f2c060669b56`  
		Last Modified: Thu, 16 Nov 2023 02:36:16 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19000c594d11a61850151597a4e96bbf27d59ccd9ac158dcbdd52a9a2f7d7507`  
		Last Modified: Thu, 16 Nov 2023 02:36:16 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e3e3a6ccfa0ad291175e9aa8d7b56661c012730cf40821b17a9c24cd81f4ff`  
		Last Modified: Thu, 16 Nov 2023 02:36:17 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea0fa6e5a93366f9ab44f64ea7cb59f6dfba280202e7a1d9d7312959b5be750`  
		Last Modified: Thu, 16 Nov 2023 02:36:15 GMT  
		Size: 71.4 KB (71408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552a786118de89d9b566cf983c928ff2585c7ef7e8a8fa768aae003aa10f563e`  
		Last Modified: Thu, 16 Nov 2023 02:36:14 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9251d7aadd9f315ef6e9afce35f042dcbdce42465dbb1977c3278e7823153f`  
		Last Modified: Thu, 16 Nov 2023 02:36:35 GMT  
		Size: 201.0 MB (200994805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5023026dfcbabc3ef372028e1206d1ebc3d6dc8a6f024bb71179e771239468b`  
		Last Modified: Thu, 16 Nov 2023 02:36:16 GMT  
		Size: 3.8 MB (3823201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efeffc490da1921d44ea5283f9e6610cea97b30ccfb92436da75998a73a9d142`  
		Last Modified: Thu, 16 Nov 2023 02:36:14 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
