## `eclipse-temurin:17-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:1665d9d8fe84b3ee8970fc2155ab7d4b963b9655f37410bfb892904dc7604eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `eclipse-temurin:17-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull eclipse-temurin@sha256:d502093ef095ef76a08b1f1503df3b8eba73a3596d5c892fa8351d0411b24034
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.4 MB (314397880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e3ca069984ca63e52cb60c2a230b21a22a87042d8ac373a42816534be3b6c1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Thu, 05 Feb 2026 22:39:36 GMT
SHELL [cmd /s /c]
# Thu, 05 Feb 2026 22:39:36 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Thu, 05 Feb 2026 22:39:37 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 05 Feb 2026 22:39:37 GMT
USER ContainerAdministrator
# Thu, 05 Feb 2026 22:39:41 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 05 Feb 2026 22:39:41 GMT
USER ContainerUser
# Thu, 05 Feb 2026 22:40:01 GMT
COPY dir:fb23a79434a3e7defa51a1bec1a7ef896ff849f7ba85f2629e1913957db57a2e in C:\openjdk-17 
# Thu, 05 Feb 2026 22:40:06 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 05 Feb 2026 22:40:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76641f9daa2d5f53c0a9fac3dc6cce16a489305e65371bf2ae2c47def131bcf6`  
		Last Modified: Thu, 05 Feb 2026 22:40:13 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b02ee63adef873cc1e4ee635334739f4d1bfd4b39b7b6d67d709b3b8af04a9c`  
		Last Modified: Thu, 05 Feb 2026 22:40:13 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b03646964c9434e116d96734b6526532135e3c0e7a277ae3772ec9a77fd1c2f`  
		Last Modified: Thu, 05 Feb 2026 22:40:12 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd6f4c8a12f97d924acdc2f5bd1b93f318b59d6f08ca6f0ff5c1531db1539081`  
		Last Modified: Thu, 05 Feb 2026 22:40:12 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44415dd5663ecfb0a19eb41d5144dd43705f0f0ba5c4d0b635e51611c38fdaf5`  
		Last Modified: Thu, 05 Feb 2026 22:40:11 GMT  
		Size: 71.5 KB (71489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d962b59368672ed783c2c0924751c5c3795543e7419b1002b67e26d0bbc28185`  
		Last Modified: Thu, 05 Feb 2026 22:40:11 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282c9d8ee3544f02dfc7f7ddb15311edbca154f369be9d3fa80854e08d64ba11`  
		Last Modified: Thu, 05 Feb 2026 22:40:24 GMT  
		Size: 187.5 MB (187486597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad364bb30579e7bba20046f512f3f376732e33d304ee4ac7b350e25e840a9c2`  
		Last Modified: Thu, 05 Feb 2026 22:40:11 GMT  
		Size: 136.6 KB (136595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28bad7d714e25c51b49e00054c6e3c76a3a6c58988940e515b7d33db4a15843`  
		Last Modified: Thu, 05 Feb 2026 22:40:11 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
