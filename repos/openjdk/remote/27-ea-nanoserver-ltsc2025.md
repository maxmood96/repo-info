## `openjdk:27-ea-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:7beb46c1c0d297a2e817194368f28d723363558319913497869b5e3779561f6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `openjdk:27-ea-nanoserver-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull openjdk@sha256:801c63de6c198980882b3d121849ddb3c3d9d3da15ff8c753a0ffa2b0e3d609f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.5 MB (424452821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397e50206d42d94a22701115f8da15f6c8584e5537fead584013c22581216264`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 06:39:57 GMT
RUN Apply image 10.0.26100.32690
# Mon, 20 Apr 2026 18:09:33 GMT
SHELL [cmd /s /c]
# Mon, 20 Apr 2026 18:09:34 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 20 Apr 2026 18:09:35 GMT
USER ContainerAdministrator
# Mon, 20 Apr 2026 18:09:50 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 20 Apr 2026 18:09:51 GMT
USER ContainerUser
# Mon, 20 Apr 2026 18:09:51 GMT
ENV JAVA_VERSION=27-ea+18
# Mon, 20 Apr 2026 18:10:31 GMT
COPY dir:a5a96ee23a9a9a0ed76c7b441bc5d94cd3b4aa83f20a322d859f026439d5f3a3 in C:\openjdk-27 
# Mon, 20 Apr 2026 18:10:38 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 20 Apr 2026 18:10:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8af320c3b6d19296bcc7947e3beb8bc0c69cb12143db52efe988dc998ac088dc`  
		Last Modified: Tue, 14 Apr 2026 21:00:37 GMT  
		Size: 199.7 MB (199717094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b97211ea280f46225551fbddbc36f033e1cf8515d8f39f3f4bd35636561df4`  
		Last Modified: Mon, 20 Apr 2026 18:10:45 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5c83ffd90088ac9d8921fb4f9c31bf45ebb528422daae5a8956d6af3cd6dc1`  
		Last Modified: Mon, 20 Apr 2026 18:10:44 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1d560543cb328b231f4c5e0f29618ca294ca07882f4c34d300507eabdb59ac`  
		Last Modified: Mon, 20 Apr 2026 18:10:44 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9960e519b707a5ef80e591458fdf7866d40e2cd19b82f71a6581a86cb4d5e189`  
		Last Modified: Mon, 20 Apr 2026 18:10:45 GMT  
		Size: 78.2 KB (78189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51eeab9a88a2019c2bde99d7a1dc210ac56d2310f77124eb90468b2a8fd0216e`  
		Last Modified: Mon, 20 Apr 2026 18:10:43 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac228b4e0e691ffa678e187a10ee03caeb931e9f9851de3c4ca9d1c727778671`  
		Last Modified: Mon, 20 Apr 2026 18:10:43 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978d6688b0824c4adf8888be0ed36981551080525e97f5d466a58036b0b25b03`  
		Last Modified: Mon, 20 Apr 2026 18:10:57 GMT  
		Size: 224.6 MB (224572902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5f525d96a7f8c54c7eb22360aa0a91b9c3743506f39a15f2a1ee934816402e`  
		Last Modified: Mon, 20 Apr 2026 18:10:43 GMT  
		Size: 78.3 KB (78271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b432623c9943a1cfec02bb7bd98f3281c3bc95658882c1831b62c443485161ce`  
		Last Modified: Mon, 20 Apr 2026 18:10:43 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
