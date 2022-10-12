## `eclipse-temurin:11-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:fc0abdac6423795488bc6a92672472323fdb182011b9c5ec6841c24c4c684468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1129; amd64
	-	windows version 10.0.17763.3532; amd64

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.20348.1129; amd64

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

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.17763.3532; amd64

```console
$ docker pull eclipse-temurin@sha256:ff6a6440efb7505f2802836fd249eeb1c362ad686fe8f6fb2938dd05018e1672
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295932990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb6995410e3200341691fce8c41f5a1955f455f374fb45180b7bd101aaa8cb4e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Wed, 12 Oct 2022 15:20:49 GMT
SHELL [cmd /s /c]
# Wed, 12 Oct 2022 15:31:01 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Wed, 12 Oct 2022 15:31:01 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 12 Oct 2022 15:31:02 GMT
USER ContainerAdministrator
# Wed, 12 Oct 2022 15:31:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Oct 2022 15:31:15 GMT
USER ContainerUser
# Wed, 12 Oct 2022 15:31:29 GMT
COPY dir:b7b3112beefc8be2dd5c6a3897a52ba756c9a344294f20db387fa022b341211c in C:\openjdk-11 
# Wed, 12 Oct 2022 15:31:43 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Oct 2022 15:31:44 GMT
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
	-	`sha256:95a5b3e1e569bda6c7c0f790d1a667813abefc5cae113d210ec6205941111d2e`  
		Last Modified: Wed, 12 Oct 2022 16:05:35 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde07e341e8acc4b8b07533e6d42bbc3dfa2a41511a76e65bdd2ff12faf517e0`  
		Last Modified: Wed, 12 Oct 2022 16:05:34 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d9d4e7a18b9439d8bcf71483c2450a4be68f4631870f38197439e1fcdd7785`  
		Last Modified: Wed, 12 Oct 2022 16:05:34 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1860ca093ea655e0f934c3258432233e68af7d44389b5f369fc75f37a134ed42`  
		Last Modified: Wed, 12 Oct 2022 16:05:32 GMT  
		Size: 78.8 KB (78849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa891f591bff349d725f02ea0e7f95c0694585653e8535664adc8e9654b7e61b`  
		Last Modified: Wed, 12 Oct 2022 16:05:32 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c518e2c090f7422dbabbdad00fe0b1337d3de05ee65cbf7867074b2a2784747`  
		Last Modified: Wed, 12 Oct 2022 16:05:50 GMT  
		Size: 192.4 MB (192371074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bab5613f98cf44d0f7a82444c3fd8e2129497f9e53e6f95066fc3c49ac27f8`  
		Last Modified: Wed, 12 Oct 2022 16:05:32 GMT  
		Size: 99.3 KB (99258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c47dab858c7296d1a1fde21290de845a7d0f9e792597d5979ac4c0aeeca26f`  
		Last Modified: Wed, 12 Oct 2022 16:05:32 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
