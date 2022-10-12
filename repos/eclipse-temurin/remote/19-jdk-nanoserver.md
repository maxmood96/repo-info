## `eclipse-temurin:19-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:6da35acb2675e1bed53cd054043ea7a278d88a61c2c82b4f811ea99f5f6963e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1129; amd64
	-	windows version 10.0.17763.3532; amd64

### `eclipse-temurin:19-jdk-nanoserver` - windows version 10.0.20348.1129; amd64

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

### `eclipse-temurin:19-jdk-nanoserver` - windows version 10.0.17763.3532; amd64

```console
$ docker pull eclipse-temurin@sha256:1c153b382c8e785b7429c1dd730e35bce9b09cda61bf3e1ead0c9fdf03d22943
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 MB (300347112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bf851b1af77b360a4b0e6b630e25a520f3b06ebf2fc956888b90e8dd3d4aa9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Wed, 12 Oct 2022 15:20:49 GMT
SHELL [cmd /s /c]
# Wed, 12 Oct 2022 15:49:40 GMT
ENV JAVA_VERSION=jdk-19+36
# Wed, 12 Oct 2022 15:49:40 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 12 Oct 2022 15:49:41 GMT
USER ContainerAdministrator
# Wed, 12 Oct 2022 15:49:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Oct 2022 15:49:50 GMT
USER ContainerUser
# Wed, 12 Oct 2022 15:50:04 GMT
COPY dir:f9e4978cc3e169a38f06094f4d9bd0ec177b4256ff40cd3387fc1d393235d05c in C:\openjdk-19 
# Wed, 12 Oct 2022 15:50:16 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Oct 2022 15:50:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5ead999142ecce15e02523c49706a633fa708374d94bb65a254e3a3c117d609b`  
		Size: 103.4 MB (103377244 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4a6a667d76c19fca171390d60fb90c40e16c777050e943a7fe17ad7686841f0f`  
		Last Modified: Wed, 12 Oct 2022 16:02:59 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30097ca6d1d1e22585cebbc642cd4ef89dd3e2b6099e607d6273094d02e4390`  
		Last Modified: Wed, 12 Oct 2022 16:11:20 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e93472d5cae1a3796bc8611a28845b93f3fbd8ce1227629553340262f85530`  
		Last Modified: Wed, 12 Oct 2022 16:11:20 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaef6dce2ef28ca7e9d90ec78acf76ecd1b44bddc4483980ef93b559485616ae`  
		Last Modified: Wed, 12 Oct 2022 16:11:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab5cb4797cf8a3306503f588c34ee6b45e7c5568de6072b49e61368d6ce76cd`  
		Last Modified: Wed, 12 Oct 2022 16:11:18 GMT  
		Size: 68.3 KB (68329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17b04d0489735abb2f8e7028d93ec2ce99c5797854147065d2a8ee6f970e8cc`  
		Last Modified: Wed, 12 Oct 2022 16:11:18 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065ce5e707589d3792787c9210b36ca33ee8af3da4a4139d3649169bd96811e5`  
		Last Modified: Wed, 12 Oct 2022 16:11:38 GMT  
		Size: 193.2 MB (193177021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f00ca5f4e5f211b98bf596d36dca78cb5fc7947f6851cd1138001ca168628a7`  
		Last Modified: Wed, 12 Oct 2022 16:11:19 GMT  
		Size: 3.7 MB (3717542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5bcc253034205aa6751bd76983b55e9be9a32a0e9b1898151b3594933106e0e`  
		Last Modified: Wed, 12 Oct 2022 16:11:18 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
