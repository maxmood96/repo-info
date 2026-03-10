## `eclipse-temurin:17-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:6dfe5969ae4bbc4ed112b23b08e634e9d3aba87aa334acea1554a2a94ce63609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull eclipse-temurin@sha256:f9f9a295453af382cbba1804d8a490f1be5330ad8ddd876cf2a02670b2a06857
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170630191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad51e4ebbc89cda6d6419fad72da6bf077e0db64bfb390f51c11138bca476e1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 10 Mar 2026 22:37:01 GMT
SHELL [cmd /s /c]
# Tue, 10 Mar 2026 22:37:01 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 10 Mar 2026 22:37:02 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 10 Mar 2026 22:37:02 GMT
USER ContainerAdministrator
# Tue, 10 Mar 2026 22:37:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Mar 2026 22:37:04 GMT
USER ContainerUser
# Tue, 10 Mar 2026 22:37:10 GMT
COPY dir:064fca0b30194d02fe341355ba6a62fc1748c82418561395eb5bec357779f4c8 in C:\openjdk-17 
# Tue, 10 Mar 2026 22:37:13 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab158ec47dd7f3d690f266b342613aecc1ef28aaa2d4dc17dcdb6ed37ef95bc`  
		Last Modified: Tue, 10 Mar 2026 22:37:19 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ebeeaf1eb142018416b83d6517d11533a3acfc83d31e0fc3041974b94337ee`  
		Last Modified: Tue, 10 Mar 2026 22:37:18 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3a0b0bcb1dd146c7de717c32ec2e2625e0be8a6c81e85f2754c045ff6e2087`  
		Last Modified: Tue, 10 Mar 2026 22:37:19 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f2c7f6765fa63f4e30a23acad01cdc38ba8d5ebc5215c5454bbbc3ce0a40bc`  
		Last Modified: Tue, 10 Mar 2026 22:37:17 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244ecb504540dfa754234d617c294746753c331aceebe61cb64ee4312a8696c1`  
		Last Modified: Tue, 10 Mar 2026 22:37:17 GMT  
		Size: 87.1 KB (87142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a7b1fd4a39e44451b4bc98ae7c3e143598657de438e2840a985fc48bbb76c8`  
		Last Modified: Tue, 10 Mar 2026 22:37:17 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42da5df7070bc27d75d2f27314fabacea6032e800607d421db27d8c8a6e9ea62`  
		Last Modified: Tue, 10 Mar 2026 22:37:23 GMT  
		Size: 43.8 MB (43794762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705981bb49c78d71518c8ad51f33b9631f8d1b50fa1702e5c2087cdb932e893b`  
		Last Modified: Tue, 10 Mar 2026 22:37:17 GMT  
		Size: 92.5 KB (92497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
