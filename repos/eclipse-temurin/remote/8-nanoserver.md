## `eclipse-temurin:8-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:9e79b3efac5b0d78717b54c418621dd3efa32c329e5453fff51093ab79b4516c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1970; amd64
	-	windows version 10.0.17763.4851; amd64

### `eclipse-temurin:8-nanoserver` - windows version 10.0.20348.1970; amd64

```console
$ docker pull eclipse-temurin@sha256:4a8288c826e8f58496981256b68d2743e4908482306486b14dc0cd31065fb3bb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.2 MB (222198271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c566b00c630fb295b9471bca51acc75e2508a340b2a6ca5e7533d04e5642b4`
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
# Wed, 13 Sep 2023 03:29:22 GMT
COPY dir:809f08e9d949f52aad6441d5338932efbf6208a06192d58db41d3e3c11ba3f9f in C:\openjdk-8 
# Wed, 13 Sep 2023 03:29:35 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:43cab55a8d3900b6744dbc55b4054c600c71bf2b951c43a51c98b53a21710b0b`  
		Last Modified: Wed, 13 Sep 2023 03:47:14 GMT  
		Size: 101.5 MB (101470114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37becbd91d78bde7e45e79bbea3f4924612eae87a9858b8c9b3d54d4a6146f59`  
		Last Modified: Wed, 13 Sep 2023 03:47:01 GMT  
		Size: 76.0 KB (75951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-nanoserver` - windows version 10.0.17763.4851; amd64

```console
$ docker pull eclipse-temurin@sha256:3e540225f133bbcd89c92a3202867a0f582e3394b4b81093b80f7026157b7ce2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.1 MB (206101047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2e36dee52d62b43de6956fd966f219b5c3e00d06eb263efbf6d446027471d7`
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
# Wed, 13 Sep 2023 02:30:06 GMT
COPY dir:809f08e9d949f52aad6441d5338932efbf6208a06192d58db41d3e3c11ba3f9f in C:\openjdk-8 
# Wed, 13 Sep 2023 02:30:17 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:0f9e2a7eb08617a32b8ae48d6ea253ddf3c3158f5d480c018c9159be9fe68809`  
		Last Modified: Wed, 13 Sep 2023 03:36:45 GMT  
		Size: 101.5 MB (101479470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce653b93467b23037ef7a748c1c5f10b80ff660e82ad73f36d0f059a2c892f9e`  
		Last Modified: Wed, 13 Sep 2023 03:36:30 GMT  
		Size: 46.8 KB (46783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
