## `eclipse-temurin:21-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:581034aff1bc82b804b6899365f8dee3c97a54755cefb6b573919379aad5945f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `eclipse-temurin:21-jre-nanoserver-ltsc2022` - windows version 10.0.20348.4294; amd64

```console
$ docker pull eclipse-temurin@sha256:3e763bb7058ace6bcbe693ba59d31127b5294c8fa3e79e57fabe54b0b16ba451
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171902759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd08b77c932fe1f4442ef2bb2e21a7d927f5f1977124f92e34726cf14c22662`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Oct 2025 07:34:08 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 21:12:23 GMT
SHELL [cmd /s /c]
# Tue, 14 Oct 2025 21:13:18 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Tue, 14 Oct 2025 21:13:18 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 14 Oct 2025 21:13:18 GMT
USER ContainerAdministrator
# Tue, 14 Oct 2025 21:13:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Oct 2025 21:13:20 GMT
USER ContainerUser
# Tue, 14 Oct 2025 21:13:23 GMT
COPY dir:1d2e38188fefbb829677ed8e6106bab9aec7034078d0a523158404f660841581 in C:\openjdk-21 
# Tue, 14 Oct 2025 21:13:26 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:f68a3bbf3ee20b515c5b8b801e5627a9dac3782ef264e37060c34ed80e5d8874`  
		Last Modified: Tue, 14 Oct 2025 20:41:53 GMT  
		Size: 122.7 MB (122688886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c23b710b333987aafcdf1771380232af85431ac0f5fff7fe41a912c36003916`  
		Last Modified: Tue, 14 Oct 2025 21:13:11 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09197169da9705bc8fb2709ffadb66f04574f0977d930c4c00b65eefeef89d61`  
		Last Modified: Tue, 14 Oct 2025 21:13:44 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43a2e55460b52f8cdbb2cf5fe2ec5894f3651e464c26bae5c2759f2532c9b09`  
		Last Modified: Tue, 14 Oct 2025 21:13:44 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef28883e6615c3cb57ab21536af9363d62848a14f2eb2619a9b2caf610c797d7`  
		Last Modified: Tue, 14 Oct 2025 21:13:44 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6386c55f240426cd33484a6dc548404a4ca89b4608adcc7de1a6c549858b4137`  
		Last Modified: Tue, 14 Oct 2025 21:13:44 GMT  
		Size: 77.4 KB (77383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c53ba99e996f3f3a0d04bfcf08db39b6522427480a9829dd8cc4cad9b59ce9`  
		Last Modified: Tue, 14 Oct 2025 21:13:44 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e20b7b442c298d51838f550fdfceac8a92673118763a55e3e7d8bba1f8ddfeb`  
		Last Modified: Tue, 14 Oct 2025 21:13:54 GMT  
		Size: 49.0 MB (49011301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60310f6e7e63337bb4302dc8f5d2920e6f789a14df71fa3577356c68ed905d4`  
		Last Modified: Tue, 14 Oct 2025 21:13:44 GMT  
		Size: 119.8 KB (119846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
