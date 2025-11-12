## `eclipse-temurin:21-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:73300111b8122f0456b647ffe0266c7dae53a0e09fde7ca5765d243c24bb8333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `eclipse-temurin:21-jre-nanoserver-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull eclipse-temurin@sha256:8f1ca37a0c896479701bc7e5913b09154837b0498ac17d9812bab9a8b9821b75
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247162016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009e709a21f3b5c3e78eb85c2bd0eb1811aa7b33b3d0199f0ea1cd9197b0419e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 09 Nov 2025 10:04:50 GMT
RUN Apply image 10.0.26100.7171
# Tue, 11 Nov 2025 20:11:08 GMT
SHELL [cmd /s /c]
# Tue, 11 Nov 2025 20:13:11 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Tue, 11 Nov 2025 20:13:11 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 11 Nov 2025 20:13:12 GMT
USER ContainerAdministrator
# Tue, 11 Nov 2025 20:13:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 11 Nov 2025 20:13:14 GMT
USER ContainerUser
# Tue, 11 Nov 2025 20:13:19 GMT
COPY dir:1612d20d6d454244847586ca6f13699611833617704a1c55730e9c479e5d220d in C:\openjdk-21 
# Tue, 11 Nov 2025 20:13:23 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:87c91227213eb6e7c8cfe33b6bd0429350e524756878f37f3860b013f804bf59`  
		Last Modified: Tue, 11 Nov 2025 20:41:49 GMT  
		Size: 197.9 MB (197936447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6194cd77702c569004d9457e0c06be0662b8256bcd8f00c1d770f01827ff09e`  
		Last Modified: Tue, 11 Nov 2025 20:12:01 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a01dbe9d8fe40b9e3fca9056a532e797bd4586e3117f6ad83a58e6229d60d0`  
		Last Modified: Tue, 11 Nov 2025 20:13:40 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309184c72a4a89bf9c425559ebc1ef5253234e948cf895c141fce93289956515`  
		Last Modified: Tue, 11 Nov 2025 20:13:40 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1157b2b7032c08cf41497ff2b6d988be27a1d34cbaa51992c89034778ac11cf7`  
		Last Modified: Tue, 11 Nov 2025 20:13:40 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7a3e35f49094362e9a36ee642bd419c1c202ee2d7b4a35199060a77a7396bb`  
		Last Modified: Tue, 11 Nov 2025 20:13:40 GMT  
		Size: 72.0 KB (71976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11efe35c505b80641e337f9c22158416876746226577421dedb5ad25388b108c`  
		Last Modified: Tue, 11 Nov 2025 20:13:40 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc23eacdeda43ad0c5ba214239aa05159b0a315de63d0c1b4c9f8779d8299ad2`  
		Last Modified: Tue, 11 Nov 2025 20:13:46 GMT  
		Size: 49.0 MB (49034920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376b202907a53f3636369a70f607cf40b05464ee927b58ce294674309b51b57f`  
		Last Modified: Tue, 11 Nov 2025 20:13:40 GMT  
		Size: 113.4 KB (113398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
