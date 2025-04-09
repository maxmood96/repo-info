## `eclipse-temurin:21-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:608d71440310c6a9cb2f6ac40deac22716ad26e5d62a55f9aff88154048a5adb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7136; amd64

### `eclipse-temurin:21-jdk-nanoserver` - windows version 10.0.26100.3775; amd64

```console
$ docker pull eclipse-temurin@sha256:bac63069e3306e31d47a1050d55c9245c36e0b3f3b742942466afbb4f5b85658
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.8 MB (391787460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414762e44d12aa4097d36c0ad9d7e6a65896ef09283c9a7f064c8edb85307103`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Apr 2025 07:26:08 GMT
RUN Apply image 10.0.26100.3775
# Wed, 09 Apr 2025 01:48:58 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:48:59 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Wed, 09 Apr 2025 01:49:00 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 09 Apr 2025 01:49:01 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:49:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:49:05 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:49:14 GMT
COPY dir:87fb2a3fe15bf051f07e33b0f4d627a83582ff5ee0a30a4b75036496ad24f723 in C:\openjdk-21 
# Wed, 09 Apr 2025 01:49:22 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 09 Apr 2025 01:49:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:79b2ed45f890e91d23d7d22491a8fb6909c9268c668dc6a0e3b40131da02ed74`  
		Last Modified: Wed, 09 Apr 2025 00:36:30 GMT  
		Size: 190.1 MB (190113206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e549d6300b7c9dbe3837adb59ddcf6f523587df6ea304fe9fe2a97b101d53ef6`  
		Last Modified: Wed, 09 Apr 2025 01:49:30 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a8ec185fef8c2413b31b9b33de20e720d6a69c1fa3a4fa757294d7e3442d46`  
		Last Modified: Wed, 09 Apr 2025 01:49:29 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9e480055aae7693a113a33cce2e14d09850008160cf8b3b6e8d56214b3f9c6`  
		Last Modified: Wed, 09 Apr 2025 01:49:29 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c1a18b756a8092d4f8234aa40de3406fcea65df07252652c953b0c7b296834`  
		Last Modified: Wed, 09 Apr 2025 01:49:29 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2ad7918c8c1a90514782f4e83e817ef7caed717c271b410c0a72a6f4b1a789`  
		Last Modified: Wed, 09 Apr 2025 01:49:27 GMT  
		Size: 77.1 KB (77115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ad3862c065dc84e2c88693cb8eeeed9969716787015d5246a1df11636b5c45`  
		Last Modified: Wed, 09 Apr 2025 01:49:27 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1a9af3f70a3a2cc21eaa3a9abe8514053b3327dab802f9cc608a22762a481e`  
		Last Modified: Wed, 09 Apr 2025 01:49:40 GMT  
		Size: 201.5 MB (201476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5954df206eb7e535d1d72655020b31c0c79e160694dbf02918cd876759dc31`  
		Last Modified: Wed, 09 Apr 2025 01:49:27 GMT  
		Size: 114.7 KB (114693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0072c03e3426aeef3c2f34b8b16063ab5fb81a7dec28e3b898db9077d895cb3`  
		Last Modified: Wed, 09 Apr 2025 01:49:27 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jdk-nanoserver` - windows version 10.0.20348.3453; amd64

```console
$ docker pull eclipse-temurin@sha256:e353152beccfe24e2f754d1eff64c4485cd9a24b38b47ac245c0213b6dc3e0df
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322401262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08297ed58ef6d81b9231e415dfcafdfd6ebff384b0ee5034f373e0f329dfdeb1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Apr 2025 22:57:50 GMT
RUN Apply image 10.0.20348.3453
# Wed, 09 Apr 2025 01:23:10 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:23:11 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Wed, 09 Apr 2025 01:23:12 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 09 Apr 2025 01:23:13 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:23:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:23:16 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:23:24 GMT
COPY dir:87fb2a3fe15bf051f07e33b0f4d627a83582ff5ee0a30a4b75036496ad24f723 in C:\openjdk-21 
# Wed, 09 Apr 2025 01:23:29 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 09 Apr 2025 01:23:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5caa30147a287e99992660f7f85276c53fe3299503a06c47d476387410721453`  
		Last Modified: Wed, 09 Apr 2025 01:13:36 GMT  
		Size: 120.7 MB (120736312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c01886e5055c0fff62751f1e661c8aa2b5c4e80897195248a0c5f9c853ad69`  
		Last Modified: Wed, 09 Apr 2025 01:23:34 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322df9f3e756690e7220e653f783337cb8695d654f09eff46a1e54b6aa6cd34c`  
		Last Modified: Wed, 09 Apr 2025 01:23:33 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad875d24a40c90a58413ce116acbabb5374e20c05df438ae489f0a9f4037f3f`  
		Last Modified: Wed, 09 Apr 2025 01:23:33 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b3333cbf436458f59e6a7546bb0bf8e1cd50e239f6aba70b6cb5ee3911c7ff`  
		Last Modified: Wed, 09 Apr 2025 01:23:33 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb43bef8f2d92c30bef1e239ef22faeb5e51043e61d9618bdab3b3dc358c449`  
		Last Modified: Wed, 09 Apr 2025 01:23:32 GMT  
		Size: 76.3 KB (76289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c92bc30951db16858f249325566139be8dea95bbd878183afb8f3fc0fd3497`  
		Last Modified: Wed, 09 Apr 2025 01:23:32 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6bb068ace185eb2546ba59d16f6b4311ac3031cba75ab20763d103398fbbe70`  
		Last Modified: Wed, 09 Apr 2025 01:23:44 GMT  
		Size: 201.5 MB (201475434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d57eb805366d987bd8c9a0d37665ae866dbb6318c470d1bbefe460d03eeffe`  
		Last Modified: Wed, 09 Apr 2025 01:23:33 GMT  
		Size: 107.0 KB (107042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9071033378615c5901f4b0ccf4edd6d273ebaccb195a9931454785ec669fc61a`  
		Last Modified: Wed, 09 Apr 2025 01:23:32 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jdk-nanoserver` - windows version 10.0.17763.7136; amd64

```console
$ docker pull eclipse-temurin@sha256:dcf71dc3687eba8c3f8290c4ab1d0d4f5aa2b15abbeae065cb019e9569d0fd06
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.3 MB (312292302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d039b03e62835a0519a23bc9f7a73b48a2f77ee47f32a531b853e165988ab9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Apr 2025 01:31:28 GMT
RUN Apply image 10.0.17763.7136
# Wed, 09 Apr 2025 02:52:45 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 02:52:48 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Wed, 09 Apr 2025 02:52:48 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 09 Apr 2025 02:52:49 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 02:52:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 02:52:53 GMT
USER ContainerUser
# Wed, 09 Apr 2025 02:53:01 GMT
COPY dir:87fb2a3fe15bf051f07e33b0f4d627a83582ff5ee0a30a4b75036496ad24f723 in C:\openjdk-21 
# Wed, 09 Apr 2025 02:53:06 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 09 Apr 2025 02:53:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a06e0965a0fa3715e629889bd9332aa22aadd75654cac5c9818b67c0264b3ee1`  
		Last Modified: Tue, 08 Apr 2025 20:16:02 GMT  
		Size: 106.9 MB (106922524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5ec35a1c747082270344b596202219a29b47f141bfcb21d531fd2378a85f61`  
		Last Modified: Wed, 09 Apr 2025 02:53:11 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744cf1c63b5abda24a95e14e810f08a2d8fc02f478c8568a4ef62147960b52fe`  
		Last Modified: Wed, 09 Apr 2025 02:53:10 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d529dd9e1cb63a1c8da2a70d1fcb93068d939f7fc3e0b429a533f29c63e71a18`  
		Last Modified: Wed, 09 Apr 2025 02:53:10 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b5c7788df208df865f65883b163b7d51dc00c180dc3ffc8d027d37e7f6c035`  
		Last Modified: Wed, 09 Apr 2025 02:53:10 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ff3c1e42d8fd03da301dc07bd32006fa40dddd9c5672b583f5718f2f0cfc48`  
		Last Modified: Wed, 09 Apr 2025 02:53:09 GMT  
		Size: 70.7 KB (70706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4eb7bab803758e6f0d4ccc8a3628174fb2751cac45c83732e9c467a375d2639`  
		Last Modified: Wed, 09 Apr 2025 02:53:09 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c8a3e7c4bb4bf14cd0f1c7e88ef9d8afe4ce07f4f39c28a8e08867aaf6bbda`  
		Last Modified: Wed, 09 Apr 2025 02:53:21 GMT  
		Size: 201.5 MB (201475550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ebbc5dd456f1ade84e0becf975fc22483119a9697cf89672f62c3e4447951b`  
		Last Modified: Wed, 09 Apr 2025 02:53:10 GMT  
		Size: 3.8 MB (3817283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227e8c3aecad0841df03fd7604fdff484eaebdc3e0cdc3b1188b2cb7e284bf02`  
		Last Modified: Wed, 09 Apr 2025 02:53:09 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
