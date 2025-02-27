## `eclipse-temurin:21-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:a110f54c2e6e05159afb34113b4f01148fb7899a48aedd3a2001341d163fff51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `eclipse-temurin:21-jre-nanoserver-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull eclipse-temurin@sha256:3f0e49156826636d357477ad4df48900bfeb787df5a3dcbf579c701dfdff5fc2
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (255005459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf522cd7acda991b9bc845ebdd4e0b587d059140a627a53a30df9b0f72699703`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 08 Feb 2025 22:31:47 GMT
RUN Apply image 10.0.26100.3194
# Thu, 27 Feb 2025 19:13:40 GMT
SHELL [cmd /s /c]
# Thu, 27 Feb 2025 19:13:42 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 27 Feb 2025 19:13:42 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 27 Feb 2025 19:13:43 GMT
USER ContainerAdministrator
# Thu, 27 Feb 2025 19:13:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 27 Feb 2025 19:13:46 GMT
USER ContainerUser
# Thu, 27 Feb 2025 19:13:49 GMT
COPY dir:c0b7c132c85049081486a93cd76fe016c559b0b921796f63592a768b082ae9e2 in C:\openjdk-21 
# Thu, 27 Feb 2025 19:13:53 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:e075dd07cbf907b7da8dbd8365b73a71ac92a834b78f520bd976cb97e0fcc0a1`  
		Last Modified: Wed, 12 Feb 2025 22:34:59 GMT  
		Size: 205.9 MB (205890263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e05e8f636d24ff95e360d5ef256133ec350ac25e34caca96bc6612c18e7b70`  
		Last Modified: Thu, 27 Feb 2025 19:13:58 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083abc61ff01fa4b9a7d4e15c40a7d91f2514eaac5abfb17a954a9bd6f8e0c6c`  
		Last Modified: Thu, 27 Feb 2025 19:13:58 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f537c10dd75ed9823cfef1f45a877f38f74880c207fc42ee84b3579c3e6dfd01`  
		Last Modified: Thu, 27 Feb 2025 19:13:58 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9568187755cfa9cefc20925493a008e8dc4568494daad1ce9f5255a8f51e7815`  
		Last Modified: Thu, 27 Feb 2025 19:13:57 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190d8599969fd3ad44cb7431693d46897cdd955c1055f703010a432d34e808a5`  
		Last Modified: Thu, 27 Feb 2025 19:13:57 GMT  
		Size: 76.2 KB (76183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bad2cf06341e769c247d1f2636c13658cf58c84bec8e7f7eaf06f3ccae4f70`  
		Last Modified: Thu, 27 Feb 2025 19:13:57 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28fd3a4d93f739531e37f858a295902f6dc77e80ddd01b2382ef21feb20995a3`  
		Last Modified: Thu, 27 Feb 2025 19:14:02 GMT  
		Size: 48.9 MB (48940988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3cdfa6c2d81cac77d91e0a9a4695bf55e598bf856c23429740c313a4907129`  
		Last Modified: Thu, 27 Feb 2025 19:13:57 GMT  
		Size: 92.7 KB (92729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
