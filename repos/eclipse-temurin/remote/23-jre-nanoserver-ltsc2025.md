## `eclipse-temurin:23-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:ae3905e1f4400e985f25544b63de1100dd59078181eab128f98d6465f4e2878a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `eclipse-temurin:23-jre-nanoserver-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:37eaeec837b24737cdb9366a9a1292e88e6ea7837fc266859e85ff653e1325ce
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.2 MB (248220072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82fd71ac654b6e7d93a6950c670e3aa289d1d5f5ad1e2f1f4b26f724b604f20c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Fri, 31 Jan 2025 02:17:15 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 02:17:16 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Fri, 31 Jan 2025 02:17:17 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 31 Jan 2025 02:17:18 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 02:17:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 02:17:22 GMT
USER ContainerUser
# Fri, 31 Jan 2025 02:17:26 GMT
COPY dir:f0b8f3d1970d52810d59047a7e1dfff98787b37140cc4aafc37fc86b09fa8be8 in C:\openjdk-23 
# Fri, 31 Jan 2025 02:17:32 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66cb1e6af4b76d49f1b3df912e0ac2ff70ee7ebbfdad90b32af53d757f0ae6ce`  
		Last Modified: Fri, 31 Jan 2025 02:17:35 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4061c7506ae0bfbb5728a19fc2a31d7b7b89294a796a8240a8a4849883662b`  
		Last Modified: Fri, 31 Jan 2025 02:17:36 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766ec3c7efd2fb1ed701481ff40a97187091d8a07ec9af04b387f9f1c9affbcc`  
		Last Modified: Fri, 31 Jan 2025 02:17:35 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079a73dffaef9d1b2d199d4eca02b10a348a1a6cedf1598c9a91d1561b91ab1d`  
		Last Modified: Fri, 31 Jan 2025 02:17:34 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e844092cb5c62635fd88f839797e04101b339f43f4235e56dd1689ad871211ea`  
		Last Modified: Fri, 31 Jan 2025 02:17:35 GMT  
		Size: 76.7 KB (76661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d77d092e356cabca12b59f5fc6741aae0fa0a6d29bae3be71eca952a258512b`  
		Last Modified: Fri, 31 Jan 2025 02:17:34 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c894ceb20f08b3a91d8318e978218e63e51f39ee902c1f881b199feadff20217`  
		Last Modified: Fri, 31 Jan 2025 02:17:40 GMT  
		Size: 49.0 MB (48979514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199a402f7f4cb79e6baa0c84d0e55f725ad40008313c80c179f711432794dc9a`  
		Last Modified: Fri, 31 Jan 2025 02:17:35 GMT  
		Size: 104.4 KB (104404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
