## `eclipse-temurin:20-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:682edfbd42edac1d67ae1368277956a9b32559f31bb869811822ba8375885287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1607; amd64
	-	windows version 10.0.17763.4131; amd64

### `eclipse-temurin:20-jdk-nanoserver` - windows version 10.0.20348.1607; amd64

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

### `eclipse-temurin:20-jdk-nanoserver` - windows version 10.0.17763.4131; amd64

```console
$ docker pull eclipse-temurin@sha256:d0eec852297b6f17efdad3c85103233f9863d22693f938800faf31dd042d4ef1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.8 MB (305800251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92314cd796b1295802f55e46b239fdd465803831a997e64405dfc1a9e1f25f81`
-	Default Command: `["jshell"]`
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
# Mon, 27 Mar 2023 20:25:57 GMT
COPY dir:0bba24b8a26333fabbf995368b29d05051d1ff1f33d04d60afd33310da1fd9b4 in C:\openjdk-20 
# Mon, 27 Mar 2023 20:26:26 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 27 Mar 2023 20:26:27 GMT
CMD ["jshell"]
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
	-	`sha256:6e8677dddc2cd346ba4928dbf48560b3ea8c0e97f7e8f1635e7b00074f2c9f7f`  
		Last Modified: Mon, 27 Mar 2023 20:38:49 GMT  
		Size: 195.2 MB (195240856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317bb24c2d2274236a0c6de05b72dba89022b9c2486614ab7d4b30a01037fcfd`  
		Last Modified: Mon, 27 Mar 2023 20:38:29 GMT  
		Size: 3.8 MB (3798525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e2022d2c841336b12de3e3ff11ed89eae07111043fc6a9ea56ff9b053864fd2`  
		Last Modified: Mon, 27 Mar 2023 20:38:28 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
