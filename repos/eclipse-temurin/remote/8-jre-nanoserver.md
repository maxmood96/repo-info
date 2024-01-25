## `eclipse-temurin:8-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:6ea2e32b9855c2e81a2c61a1807231d096559c2f87bb816a9414d0fb5c129248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.20348.2227; amd64

```console
$ docker pull eclipse-temurin@sha256:b691040e5b394507f8a4b004ef9073363b49fa9654e48be841313caa6607f22c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (161032870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdd542a5ab9ae7b555587c489aae1853f451d5554eb90e4bfa76842fb9d50f8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 04 Jan 2024 03:13:36 GMT
RUN Apply image 10.0.20348.2227
# Wed, 10 Jan 2024 23:17:03 GMT
SHELL [cmd /s /c]
# Wed, 24 Jan 2024 21:53:23 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 24 Jan 2024 21:53:24 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 24 Jan 2024 21:53:24 GMT
USER ContainerAdministrator
# Wed, 24 Jan 2024 21:53:46 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Jan 2024 21:53:47 GMT
USER ContainerUser
# Wed, 24 Jan 2024 21:54:30 GMT
COPY dir:db8ed4bc6cf3fc1a9a530d737bd8bcda792821f4f1e3e610cedaee77629ebb36 in C:\openjdk-8 
# Wed, 24 Jan 2024 21:54:43 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:11d5cdc5eaac7bace3ae1ecd3c0df2a27ef5005ab296c56b7f83e24bf25c236c`  
		Last Modified: Tue, 09 Jan 2024 20:57:18 GMT  
		Size: 120.8 MB (120769267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a5f2601f3a3b05b34c1f8683e3c9ea81ea63dbe1b04c37b85d09170f020fc0`  
		Last Modified: Thu, 11 Jan 2024 04:18:57 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bc6f55d94ad6babb64b648ddd4e3d6d8072a6266be4c48a8381f0c374a7724`  
		Last Modified: Wed, 24 Jan 2024 22:11:23 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8550800dcda4ebc8d1cc88204963b26f3442312b25f671aac3d9560aa39b4df2`  
		Last Modified: Wed, 24 Jan 2024 22:11:23 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520937eeb616efcc621cdf2db195eef5183f5b7517ef9ccf1a110e4eb1c01c39`  
		Last Modified: Wed, 24 Jan 2024 22:11:21 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c41f39f8cd5ecc958ed1cad2cb8d774b184e8e399d3ad9b793e5a98904d4a6`  
		Last Modified: Wed, 24 Jan 2024 22:11:22 GMT  
		Size: 85.9 KB (85881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605c359866d83e1868c6b725a8294b3ff8f2e73ae0272190ab7c80a25ceb1d9b`  
		Last Modified: Wed, 24 Jan 2024 22:11:21 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc21c241b24e3b3202722169a41841937db29fc3d82928c48ddccc9abcfd5bbb`  
		Last Modified: Wed, 24 Jan 2024 22:11:51 GMT  
		Size: 40.1 MB (40113273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89c515faf860c6be9701258b9d061a98a38c8bb26ae7f6be84d4ab7fe96f761`  
		Last Modified: Wed, 24 Jan 2024 22:11:46 GMT  
		Size: 58.7 KB (58704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull eclipse-temurin@sha256:5f2370ac79146b29388926440fc76703b57a19f55286e5aab316745731bb6f60
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.9 MB (144864382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cfef19bb8843243017468fa957d7362a37ea652927b95a938b81261e59a086d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Wed, 10 Jan 2024 22:41:06 GMT
SHELL [cmd /s /c]
# Wed, 24 Jan 2024 21:19:51 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 24 Jan 2024 21:19:52 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 24 Jan 2024 21:19:52 GMT
USER ContainerAdministrator
# Wed, 24 Jan 2024 21:20:11 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Jan 2024 21:20:11 GMT
USER ContainerUser
# Wed, 24 Jan 2024 21:24:41 GMT
COPY dir:db8ed4bc6cf3fc1a9a530d737bd8bcda792821f4f1e3e610cedaee77629ebb36 in C:\openjdk-8 
# Wed, 24 Jan 2024 21:24:51 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec88c6fd1d0cd14082069642ccb3b0dd5a7538a4b8b0c2d430549f345d8fd53`  
		Last Modified: Thu, 11 Jan 2024 04:09:21 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:903bc5f9b43cb057943f9039188b4649c9d793100527ab3baecd1ab7392e8ddb`  
		Last Modified: Wed, 24 Jan 2024 22:02:03 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd811e96e6a429ac10c64b48f4456224dea65509d2dade4123a68cf9bd68eda`  
		Last Modified: Wed, 24 Jan 2024 22:02:03 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9d1fd70089e92424c993da2b4648d7cb837c6d796b6c0e106fed58679b89c9`  
		Last Modified: Wed, 24 Jan 2024 22:02:01 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8c01d27c73d63005431f8cfe1289242313497076ebda8bc0bf6913b06f180c`  
		Last Modified: Wed, 24 Jan 2024 22:02:01 GMT  
		Size: 67.2 KB (67153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0871f39eccd4268560a92561806bcc18b963dc148b831fc86179cf5c14025ce`  
		Last Modified: Wed, 24 Jan 2024 22:02:01 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2c19d4fd0adfded2a27bc5ccfabd897976141da4e28093a27ed68ded10b86f`  
		Last Modified: Wed, 24 Jan 2024 22:03:06 GMT  
		Size: 40.1 MB (40113381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3f29b3600bb84597d9583e51e75aa1772d8d0b5e803556660583e4c5b0daeb`  
		Last Modified: Wed, 24 Jan 2024 22:03:00 GMT  
		Size: 86.8 KB (86830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
