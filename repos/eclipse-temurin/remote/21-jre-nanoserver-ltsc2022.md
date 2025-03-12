## `eclipse-temurin:21-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:3b09e71fd2c8888a39b327d1975e9a4949096a4c2a08d948dedf689b33b630c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `eclipse-temurin:21-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull eclipse-temurin@sha256:329740d2b1e4007437125ce77eaf14611ca73574eaa22ec43747e132acf4ff16
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.8 MB (169814940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e821507d713b2ef591a877f26a036343d9a364b57e7bd3bcb2f11a48523d0703`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Wed, 12 Mar 2025 19:15:14 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:15:15 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Wed, 12 Mar 2025 19:15:15 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 12 Mar 2025 19:15:16 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:15:19 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:15:19 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:15:23 GMT
COPY dir:c0b7c132c85049081486a93cd76fe016c559b0b921796f63592a768b082ae9e2 in C:\openjdk-21 
# Wed, 12 Mar 2025 19:15:28 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329ad47753b94e85fcf58c2a6c3e12aa4ccb2f1e1a5c8fe94952900196a98aab`  
		Last Modified: Wed, 12 Mar 2025 19:15:33 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47747f3460d912190ac7dd143f610211b1b2cdeafde82820d3230c1c0a81473`  
		Last Modified: Wed, 12 Mar 2025 19:15:33 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7df28049186c13916aa4a1bc86deb9236b654fefa3e01a380f115efb09a97be`  
		Last Modified: Wed, 12 Mar 2025 19:15:33 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8611e5eb5ccfc5a11c01ea750fcf1be18941906621fd0fa7557fa85333a6e504`  
		Last Modified: Wed, 12 Mar 2025 19:15:32 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f315a4ff327548bb71de061ca5ffb98bdaabf0cb805fb7951cbe25f2779b3658`  
		Last Modified: Wed, 12 Mar 2025 19:15:32 GMT  
		Size: 76.6 KB (76566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf279050847e7fe0da3c9a722c0c8761a8a5fe9b143df5b5d8d3d8993637604`  
		Last Modified: Wed, 12 Mar 2025 19:15:31 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aca050587b075e498e45cefc757b26ccb49cdd86bc78e179e23c9f9dcbb3844`  
		Last Modified: Wed, 12 Mar 2025 19:15:37 GMT  
		Size: 48.9 MB (48940863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d8567f37242b6f08e32d90b9bcecbd65bb01648cd7fb19f1e39fc442abb6b6`  
		Last Modified: Wed, 12 Mar 2025 19:15:32 GMT  
		Size: 96.8 KB (96824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
