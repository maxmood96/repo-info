## `eclipse-temurin:21-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:fd3756f96a8358185febe6179dd15ab39bb8a5436a9c7616e0eaaa2046220faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `eclipse-temurin:21-jre-nanoserver-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:823cb728a5e3769adf7d5c42d4e52c08fb6652c1befc333e730fdc1141e61911
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.2 MB (248168183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ad74a8014e86720f2033c8e2cd20dca578ea8c2c9ebd57df5d33723c042e85`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Fri, 31 Jan 2025 02:17:10 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 02:17:11 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Fri, 31 Jan 2025 02:17:11 GMT
ENV JAVA_HOME=C:\openjdk-21
# Fri, 31 Jan 2025 02:17:13 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 02:17:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 02:17:16 GMT
USER ContainerUser
# Fri, 31 Jan 2025 02:17:19 GMT
COPY dir:c0b7c132c85049081486a93cd76fe016c559b0b921796f63592a768b082ae9e2 in C:\openjdk-21 
# Fri, 31 Jan 2025 02:17:23 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd3eea7c8ff8fae31177beefda7f4f0b7d9e147f12ecd8a19a9fc588162b05a`  
		Last Modified: Fri, 31 Jan 2025 02:17:27 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:405a62ad199d0e74154a166c2880158804607ad87809ec4c39521fa8fac2965e`  
		Last Modified: Fri, 31 Jan 2025 02:17:26 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464b89b3ea99e3b293630b002ef978405d9f11067fa84799f529b17fb79893da`  
		Last Modified: Fri, 31 Jan 2025 02:17:26 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c77d4a33509d271e90bf9e726928529124b3ef2ff76158abd3e737416a4433`  
		Last Modified: Fri, 31 Jan 2025 02:17:26 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47e9eb3bf4052bf60f90d54bc66e8555963fd09f6c2d0e5a2aaa7047df3c9cd`  
		Last Modified: Fri, 31 Jan 2025 02:17:26 GMT  
		Size: 75.9 KB (75890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b879655de44c37d4990da528967ebf06aa7e4906f21d7f2af67c9120949409a`  
		Last Modified: Fri, 31 Jan 2025 02:17:26 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047d7ad6807fe75ead5a09b330f28671984b74c44d59ac040793c6631aec3725`  
		Last Modified: Fri, 31 Jan 2025 02:17:31 GMT  
		Size: 48.9 MB (48941212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5669b4d2ad12f0129a46bfbed6da19d1aade89773361a84bbffecb3d7f33e1`  
		Last Modified: Fri, 31 Jan 2025 02:17:26 GMT  
		Size: 91.6 KB (91623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
