## `eclipse-temurin:17-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:8cff991a217bd6025ce70c262628903cba6ef8452ca2982c0b47b1127e5d7c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull eclipse-temurin@sha256:5d77c963a46b83cd956a7664a986e06cbafb6a391aaf1fac70a6ddbf15a3a586
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170612732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb3854ae071e32694c119fd9327c6c0bc644d8b8e19903efa7345c1210d6a57d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Tue, 10 Feb 2026 23:30:05 GMT
SHELL [cmd /s /c]
# Tue, 10 Feb 2026 23:30:52 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 10 Feb 2026 23:30:52 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 10 Feb 2026 23:30:52 GMT
USER ContainerAdministrator
# Tue, 10 Feb 2026 23:30:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Feb 2026 23:30:54 GMT
USER ContainerUser
# Tue, 10 Feb 2026 23:30:58 GMT
COPY dir:064fca0b30194d02fe341355ba6a62fc1748c82418561395eb5bec357779f4c8 in C:\openjdk-17 
# Tue, 10 Feb 2026 23:31:01 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88bd703ad3be2a352cd766b66162d651fa380534f38e60a0bd66c13f3a03b45b`  
		Last Modified: Tue, 10 Feb 2026 23:30:24 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43eb297a4d65a1b6dfd051a80957c6229a91a6f87f027220f9996856813ff54f`  
		Last Modified: Tue, 10 Feb 2026 23:31:06 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c99754b76cf7f8d8a2fd7986484ef96206ee1dcef73ba8f61829ea8cc8895db`  
		Last Modified: Tue, 10 Feb 2026 23:31:06 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d88556e7e0eeb340367d56bed772b721cda6a5c12647b758c0e4055c9f47200`  
		Last Modified: Tue, 10 Feb 2026 23:31:05 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e386950385462a0276c80c8626ce45485ec833ad144081f256317a71def7dc16`  
		Last Modified: Tue, 10 Feb 2026 23:31:05 GMT  
		Size: 76.4 KB (76441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27901ea09cbb5f27cee8081729ecd541126206f56731ef0b39a2c25afdc54b84`  
		Last Modified: Tue, 10 Feb 2026 23:31:05 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df44eb4acd0502a2bb757da5dcd100c5154ba40da2fcca9841374f3d5aded3f`  
		Last Modified: Tue, 10 Feb 2026 23:31:11 GMT  
		Size: 43.8 MB (43794894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc0bfd54829d64def749b937830040a4d740a0aa0cc2fc855b35d2af2e15b07`  
		Last Modified: Tue, 10 Feb 2026 23:31:05 GMT  
		Size: 90.2 KB (90250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
