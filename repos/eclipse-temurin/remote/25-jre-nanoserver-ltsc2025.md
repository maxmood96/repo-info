## `eclipse-temurin:25-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:01f3358f851f94338f9914ff971f7467126817abc3e508823b5a3045a069fc3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `eclipse-temurin:25-jre-nanoserver-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull eclipse-temurin@sha256:fb3f3f6a78da17376db38055617fd6164c4e10d2023389302686caff23fa18ae
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.3 MB (252260338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d5380543bae4f6ba04f33ab09fd52a604d1e5253d83b29a710963c0eed6e1d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Sep 2025 02:12:39 GMT
RUN Apply image 10.0.26100.6584
# Thu, 25 Sep 2025 22:14:24 GMT
SHELL [cmd /s /c]
# Thu, 25 Sep 2025 22:14:26 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 22:14:26 GMT
ENV JAVA_HOME=C:\openjdk-25
# Thu, 25 Sep 2025 22:14:27 GMT
USER ContainerAdministrator
# Thu, 25 Sep 2025 22:14:37 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 25 Sep 2025 22:14:38 GMT
USER ContainerUser
# Thu, 25 Sep 2025 22:14:54 GMT
COPY dir:8aa8ce0e84e7e6f80be28438d765894541d9d2eadfccff43ebe7257923223c3b in C:\openjdk-25 
# Thu, 25 Sep 2025 22:14:58 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:a75a4ab04983f989d9a1442633d6c3952b863719a00dd77cf160f7055beaded9`  
		Last Modified: Tue, 09 Sep 2025 22:28:08 GMT  
		Size: 193.6 MB (193550846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff128ff4bb0380e5aa3fc2fcd12661a8e45f701475407f6973693543bed99c27`  
		Last Modified: Thu, 25 Sep 2025 22:15:20 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081dca6d17038ada956a58402c1d2faae969092dd562a637a071496160197889`  
		Last Modified: Thu, 25 Sep 2025 22:15:20 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d97162524754fff9bbcdc75511ae84e525d9ef9a79038355a486f9257a6e04`  
		Last Modified: Thu, 25 Sep 2025 22:15:21 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0fd5b323622afbde0912cdb6b4b5ac60f48c0664609f8bf2ffa165de506c115`  
		Last Modified: Thu, 25 Sep 2025 22:15:20 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f176133c0fb6ee7c7d6a7269cd0562f9fadef851908d6003bcc80ed88f0c189`  
		Last Modified: Thu, 25 Sep 2025 22:15:20 GMT  
		Size: 70.5 KB (70474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d320f474c7b0abdc42565a2693182598d93d854f1ea557fa60ffb00f3580bcb3`  
		Last Modified: Thu, 25 Sep 2025 22:15:20 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbde4cebb4d84bf05961ad1cdd45421a54b94fcee4eb26da4ecfb494a0d0de4e`  
		Last Modified: Thu, 25 Sep 2025 22:15:26 GMT  
		Size: 58.6 MB (58550762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc077796fd51500e1b9988b87178d16e96d90bae7cf1097ea506f88994f1f84`  
		Last Modified: Thu, 25 Sep 2025 22:15:20 GMT  
		Size: 82.9 KB (82891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
