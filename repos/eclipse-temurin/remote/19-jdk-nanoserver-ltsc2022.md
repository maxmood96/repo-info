## `eclipse-temurin:19-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:0d191657390ee0f8851f633317480404ed6aa57fe40f2c1271385a5be9ef9176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1129; amd64

### `eclipse-temurin:19-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.1129; amd64

```console
$ docker pull eclipse-temurin@sha256:2e9920fdec416d28bc814092abf3fab8d6ec7f7c75fb59ec3c3bc92061d0bfbe
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.6 MB (311557981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:335067bcb7a4d834586c92bcd343034d242e583ccf3a480ed46c0d93c73136fa`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Oct 2022 21:37:41 GMT
RUN Apply image 10.0.20348.1129
# Wed, 12 Oct 2022 15:54:21 GMT
SHELL [cmd /s /c]
# Wed, 12 Oct 2022 15:58:19 GMT
ENV JAVA_VERSION=jdk-19+36
# Wed, 12 Oct 2022 15:58:20 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 12 Oct 2022 15:58:21 GMT
USER ContainerAdministrator
# Wed, 12 Oct 2022 15:58:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Oct 2022 15:58:31 GMT
USER ContainerUser
# Wed, 12 Oct 2022 15:58:46 GMT
COPY dir:f9e4978cc3e169a38f06094f4d9bd0ec177b4256ff40cd3387fc1d393235d05c in C:\openjdk-19 
# Wed, 12 Oct 2022 15:59:01 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Oct 2022 15:59:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:38fa349577729651ac1fc3ec785f908719a8100da5f5ba9bd3f549411061f583`  
		Size: 118.2 MB (118202895 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e0ed0041e3584df1952980c3f73fd2b6e154328c7a0165f37dbe92ef94ae8a95`  
		Last Modified: Wed, 12 Oct 2022 16:12:53 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6600c5961e588d1043da5291c8ff4ae24eb763a46b37646c7eed3595563cb7`  
		Last Modified: Wed, 12 Oct 2022 16:15:13 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aea4aed78ddd1a041967cfed00e5d1b62a44f502cdefc523c6f065215e984df`  
		Last Modified: Wed, 12 Oct 2022 16:15:13 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c75b72fa9bce3569f8c2c8b26da3d331bebf435a9dea945d5bee6c78731c256`  
		Last Modified: Wed, 12 Oct 2022 16:15:13 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2381ef0d8a47f6f87b637d450f7053ce3f57cf77ae3109708410d404cce34c01`  
		Last Modified: Wed, 12 Oct 2022 16:15:10 GMT  
		Size: 85.1 KB (85058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0291d1068cddc207235531c946aa2b96927e6fb63cd4f124d88e26ab4d83e0eb`  
		Last Modified: Wed, 12 Oct 2022 16:15:10 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47da0def6c5672f3b3484dbc10eeb54547b6ef8e3a1ee4e9c4f117bcbf588c61`  
		Last Modified: Wed, 12 Oct 2022 16:15:31 GMT  
		Size: 193.2 MB (193171857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb862559520a3d37dcc3ea02684c14c3b11d2350c0668381c008e99c8e39efc5`  
		Last Modified: Wed, 12 Oct 2022 16:15:10 GMT  
		Size: 91.3 KB (91299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680b7cd05654350f8ab7e5655445394496fddaee8b044b88300c22d50f7969e7`  
		Last Modified: Wed, 12 Oct 2022 16:15:10 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
