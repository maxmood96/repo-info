## `eclipse-temurin:25-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:7de3e6ffde4ca60e66d41b0aeab0c6e07f220d0ce58fd688615a4ac3c4c80969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `eclipse-temurin:25-jre-nanoserver` - windows version 10.0.26100.6584; amd64

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

### `eclipse-temurin:25-jre-nanoserver` - windows version 10.0.20348.4171; amd64

```console
$ docker pull eclipse-temurin@sha256:526485b19b136857b54ee12c07b040829d0b9f8f21534a5068ec009a024c1e6e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181472466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35839ffaaf1b7c8f246c994c145c691d059b022e8cbb116b0124af962b8f1591`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Thu, 25 Sep 2025 22:12:47 GMT
SHELL [cmd /s /c]
# Thu, 25 Sep 2025 22:12:48 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 22:12:49 GMT
ENV JAVA_HOME=C:\openjdk-25
# Thu, 25 Sep 2025 22:12:49 GMT
USER ContainerAdministrator
# Thu, 25 Sep 2025 22:12:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 25 Sep 2025 22:12:58 GMT
USER ContainerUser
# Thu, 25 Sep 2025 22:14:55 GMT
COPY dir:8aa8ce0e84e7e6f80be28438d765894541d9d2eadfccff43ebe7257923223c3b in C:\openjdk-25 
# Thu, 25 Sep 2025 22:15:00 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc44f684fa662a44ac5b5fdb2c6bf679052cd2d8ffbbd0649e5c186ad49ac5f5`  
		Last Modified: Thu, 25 Sep 2025 22:14:16 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c71fbba26ccdbd7a60d6ef3a48c82fbefbee275341b6784a2076f9bc61b955`  
		Last Modified: Thu, 25 Sep 2025 22:14:16 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdb1175fae153d8d5bd8ef1d8927b294bf8b3db598b2c37949a160f75b4ad6c`  
		Last Modified: Thu, 25 Sep 2025 22:14:16 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26916416afde07316880254c82e0a6ba3832ed32743e01d44435dd14d47e025a`  
		Last Modified: Thu, 25 Sep 2025 22:14:16 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db585771e906d79dcc800547cc747763294d71921f77e1df13f53ef3c4172fe8`  
		Last Modified: Thu, 25 Sep 2025 22:14:16 GMT  
		Size: 83.9 KB (83932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317ef0bf3caeb82f3ca2dd89ed5f2c21b6473555cb9a3a753888167c899fdc7c`  
		Last Modified: Thu, 25 Sep 2025 22:14:16 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe5b55f211e15e492d202216cf2c40b3e450df2a456e1131316cbde3962f15b`  
		Last Modified: Thu, 25 Sep 2025 22:15:24 GMT  
		Size: 58.6 MB (58551017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126c6ac628de928cce8c51600bbef9ffae5931e6af7c46320cc0f332e9d82036`  
		Last Modified: Thu, 25 Sep 2025 22:15:19 GMT  
		Size: 112.3 KB (112284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
