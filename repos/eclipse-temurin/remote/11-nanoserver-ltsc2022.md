## `eclipse-temurin:11-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:7f38a7f5533fa2df62b303472866541605450964bb909830c34197eaa6b55073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1607; amd64

### `eclipse-temurin:11-nanoserver-ltsc2022` - windows version 10.0.20348.1607; amd64

```console
$ docker pull eclipse-temurin@sha256:4a37d7b863444408ac30c91f4c5dc29351b2ba77a0e3546f13af234b90e4b6a1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.2 MB (315223029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ede6b401ade0eb23968c1f8017c58b6e4167f6f6ccaf0269f330ca702acd503`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 10 Mar 2023 06:31:34 GMT
RUN Apply image 10.0.20348.1607
# Thu, 16 Mar 2023 01:29:33 GMT
SHELL [cmd /s /c]
# Thu, 16 Mar 2023 01:31:36 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 16 Mar 2023 01:31:37 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 16 Mar 2023 01:31:37 GMT
USER ContainerAdministrator
# Thu, 16 Mar 2023 01:31:50 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 16 Mar 2023 01:31:51 GMT
USER ContainerUser
# Thu, 16 Mar 2023 01:32:07 GMT
COPY dir:3631bd3b4ae70db635b51d6f7ad3f3254aa758db5b0d079379d506c898ecba14 in C:\openjdk-11 
# Thu, 16 Mar 2023 01:32:38 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 01:32:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7abf0a70d48bf65f3d985f5780d4bdaece36f1f4bb8be10d5a6aacce33dacc75`  
		Last Modified: Thu, 16 Mar 2023 01:54:24 GMT  
		Size: 122.2 MB (122171731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a611a20686e9374e3a55a49399506f83c041ae711ed47018c2267c341156dd97`  
		Last Modified: Thu, 16 Mar 2023 01:53:50 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34dda0a3c258027bfdb890bbcc59b5303cf3031bc873b4df33a4507d609728e8`  
		Last Modified: Thu, 16 Mar 2023 01:54:55 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc4a9fded480c4566213f84794548301ce650626bf9383606dea182743fc055`  
		Last Modified: Thu, 16 Mar 2023 01:54:54 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e90f6ebc0e7a1169e9642c5c4ccc9cd40efcfd9780eb5fc1a200f1a25515dd`  
		Last Modified: Thu, 16 Mar 2023 01:54:55 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b7161ca4c60d5109587475052f91d31dbab1302644455f6e96bfb4167f3b91`  
		Last Modified: Thu, 16 Mar 2023 01:54:52 GMT  
		Size: 81.6 KB (81594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f083ff53e043d6f96641b7f3cc16229c1a4cd188409bd143ad3bfce61271bad`  
		Last Modified: Thu, 16 Mar 2023 01:54:52 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21448cd7ed4bb0dfef2d651fbc5bc6791b47a46bc185055a1fa2d45865484944`  
		Last Modified: Thu, 16 Mar 2023 01:55:14 GMT  
		Size: 192.9 MB (192899953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05b47c710c65cd42762a9194df783fbe2432d6673fd343067611b3836053f32`  
		Last Modified: Thu, 16 Mar 2023 01:54:53 GMT  
		Size: 62.8 KB (62789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f9aaacc0060d205fd5ac50dbab0560adee5d91cf4a76a87a2ec3c1f58a940a`  
		Last Modified: Thu, 16 Mar 2023 01:54:52 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
