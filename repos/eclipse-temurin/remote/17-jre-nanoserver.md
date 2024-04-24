## `eclipse-temurin:17-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:2fd2816159918024b311da0baac167e7b1cc0b318bba85061f1679cb265e3df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.20348.2402; amd64

```console
$ docker pull eclipse-temurin@sha256:796399abb19164d0c763129b399372de55c4cd9745ff2fda45ae8b7f8ac6ec80
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164590872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e227d0db47901047d69272acdb43a3d003f617bebcd8c47aaebe4ccb381af446`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Apr 2024 08:53:11 GMT
RUN Apply image 10.0.20348.2402
# Wed, 10 Apr 2024 00:34:53 GMT
SHELL [cmd /s /c]
# Wed, 24 Apr 2024 19:25:30 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Wed, 24 Apr 2024 19:25:30 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 24 Apr 2024 19:25:31 GMT
USER ContainerAdministrator
# Wed, 24 Apr 2024 19:25:42 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Apr 2024 19:25:43 GMT
USER ContainerUser
# Wed, 24 Apr 2024 19:26:30 GMT
COPY dir:a78f43753c24e3e0717a998b116850ca8c6149210b4cd2529d3fd312f361a7bd in C:\openjdk-17 
# Wed, 24 Apr 2024 19:26:43 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:42eb36e5aa255e6c8bcc5cb9c18ad4ccedf49c530604ba9b02f35889b6789bc2`  
		Last Modified: Wed, 24 Apr 2024 19:47:32 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5103f34aabbf52af3e05a6061a8c9fe58743749baef21a50077996c099dfd1d`  
		Last Modified: Wed, 24 Apr 2024 19:47:32 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a5625897aaeb515cfb6a9221b8d8d2cf1541e3fbd456171ae8338db81d2e30b`  
		Last Modified: Wed, 24 Apr 2024 19:47:32 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed26b360d3020288e8e6e73c9fddd58351aa69594dae081e1ce1f98f4797c9e3`  
		Last Modified: Wed, 24 Apr 2024 19:47:30 GMT  
		Size: 84.2 KB (84193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:215072bfc2c5689e9b3ecdc551fed92b03bf464046c64f0539ca4b8a1b3aa0b9`  
		Last Modified: Wed, 24 Apr 2024 19:47:30 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140d45eb3209114967a6a3e4439b5e34027707565086e5abead670905793cd7f`  
		Last Modified: Wed, 24 Apr 2024 19:48:09 GMT  
		Size: 43.5 MB (43454123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60411d94c8ce95dfb8771905d9f45d3aaf2b483a37ed2d0ac7bea90551f97f1e`  
		Last Modified: Wed, 24 Apr 2024 19:48:01 GMT  
		Size: 53.1 KB (53145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.17763.5696; amd64

```console
$ docker pull eclipse-temurin@sha256:3cdb992984b4dfe8ade4ebc1b8b81ace50a809f1735b8cc27f241d6399e74a31
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151392333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc1a61af9c0543c9d221886940c8429d83468eabaaf569712a1882fd03cc8e25`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Tue, 09 Apr 2024 23:42:55 GMT
SHELL [cmd /s /c]
# Wed, 24 Apr 2024 18:53:20 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Wed, 24 Apr 2024 18:53:21 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 24 Apr 2024 18:53:21 GMT
USER ContainerAdministrator
# Wed, 24 Apr 2024 18:53:31 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Apr 2024 18:53:31 GMT
USER ContainerUser
# Wed, 24 Apr 2024 18:59:10 GMT
COPY dir:a78f43753c24e3e0717a998b116850ca8c6149210b4cd2529d3fd312f361a7bd in C:\openjdk-17 
# Wed, 24 Apr 2024 18:59:24 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:197d37e4968e8edb83a3fadac388b0321ef91ab0ac4044d94c4677b22974d058`  
		Last Modified: Wed, 24 Apr 2024 19:38:47 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fa4d55aabc309b11a6e77bb489a14be3ba5fe5082275a21f4e19d40d869d7d`  
		Last Modified: Wed, 24 Apr 2024 19:38:46 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690f06c9a9b477984bb86049990f07c58444c88d4d637e1e5d7cf783384814f9`  
		Last Modified: Wed, 24 Apr 2024 19:38:46 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07757049b343da1224e7423ee382f9a4cd02b197a15106d81543b7ebcf7ecdf3`  
		Last Modified: Wed, 24 Apr 2024 19:38:44 GMT  
		Size: 65.9 KB (65879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c202c241ed06ebcaf4b839aca68d95e26fbb5686840a344ba14eb3ffc3674f9`  
		Last Modified: Wed, 24 Apr 2024 19:38:44 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82fdb6a0e6ba74d1eb2e6b6b5bfa6f4aafd143933246f717dabd29064abbad7a`  
		Last Modified: Wed, 24 Apr 2024 19:40:04 GMT  
		Size: 43.5 MB (43454478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4531ce564412c3bb7456b7f976b3c39ce9aa85224511d7cfb0b46f162137922`  
		Last Modified: Wed, 24 Apr 2024 19:39:56 GMT  
		Size: 3.0 MB (2977088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
