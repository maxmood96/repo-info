## `eclipse-temurin:17-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:181fa654823ee5d0cc3d786cc310d0694d241a7b830589787a70375114af1d85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2527; amd64
	-	windows version 10.0.17763.5936; amd64

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.20348.2527; amd64

```console
$ docker pull eclipse-temurin@sha256:a7df6a9cf61b29e2740872ed5ce9e22a5da882bca97e3744a7f4fd87ae2aea78
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.1 MB (164088875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52f92d370c079f02a4a142beaf6418ba26281907239b5c3a82b6f777b4a3785`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jun 2024 08:41:16 GMT
RUN Apply image 10.0.20348.2527
# Wed, 12 Jun 2024 18:27:44 GMT
SHELL [cmd /s /c]
# Wed, 12 Jun 2024 18:30:22 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Wed, 12 Jun 2024 18:30:22 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 12 Jun 2024 18:30:23 GMT
USER ContainerAdministrator
# Wed, 12 Jun 2024 18:30:33 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Jun 2024 18:30:33 GMT
USER ContainerUser
# Wed, 12 Jun 2024 18:31:21 GMT
COPY dir:a78f43753c24e3e0717a998b116850ca8c6149210b4cd2529d3fd312f361a7bd in C:\openjdk-17 
# Wed, 12 Jun 2024 18:31:34 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:f9825bcd6f9509654677a23b5fa1d32b32e1e32ff51914ebfaa76d5e79c22b50`  
		Last Modified: Wed, 12 Jun 2024 02:27:19 GMT  
		Size: 120.5 MB (120488969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ae17666c85b2b00f8e5aa24951a59f0b01a1eb41704faa32e1282e0f0ef217`  
		Last Modified: Wed, 12 Jun 2024 18:52:48 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379f1a30d61a338b36299534cf82fb4e3627f57850ce24f5404a5afda9eea752`  
		Last Modified: Wed, 12 Jun 2024 18:54:19 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5c4d9582b52aadd1d2bb6e492d05ba62d6cb0338b3fc03ef015824dd5ba7f1`  
		Last Modified: Wed, 12 Jun 2024 18:54:19 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93d6b8c3ba849e7f0cec95f9690a297dbb27ab15f9cf2684e52e501d8fb37f6`  
		Last Modified: Wed, 12 Jun 2024 18:54:19 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a51cf5df365f8a070fdaaae831ad485c407b3870516e0e9b243f747fb45aa62`  
		Last Modified: Wed, 12 Jun 2024 18:54:17 GMT  
		Size: 81.2 KB (81221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e39326053ebbd46753185cabac599579c906fa6f4d81c2263b8f581c46055b4`  
		Last Modified: Wed, 12 Jun 2024 18:54:17 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71d04521942ca917063bf5548bf4e32819bf4f52a4eef3d1cd7f521347a6f34`  
		Last Modified: Wed, 12 Jun 2024 18:54:54 GMT  
		Size: 43.5 MB (43454208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6772dcdcb2dea3575ac5ddeaa100c1b96d31badb766ad2e9cccc6041c32d40fa`  
		Last Modified: Wed, 12 Jun 2024 18:54:46 GMT  
		Size: 58.7 KB (58704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull eclipse-temurin@sha256:c58bfa57cad89bade4c1dbcd535c3f960f8f5bb4238ef19dfd6d954ed1d7fd19
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.5 MB (201545011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:521ba5904e51ff9b3fdde77d319e9e413e22bfd16c6469415e780fa065e03bac`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 17:41:08 GMT
SHELL [cmd /s /c]
# Wed, 12 Jun 2024 18:01:17 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Wed, 12 Jun 2024 18:01:17 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 12 Jun 2024 18:01:18 GMT
USER ContainerAdministrator
# Wed, 12 Jun 2024 18:01:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Jun 2024 18:01:27 GMT
USER ContainerUser
# Wed, 12 Jun 2024 18:06:11 GMT
COPY dir:a78f43753c24e3e0717a998b116850ca8c6149210b4cd2529d3fd312f361a7bd in C:\openjdk-17 
# Wed, 12 Jun 2024 18:06:22 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce076c01ab33a997d8fa4a6a49752f31455fef6df331991ad3b3736b3567321`  
		Last Modified: Wed, 12 Jun 2024 18:40:43 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef4283eaec67ab82eb2eaf1394d348ef4b8095aae26938603564e9753ed3dd7`  
		Last Modified: Wed, 12 Jun 2024 18:46:00 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0971dcb75451d4945808f751c16bd6b1107708957392106f500273c3cf43c75`  
		Last Modified: Wed, 12 Jun 2024 18:45:59 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3fca7aa45609ebcb6f1aa65ba03489b6c380371840a7fc5a632bcd0ac82392`  
		Last Modified: Wed, 12 Jun 2024 18:45:59 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba8307dff66a644bbf0fc5a0ff9fade24aa29f5e1cb3bffbacb7750b6cad920`  
		Last Modified: Wed, 12 Jun 2024 18:45:57 GMT  
		Size: 69.0 KB (69006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc382ff7ccb019cad431b62ae9298ebe9978a095189f90effbaad82ad26c18b`  
		Last Modified: Wed, 12 Jun 2024 18:45:57 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbeaeecd9aeecc925908dedfd5bb4f0c4a5e179bb02ac449047259aee6e438d8`  
		Last Modified: Wed, 12 Jun 2024 18:47:13 GMT  
		Size: 43.5 MB (43456477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ae742f0743fe65ede7326c0490273bbc5c490a68c3f9542671998c97b2f0b5`  
		Last Modified: Wed, 12 Jun 2024 18:47:05 GMT  
		Size: 3.0 MB (2980522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
