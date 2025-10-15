## `eclipse-temurin:25_36-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:37ac33e13b7f4809537ceb1b7f5010ea5f915cc6f08e0578b6226295ce83d482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `eclipse-temurin:25_36-jre-nanoserver-ltsc2022` - windows version 10.0.20348.4294; amd64

```console
$ docker pull eclipse-temurin@sha256:ca76dfb3de5999fea4f48713fd6d3daeb19f9a0b873c884f0153d2be03d36b86
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181411895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56328491f7ad1f1cfb4c17bedf42537bb13cfc8f03a0879313e63a3a8a35217a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Oct 2025 07:34:08 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 21:12:07 GMT
SHELL [cmd /s /c]
# Tue, 14 Oct 2025 21:13:29 GMT
ENV JAVA_VERSION=jdk-25+36
# Tue, 14 Oct 2025 21:13:29 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 14 Oct 2025 21:13:29 GMT
USER ContainerAdministrator
# Tue, 14 Oct 2025 21:13:31 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Oct 2025 21:13:31 GMT
USER ContainerUser
# Tue, 14 Oct 2025 21:13:35 GMT
COPY dir:8aa8ce0e84e7e6f80be28438d765894541d9d2eadfccff43ebe7257923223c3b in C:\openjdk-25 
# Tue, 14 Oct 2025 21:13:38 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:f68a3bbf3ee20b515c5b8b801e5627a9dac3782ef264e37060c34ed80e5d8874`  
		Last Modified: Tue, 14 Oct 2025 20:41:53 GMT  
		Size: 122.7 MB (122688886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97004b1f45dbb42e74fcf45291378b73026f24a385f84780f274b7ff65e64f78`  
		Last Modified: Tue, 14 Oct 2025 21:13:14 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72254ac55b809ad01ad6da1d4e002cd519b30a12ea3f46649550173acbb89dce`  
		Last Modified: Tue, 14 Oct 2025 21:14:09 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed6dbdd8bb104fed1e39891f942cf37eb803d665d69151b315417444144d7558`  
		Last Modified: Tue, 14 Oct 2025 21:14:09 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f0222870d0a05487949e4ee81e611c9e4e4bdad70b8e6c8fc5d4eb70f065c1`  
		Last Modified: Tue, 14 Oct 2025 21:14:09 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be078139607dc728a5cd67277ee4ec2303a94bf32d64c3a70f0745341f1fbc3`  
		Last Modified: Tue, 14 Oct 2025 21:14:09 GMT  
		Size: 76.6 KB (76644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f149635137a9a3a66b68e1df257c066b7e6d922a9c235e47b555b871c42a0af`  
		Last Modified: Tue, 14 Oct 2025 21:14:09 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c72ef29a17eca7d8646c1e8b154f737f7852342db196d4206aa11388a60a7b`  
		Last Modified: Tue, 14 Oct 2025 21:14:26 GMT  
		Size: 58.6 MB (58550991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cb4db7a121728323e20e0169b7fe4f9fbd1e6dfb643399d5aa7ade6eec3443`  
		Last Modified: Tue, 14 Oct 2025 21:14:09 GMT  
		Size: 90.1 KB (90067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
