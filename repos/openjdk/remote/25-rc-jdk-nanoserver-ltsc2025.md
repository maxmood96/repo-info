## `openjdk:25-rc-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:e423ec09f5d402d2ba3c49bd694db49a888123f776c63b5f48aaefc577b53d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `openjdk:25-rc-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull openjdk@sha256:4ba9345c07f8988a96dbfe8768b3fd2d127e8e29095221132b2340473e6871a1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.2 MB (412217730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7a3a18b1f6ba4607314c190a2962f473401403895a2e5cf7bda842dc71e579`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 Aug 2025 02:44:20 GMT
RUN Apply image 10.0.26100.4946
# Mon, 18 Aug 2025 19:13:05 GMT
SHELL [cmd /s /c]
# Mon, 18 Aug 2025 19:13:05 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 18 Aug 2025 19:13:05 GMT
USER ContainerAdministrator
# Mon, 18 Aug 2025 19:13:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 18 Aug 2025 19:13:08 GMT
USER ContainerUser
# Mon, 18 Aug 2025 19:13:08 GMT
ENV JAVA_VERSION=25
# Mon, 18 Aug 2025 19:13:14 GMT
COPY dir:72a77cd8dd8fd9224e7c68e3876c18f0a900359f2fadd93c9163ab7d4997de07 in C:\openjdk-25 
# Mon, 18 Aug 2025 19:13:17 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 18 Aug 2025 19:13:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6d63d98dae9e3419e8c965c24a11d30e40947cf35ee17c204c5d8b7bae7ff2ef`  
		Last Modified: Tue, 12 Aug 2025 21:13:38 GMT  
		Size: 193.5 MB (193469373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0221ac58abc503b742be752747e7b01ff3069fcc200826abf3d5ec4e827dceac`  
		Last Modified: Mon, 18 Aug 2025 19:14:01 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367d824426a232d61f2fcbcf139f8be28c638bbb1ea80ad4cdf677ccf52238d5`  
		Last Modified: Mon, 18 Aug 2025 19:14:02 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60a130b0ea86e2a4a9743c3a926274961e171890f3293970977c52ed3261c41`  
		Last Modified: Mon, 18 Aug 2025 19:14:01 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10efc14e4d466d196473f0cae1610033d9e2e52e94e4b08a0dad16dc6fed988`  
		Last Modified: Mon, 18 Aug 2025 19:14:03 GMT  
		Size: 75.7 KB (75679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe307594353a94e2658232447ff4d9236cd8538f22e394d0c72491723ce3c44`  
		Last Modified: Mon, 18 Aug 2025 19:14:02 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d31f6cf2e305acfab2e2cf24299f6e0fcc1e2a5155c0e1063011e01fefaa3618`  
		Last Modified: Mon, 18 Aug 2025 19:14:04 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5f5b5d6bc1ed90f1d449c4d7e94a7f0f7cdbd1e872849dc19aa33f447d3d9e`  
		Last Modified: Mon, 18 Aug 2025 21:24:03 GMT  
		Size: 218.6 MB (218553034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d3f747e5a2f4f2df6eacb6e62ffa1ca487a7c2f0eeb22002e3979917b4ec824`  
		Last Modified: Mon, 18 Aug 2025 19:14:05 GMT  
		Size: 113.4 KB (113356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c5d0e50e7149bac07d4c3bf9e981dd95e306aca43d2721c4608932d1c3687c`  
		Last Modified: Mon, 18 Aug 2025 19:14:05 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
