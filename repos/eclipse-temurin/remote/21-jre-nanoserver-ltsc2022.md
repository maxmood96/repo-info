## `eclipse-temurin:21-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:292951f705cb17743a75cc221cec5e13ca323e33cee3be65e64228a3fd81c2c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `eclipse-temurin:21-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull eclipse-temurin@sha256:de6552fc2dde06597368dc047fb1b04a0e2d6916cfae80e5a4896528ddd23faf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171674776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b66a021659654e917c5b6c3473f851bfd9e7ffd98d6b25de2f502eccfc726b64`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Wed, 23 Apr 2025 17:14:03 GMT
SHELL [cmd /s /c]
# Wed, 23 Apr 2025 17:14:03 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 17:14:04 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 23 Apr 2025 17:14:05 GMT
USER ContainerAdministrator
# Wed, 23 Apr 2025 17:14:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 23 Apr 2025 17:14:08 GMT
USER ContainerUser
# Wed, 23 Apr 2025 17:14:12 GMT
COPY dir:e77a568eefeac18db14cfb92f416dab13c56713fa78f747642b83f8e2eb5149f in C:\openjdk-21 
# Wed, 23 Apr 2025 17:14:16 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Wed, 16 Apr 2025 23:30:29 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bfa7e86698e5ad41a678f521098c6e24b8a2014deb19ce156054499e26dfe52`  
		Last Modified: Wed, 23 Apr 2025 17:14:23 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbff0a07cb32994a9adb730468ddaadbf95f6b2ce8c0c31d9c0d258751b64510`  
		Last Modified: Wed, 23 Apr 2025 17:14:22 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ef1ab0a7a8787895002057a9dec406c258b72ee2c4f3305bc240c659227b1d`  
		Last Modified: Wed, 23 Apr 2025 17:14:22 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d850fac08e87f648c6e88500e5347de972ec84647452a5586691d1e743c507`  
		Last Modified: Wed, 23 Apr 2025 17:14:20 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae1f5a624034dee1b31eb9e8d76c6bd97e89ee9b0d29644a4a2c4435474d007`  
		Last Modified: Wed, 23 Apr 2025 17:14:21 GMT  
		Size: 77.1 KB (77140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1bd502903f313b84a35f550eb4f0659d0d19315edbc96e7ccae2d6d6adf63be`  
		Last Modified: Wed, 23 Apr 2025 17:14:20 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17225d900fda94cc39f871ca3ec819e0785cd4b737919f325116d8cd3e0cf0d7`  
		Last Modified: Wed, 23 Apr 2025 17:14:26 GMT  
		Size: 48.9 MB (48944563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d63528ae47367e98a3f1d02dd332fa0790b3beea75320da485ac15090ba9160`  
		Last Modified: Wed, 23 Apr 2025 17:14:21 GMT  
		Size: 108.8 KB (108842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
