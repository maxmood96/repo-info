## `eclipse-temurin:17-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:766fd1ea219ce690999fb82f031f40f5e076e4403dd96979ff85f2d8f58814ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `eclipse-temurin:17-jdk-nanoserver-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull eclipse-temurin@sha256:5781bff5bf816d006fdf018e8a30d805b89d720d1f282fc5235b2a047772b768
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297843428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc8cdc418919092d41011876fa4cddb8d322b50b550bf22c14948fe7fed2b2d5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Wed, 12 Mar 2025 19:15:39 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Wed, 12 Mar 2025 19:15:41 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 12 Mar 2025 19:15:42 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:15:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:15:45 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:15:53 GMT
COPY dir:5f87ec570fea10148b246e6a91d6cf8396b47b1e19a7e8d79bcea78e84a1d159 in C:\openjdk-17 
# Wed, 12 Mar 2025 19:15:58 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Mar 2025 19:15:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:294bbf52e270ab816d64354fff14480e82044563ea516cfe2445c5752f0917e8`  
		Last Modified: Wed, 12 Mar 2025 19:16:06 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45d7d0c8a26f9a9fbb260891940d19b7113b90a6b8619af63234387f5d425f3`  
		Last Modified: Wed, 12 Mar 2025 19:16:06 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34032e84939bc7494ecd3353b22a0d3e3f65676930a072dae27d8427c495d64c`  
		Last Modified: Wed, 12 Mar 2025 19:16:05 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46860f768eb968b93f75901082396b49ee09bb3c0895adebf8ef5ade288b604b`  
		Last Modified: Wed, 12 Mar 2025 19:16:05 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efc3cb3447e237cf506088adc1a73b0f666d0be9ecd752abbe18084e782c12f`  
		Last Modified: Wed, 12 Mar 2025 19:16:03 GMT  
		Size: 73.5 KB (73478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199f81bfc1dbdc528506dd1a3f47c6c9def7079d1dd2949844e434713d49f5b0`  
		Last Modified: Wed, 12 Mar 2025 19:16:03 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66306db801092627164406ae79e63a0be134f362000e4c1c736cd00e45e9861`  
		Last Modified: Wed, 12 Mar 2025 19:16:13 GMT  
		Size: 187.2 MB (187234969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22fa28e36d3030d8518cf061f52830c60a6c328eeb526090c6332089219a9d1`  
		Last Modified: Wed, 12 Mar 2025 19:16:04 GMT  
		Size: 3.6 MB (3621041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a503efcfb8c3585d2ec404571b6e6a1f46c9a44c0b0328950cf46be0ce837a4`  
		Last Modified: Wed, 12 Mar 2025 19:16:03 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
