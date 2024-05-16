## `openjdk:23-ea-22-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:1c53f9885eb735db8fd0c0b1e5fd9fee445a3db558c9f376493c33e6dc051fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `openjdk:23-ea-22-jdk-nanoserver-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull openjdk@sha256:fbceeac6053472208d2ff5cce5e74e7e68e0491ade49aef467b6dd749b778b9f
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.3 MB (364333848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4bb9affd57ce27e6ab784fe39eeadd0bf49da8dce03951fafbc648e59631f3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 22:52:59 GMT
SHELL [cmd /s /c]
# Wed, 15 May 2024 22:53:00 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 15 May 2024 22:53:00 GMT
USER ContainerAdministrator
# Wed, 15 May 2024 22:53:11 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 15 May 2024 22:53:11 GMT
USER ContainerUser
# Wed, 15 May 2024 22:53:12 GMT
ENV JAVA_VERSION=23-ea+22
# Wed, 15 May 2024 22:53:21 GMT
COPY dir:7b3c1c136106da79beeeffd37c21e2a06ca76287054566b14288aed4c2dc0808 in C:\openjdk-23 
# Wed, 15 May 2024 22:53:33 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 15 May 2024 22:53:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4b566ba2721a31216cff10e8828691e37922ef366a2ad54498bfc64138af20`  
		Last Modified: Wed, 15 May 2024 22:53:38 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf4ff2fb771930318c88dd727153d31ab2ab31bdc64384fc73f36260703a9b2`  
		Last Modified: Wed, 15 May 2024 22:53:37 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a79026d7d009d9d5b76b6348a6364d66afd8414da35e1bafa4af49bf0aa4279`  
		Last Modified: Wed, 15 May 2024 22:53:37 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c987f25b823fb8402ed78d357f0a191b34ad45ef3dd98f992ef5024c1bbf0c6c`  
		Last Modified: Wed, 15 May 2024 22:53:37 GMT  
		Size: 67.3 KB (67346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7b7d54b8f152568d658b562e16346b7cc9ef46812ab09c0761600236d3521f`  
		Last Modified: Wed, 15 May 2024 22:53:36 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca9809b46908e0086acd1b61fdf8562ea517cd334956b52f9ee5012df695c05`  
		Last Modified: Wed, 15 May 2024 22:53:36 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f8225b04182fd86fc559cf60d27adcf61a046bc49e4a0430448fa4939e0480`  
		Last Modified: Wed, 15 May 2024 22:53:47 GMT  
		Size: 204.4 MB (204409172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f6bb345e9dfda524692d1263226a68798a299380b3f8324accb5a3f5e6ede5d`  
		Last Modified: Wed, 15 May 2024 22:53:37 GMT  
		Size: 4.9 MB (4909741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1f1a7b379ce25e755cf4ab62ab4504fb2a390091e7082b1b885d29186a0947`  
		Last Modified: Wed, 15 May 2024 22:53:36 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
