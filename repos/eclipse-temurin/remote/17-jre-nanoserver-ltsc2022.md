## `eclipse-temurin:17-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:49ad535a8485341b2aa50ab8f700c5f6611666b225b3f15c5404a3b63c632547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull eclipse-temurin@sha256:b39057db21f093c831c51fdacbefe3bf4ac236c0f83023f1434bd04f53eb7cd3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164018194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd1731a2601633ed69382313d2c62ffd898012f8d4ecb466c25cb19d7dc6339`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 09:30:07 GMT
RUN Apply image 10.0.20348.2582
# Wed, 10 Jul 2024 17:17:20 GMT
SHELL [cmd /s /c]
# Tue, 23 Jul 2024 00:32:37 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Tue, 23 Jul 2024 00:32:37 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 23 Jul 2024 00:32:38 GMT
USER ContainerAdministrator
# Tue, 23 Jul 2024 00:32:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 23 Jul 2024 00:32:49 GMT
USER ContainerUser
# Tue, 23 Jul 2024 00:33:26 GMT
COPY dir:4243678b5415f703b690863e65df7851d84efb271bd792cb5cbd95ab7bb17263 in C:\openjdk-17 
# Tue, 23 Jul 2024 00:33:36 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:652774a5d82a114642848f8b0b8d486ec1b4995f9dda56e36fe4ac7563429990`  
		Last Modified: Tue, 09 Jul 2024 20:33:26 GMT  
		Size: 120.5 MB (120490378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1dbb650483c31087741ccfe7cfef17abfd7465711d0851e35d39eabc775bdae`  
		Last Modified: Wed, 10 Jul 2024 17:38:52 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f6cedd9abf2a19d51a511b77107257f2572e79669cc404ad4a1430239713b4`  
		Last Modified: Tue, 23 Jul 2024 00:41:49 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd27a9bb8d7c8942a0f2333ea217e0d3e29ab4434087220de85831121fc1330`  
		Last Modified: Tue, 23 Jul 2024 00:41:49 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a5083ccb916e67b97dc1dd9b8639b4df6fa71d10f1d598d3a5eb0f295844d26`  
		Last Modified: Tue, 23 Jul 2024 00:41:49 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc084be9fd1b2b08834d0ea06d4b92b10fb1d5425b3f5c50d5614ef5dc0bb29`  
		Last Modified: Tue, 23 Jul 2024 00:41:48 GMT  
		Size: 91.5 KB (91486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e84d48037f6533f36f4ae2aeb9f5a9900baab424efff85eeca0ce7e172728b`  
		Last Modified: Tue, 23 Jul 2024 00:41:47 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9f052bf8dfff27a3501fbe2063be745170bb91c4c50e6b28de5e7ce892cc09`  
		Last Modified: Tue, 23 Jul 2024 00:42:18 GMT  
		Size: 43.4 MB (43357284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b5401e2db8bb592c35c5bebb879024f73e20047cf1628149582249c15af588`  
		Last Modified: Tue, 23 Jul 2024 00:42:11 GMT  
		Size: 73.3 KB (73269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
