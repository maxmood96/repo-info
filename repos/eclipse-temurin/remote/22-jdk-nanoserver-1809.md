## `eclipse-temurin:22-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:b1764ea709470c9b07b2ab135de26fac0f46f4790e6a5d68909922b753d056e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:22-jdk-nanoserver-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull eclipse-temurin@sha256:6fbcab6da732c486f85d62a2f54df874d78f3324f8ea88237284d26a30161a7d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.6 MB (358616326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab181accf0f64cbd8a1100565908dfad2728aa206124b5a43ec1f51249c66291`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 16:38:43 GMT
SHELL [cmd /s /c]
# Wed, 24 Jul 2024 01:31:35 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Wed, 24 Jul 2024 01:31:36 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 24 Jul 2024 01:31:36 GMT
USER ContainerAdministrator
# Wed, 24 Jul 2024 01:31:43 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Jul 2024 01:31:44 GMT
USER ContainerUser
# Wed, 24 Jul 2024 01:31:56 GMT
COPY dir:bb8037d92e17293fdab4a72c09c9eb83e6a7b620b5e832c71d656bbaf7bd694c in C:\openjdk-22 
# Wed, 24 Jul 2024 01:32:07 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 24 Jul 2024 01:32:08 GMT
CMD ["jshell"]
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
	-	`sha256:00c82941c8847f46f3abb44013c628dce3a04bd9b35c64e0c75ad1e3efeb5d14`  
		Last Modified: Wed, 24 Jul 2024 02:25:50 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4093fa16807be9336588c4af670f751fe872cace5bd8c244992868f2da30d4`  
		Last Modified: Wed, 24 Jul 2024 02:25:50 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9617cc683bc9bcad6d3f3c19a5574f82d364531847b57f9ec1adc031901237`  
		Last Modified: Wed, 24 Jul 2024 02:25:50 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679086a23836613457fe0818e8a433c17497f677ae6958b7fc0cdda845b1374d`  
		Last Modified: Wed, 24 Jul 2024 02:25:48 GMT  
		Size: 68.4 KB (68417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e5b91d2a5fe412cb2a8c2f7be0f2e0e67aed42c5de9a1ef55bf0d2e60b01b0`  
		Last Modified: Wed, 24 Jul 2024 02:25:48 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6227cdf5e9616d385c15de9781fd1749b3ff7b5a1e79144f055715da4b9601a`  
		Last Modified: Wed, 24 Jul 2024 02:26:07 GMT  
		Size: 199.6 MB (199623271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca53c743c4c3c9ad1e44b0c350ae366c559068e47fa97227b74f0829bcef416`  
		Last Modified: Wed, 24 Jul 2024 02:25:49 GMT  
		Size: 3.8 MB (3836387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801e25086323f3ed9d381865a2459e31e173f9123557daac17cdd3b00ef91640`  
		Last Modified: Wed, 24 Jul 2024 02:25:48 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
