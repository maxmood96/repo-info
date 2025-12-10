## `eclipse-temurin:17-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:70f4b17f0697cac7f08375baa0096de3263fb7d592d8297c8888b2f2b39eb252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.26100.7462; amd64

```console
$ docker pull eclipse-temurin@sha256:e8b1e62d1ca040d928fea42526f6669455f59425732c439e38e32a3deff38027
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242869168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a0c2bda3350359d1bcab3585411566270104284b55e532b1a4189fb88106dd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Dec 2025 21:31:34 GMT
RUN Apply image 10.0.26100.7462
# Tue, 09 Dec 2025 21:12:48 GMT
SHELL [cmd /s /c]
# Tue, 09 Dec 2025 21:14:32 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Tue, 09 Dec 2025 21:14:32 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 09 Dec 2025 21:14:33 GMT
USER ContainerAdministrator
# Tue, 09 Dec 2025 21:14:34 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Dec 2025 21:14:35 GMT
USER ContainerUser
# Tue, 09 Dec 2025 21:14:41 GMT
COPY dir:6bccbcbb352f3cf6e189ef0696470e3588f387208e54e5af3934c804c91ec072 in C:\openjdk-17 
# Tue, 09 Dec 2025 21:14:44 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:1a092205b76ca656d8483e99445def9f0619cb3acb2688bf9a33244c43ad44ce`  
		Last Modified: Tue, 09 Dec 2025 22:15:12 GMT  
		Size: 198.9 MB (198873947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acfb819e594e1d08813b5a2124af39d689e54a1c03ce6e66c31fd39ac284a05`  
		Last Modified: Tue, 09 Dec 2025 21:13:34 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:115207245df0e5f6426e5588d8b8ec77cbeecb6c7de34a768992c22f4c9c0293`  
		Last Modified: Tue, 09 Dec 2025 21:15:01 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96434ceda7f0d56b5ee433bcaacf3137ab3145c2960cc36b47a8021e86d9f63f`  
		Last Modified: Tue, 09 Dec 2025 21:15:01 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274a3dcf8ab3c3985b8eacf66fadca77d638fcd6ea5bf822219a2347d6c906dd`  
		Last Modified: Tue, 09 Dec 2025 21:15:01 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e242dd8ba464b847c2361ba6f4a661432661f454098e60b6626773664d6d9e44`  
		Last Modified: Tue, 09 Dec 2025 21:15:01 GMT  
		Size: 73.7 KB (73710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eabb5b453bf6d42ee2e75bb6d4c4c12a3ff5b4ddda617cafc545145a2da9c93b`  
		Last Modified: Tue, 09 Dec 2025 21:15:01 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962e900efb497976bb8332c3b1794f43b10aea2b45466ac36203f32aaba19f28`  
		Last Modified: Tue, 09 Dec 2025 21:15:04 GMT  
		Size: 43.8 MB (43796196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e94f1af2447f03d222f63f664c7395cf4f308f117bbe78e1bc27eb563ecf82`  
		Last Modified: Tue, 09 Dec 2025 21:15:01 GMT  
		Size: 120.0 KB (119956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.20348.4529; amd64

```console
$ docker pull eclipse-temurin@sha256:d79f15691c3eedd55de7f0f2aea9b4227e8f6c8da395b5ae2d9ad610f54b7295
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170328041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf1a10e9b7ca848219171db65ef6c1c0421079d72bbbec62db5e16d5439ff1a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 09 Dec 2025 21:12:49 GMT
SHELL [cmd /s /c]
# Tue, 09 Dec 2025 21:12:50 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Tue, 09 Dec 2025 21:12:50 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 09 Dec 2025 21:12:51 GMT
USER ContainerAdministrator
# Tue, 09 Dec 2025 21:12:53 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Dec 2025 21:12:53 GMT
USER ContainerUser
# Tue, 09 Dec 2025 21:13:07 GMT
COPY dir:6bccbcbb352f3cf6e189ef0696470e3588f387208e54e5af3934c804c91ec072 in C:\openjdk-17 
# Tue, 09 Dec 2025 21:13:09 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39379f4668f7979dc09bdc5a0a70c7fe2057bbe447911ca76de5488139977d7`  
		Last Modified: Tue, 09 Dec 2025 21:13:27 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9713517f30967be19703ff2c9241b1cee2f4d5440f72c943a57cc0acaa46441`  
		Last Modified: Tue, 09 Dec 2025 21:13:27 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6ad364c489a161d4fdcfcb8417b752a7d88bbb7960536d1aa35eee07f2fce4`  
		Last Modified: Tue, 09 Dec 2025 21:13:27 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6511dc1b7b846792caf025249f6df9dd5729e6d6cbe0f950bc303c9ac67904e`  
		Last Modified: Tue, 09 Dec 2025 21:13:27 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf62b5ab5e958afc38c006842bbccae84540f5027da221b48f2511de2ff2637`  
		Last Modified: Tue, 09 Dec 2025 21:13:27 GMT  
		Size: 76.5 KB (76540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766f7e0033d31a55cba66dfe0f2773022843da82aa274050a25a13f2e48025d0`  
		Last Modified: Tue, 09 Dec 2025 21:13:27 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7e807a57d55ecb0a42f2326cf21fa0e0152d3b8de4c3a7c39b574917dfcc0e`  
		Last Modified: Tue, 09 Dec 2025 21:13:34 GMT  
		Size: 43.8 MB (43796086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04c494407870408201ad7aa1c8ebccd856aa6dc4880dffa74e85d625c9bf844`  
		Last Modified: Tue, 09 Dec 2025 21:13:27 GMT  
		Size: 91.8 KB (91758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
