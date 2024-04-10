## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:ec40de8bda4272e2f49eb35f1f1bf2c48e9b40a4145d1269afea3cffe86a9acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.20348.2402; amd64

```console
$ docker pull eclipse-temurin@sha256:74a28d28a314b1a0e282210df7dedfa00d0a41e99d38cad92bdc819de770cae0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.5 MB (164480282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc34bbe9163dcc86063716efd4fa61f8225c87399a7009a9df6582d73b55529`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Apr 2024 08:53:11 GMT
RUN Apply image 10.0.20348.2402
# Wed, 10 Apr 2024 00:34:53 GMT
SHELL [cmd /s /c]
# Wed, 10 Apr 2024 00:36:12 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 10 Apr 2024 00:36:13 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 10 Apr 2024 00:36:13 GMT
USER ContainerAdministrator
# Wed, 10 Apr 2024 00:36:25 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Apr 2024 00:36:25 GMT
USER ContainerUser
# Wed, 10 Apr 2024 00:37:13 GMT
COPY dir:dc1e2da1c34561e3d80ae1d96f99e65841adfcbd6fe35da2f57cba6532915179 in C:\openjdk-11 
# Wed, 10 Apr 2024 00:37:26 GMT
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
	-	`sha256:fe62c8f081ea94a2840d89a47a30f866461fb652b13420a361d22749e8d09ff6`  
		Last Modified: Wed, 10 Apr 2024 01:00:51 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7362c835f62465014a8f53d706a07a1c7592958e8a8b3eb8d336811a94abd2`  
		Last Modified: Wed, 10 Apr 2024 01:00:51 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d72dee54d13dfb5a7c9be8a78d200fb7e1e432dfa934c19bd751f29eba4764`  
		Last Modified: Wed, 10 Apr 2024 01:00:51 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a2d872d1a8c8ca8f858ef0e089f456f747b9c89290beb05d79ea68b4c9852e`  
		Last Modified: Wed, 10 Apr 2024 01:00:49 GMT  
		Size: 76.3 KB (76314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfdfb98f977eea3476d922090d5b0fed8cd14c9beba7b6768c36b32d4e1b669`  
		Last Modified: Wed, 10 Apr 2024 01:00:49 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ee9283dc2ce1b8dd7a430f687fbe54748643c8554d8c6c5a33d15143113fc1`  
		Last Modified: Wed, 10 Apr 2024 01:01:29 GMT  
		Size: 43.3 MB (43345149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc84c80f8ee493873056ae6a6ead99383f798f386f902a280d52401845d34ac`  
		Last Modified: Wed, 10 Apr 2024 01:01:20 GMT  
		Size: 59.7 KB (59714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.17763.5696; amd64

```console
$ docker pull eclipse-temurin@sha256:1301f6e2d210a8b95fa2739374ea3b2b61c8d0b426599708120d28cbe139f6d8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148385431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f92621e8a2fefe49718032f40c6009b8ad5ef328448c166fe54a99e3245e4afb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Tue, 09 Apr 2024 23:42:55 GMT
SHELL [cmd /s /c]
# Tue, 09 Apr 2024 23:54:30 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Tue, 09 Apr 2024 23:54:31 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 09 Apr 2024 23:54:32 GMT
USER ContainerAdministrator
# Tue, 09 Apr 2024 23:54:43 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Apr 2024 23:54:44 GMT
USER ContainerUser
# Wed, 10 Apr 2024 00:00:15 GMT
COPY dir:dc1e2da1c34561e3d80ae1d96f99e65841adfcbd6fe35da2f57cba6532915179 in C:\openjdk-11 
# Wed, 10 Apr 2024 00:00:27 GMT
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
	-	`sha256:5f16f0e7f86e5499e3d870364f63dbd370a55ff738ee6bef4c4340829890d900`  
		Last Modified: Wed, 10 Apr 2024 00:50:28 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593504936f0edbc3eaab1525ed4b17a82433d794bb0f04f856685cf375b1a661`  
		Last Modified: Wed, 10 Apr 2024 00:50:28 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609f4d236ddb5c89d5b366972ac4d2a64e250c154ea152d3d5e87f030c95c497`  
		Last Modified: Wed, 10 Apr 2024 00:50:27 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06f9df0f7cd204cb5a1f15c97f306b3fa7a380939dd6371f272cb1fbf3c6a978`  
		Last Modified: Wed, 10 Apr 2024 00:50:26 GMT  
		Size: 66.8 KB (66824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4622d3a63be6fea5cefae36fd00c8ba5ecd94c84b47c17e60d84a3d87a3ae48`  
		Last Modified: Wed, 10 Apr 2024 00:50:25 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9e747101b5216fe4474fec08fe1338652eeb02fe96cc83b099ee82806f9256`  
		Last Modified: Wed, 10 Apr 2024 00:51:39 GMT  
		Size: 43.3 MB (43345035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb9835e7c7e728c9b75f9a26c04f88d2fc41fb35a36d7d4ad21fff07020e1b2`  
		Last Modified: Wed, 10 Apr 2024 00:51:32 GMT  
		Size: 78.7 KB (78663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
