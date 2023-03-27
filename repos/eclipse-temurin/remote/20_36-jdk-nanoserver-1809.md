## `eclipse-temurin:20_36-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:b7fd8b0ca6960214dd0a5eff51dad1c7d47a3c08e2b25ed651d17998050a0bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4131; amd64

### `eclipse-temurin:20_36-jdk-nanoserver-1809` - windows version 10.0.17763.4131; amd64

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
