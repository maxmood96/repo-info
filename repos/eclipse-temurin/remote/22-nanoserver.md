## `eclipse-temurin:22-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:9590c4e21816b92a292162194bbb727ff6a4050ee2af7e363eee353d20fb2ad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `eclipse-temurin:22-nanoserver` - windows version 10.0.20348.2402; amd64

```console
$ docker pull eclipse-temurin@sha256:9406e02be4d0d3ec615116d086c1361eecb87b5abec875b0185ed431d89bf9b0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.2 MB (321174056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46f376eee9c9ff81700fb0c6e583e86e0db6f4315cbb7534b98b213ea20417b6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Apr 2024 08:53:11 GMT
RUN Apply image 10.0.20348.2402
# Wed, 10 Apr 2024 00:34:53 GMT
SHELL [cmd /s /c]
# Wed, 10 Apr 2024 00:40:19 GMT
ENV JAVA_VERSION=jdk-22+36
# Wed, 10 Apr 2024 00:40:20 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 10 Apr 2024 00:40:21 GMT
USER ContainerAdministrator
# Wed, 10 Apr 2024 00:40:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Apr 2024 00:40:31 GMT
USER ContainerUser
# Wed, 10 Apr 2024 00:40:46 GMT
COPY dir:50e69279b8e7c7c9492973898e59a003d16331dced94fbda5fe70c6e2f10acc9 in C:\openjdk-22 
# Wed, 10 Apr 2024 00:41:00 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Apr 2024 00:41:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:755fc767289b8847bd0d0d8d75efc308c040140acf2a3426973ba9fbf022c4c0`  
		Last Modified: Tue, 09 Apr 2024 23:50:18 GMT  
		Size: 121.0 MB (120993754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70887eeae6a5d6d5fd81661024afc84fee637f674dee5e7127112cbfce90750`  
		Last Modified: Wed, 10 Apr 2024 01:00:01 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2fb0d9a77a72d9bcd9e2571d43678ec7cdbd36fa04817c766e3629434c90ace`  
		Last Modified: Wed, 10 Apr 2024 01:03:20 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7584ce14c659083fbc4898e8fc6dd6813e919285f680b44a48916c549504fb`  
		Last Modified: Wed, 10 Apr 2024 01:03:20 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113fffa2e102ada8b3611a56f23c0b15a5118850881d7c58ce938c8190d3e4f8`  
		Last Modified: Wed, 10 Apr 2024 01:03:20 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf022c1012c448e2444fd3ac66c18203719fe5307e49ac8c8823db4428296274`  
		Last Modified: Wed, 10 Apr 2024 01:03:18 GMT  
		Size: 76.9 KB (76881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3d2f58650e4ea177e80de5227843bec54db0abfad8bcf0a22549cb7fa9d5ff`  
		Last Modified: Wed, 10 Apr 2024 01:03:18 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f275f8b636cd42809ba339c8f6cc49771a2ab50735fbda47e5544c948c524c95`  
		Last Modified: Wed, 10 Apr 2024 01:03:39 GMT  
		Size: 200.0 MB (200037387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77846923089410e0cf3d648453d1edf00a2791a7f322dd384601667b6e9da4e6`  
		Last Modified: Wed, 10 Apr 2024 01:03:18 GMT  
		Size: 59.6 KB (59639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540e32c9d6c861f391ee55bd0866f4b190625a43a826bb04276586804536fec9`  
		Last Modified: Wed, 10 Apr 2024 01:03:18 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22-nanoserver` - windows version 10.0.17763.5696; amd64

```console
$ docker pull eclipse-temurin@sha256:495d0f4057d2040684f81d538816b5171517004e8a082a8d2dc3cb833e722e24
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.8 MB (308833351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3412567234e6e805842da85a9c3f5764b90d4b0c6955d6c4f5f2e09f4e579b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Tue, 09 Apr 2024 23:42:55 GMT
SHELL [cmd /s /c]
# Wed, 10 Apr 2024 00:29:04 GMT
ENV JAVA_VERSION=jdk-22+36
# Wed, 10 Apr 2024 00:29:05 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 10 Apr 2024 00:29:06 GMT
USER ContainerAdministrator
# Wed, 10 Apr 2024 00:29:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Apr 2024 00:29:15 GMT
USER ContainerUser
# Wed, 10 Apr 2024 00:29:31 GMT
COPY dir:50e69279b8e7c7c9492973898e59a003d16331dced94fbda5fe70c6e2f10acc9 in C:\openjdk-22 
# Wed, 10 Apr 2024 00:29:44 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Apr 2024 00:29:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b591b5f81c02344da39dc8a9084b5791cbf552c1eb85e79db1f38dfc715a681`  
		Last Modified: Wed, 10 Apr 2024 00:47:46 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4af1a61fa1468ae79b53f42f8af23a93d321f74d116f4288cd7d7babbd41b4a`  
		Last Modified: Wed, 10 Apr 2024 00:58:33 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438da6a337d2fc0f98f65dd0bdf2976cb7a23a7559a0a1977397018158346fbb`  
		Last Modified: Wed, 10 Apr 2024 00:58:33 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd60f7f19a881ba7cde39a4da8c2a6b9a7eb3101cb25974cbeeacab094ed646`  
		Last Modified: Wed, 10 Apr 2024 00:58:33 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27d27098f47173b90e24c0243907c4bc956cf59279762c933d3b236f5467350`  
		Last Modified: Wed, 10 Apr 2024 00:58:31 GMT  
		Size: 67.9 KB (67895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8380d41d8bd639dadc09f22747b99fa78fc08923e1af1f533e79f8b1a86eff0`  
		Last Modified: Wed, 10 Apr 2024 00:58:31 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e96844c930ae1ea91abb4c1576bc3e90e5eebf12dd72639fe38253d715028b`  
		Last Modified: Wed, 10 Apr 2024 00:58:51 GMT  
		Size: 200.0 MB (200037279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea32bb444daedcb2864236876fd452009e8dbb22563f1102d67a261c6ad3eb8`  
		Last Modified: Wed, 10 Apr 2024 00:58:32 GMT  
		Size: 3.8 MB (3832443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1659e7278c6de125480dc3a51e3cb29bf5704877d9a5ad85441bad6d5dbcd7da`  
		Last Modified: Wed, 10 Apr 2024 00:58:31 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
