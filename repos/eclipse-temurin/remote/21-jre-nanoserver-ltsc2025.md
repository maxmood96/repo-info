## `eclipse-temurin:21-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:aca2318c1e318e303825fea92c37c5a2ce3d5fa7f3003eb698c691fad201017f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4652; amd64

### `eclipse-temurin:21-jre-nanoserver-ltsc2025` - windows version 10.0.26100.4652; amd64

```console
$ docker pull eclipse-temurin@sha256:a1ca72d67ec9518d899ae90e58b4caba7e8dd81e2555c893c7162b3bc8175d37
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242283484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0bded9206820c203a71d31b7853ae4990ef6cc921cd0f251ca573c36d7f94d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Jul 2025 18:13:07 GMT
RUN Apply image 10.0.26100.4652
# Wed, 09 Jul 2025 19:14:43 GMT
SHELL [cmd /s /c]
# Wed, 09 Jul 2025 19:14:46 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 09 Jul 2025 19:14:47 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 09 Jul 2025 19:14:48 GMT
USER ContainerAdministrator
# Wed, 09 Jul 2025 19:14:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Jul 2025 19:14:54 GMT
USER ContainerUser
# Wed, 09 Jul 2025 19:14:58 GMT
COPY dir:e77a568eefeac18db14cfb92f416dab13c56713fa78f747642b83f8e2eb5149f in C:\openjdk-21 
# Wed, 09 Jul 2025 19:15:04 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:2fd4507679915420227c89c4f57165747b37deaa62748936e2af8c2f38de0b4e`  
		Last Modified: Wed, 09 Jul 2025 01:51:41 GMT  
		Size: 193.2 MB (193150329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498d1b10b0b7ab517845091724195ea4fece6d1d3f84ee47496c0fe7b2ad3bc3`  
		Last Modified: Wed, 09 Jul 2025 19:15:33 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b183a251448bf6642f887719e863051b0a8bd60c0139b7052735cb1f4d91c51`  
		Last Modified: Wed, 09 Jul 2025 19:15:36 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1794b575572b9dff81c3031ed580d4a04cf90db557f06b999df14d14adf6d6b7`  
		Last Modified: Wed, 09 Jul 2025 19:15:34 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ebeb5bcf8d1d70f13ebec0b9dbcd1398c928261ce7076c3237f6fa21650ed6d`  
		Last Modified: Wed, 09 Jul 2025 19:15:33 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945fa46b8c4f631bb18373b96254336c4ea8cf835f0f7fc37a9044356830b70a`  
		Last Modified: Wed, 09 Jul 2025 19:15:34 GMT  
		Size: 76.3 KB (76278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c92d1ed6737bda43327bbae112b1e2b50cad5a864115a317895399e42035f5`  
		Last Modified: Wed, 09 Jul 2025 19:15:34 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696f73c34d726ec8c781f100fbaa62d8a11cd8b9377623f8d5cfa1a675bc0769`  
		Last Modified: Wed, 09 Jul 2025 19:15:44 GMT  
		Size: 48.9 MB (48947417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c092bb6af5144dbafb5c9b24aaf9bdcb7882c1245f59c5d42bf02d14636558b0`  
		Last Modified: Wed, 09 Jul 2025 19:15:34 GMT  
		Size: 104.2 KB (104175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
