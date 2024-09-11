## `eclipse-temurin:22-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:e7826c9d66bc42f3c297c9feedc5981059bacf095684bd76ce1871351a6841c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `eclipse-temurin:22-jre-nanoserver-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull eclipse-temurin@sha256:4c0d0513cdbb6a72b18cf70e2742384c7e0e5446a150b0189837f6ceb9fa24f5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.9 MB (206901426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a85b07182908ecfff9784b09d02d4e7678c01aa64e7aa840640dc1989d78ec6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:38:01 GMT
SHELL [cmd /s /c]
# Wed, 11 Sep 2024 01:02:38 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Wed, 11 Sep 2024 01:02:39 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 11 Sep 2024 01:02:40 GMT
USER ContainerAdministrator
# Wed, 11 Sep 2024 01:02:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Sep 2024 01:02:48 GMT
USER ContainerUser
# Wed, 11 Sep 2024 01:05:33 GMT
COPY dir:65be971618b84fe71c044bdca6efe8a2b46f4ab6c5b677a6f304a9c5505af541 in C:\openjdk-22 
# Wed, 11 Sep 2024 01:05:41 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340318059288cbbdb326eea5b7079e789361251409038a37867d4e395c9404a5`  
		Last Modified: Wed, 11 Sep 2024 01:21:36 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c236eabf1692aa5b9df809f05092ea123d2981c2f03c8c2614a56a6dc91f38e4`  
		Last Modified: Wed, 11 Sep 2024 01:31:52 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95ad8e46da66c1f7d579def1a776f99e3b63d710d2db74aa6108b45614c19e9`  
		Last Modified: Wed, 11 Sep 2024 01:31:51 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd8eb7d82b9037502824973aead7bb4bc553b067d394f8dcb440e4bfacafd3f`  
		Last Modified: Wed, 11 Sep 2024 01:31:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439205c68ff44a87736d8463b1b27aa383bef80fa5013e85c4bc42a1022cdf54`  
		Last Modified: Wed, 11 Sep 2024 01:31:50 GMT  
		Size: 67.9 KB (67899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b19966c2ae318bd6bf3301b5a61b21486fb24665cd8f377895d8d3410b2ca5`  
		Last Modified: Wed, 11 Sep 2024 01:31:50 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff423c106ad052cb9b001d5097a5feceea5ed1ee0131a0a566d34e44ce261ee`  
		Last Modified: Wed, 11 Sep 2024 01:33:01 GMT  
		Size: 48.4 MB (48367340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94137bf1c145636a5a41b7f5b2ce73475d547511dfe56eee4396f130523b0f29`  
		Last Modified: Wed, 11 Sep 2024 01:32:53 GMT  
		Size: 3.4 MB (3379595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
