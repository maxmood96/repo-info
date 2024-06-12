## `eclipse-temurin:8-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:0fdccb6f80c96e6b9efa1cb63ba8aa4b8153c969075696a6849a3c598dcf92a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2527; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2527; amd64

```console
$ docker pull eclipse-temurin@sha256:7484e68c73d9c045ef4eabeb901b4d01802ac89a115e8dbc815851b16228333d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160749234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ac1caf64c85596aae688483ebcb39bc8a9baba3f27d1f8b729403c388bf9cd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jun 2024 08:41:16 GMT
RUN Apply image 10.0.20348.2527
# Wed, 12 Jun 2024 18:27:44 GMT
SHELL [cmd /s /c]
# Wed, 12 Jun 2024 18:27:45 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Wed, 12 Jun 2024 18:27:45 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 12 Jun 2024 18:27:46 GMT
USER ContainerAdministrator
# Wed, 12 Jun 2024 18:27:59 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Jun 2024 18:28:00 GMT
USER ContainerUser
# Wed, 12 Jun 2024 18:28:42 GMT
COPY dir:2b748c8b95a49802258ef446e3948354b660cf39e9ffa8b2cf36461ec042c5c0 in C:\openjdk-8 
# Wed, 12 Jun 2024 18:28:55 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:f9810bd1ece92cc8c6b01d420e14565e774bed05f414b93e3cd71a54f70dda26`  
		Last Modified: Wed, 12 Jun 2024 18:52:48 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421c68de0fd45f05a2752b0c83793739cd30c57b5ae5491c3141160c219ac360`  
		Last Modified: Wed, 12 Jun 2024 18:52:47 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1858de9f088ee1b7e4f02b6a9fa76de8ed7f8afecd0eda55247112ff4223401`  
		Last Modified: Wed, 12 Jun 2024 18:52:45 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce46f48606178dcedec80045637615eab0fdd951fea4a6bd49c5083e076a856b`  
		Last Modified: Wed, 12 Jun 2024 18:52:45 GMT  
		Size: 77.6 KB (77610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7353e8c7cb28d9c7bb89e81aeb4007a9fe70557ad72c8a17e96ac1e74f611086`  
		Last Modified: Wed, 12 Jun 2024 18:52:45 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df9be096b14943fb9b707f013ec7d23e5819b8617240fea9ce6da24afbb1e516`  
		Last Modified: Wed, 12 Jun 2024 18:53:24 GMT  
		Size: 40.1 MB (40115822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8473b66dc0ff7f446235b36a2b9b6611c152979de24a1e543f3b264032af4b71`  
		Last Modified: Wed, 12 Jun 2024 18:53:19 GMT  
		Size: 61.1 KB (61120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
