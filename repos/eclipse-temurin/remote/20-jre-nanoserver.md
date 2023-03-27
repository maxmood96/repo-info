## `eclipse-temurin:20-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:6b243218b08db3a47e3f1a2bfa2e4825591f8091e65d9e5fc70e3c0ce54bd80b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1607; amd64
	-	windows version 10.0.17763.4131; amd64

### `eclipse-temurin:20-jre-nanoserver` - windows version 10.0.20348.1607; amd64

```console
$ docker pull eclipse-temurin@sha256:8b55d46607fc53de982d13e2351ab3927eeb5e2bc33201dadb8b60ef14a2d6b9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168058001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6d3737e6f833197869906b7b66682f75baa134b1f9101a99ecd74440d27a77e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 10 Mar 2023 06:31:34 GMT
RUN Apply image 10.0.20348.1607
# Thu, 16 Mar 2023 01:29:33 GMT
SHELL [cmd /s /c]
# Mon, 27 Mar 2023 20:32:24 GMT
ENV JAVA_VERSION=jdk-20+36
# Mon, 27 Mar 2023 20:32:25 GMT
ENV JAVA_HOME=C:\openjdk-20
# Mon, 27 Mar 2023 20:32:26 GMT
USER ContainerAdministrator
# Mon, 27 Mar 2023 20:32:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Mon, 27 Mar 2023 20:32:47 GMT
USER ContainerUser
# Mon, 27 Mar 2023 20:33:47 GMT
COPY dir:88253b833ff2634324ea23b2cdfd627ca2e30273c5f29426251a8626a4f6baa7 in C:\openjdk-20 
# Mon, 27 Mar 2023 20:34:08 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:7abf0a70d48bf65f3d985f5780d4bdaece36f1f4bb8be10d5a6aacce33dacc75`  
		Last Modified: Thu, 16 Mar 2023 01:54:24 GMT  
		Size: 122.2 MB (122171731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a611a20686e9374e3a55a49399506f83c041ae711ed47018c2267c341156dd97`  
		Last Modified: Thu, 16 Mar 2023 01:53:50 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80bdb9d78f38bff303650fbea906414522cf6d571757c0632152be14da71b97`  
		Last Modified: Mon, 27 Mar 2023 20:40:11 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b20ba59e27bd7b551ebe0f8cff0ebc834c5a4bed36d2677f8e9db94e258ef2`  
		Last Modified: Mon, 27 Mar 2023 20:40:11 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90f5a5d9f6f933fe25b652a405cf5feb90cceb59f6c2f339e7986d20bfd7e9c5`  
		Last Modified: Mon, 27 Mar 2023 20:40:11 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f372304005707d2f4daf8716e6ec33b1561cb6fabe6644e9420aae9507b19286`  
		Last Modified: Mon, 27 Mar 2023 20:40:10 GMT  
		Size: 76.5 KB (76531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:315a2012d3e38aeedb03d677399e9cd20d2ad6d7de6879b32bd7b9c0ef0fb4e7`  
		Last Modified: Mon, 27 Mar 2023 20:40:09 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c372a17a39ceefc32d08a88a507964c3ff991a36b18d8af95fc06d71f7fc574`  
		Last Modified: Mon, 27 Mar 2023 20:40:51 GMT  
		Size: 45.7 MB (45741264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339334234971b96d18338995370010d67db9e1acf5bc6fc670add54a2c8b8d4c`  
		Last Modified: Mon, 27 Mar 2023 20:40:42 GMT  
		Size: 62.8 KB (62771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:20-jre-nanoserver` - windows version 10.0.17763.4131; amd64

```console
$ docker pull eclipse-temurin@sha256:a206be1cfa44b776926eb5009069d1c143568da66fc05b0e0b73d37e28ecda70
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155640031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87487eb7b82e971deafdc3bfe9eec9607384c14855cbba418989353b9b8a88e0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 11 Mar 2023 10:09:02 GMT
RUN Apply image 10.0.17763.4131
# Thu, 16 Mar 2023 00:45:50 GMT
SHELL [cmd /s /c]
# Mon, 27 Mar 2023 20:25:22 GMT
ENV JAVA_VERSION=jdk-20+36
# Mon, 27 Mar 2023 20:25:23 GMT
ENV JAVA_HOME=C:\openjdk-20
# Mon, 27 Mar 2023 20:25:23 GMT
USER ContainerAdministrator
# Mon, 27 Mar 2023 20:25:40 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Mon, 27 Mar 2023 20:25:41 GMT
USER ContainerUser
# Mon, 27 Mar 2023 20:31:15 GMT
COPY dir:88253b833ff2634324ea23b2cdfd627ca2e30273c5f29426251a8626a4f6baa7 in C:\openjdk-20 
# Mon, 27 Mar 2023 20:31:36 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:95eb2f0f3287f5ec687287cc244924aafc74c7ada3121d43f54223487f3f2d8d`  
		Last Modified: Thu, 16 Mar 2023 01:43:14 GMT  
		Size: 106.7 MB (106684240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5837fe68a36caddf38b0aaa99f4ef20ca36d8dfe2825fa6ffbcf0d38b9d59a`  
		Last Modified: Thu, 16 Mar 2023 01:42:43 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a050615a5658d34dee1f4726c584172c21cedd3b74b2671b5114da5761cf97`  
		Last Modified: Mon, 27 Mar 2023 20:38:30 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5698c0b93413a695e707079ac23b84f41915d4152b0db3fa50773e67a9c7489`  
		Last Modified: Mon, 27 Mar 2023 20:38:30 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50d296e29a01df8d3e6cd716078cc0952ca0fe17ff24c509954c7ef93df32160`  
		Last Modified: Mon, 27 Mar 2023 20:38:30 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3cc9ae73184a25ef98d9f482cb0458b8eae9ac840fc63df8e325bd2a6d156a`  
		Last Modified: Mon, 27 Mar 2023 20:38:28 GMT  
		Size: 69.7 KB (69693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7baf23d82020ec8dcd5f4f1ea2de2a211728be7bbf87709313a4883d0e5f33d6`  
		Last Modified: Mon, 27 Mar 2023 20:38:28 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6f13f0794d488b038698ee83e31a4f424e02d2895132fa5cb0e25fe3f0ffe4`  
		Last Modified: Mon, 27 Mar 2023 20:39:53 GMT  
		Size: 45.7 MB (45745409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378a41cea70d15a700b21f7d6ba566badd43cf56ce5668f0123ff9af0e7f1d4e`  
		Last Modified: Mon, 27 Mar 2023 20:39:44 GMT  
		Size: 3.1 MB (3134886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
