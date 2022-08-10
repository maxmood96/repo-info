## `eclipse-temurin:11-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:3d2cb3dae81b6737843e8b145ee2007f822e8961c41111031398de664fc940f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.887; amd64
	-	windows version 10.0.17763.3287; amd64

### `eclipse-temurin:11-nanoserver` - windows version 10.0.20348.887; amd64

```console
$ docker pull eclipse-temurin@sha256:a2b58ca80a853fb4387fac5292494a956e41b83852d092499c664a7be6d0a981
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 MB (310652895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49db5a80d91b2000a0f0707ea9f4232072dd899b818529d94e4f937284b84ca3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Aug 2022 18:05:23 GMT
RUN Apply image 10.0.20348.887
# Wed, 10 Aug 2022 16:28:17 GMT
SHELL [cmd /s /c]
# Wed, 10 Aug 2022 16:29:53 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Wed, 10 Aug 2022 16:29:54 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 10 Aug 2022 16:29:55 GMT
USER ContainerAdministrator
# Wed, 10 Aug 2022 16:30:17 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Aug 2022 16:30:18 GMT
USER ContainerUser
# Wed, 10 Aug 2022 16:30:35 GMT
COPY dir:311b50e59d3b0be0ca838f3cd712deaf9388198aeb821aea34d4de0537bd9b6e in C:\openjdk-11 
# Wed, 10 Aug 2022 16:30:55 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Aug 2022 16:30:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ebf439f800cd4c1fccaf4a0545e6bff60caa5141295c8ab81f6c525073c423d`  
		Size: 118.1 MB (118088450 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5f1e06146ab0490d235fe89786637467a4b71853ee428e8740ea6efbc536c47c`  
		Last Modified: Wed, 10 Aug 2022 16:48:40 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4f00e89b19d1ce99daab79ba1bcca3e29ad052342fc52687679c6a9e6bdec0`  
		Last Modified: Wed, 10 Aug 2022 16:49:19 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2afc3c37badc7edc01952be676e9530d9ec3492ccf678d80c67b9548b96bee`  
		Last Modified: Wed, 10 Aug 2022 16:49:19 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef6a0937662bedc3cabcdb61a1381d73205583cc8305c01e7a454d9d497173d8`  
		Last Modified: Wed, 10 Aug 2022 16:49:19 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0950a807fee1581948edb4112ce7ac3456a011f5420c15f19c5a429ecac0ac3e`  
		Last Modified: Wed, 10 Aug 2022 16:49:17 GMT  
		Size: 87.6 KB (87631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5c928d9674ef57d0d85aa68dbff73f5992d86b39e5bc4f23d6db42329416c4`  
		Last Modified: Wed, 10 Aug 2022 16:49:17 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57743c30113de140ed6253db93e7b17fe173a490009f309d1d5c46cfacca0fea`  
		Last Modified: Wed, 10 Aug 2022 16:49:35 GMT  
		Size: 192.4 MB (192370328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb4db824b42bc00c2d20d3fe424f0f123f098592d44c5be9b190d98c954b2a3`  
		Last Modified: Wed, 10 Aug 2022 16:49:17 GMT  
		Size: 99.6 KB (99586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b4ebd7b6108c093033d28af8d577e0327ce4d137cfd41589b22c68087287863`  
		Last Modified: Wed, 10 Aug 2022 16:49:17 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-nanoserver` - windows version 10.0.17763.3287; amd64

```console
$ docker pull eclipse-temurin@sha256:633336d3dacaea3c443dc052f99957ec9af2df3c4a37a0c0da8bce4566d7dd7c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295732102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62350c30b8d0cb922b779522577984b8955c357332c77dbd0dc3d1bce1258ba`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Aug 2022 18:08:38 GMT
RUN Apply image 10.0.17763.3287
# Wed, 10 Aug 2022 15:57:07 GMT
SHELL [cmd /s /c]
# Wed, 10 Aug 2022 16:05:32 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Wed, 10 Aug 2022 16:05:32 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 10 Aug 2022 16:05:33 GMT
USER ContainerAdministrator
# Wed, 10 Aug 2022 16:05:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Aug 2022 16:05:46 GMT
USER ContainerUser
# Wed, 10 Aug 2022 16:06:02 GMT
COPY dir:311b50e59d3b0be0ca838f3cd712deaf9388198aeb821aea34d4de0537bd9b6e in C:\openjdk-11 
# Wed, 10 Aug 2022 16:06:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Aug 2022 16:06:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5c9d6483dab113d2d9b50fdf3156622aa2ec3d6faaed5664d15a5568032d1714`  
		Size: 103.2 MB (103204200 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0f4438539876006761cb687527bd8cb94cc7a273cf8bb47563981044f2e1771e`  
		Last Modified: Wed, 10 Aug 2022 16:38:40 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657f852163df6cebfdf48240b33ab5eea4779e39e44141bc456671ce1aa1425e`  
		Last Modified: Wed, 10 Aug 2022 16:41:18 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449b42af65b7afcbbbbe1c63accbdf920def5029a2e6b1ee4ff4d5abe46c69bd`  
		Last Modified: Wed, 10 Aug 2022 16:41:18 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b17c585212e74e450fb63d27950a921745936476bc2e8456acb6e15be08b194e`  
		Last Modified: Wed, 10 Aug 2022 16:41:18 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae2de8d8bba305ce1fc7a9be34d0e0dc042978d170c3111a862ad186d46f6b3`  
		Last Modified: Wed, 10 Aug 2022 16:41:16 GMT  
		Size: 70.1 KB (70072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f810f1b70fd32f557675c11c5d40ede431212f45cef74be03da1470c029346ce`  
		Last Modified: Wed, 10 Aug 2022 16:41:16 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13b16bae2a09adcf85ed424e557bd6cb5dfc1c45420406ff80eb0a710745be5`  
		Last Modified: Wed, 10 Aug 2022 16:41:35 GMT  
		Size: 192.4 MB (192367546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2be7164081e9998c5731aa9464942f9fd51df321b5a5d1b5bec48d87f11987`  
		Last Modified: Wed, 10 Aug 2022 16:41:16 GMT  
		Size: 83.4 KB (83373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14cc6ef9d833e9e57f5cf13b7ccaa98f612b49976dd64ae6fb8f13fb3b540ad3`  
		Last Modified: Wed, 10 Aug 2022 16:41:16 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
