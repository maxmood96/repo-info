## `eclipse-temurin:17-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:498550f57ac19f7023561f9ae076f1d5a559bb8ac43b78bb7180d6df605be974
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `eclipse-temurin:17-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull eclipse-temurin@sha256:15c541b91b249049df2179c267fd27e49369c5169dfdcf36dc6b9e9343faa3fe
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.0 MB (310026471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f651dbc604d50268b39f203a21abe88fbceccaae477eb93d586effa13f1b609a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Wed, 23 Apr 2025 17:13:57 GMT
SHELL [cmd /s /c]
# Wed, 23 Apr 2025 17:13:58 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 17:13:59 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 23 Apr 2025 17:14:00 GMT
USER ContainerAdministrator
# Wed, 23 Apr 2025 17:14:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 23 Apr 2025 17:14:07 GMT
USER ContainerUser
# Wed, 23 Apr 2025 17:14:14 GMT
COPY dir:642284f27aa03ba1e21a689edd99e2d493ba3e3290e848ff1bdf623fc783a5e1 in C:\openjdk-17 
# Wed, 23 Apr 2025 17:14:19 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 23 Apr 2025 17:14:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Wed, 16 Apr 2025 23:30:29 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78ce9d306720ddd26a2b05036f059e1721b777b68208ecdb5aba3925a93956a`  
		Last Modified: Wed, 23 Apr 2025 17:14:26 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c813c96db31c71ccc051b8501e093bbbae9bfe3c6429ba7229e1e597b6e07a1`  
		Last Modified: Wed, 23 Apr 2025 17:14:26 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc970e146571387f437c074e8a9986c19a909ce7b87435cf0f3bb2bab9df6c7`  
		Last Modified: Wed, 23 Apr 2025 17:14:26 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a3f8ee7bec665b3cb98fcc14822e03d952ffa4a48a20c474666ab908c4ecc1`  
		Last Modified: Wed, 23 Apr 2025 17:14:26 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c905276405d0281414aa38d4aea04da0ba4a98014d1900b9fddfe34203a68c`  
		Last Modified: Wed, 23 Apr 2025 17:14:24 GMT  
		Size: 72.8 KB (72764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247bc36e8f84863f7e08fa114d31154215f83becbc0168f819e8a927762649c1`  
		Last Modified: Wed, 23 Apr 2025 17:14:24 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fa4e9ddd67fd5af83fa5be9db4639d5e06845b2c9945b762780a648f591bd2`  
		Last Modified: Wed, 23 Apr 2025 17:14:34 GMT  
		Size: 187.3 MB (187308640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f09f9aea927374c39a5682a5dc2d1153b068301fdb151ae42d2ef28a4f3c7a5`  
		Last Modified: Wed, 23 Apr 2025 17:14:24 GMT  
		Size: 99.8 KB (99806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe2070e4ba58ce99d2682ed31137488be9d14cb6d8e331df7e1ba7bb6ee56a7d`  
		Last Modified: Wed, 23 Apr 2025 17:14:24 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
