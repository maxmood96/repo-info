## `eclipse-temurin:11-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:1d353d7a2b690b4860d8059d0438d1c47fb22ea5274b4599256d2b62fc5a030b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1129; amd64

### `eclipse-temurin:11-nanoserver-ltsc2022` - windows version 10.0.20348.1129; amd64

```console
$ docker pull eclipse-temurin@sha256:781459cd502c0e8cef9b1d61689de3e931852379e4f847259203b27661533fe0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 MB (310719905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932e9861f3f70a574c00334871bd7100a0dba3237cd2c4936ea4cf17280766ad`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Oct 2022 21:37:41 GMT
RUN Apply image 10.0.20348.1129
# Wed, 12 Oct 2022 15:54:21 GMT
SHELL [cmd /s /c]
# Wed, 12 Oct 2022 15:55:36 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Wed, 12 Oct 2022 15:55:37 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 12 Oct 2022 15:55:38 GMT
USER ContainerAdministrator
# Wed, 12 Oct 2022 15:55:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Oct 2022 15:55:47 GMT
USER ContainerUser
# Wed, 12 Oct 2022 15:56:02 GMT
COPY dir:b7b3112beefc8be2dd5c6a3897a52ba756c9a344294f20db387fa022b341211c in C:\openjdk-11 
# Wed, 12 Oct 2022 15:56:17 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Oct 2022 15:56:18 GMT
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
	-	`sha256:66ab62c13bec3daa2374e11924aff5844b58c17b97bf040906ea46e9d87126a5`  
		Last Modified: Wed, 12 Oct 2022 16:13:33 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37bbee8665c328438506c0329be6a2cc1854075fe5e2801d0b3c952b998a9107`  
		Last Modified: Wed, 12 Oct 2022 16:13:33 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e66cbf95270899e6f6482b57a9938446196777f75df9ac4cba512c6ea10d0d5`  
		Last Modified: Wed, 12 Oct 2022 16:13:33 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faaf96570d1a87f06ff0a504d54b541e39782a17fc7c2fcb2545ef8f313a85b1`  
		Last Modified: Wed, 12 Oct 2022 16:13:30 GMT  
		Size: 80.4 KB (80425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c27c4f4546488e95308e2f98edae9e1b084f46a560454acb4c4c5a273afc66`  
		Last Modified: Wed, 12 Oct 2022 16:13:30 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f57e586089176b925c61fdf7ddb8229d60060842b5762a9a7f73bc71272e2f`  
		Last Modified: Wed, 12 Oct 2022 16:13:50 GMT  
		Size: 192.4 MB (192371199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292733ed4e62156152c10c0b889a9bb54c8a436c14dfd70a9d8317d58be447d4`  
		Last Modified: Wed, 12 Oct 2022 16:13:31 GMT  
		Size: 58.5 KB (58480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1c3404ce93585ea8d9ff56acc00485e9b5d83057ef220d46fd03e673dacf70`  
		Last Modified: Wed, 12 Oct 2022 16:13:31 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
