## `eclipse-temurin:20-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:10be01e448eb25737ab693c9e40b8b829f3ee9ce8567926bc28bd7b7217781b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1607; amd64

### `eclipse-temurin:20-nanoserver-ltsc2022` - windows version 10.0.20348.1607; amd64

```console
$ docker pull eclipse-temurin@sha256:80c1b1e7372cd980a506034ad08ab770731393fb839070146f765cd546ca5e3e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.6 MB (317587857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cdf24f416e7fbdc5a54cec26ae92822d264380cdf116d322544de7d17f68064`
-	Default Command: `["jshell"]`
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
# Mon, 27 Mar 2023 20:33:04 GMT
COPY dir:0bba24b8a26333fabbf995368b29d05051d1ff1f33d04d60afd33310da1fd9b4 in C:\openjdk-20 
# Mon, 27 Mar 2023 20:33:30 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 27 Mar 2023 20:33:31 GMT
CMD ["jshell"]
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
	-	`sha256:aa59dea2447cd358b6e9cbc3ce7482aa9e8cde492a650f1d8504b78fba4486d1`  
		Last Modified: Mon, 27 Mar 2023 20:40:30 GMT  
		Size: 195.2 MB (195242930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02d9aa4f186ba7de8c7b3c09b0bf9a6c4d9a6b3ca5a40ac23d7a3a048946642`  
		Last Modified: Mon, 27 Mar 2023 20:40:09 GMT  
		Size: 89.8 KB (89837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a102c126a42a0809a4f9f1bbefef411dab62faed0401c52457cfa44718799221`  
		Last Modified: Mon, 27 Mar 2023 20:40:09 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
