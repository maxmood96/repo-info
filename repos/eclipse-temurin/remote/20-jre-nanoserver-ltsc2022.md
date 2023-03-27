## `eclipse-temurin:20-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:842f2c2ebbc3f1e77e1725b8ba746ce348a8bf4e041408ef602bc7e58651a0e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1607; amd64

### `eclipse-temurin:20-jre-nanoserver-ltsc2022` - windows version 10.0.20348.1607; amd64

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
