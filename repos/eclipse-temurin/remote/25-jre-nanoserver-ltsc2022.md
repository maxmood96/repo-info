## `eclipse-temurin:25-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:9a2d6e8b440ad2ee0164e918e169ef941af243ffb685e7d1f4bb15682d5180a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `eclipse-temurin:25-jre-nanoserver-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull eclipse-temurin@sha256:c1ddd640c64fcf7e189e0056e3ee4a2131a7393454ffb0785df8464644aed97f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182811988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295df5ba92c07832b54e5596b20ffb8970f32af45b7b53d1a2793bcf76900a4e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Tue, 09 Jun 2026 23:21:49 GMT
SHELL [cmd /s /c]
# Tue, 09 Jun 2026 23:22:39 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 09 Jun 2026 23:22:39 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 09 Jun 2026 23:22:40 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2026 23:22:42 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Jun 2026 23:22:43 GMT
USER ContainerUser
# Tue, 09 Jun 2026 23:22:53 GMT
COPY dir:fd8baea77fa86bd13952f69621f69e815eb87406af0c0441c94fb1b8a78482df in C:\openjdk-25 
# Tue, 09 Jun 2026 23:22:56 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e97e8b9098cc4d050c642b320fe6d5a7ddda866e0c41c7a307e5ca8734409b`  
		Last Modified: Tue, 09 Jun 2026 23:22:09 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4ac2226abdf401f6a9f19ad659e88e229401ad2eec8f154d29869b7df5634d`  
		Last Modified: Tue, 09 Jun 2026 23:23:02 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7891d3419bc79115a202f01b799fcf2d4e246dd786406bd1ddbaa8e720f4d2f0`  
		Last Modified: Tue, 09 Jun 2026 23:23:02 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be63db47c9ff52a29796782e2b7898c67a996cc667aeaedb470c48840295879`  
		Last Modified: Tue, 09 Jun 2026 23:23:00 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc63edcdf4f79f38a787da1e8ed698735412a27968edc3afd287626999f0a30`  
		Last Modified: Tue, 09 Jun 2026 23:23:00 GMT  
		Size: 85.8 KB (85789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04716c18d4f2d34e6128b3f850ff5dc1e710d4c528e1a8f261f63abbe914ea9`  
		Last Modified: Tue, 09 Jun 2026 23:23:00 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5638800a1e4d2076308ab89d41ac4892f89156afac6d3d69ad031949874593`  
		Last Modified: Tue, 09 Jun 2026 23:23:08 GMT  
		Size: 58.6 MB (58619917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5035a31724b9a6295ce5f191bed2d2d039b642e9057ecc6e4cce8e73d4a40dc2`  
		Last Modified: Tue, 09 Jun 2026 23:23:00 GMT  
		Size: 103.5 KB (103489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
