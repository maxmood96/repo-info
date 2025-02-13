## `eclipse-temurin:11-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:99ef1d2badbba78af522ad0f9e0cff2d8ec7005d705132e595c6ee919530a74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `eclipse-temurin:11-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull eclipse-temurin@sha256:ade93d863953bd2cb86ab15eac4ebfd43f8e7696c0dc0651f81b22ac117541b2
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.4 MB (315413732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d07fad728c329034da99dd31830854fa06c2d08c0d2ed830ad6db59522c3723`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 20:45:43 GMT
RUN Apply image 10.0.20348.3207
# Thu, 13 Feb 2025 01:18:39 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:18:40 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 13 Feb 2025 01:18:41 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 13 Feb 2025 01:18:42 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:18:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Feb 2025 01:18:46 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:18:53 GMT
COPY dir:9a97e9a1ce762bb8542962ee0a2b0ca6fa379668e092b80acfc01b297b3b57a6 in C:\openjdk-11 
# Thu, 13 Feb 2025 01:19:00 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 13 Feb 2025 01:19:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:938e4585b186fc3df3c1959d47ba7a634fea121cec7545db7923ceb191d99a33`  
		Last Modified: Tue, 11 Feb 2025 22:49:39 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a10a0feedc7dc71d6069a1910fa2f6c6fab8d26c3eb9258ddd4a452600e15e`  
		Last Modified: Thu, 13 Feb 2025 04:12:38 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8f394aef31637bf2d62726e45fa921c1f69858cdb7fad7c8a8009cfba1ca62`  
		Last Modified: Thu, 13 Feb 2025 04:12:38 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7eb79eb3be23dc422362e030b2683cae6213181b9cc1009595323c6bf7a38a`  
		Last Modified: Thu, 13 Feb 2025 04:12:38 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df56be39d92120c3b06aef88f3bedadd3ae11c1a679ba7ca0f0e978fd172124`  
		Last Modified: Thu, 13 Feb 2025 04:12:38 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df1843bbecab426366124d35064d251ca9a6ac50bdeb27e103e272da2142e6d`  
		Last Modified: Thu, 13 Feb 2025 04:12:38 GMT  
		Size: 77.0 KB (76995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc9c62487efe4fb7fa3b070e4be6b896e1fce2c7c1c80cd04883a12213e1f6d`  
		Last Modified: Thu, 13 Feb 2025 04:12:38 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7c651ef068fd24f841439b3903587e5efd50025359639cd55f38b9934bb308`  
		Last Modified: Thu, 13 Feb 2025 04:12:46 GMT  
		Size: 194.6 MB (194556786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e9bb039ca0dcc2b26abcf9fb8ae71c28d0b6727ce59cf377e27b9f1a9699c8`  
		Last Modified: Thu, 13 Feb 2025 04:12:38 GMT  
		Size: 106.9 KB (106877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b482822ecd365f70f4ed5389b779b9d410d35ef2a3225f5e2f5841261e4ce10`  
		Last Modified: Thu, 13 Feb 2025 04:12:38 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
