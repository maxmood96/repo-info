## `eclipse-temurin:17-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:0a3f7c92b0196a43ebdb5cd5259bf93e394edb4355143e9d3825a64cd4e03a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1366; amd64

### `eclipse-temurin:17-nanoserver-ltsc2022` - windows version 10.0.20348.1366; amd64

```console
$ docker pull eclipse-temurin@sha256:94342a5e8e1f03dbe0bb79b5edd14713637c727fc50bdcf3a1484ee6f119d6e8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307718252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fccab237e185993631eacea98f0598962d93691c44e75bde9b821780c6424d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 Dec 2022 09:19:21 GMT
RUN Apply image 10.0.20348.1366
# Tue, 13 Dec 2022 23:42:18 GMT
SHELL [cmd /s /c]
# Tue, 13 Dec 2022 23:45:41 GMT
ENV JAVA_VERSION=jdk-17.0.5+8
# Tue, 13 Dec 2022 23:45:42 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 13 Dec 2022 23:45:43 GMT
USER ContainerAdministrator
# Tue, 13 Dec 2022 23:45:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Dec 2022 23:45:55 GMT
USER ContainerUser
# Tue, 13 Dec 2022 23:46:10 GMT
COPY dir:a12ba5a18c812bc88dc6c1e12f0d0bdbacab70db88697cd6bad273d4570ac4fb in C:\openjdk-17 
# Tue, 13 Dec 2022 23:46:34 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 13 Dec 2022 23:46:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:70d3e1cc3b0ea172dcc93064fe6fb9f1f2c8fec6962c90e39991fe89a3c1ca03`  
		Last Modified: Wed, 14 Dec 2022 00:08:13 GMT  
		Size: 122.1 MB (122108200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8147315b2e02d672b57634f58ed466ba0f8747ed03b8d3d40b71ddb17275cf`  
		Last Modified: Wed, 14 Dec 2022 00:07:43 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab55c9d8171770627f24b2883daf5f63f99e0729d259675d3d377f6d14f0fbe`  
		Last Modified: Wed, 14 Dec 2022 00:09:33 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e72b0dd103f7851e69e7ee52957c5736e7b1d148570e2ac1d8905e21b5ea40`  
		Last Modified: Wed, 14 Dec 2022 00:09:33 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e768a2018c40246caf7a29bb22c35c4a9ccd877c06e2178df3f8c7e51b5b9fd`  
		Last Modified: Wed, 14 Dec 2022 00:09:33 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c3e35e0b5e6faf53bd3659967f5cc9323c49bcf6d02f07d9e93be948eee6f9`  
		Last Modified: Wed, 14 Dec 2022 00:09:31 GMT  
		Size: 84.5 KB (84535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90911701241e7bc1baaa4748c02117f0ce3366ce1e39d67f167d5070585e61c2`  
		Last Modified: Wed, 14 Dec 2022 00:09:31 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ea9f960a00fdced1a542c18c963bec300366ed2ad921dde994ced14e47ed9c`  
		Last Modified: Wed, 14 Dec 2022 00:09:52 GMT  
		Size: 185.4 MB (185429507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216c391ae9429d1f8910e6b7bfc99935acc49bee0df29597d56630690338a6f2`  
		Last Modified: Wed, 14 Dec 2022 00:09:31 GMT  
		Size: 89.4 KB (89356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f21734c98037af6b51cfd000dba6f33daecd731cbc26319b9179853774732a6`  
		Last Modified: Wed, 14 Dec 2022 00:09:31 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
