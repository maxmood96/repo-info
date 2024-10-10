## `eclipse-temurin:8-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:cfeb4c007ec8d53c2eeb83718e59512b91281f2803cd83caab08bf3649dbea57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `eclipse-temurin:8-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:1068ec19b8ea6f7e4c3aaf27c2d2e342d446bc9c2060596fb59ef3acef9f5152
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.2 MB (222206284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31f12ded867702cc82d143e20aa213b03f866fec740785fc95118b1550188a0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Thu, 10 Oct 2024 00:11:44 GMT
SHELL [cmd /s /c]
# Thu, 10 Oct 2024 00:11:45 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 10 Oct 2024 00:11:46 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 10 Oct 2024 00:11:47 GMT
USER ContainerAdministrator
# Thu, 10 Oct 2024 00:12:01 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 10 Oct 2024 00:12:01 GMT
USER ContainerUser
# Thu, 10 Oct 2024 00:12:11 GMT
COPY dir:cf98fec7e439356342f3bf03fb67b0dac0e213296a20d5e427a9ebba9080193e in C:\openjdk-8 
# Thu, 10 Oct 2024 00:12:27 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96818114ce85fcf68e8af61951767bf11ed374ffe6a9023b6150122fbad46d51`  
		Last Modified: Thu, 10 Oct 2024 00:32:47 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702dd5af34f5a288dc9f423ce99dc45f825e5908a5abd9751b25875f6d11356c`  
		Last Modified: Thu, 10 Oct 2024 00:32:47 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e73b3fbec6ab963baeaf37902cf7c4cded0dd4140d7cd8304507e705b4885cc`  
		Last Modified: Thu, 10 Oct 2024 00:32:47 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e01992d787cd675fe8027e387b62953278cc86f9ff2848c3f5caf257ef8247`  
		Last Modified: Thu, 10 Oct 2024 00:32:45 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b3a5e8c630fbee27654249fdc4ab04572b3db9697412f448e3318b2a6f4b0a`  
		Last Modified: Thu, 10 Oct 2024 00:32:45 GMT  
		Size: 83.7 KB (83726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f39cd6234ef7bb6fab55d144f75a01753b9f32029fb9de2ef237ff22cbcd4b`  
		Last Modified: Thu, 10 Oct 2024 00:32:45 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e6ebc939ffe256c19a1699cf7ed03562fcce92c6629609c824ddc405b522a8`  
		Last Modified: Thu, 10 Oct 2024 00:32:57 GMT  
		Size: 101.5 MB (101546736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef1e886f74cd79ec9cfe09f09d6791e4ee19561724e8e5fbf2d43fa1cb46902`  
		Last Modified: Thu, 10 Oct 2024 00:32:45 GMT  
		Size: 59.1 KB (59052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
