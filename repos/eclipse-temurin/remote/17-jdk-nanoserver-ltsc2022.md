## `eclipse-temurin:17-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:52d7b7b2d1b8f0cfdade7f476dad2f0c39b175654fe25f41b91336ae7b2ade6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `eclipse-temurin:17-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull eclipse-temurin@sha256:a6449a4b118dca3653ba75e318a53a742a4c001b5b9180355531c6474e242482
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310377270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dac9bcde84c2c7c592e77aee3224ea1f8d5912854190837dd19071cc622b4ca`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Sat, 08 Nov 2025 19:17:28 GMT
SHELL [cmd /s /c]
# Sat, 08 Nov 2025 19:17:29 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 19:17:30 GMT
ENV JAVA_HOME=C:\openjdk-17
# Sat, 08 Nov 2025 19:17:31 GMT
USER ContainerAdministrator
# Sat, 08 Nov 2025 19:17:37 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 08 Nov 2025 19:17:38 GMT
USER ContainerUser
# Sat, 08 Nov 2025 19:18:03 GMT
COPY dir:2018c1c9eb6dc671bed9b2018ab32e648d405ad10a017a184613d399d49818ed in C:\openjdk-17 
# Sat, 08 Nov 2025 19:18:07 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 08 Nov 2025 19:18:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15efb952b2f22d1d501a059fde7122b4d36cf5401fc373dbafee91cb79e51dc`  
		Last Modified: Sat, 08 Nov 2025 19:18:35 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28735678bd442e29e1cd7171c60fbf49ff24e032b5c13c3784fe301350fd850`  
		Last Modified: Sat, 08 Nov 2025 19:18:35 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc2810f2ed5dcdd00a202bd8b3c0b2d4247a15199af6bdccf02a6bf83732a9e`  
		Last Modified: Sat, 08 Nov 2025 19:18:35 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98875ac5889e959bd1d19d9def26ecbb35f4fede5c188c24be3991310e07c304`  
		Last Modified: Sat, 08 Nov 2025 19:18:35 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d23ed7546c73c660f9a35907a6ed80a80e556f9adbe7636ca9f9e9852038e36`  
		Last Modified: Sat, 08 Nov 2025 19:18:35 GMT  
		Size: 76.8 KB (76753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2453cfbeb8c22c2a6cab37790395fc0c1816184d3197d5e334c479172f219ee`  
		Last Modified: Sat, 08 Nov 2025 19:18:35 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26ac30f36713e907e1d182c1449b43b8cf613b775606680f77f745a7fcf0c07`  
		Last Modified: Sat, 08 Nov 2025 22:14:58 GMT  
		Size: 187.5 MB (187510993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad392c4f794b2e7897e84c92b840e88f812ecefa57d269ad1cee8224a289d45e`  
		Last Modified: Sat, 08 Nov 2025 19:18:35 GMT  
		Size: 99.1 KB (99068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2ac6108044dcea77c9f842613c7e21e6bde5b5381791f2f1a0cceedf8ae4b3`  
		Last Modified: Sat, 08 Nov 2025 19:18:35 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
