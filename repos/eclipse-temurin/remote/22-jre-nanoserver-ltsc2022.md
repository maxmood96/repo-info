## `eclipse-temurin:22-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:d694f67eba5c1e1888fa743de1a0955c5a173fda2bf855a095928c452c75cc8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `eclipse-temurin:22-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull eclipse-temurin@sha256:89eb9752e5825ca26eff71f48759c699bf2d3c2abb684cd891ec5d003624f515
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.0 MB (169031949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1c1641503a5b39e3d7055d38518a6f74b9afcc576039546ca376d8f5714755`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 10 May 2024 20:16:48 GMT
RUN Apply image 10.0.20348.2461
# Wed, 15 May 2024 20:32:41 GMT
SHELL [cmd /s /c]
# Wed, 15 May 2024 20:38:17 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Wed, 15 May 2024 20:38:18 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 15 May 2024 20:38:18 GMT
USER ContainerAdministrator
# Wed, 15 May 2024 20:38:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 May 2024 20:38:30 GMT
USER ContainerUser
# Wed, 15 May 2024 20:39:24 GMT
COPY dir:b356dfbfb05ab2ab46133b6b7ad4e4cb6a7442df8599937d6806166f02780fa5 in C:\openjdk-22 
# Wed, 15 May 2024 20:39:35 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:90b3a5622f8d62905d0a3029df4f91b934558ad375bef25c596214df31acac88`  
		Last Modified: Tue, 14 May 2024 17:22:15 GMT  
		Size: 120.4 MB (120425316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5560c76ac3d9aa2d8a6dbf79d443a7e1d170aae31c940cf791c9b532d5756a1`  
		Last Modified: Wed, 15 May 2024 20:58:04 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901805c453a3db5b81fbc5d7d76e019125a99325c46faa1f0b249503920c008b`  
		Last Modified: Wed, 15 May 2024 21:01:17 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f149c4c0118609d2025fd94d42ca722b9067880f610f3fdad29b66ef847ca824`  
		Last Modified: Wed, 15 May 2024 21:01:17 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc98af44c3d06c23e98453c26b8e25353d2f83fd7b96c7ae493040b1ec15b02a`  
		Last Modified: Wed, 15 May 2024 21:01:17 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced33bf6b165e04ab1f9b71b5848ed0c96e644eb880d246c00a7153fffb77d8c`  
		Last Modified: Wed, 15 May 2024 21:01:15 GMT  
		Size: 81.0 KB (80953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9e59eaac6374219cc1d44150b7730ae29db255a59201697a09fcfc13f25285`  
		Last Modified: Wed, 15 May 2024 21:01:15 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418bf515a2e5ce43916d2a4cd2311c56386adc490eda4232b6826cdc1ebd663a`  
		Last Modified: Wed, 15 May 2024 21:01:58 GMT  
		Size: 48.5 MB (48471068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a077a2a498e600a2e7275c22fe3511db7e711104fd858e61adbf597bdc3941`  
		Last Modified: Wed, 15 May 2024 21:01:49 GMT  
		Size: 48.8 KB (48844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
