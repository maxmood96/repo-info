## `eclipse-temurin:17-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:fc515930d1b41f203ed3213c5af0173ea57c0071749cc40c516f4fc78a7624b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.26100.6905; amd64

```console
$ docker pull eclipse-temurin@sha256:9ad03d85dc5dc4da9ad22af4ca5675edf9cbe8bb8d00e96f89944f9e8ab57c2c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.7 MB (381731340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08269abfe46570cda06ef73287514670e6279ec95d0ac79cc9579895b3986f5b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 07:22:01 GMT
RUN Apply image 10.0.26100.6905
# Sat, 08 Nov 2025 19:16:45 GMT
SHELL [cmd /s /c]
# Sat, 08 Nov 2025 19:18:17 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 19:18:17 GMT
ENV JAVA_HOME=C:\openjdk-17
# Sat, 08 Nov 2025 19:18:18 GMT
USER ContainerAdministrator
# Sat, 08 Nov 2025 19:18:19 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 08 Nov 2025 19:18:20 GMT
USER ContainerUser
# Sat, 08 Nov 2025 19:18:42 GMT
COPY dir:2018c1c9eb6dc671bed9b2018ab32e648d405ad10a017a184613d399d49818ed in C:\openjdk-17 
# Sat, 08 Nov 2025 19:18:46 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 08 Nov 2025 19:18:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9188956580c47f583c927f17e42f8825823890544237141f21ca4ef10ea55e60`  
		Last Modified: Fri, 24 Oct 2025 11:13:56 GMT  
		Size: 194.0 MB (194029378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a4112a31b422a7f7b32c75013023f8fce10f4ce3b96e83d0a9ee625daaf23c`  
		Last Modified: Sat, 08 Nov 2025 19:17:36 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492cabe547101e2b7467e5fbc68bc08b531206b5796d348284aeb176c32ebda2`  
		Last Modified: Sat, 08 Nov 2025 19:19:10 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0410a33a7f99c617484e458c42d90844fe0d5c8444f9022c7d0d1f6a0ce17c8`  
		Last Modified: Sat, 08 Nov 2025 19:19:10 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5d559c83c3bddc28ce7a0b2bce5d69967a102ea3185f6cfcb8862d43cc1d2c`  
		Last Modified: Sat, 08 Nov 2025 19:19:10 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c8ef10e0e227236d85ea185d852c13306be70de0eb9e51a4e648403ebb79514`  
		Last Modified: Sat, 08 Nov 2025 19:19:10 GMT  
		Size: 71.9 KB (71858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ab8941a3b77f074dffda900f67955bb0764f7572f229ddfc07f255d1ec6b4e`  
		Last Modified: Sat, 08 Nov 2025 19:19:10 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e2f44b38ad945c611cc276c5ca56830aed9aa07793c5061c3adb734f97264f`  
		Last Modified: Sat, 08 Nov 2025 22:14:57 GMT  
		Size: 187.5 MB (187510778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bef627f003b39f1576260c0c3c537210ff238d2e29f781302d28100bfe308b`  
		Last Modified: Sat, 08 Nov 2025 19:19:10 GMT  
		Size: 112.9 KB (112938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70303c1a3258c9351b2bbfdc7a350ed324d507c5ed1b0d441ff3e5ff25aae12`  
		Last Modified: Sat, 08 Nov 2025 19:19:10 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.20348.4297; amd64

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
