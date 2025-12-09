## `eclipse-temurin:25-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:e079f9c4d2442b364ca0f655812fa17c6fdcfe235965a322ee6200dd4e2401f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `eclipse-temurin:25-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull eclipse-temurin@sha256:2fdbb70dd061d874fdf722b46630bf50874b6232a3f692a555b698348596e281
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264503706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0695ffceb12cdd193f8c7bb853fe8d7645013cd4e1b57826239294ccbece9535`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 09 Dec 2025 21:12:46 GMT
SHELL [cmd /s /c]
# Tue, 09 Dec 2025 21:13:22 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Tue, 09 Dec 2025 21:13:23 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 09 Dec 2025 21:13:23 GMT
USER ContainerAdministrator
# Tue, 09 Dec 2025 21:13:25 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Dec 2025 21:13:25 GMT
USER ContainerUser
# Tue, 09 Dec 2025 21:14:15 GMT
COPY dir:889642903e29f32ff0f0b6da5f64cf6a40ecfa6d85d0926e4981ccbc885ac0c0 in C:\openjdk-25 
# Tue, 09 Dec 2025 21:14:19 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 09 Dec 2025 21:14:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7870d3a44198dbb615532c3d59d7e87b8da8857e8ce6472008152cd114373be6`  
		Last Modified: Tue, 09 Dec 2025 21:13:11 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfca3db2b6d8c751de1c057e4cb9412f3b83f501541bb58b72f70aba8a6c4ce`  
		Last Modified: Tue, 09 Dec 2025 21:14:46 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7303dab28fbf7a2c09b3870b5c863e7d1802c0d13b0aca1b8f5c0d699996b4f4`  
		Last Modified: Tue, 09 Dec 2025 21:14:46 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2ef1d534905cb9cae1ba330997663b80067a86bbe5650ce5f659c721f46f3e`  
		Last Modified: Tue, 09 Dec 2025 21:14:46 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0add70c3e99511a3a051355918450667dbb61b5422ba039b53d6d1ac97734240`  
		Last Modified: Tue, 09 Dec 2025 21:14:46 GMT  
		Size: 78.8 KB (78812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea2015205d244c634b6776088b40787f607e621a090b6dfec798817b5c7b16a`  
		Last Modified: Tue, 09 Dec 2025 21:14:46 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da774cc8f033ba5595553170e3f9ffa26468b3e40301fd676286fcceea32ea0`  
		Last Modified: Tue, 09 Dec 2025 22:17:22 GMT  
		Size: 138.0 MB (137951635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b36cbd30f9d7a60f4efe03e11c4909c5b952cde1cdb33c3951b6b0a5162fbfa`  
		Last Modified: Tue, 09 Dec 2025 21:14:46 GMT  
		Size: 108.5 KB (108538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5bb8ef7067a2b029799befd530769991b420e8122226af2eaaac038169d205`  
		Last Modified: Tue, 09 Dec 2025 21:14:46 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
