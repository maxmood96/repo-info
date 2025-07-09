## `eclipse-temurin:8-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:320e94eed8877dc8ee5d9e315ed2e10f6b422e3ae82f9808ce710edbfaa22e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4652; amd64
	-	windows version 10.0.20348.3932; amd64

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.26100.4652; amd64

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

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.20348.3932; amd64

```console
$ docker pull eclipse-temurin@sha256:3f1ae717a017a250519b8937261ea8c011433a3384ea95cb8e813c86e3673765
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163369761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d1970f161fbf7d2c5236cb918f0959e3c266a41ee5881a0eb77bac17737d1f6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Jul 2025 05:15:23 GMT
RUN Apply image 10.0.20348.3932
# Wed, 09 Jul 2025 19:12:42 GMT
SHELL [cmd /s /c]
# Wed, 09 Jul 2025 19:12:43 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Wed, 09 Jul 2025 19:12:44 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 09 Jul 2025 19:12:45 GMT
USER ContainerAdministrator
# Wed, 09 Jul 2025 19:12:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Jul 2025 19:12:49 GMT
USER ContainerUser
# Wed, 09 Jul 2025 19:12:52 GMT
COPY dir:88632ffe03bdff97c0f2931283e9e8742ceaeaec8904ee54b87f8b4347f84ae7 in C:\openjdk-8 
# Wed, 09 Jul 2025 19:12:56 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:b1cf2c299ff70c52cb8ecf52e66d64d5068519867510919d8807ed2c58a54ba2`  
		Last Modified: Tue, 08 Jul 2025 21:55:51 GMT  
		Size: 122.6 MB (122630906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77606dd0217251d8037bc5b2bf924dbe90559080ee2c9d7d9bfc6412e44aa3d2`  
		Last Modified: Wed, 09 Jul 2025 19:13:26 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a9c9ac56321c9673b029fe3a2797d91440e63669a4facc63605f0ce860d412`  
		Last Modified: Wed, 09 Jul 2025 19:13:26 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:965e3cfed9b4560b01cd15382c3500521840b5887c1a9efd9f5f44f79c3ce435`  
		Last Modified: Wed, 09 Jul 2025 19:13:26 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18eaa974dd27b4991a52a60afe84eaf169edc339dada57502d6d7e3db4be7123`  
		Last Modified: Wed, 09 Jul 2025 19:13:26 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b0b1b5a88c751e587e3ca40c9b683cb4ceb533fd369d9af835dd33936da11b`  
		Last Modified: Wed, 09 Jul 2025 19:13:26 GMT  
		Size: 78.3 KB (78307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8b8051038fcf281479f5edb3012e901a180336c669d8e925a5e6a0ac18e1ba`  
		Last Modified: Wed, 09 Jul 2025 19:13:26 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bdc3a970b7ea52bb42f6242df2d7059f89d6b5a21d4f031c6a2ba1a8e013f9`  
		Last Modified: Wed, 09 Jul 2025 19:13:30 GMT  
		Size: 40.6 MB (40553633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d582a9bae4d8f9bd9576c1578acd32ca0a7b908e815e7720a04a4d89511d7add`  
		Last Modified: Wed, 09 Jul 2025 19:13:26 GMT  
		Size: 101.7 KB (101737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
