## `eclipse-temurin:25-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:2100e79c68488a5e127402cc3ded0997badd498609e906dcef857828ad2537d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `eclipse-temurin:25-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull eclipse-temurin@sha256:f14756b170121792a153266c696d67d2d310eaf059844c093a1947373effb289
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264491486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a95ded23a71cb078ec0b77ffb1abff8fe83a05a4c70e65edc82d98824f590c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 11 Nov 2025 20:11:06 GMT
SHELL [cmd /s /c]
# Tue, 11 Nov 2025 20:12:09 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Tue, 11 Nov 2025 20:12:09 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 11 Nov 2025 20:12:09 GMT
USER ContainerAdministrator
# Tue, 11 Nov 2025 20:12:11 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 11 Nov 2025 20:12:11 GMT
USER ContainerUser
# Tue, 11 Nov 2025 20:12:17 GMT
COPY dir:889642903e29f32ff0f0b6da5f64cf6a40ecfa6d85d0926e4981ccbc885ac0c0 in C:\openjdk-25 
# Tue, 11 Nov 2025 20:12:22 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 11 Nov 2025 20:12:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97be436214312a6298d6bd952225e6bd6e31ec3de7e85f7960b99f405d5e9ff8`  
		Last Modified: Tue, 11 Nov 2025 20:11:46 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75baa262cdf21dbf64eefb935fcfdc6757debdcaceeb24bfbcc94e3699dd21c`  
		Last Modified: Tue, 11 Nov 2025 20:12:49 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03dc38bcfc05e72df903aa7d0a52ad8cdf1ec9f694d0ffdc3e19f64d176b551a`  
		Last Modified: Tue, 11 Nov 2025 20:12:50 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49fbd3f18e59b9260f716d8d36046362deea2170f48090d242da34d9c6d723e1`  
		Last Modified: Tue, 11 Nov 2025 20:12:51 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac10aa3c5aaa55a203b4d785f9835d53f0c1d7eec8a2a8579f25aeda820619c`  
		Last Modified: Tue, 11 Nov 2025 20:12:51 GMT  
		Size: 77.0 KB (77045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bafe50eeb05fd73b3b9a13031c8d850cfc514cd8bfb6e641e338bec937841f`  
		Last Modified: Tue, 11 Nov 2025 20:12:50 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c270b5d746c2bdf6a4a7bc8b0378e392059d4ccaf1b99c707e0a8218864379`  
		Last Modified: Tue, 11 Nov 2025 22:18:32 GMT  
		Size: 138.0 MB (137952141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeced0e9b998bc4b064fe8759862563f6b12f710d82df0e6d4ec909602335941`  
		Last Modified: Tue, 11 Nov 2025 20:12:51 GMT  
		Size: 106.9 KB (106899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f44e31589ce3b3643d2c45433c356d76d835e726ed7cfc12d27960c787150d`  
		Last Modified: Tue, 11 Nov 2025 20:12:52 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
