## `eclipse-temurin:17-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:8ff3c8834422ef4758dc7c7dbb849ff692202ca51a7dc9f7c2c512cb01dedb0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2527; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2527; amd64

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
