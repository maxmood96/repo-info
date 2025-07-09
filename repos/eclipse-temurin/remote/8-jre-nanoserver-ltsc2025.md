## `eclipse-temurin:8-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:1856b1563b80aa7fec1147a1fd23d6b847bab63c140ed81b6f4dd5cb09370369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4652; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2025` - windows version 10.0.26100.4652; amd64

```console
$ docker pull eclipse-temurin@sha256:9d8907fb992955b98ff18366b4da10d7d894a04672678e7964ad2c65b40f6d2e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233879825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b08111f897fffcb57dee27e2a9b6d4c76ea1e9b97426d86e0cd0cd2a9500bb03`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Jul 2025 18:13:07 GMT
RUN Apply image 10.0.26100.4652
# Wed, 09 Jul 2025 19:15:06 GMT
SHELL [cmd /s /c]
# Wed, 09 Jul 2025 19:15:07 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Wed, 09 Jul 2025 19:15:08 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 09 Jul 2025 19:15:10 GMT
USER ContainerAdministrator
# Wed, 09 Jul 2025 19:15:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Jul 2025 19:15:14 GMT
USER ContainerUser
# Wed, 09 Jul 2025 19:15:19 GMT
COPY dir:88632ffe03bdff97c0f2931283e9e8742ceaeaec8904ee54b87f8b4347f84ae7 in C:\openjdk-8 
# Wed, 09 Jul 2025 19:15:23 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:2fd4507679915420227c89c4f57165747b37deaa62748936e2af8c2f38de0b4e`  
		Last Modified: Wed, 09 Jul 2025 01:51:41 GMT  
		Size: 193.2 MB (193150329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3949f91681cbba3f66ded4313c7e68bb82fa24ca4e2cac98ee942f7b87a62d`  
		Last Modified: Wed, 09 Jul 2025 19:15:51 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d7209189854f6cf7aaeeff81257fa392c14832aeafee9a7f2891ed6fe09c8a`  
		Last Modified: Wed, 09 Jul 2025 19:15:51 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbb8967357e8a1f8570d063c8e34492ea53b5b3f960df41ffa7a0e7f80606a8`  
		Last Modified: Wed, 09 Jul 2025 19:15:51 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330c8d4dbf222300c0348e463e816e028a90dc4130ae33dba043e387f28e4584`  
		Last Modified: Wed, 09 Jul 2025 19:15:50 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b38b14de3d30685448a898c3d54ef6c1ff2a893701287dc616bb58cacc03e6c`  
		Last Modified: Wed, 09 Jul 2025 19:15:51 GMT  
		Size: 76.9 KB (76928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95adc618b6128526c5ae6c81bbc9f04c130eda6f1f1807f9ee4b4a1a110c44f2`  
		Last Modified: Wed, 09 Jul 2025 19:15:51 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ab2ffaedf7026744755d809067977c18ec3570b85c253d7a19d77107f25788`  
		Last Modified: Wed, 09 Jul 2025 19:15:54 GMT  
		Size: 40.6 MB (40554270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffba481cf034af451b34136a5d51b8f4e257ad90bab72d687ab9e65f8df11faa`  
		Last Modified: Wed, 09 Jul 2025 19:15:51 GMT  
		Size: 92.9 KB (92947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
