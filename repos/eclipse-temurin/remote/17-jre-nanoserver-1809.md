## `eclipse-temurin:17-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:ae3acb5002db0a5a9263e71e5c4ee4fd948a5476ccc5cef267298c2d9d060696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:17-jre-nanoserver-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull eclipse-temurin@sha256:73ce1b4fd7ebc0074450cebbca22d53a4145af15273b8a9a5450a0334d7b44d6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.5 MB (201494149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be3fba88f76d7b40ddec92b5d634f3900b1f60c319c5ffd2278713d093b206a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 16:38:43 GMT
SHELL [cmd /s /c]
# Tue, 23 Jul 2024 00:19:40 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Tue, 23 Jul 2024 00:19:41 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 23 Jul 2024 00:19:41 GMT
USER ContainerAdministrator
# Tue, 23 Jul 2024 00:19:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 23 Jul 2024 00:19:53 GMT
USER ContainerUser
# Tue, 23 Jul 2024 00:23:45 GMT
COPY dir:4243678b5415f703b690863e65df7851d84efb271bd792cb5cbd95ab7bb17263 in C:\openjdk-17 
# Tue, 23 Jul 2024 00:23:54 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00a79547db1bc3ab4a5550f2ec9ba165e302f4a4984af3c1bfbbbe1726a3bf6`  
		Last Modified: Wed, 10 Jul 2024 17:28:00 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad586d68932eb4f5593d11718113bf29e815de2477942809ad435388afa4841e`  
		Last Modified: Tue, 23 Jul 2024 00:38:14 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe8249ad28f733c50edafc6a986eefeffd8a33247bcfdc8b66c207d6823afc3`  
		Last Modified: Tue, 23 Jul 2024 00:38:14 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc730398c9de27b889030709a242bd7da7ef3371588881e0a0aa2d50d5f0bda`  
		Last Modified: Tue, 23 Jul 2024 00:38:14 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9283bfea5738fe545d54136ad4cf589daa7ca9cd6b046c743d2801f60fc59ca0`  
		Last Modified: Tue, 23 Jul 2024 00:38:12 GMT  
		Size: 68.2 KB (68236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88c890511e21b6c2cf0a188d2b5d2b9d80684c0aacedc7a62399b5535209af6`  
		Last Modified: Tue, 23 Jul 2024 00:38:12 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344f1a751ed8773502eca058b00f6106e8d52975af2f8d5dca5d02fb9fe175db`  
		Last Modified: Tue, 23 Jul 2024 00:39:14 GMT  
		Size: 43.4 MB (43357462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc556d6d081142f186066301632e462f434b021be9824d60e9d58217932e14f`  
		Last Modified: Tue, 23 Jul 2024 00:39:08 GMT  
		Size: 3.0 MB (2981343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
