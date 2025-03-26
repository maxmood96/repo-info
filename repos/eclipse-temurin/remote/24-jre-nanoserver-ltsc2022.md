## `eclipse-temurin:24-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:d7dbbe71bf1b5ae7b28d6cffdb53b8d47d3189efdd50b1745fd2150c50244975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `eclipse-temurin:24-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull eclipse-temurin@sha256:57131b7ece1057a579bcf4b713fcda3b8ffa3571ded0e9939109cd35c39d8e77
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.6 MB (178575993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7cc540105e151acfa7e2bf11f45e502168d52a9884a470eb6d440edd79c5cd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Tue, 25 Mar 2025 23:23:25 GMT
SHELL [cmd /s /c]
# Tue, 25 Mar 2025 23:23:26 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 23:23:27 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 25 Mar 2025 23:23:27 GMT
USER ContainerAdministrator
# Tue, 25 Mar 2025 23:23:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 25 Mar 2025 23:23:31 GMT
USER ContainerUser
# Tue, 25 Mar 2025 23:23:35 GMT
COPY dir:90c9828944ffcd2978afe702f80884cbf787022d7dcd7becc7c91cd2ab6f7dd5 in C:\openjdk-24 
# Tue, 25 Mar 2025 23:23:40 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf9dddd7da9a70eac8a7048d104817e052046ff648b5e3a869add8fcee45e6b6`  
		Last Modified: Tue, 25 Mar 2025 23:23:45 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abb9d74c9b1b7713d1309ee4cb0bfc9641ccb2d22e71fc571dd8e97facd13c2`  
		Last Modified: Tue, 25 Mar 2025 23:23:45 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87e2b1edd7419dc29ba3c9b13ee367f8d42244eda0057c2e3617b2b486a9a91`  
		Last Modified: Tue, 25 Mar 2025 23:23:45 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e776c47f588273589d3e4b7aab1fdda4e514e9806635c3adbcff4b1fcc5148`  
		Last Modified: Tue, 25 Mar 2025 23:23:44 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b1902f7ffea612782f86025c222acb396a6bb5ea83f8c14b94a643588d870b`  
		Last Modified: Tue, 25 Mar 2025 23:23:44 GMT  
		Size: 77.0 KB (77005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b097a2b47469115f0533545676071f28c690c9e0893bc4402b7607259e89b721`  
		Last Modified: Tue, 25 Mar 2025 23:23:44 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8b28d2bcb4f16fc130f07bea062baac775e931268a5ca3e3fb2d71e68a2e35`  
		Last Modified: Tue, 25 Mar 2025 23:23:51 GMT  
		Size: 57.7 MB (57700729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b869ba14727d4d26920b073f39df29f41a9131d6e95a3e45bea0d2c63bb4fac`  
		Last Modified: Tue, 25 Mar 2025 23:23:44 GMT  
		Size: 97.5 KB (97470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
