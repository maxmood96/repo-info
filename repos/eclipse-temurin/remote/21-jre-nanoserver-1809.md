## `eclipse-temurin:21-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:19b38a2c3a3567b54ca5456c20f13dbad101424f55c61c286b2f12a3688199df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:21-jre-nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:bc43400a26f930ea5a1df1519b52fe15e128c21ae7c601daa790de0f9b2cd27d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.6 MB (207630815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a24355889b0c090d29d18fb02f0c5423ec496aa5652cf935bc366c6517c1b1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Fri, 31 Jan 2025 02:11:48 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 02:11:49 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Fri, 31 Jan 2025 02:11:50 GMT
ENV JAVA_HOME=C:\openjdk-21
# Fri, 31 Jan 2025 02:11:51 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 02:12:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 02:12:13 GMT
USER ContainerUser
# Fri, 31 Jan 2025 02:12:19 GMT
COPY dir:c0b7c132c85049081486a93cd76fe016c559b0b921796f63592a768b082ae9e2 in C:\openjdk-21 
# Fri, 31 Jan 2025 02:12:25 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Wed, 15 Jan 2025 07:23:16 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9de0d6fb318b484f1507e0606e0e335c4396b1766edda9259e1018fa1e13bd`  
		Last Modified: Fri, 31 Jan 2025 02:12:28 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d504fc50040de4c72c4827d51d953e1f5f9186d41483f63ea53b96055d1c0e4`  
		Last Modified: Fri, 31 Jan 2025 02:12:28 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b16540955ba67a65b63670b38aca47fbe442022e6013463f524461457a8631b`  
		Last Modified: Fri, 31 Jan 2025 02:12:28 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91d8f2b3311232dc8c21c77ff05e3eee0abfdf92ea5ff8060c4e1ff2e7b4002`  
		Last Modified: Fri, 31 Jan 2025 02:12:27 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c317acb0bd01440e96f66ee91a9e1ccd59b9a25cc10bf5978adddc267f32e10`  
		Last Modified: Fri, 31 Jan 2025 02:12:27 GMT  
		Size: 66.7 KB (66698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120fc00ee09587fae82a6c1d3a627b99f3434e560189256e82a36ff39ee6af0b`  
		Last Modified: Fri, 31 Jan 2025 02:12:27 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d72c126310a190a9cb58ab57e7e5f1ba5d111d9356172b414396ed3ef2b4e56`  
		Last Modified: Fri, 31 Jan 2025 02:12:32 GMT  
		Size: 48.9 MB (48941211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278ae673cca28af8aebe7531469df1e1531603b5a4d2ad73b2a167ad8077d6f9`  
		Last Modified: Fri, 31 Jan 2025 02:12:28 GMT  
		Size: 3.3 MB (3349921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
