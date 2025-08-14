## `eclipse-temurin:21-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:96bc9c557077a11b51d29eada359322e1e318d2a424912a72eee84256c0e65d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `eclipse-temurin:21-jre-nanoserver-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull eclipse-temurin@sha256:9d3bc78098349373abbe1b35a34e384ef25092c7b66b4c68bc1a969381c1da2a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.7 MB (242657685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:202691df172d83087eeb1706c864c6f1f46ac4343b4550dddfa1ad5a2491d52b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 Aug 2025 02:44:20 GMT
RUN Apply image 10.0.26100.4946
# Tue, 12 Aug 2025 20:50:13 GMT
SHELL [cmd /s /c]
# Tue, 12 Aug 2025 20:50:14 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Tue, 12 Aug 2025 20:50:14 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 12 Aug 2025 20:50:14 GMT
USER ContainerAdministrator
# Tue, 12 Aug 2025 20:50:16 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 12 Aug 2025 20:50:16 GMT
USER ContainerUser
# Tue, 12 Aug 2025 20:50:20 GMT
COPY dir:c21dbe47d2de1b48c1d9f92222d71f88b5c065d2194c2f26a7fb8e303259e21a in C:\openjdk-21 
# Tue, 12 Aug 2025 20:50:22 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:6d63d98dae9e3419e8c965c24a11d30e40947cf35ee17c204c5d8b7bae7ff2ef`  
		Last Modified: Tue, 12 Aug 2025 21:13:38 GMT  
		Size: 193.5 MB (193469373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cd7903c58f17384f40faf3bb0a5dc583db6cc3eb7be6b1fd5a5fc8e1667997`  
		Last Modified: Tue, 12 Aug 2025 21:16:54 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f554b82243d6f76b06266b0041c96aac01bba1f29e85fb3b901188a50b43190d`  
		Last Modified: Tue, 12 Aug 2025 21:16:54 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eea5dbf744d71e86ac17e6bf16d3ae9d3019799b4f7116551f40d5d21ca0820`  
		Last Modified: Tue, 12 Aug 2025 21:16:54 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f979a56fb98584cff3dec2fd540fdd324669c18ab663974933592a269ad4c1e`  
		Last Modified: Tue, 12 Aug 2025 21:16:55 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b196546fa4e2d0c50ec3a1972197bc8a60ffdcb096fcb94fcb00e4686cc5256`  
		Last Modified: Tue, 12 Aug 2025 21:16:54 GMT  
		Size: 75.7 KB (75692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367a0eda1bdbfc75675db9f2c177df03f2fec6c2f72ed808958dbc3e7f349ace`  
		Last Modified: Tue, 12 Aug 2025 21:16:55 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e242cbeb7349bc9620293c4870d77c487ddf4e862db8d6a689e40cd726c5510e`  
		Last Modified: Tue, 12 Aug 2025 21:16:58 GMT  
		Size: 49.0 MB (49011114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f96eb2a768023a1dd02808c00c904ee112e58f88ab40005f9e68272563f0b2a`  
		Last Modified: Tue, 12 Aug 2025 21:16:55 GMT  
		Size: 96.1 KB (96074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
