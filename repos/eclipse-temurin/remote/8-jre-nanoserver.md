## `eclipse-temurin:8-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:6e57830ba3b588051de858bf4ea9d161d5add6ff5858819d243212ecb96d3015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1970; amd64
	-	windows version 10.0.17763.4851; amd64

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.20348.1970; amd64

```console
$ docker pull eclipse-temurin@sha256:6237d78a28473e9db2914f8f79c684405caa717eb3615d2d8add3b49011eb779
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160695325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2467dbd6cf9fe78bcdd36fa7e11b277f7bbd2d0b2e6583c1a81edb2fc2628935`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 01 Sep 2023 00:20:14 GMT
RUN Apply image 10.0.20348.1970
# Wed, 13 Sep 2023 03:28:54 GMT
SHELL [cmd /s /c]
# Wed, 13 Sep 2023 03:28:54 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Wed, 13 Sep 2023 03:28:55 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 13 Sep 2023 03:28:55 GMT
USER ContainerAdministrator
# Wed, 13 Sep 2023 03:29:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Sep 2023 03:29:10 GMT
USER ContainerUser
# Wed, 13 Sep 2023 03:29:51 GMT
COPY dir:f24575d0fd9e2979f5a8010c202ec6d963a3eb3cd788517e3ab1d758c8e6ad81 in C:\openjdk-8 
# Wed, 13 Sep 2023 03:29:59 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:8f8cef0759210af9d01a2fb45d79956a2db738bbd3734b7244b17e14ad945cab`  
		Last Modified: Tue, 12 Sep 2023 18:47:39 GMT  
		Size: 120.6 MB (120567584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d67aef4c483590cefd40495efc212f13e4c62993e8036c20bb4e19bc8620508`  
		Last Modified: Wed, 13 Sep 2023 03:47:03 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43d2dd9d6bd96273f79aded4034d866a5bf308ff6fdb9a4fc77fc002f96629e`  
		Last Modified: Wed, 13 Sep 2023 03:47:03 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098bc84e66e639101cddcf25cf0d33716dd5a1541283c6d39575f9d0b266ca3d`  
		Last Modified: Wed, 13 Sep 2023 03:47:03 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4194e5a793aa87b0833fa13729c4e38fc062f7c7cdd646bb2edf6967bb74308f`  
		Last Modified: Wed, 13 Sep 2023 03:47:01 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4f85d1fba3b190c64bf3f6efeeb898e2f9e65e7b0f420a909e95e1f2e08a79`  
		Last Modified: Wed, 13 Sep 2023 03:47:01 GMT  
		Size: 79.4 KB (79399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9742f2dfe73293118e72bd931d6773912a26d06055e981f42f8d48120ce3dd00`  
		Last Modified: Wed, 13 Sep 2023 03:47:01 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7000541ffd9ff9b9083c292c2c0c6bdc47a1c39c0eaff1535229900f58365240`  
		Last Modified: Wed, 13 Sep 2023 03:47:32 GMT  
		Size: 40.0 MB (39981176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d200a956a697b17ba6976a288ae637e886c42f57a6251aff0b10994cd479a4be`  
		Last Modified: Wed, 13 Sep 2023 03:47:25 GMT  
		Size: 61.9 KB (61943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.17763.4851; amd64

```console
$ docker pull eclipse-temurin@sha256:5cc8b802db3e8372898c67a1b10354645ce25806c1a5ecfaafd54f119d7d0f36
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144600483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d0523e3eca216daf05f7969864017be5e74ece072af85635f46ffcdcebc872c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 29 Aug 2023 16:42:02 GMT
RUN Apply image 10.0.17763.4851
# Wed, 13 Sep 2023 02:29:44 GMT
SHELL [cmd /s /c]
# Wed, 13 Sep 2023 02:29:45 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Wed, 13 Sep 2023 02:29:45 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 13 Sep 2023 02:29:46 GMT
USER ContainerAdministrator
# Wed, 13 Sep 2023 02:29:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Sep 2023 02:29:57 GMT
USER ContainerUser
# Wed, 13 Sep 2023 02:34:49 GMT
COPY dir:f24575d0fd9e2979f5a8010c202ec6d963a3eb3cd788517e3ab1d758c8e6ad81 in C:\openjdk-8 
# Wed, 13 Sep 2023 02:35:02 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:17ba6b878467260559b72cb6f7e79c829eae67862a09efe87f6dc324f49fc086`  
		Last Modified: Tue, 12 Sep 2023 18:31:40 GMT  
		Size: 104.5 MB (104492504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a5bcbc9b0f0398bf8f14c235b24ba85d9acacf855518119cd1ce338a235a15`  
		Last Modified: Wed, 13 Sep 2023 03:36:33 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c2888b3f642e1b1385bfbf9deb93337f9ce2cc85d2b9d4bd36a6521d748567`  
		Last Modified: Wed, 13 Sep 2023 03:36:32 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac76b5fd5d37abc0b888fbadaca1529600eda8aa3cc72071592093ef8449318`  
		Last Modified: Wed, 13 Sep 2023 03:36:32 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c67d9ddb3e1826ea731a3f80884c665c21a5148abff12818787a5e47caae56f`  
		Last Modified: Wed, 13 Sep 2023 03:36:30 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e2efbb2925f0780ee2abcaff75dc2aa71939a7210d065703fbf6705008b8ac`  
		Last Modified: Wed, 13 Sep 2023 03:36:30 GMT  
		Size: 76.5 KB (76484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15e73b36640cedf631491a32e1f42dfab668944efd20ea45ecd333720639f4a`  
		Last Modified: Wed, 13 Sep 2023 03:36:30 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5c786c9ba6bb610c58930086a574117c0e47cdca19964bedd2d13208fd099a`  
		Last Modified: Wed, 13 Sep 2023 03:37:42 GMT  
		Size: 40.0 MB (39978995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76c7080e63932b6f7b521f13416780c2e7b4adb22c92174ff50034a437da43e`  
		Last Modified: Wed, 13 Sep 2023 03:37:36 GMT  
		Size: 46.7 KB (46694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
