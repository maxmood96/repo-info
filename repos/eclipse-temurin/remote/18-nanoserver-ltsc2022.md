## `eclipse-temurin:18-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:5b36fde66120a39c6f33caee25f34a1aa1b0af00b0312c7b25347d03c981fbd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.825; amd64

### `eclipse-temurin:18-nanoserver-ltsc2022` - windows version 10.0.20348.825; amd64

```console
$ docker pull eclipse-temurin@sha256:048aec52e5828ddc1c700ec02ef3bef633d1f6d6efe82a3f4d1fa03bb028d9cb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.8 MB (304767771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b483b334248b197ba6df8e4e199450017eb687914bd5f1530b17a4b695080e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Jul 2022 17:25:17 GMT
RUN Apply image 10.0.20348.825
# Wed, 13 Jul 2022 15:22:06 GMT
SHELL [cmd /s /c]
# Tue, 02 Aug 2022 18:37:57 GMT
ENV JAVA_VERSION=jdk-18.0.2+9
# Tue, 02 Aug 2022 18:37:58 GMT
ENV JAVA_HOME=C:\openjdk-18
# Tue, 02 Aug 2022 18:37:58 GMT
USER ContainerAdministrator
# Tue, 02 Aug 2022 18:38:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 02 Aug 2022 18:38:08 GMT
USER ContainerUser
# Tue, 02 Aug 2022 18:38:22 GMT
COPY dir:fe0d9ce398e3d169055678c6642e68d763dc7a30e25c08274ab6c7ec599f7aba in C:\openjdk-18 
# Tue, 02 Aug 2022 18:38:47 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 02 Aug 2022 18:38:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3719b23d309b17276277110a008a58133c9fc92465d2519f2f32c9961c39887d`  
		Size: 118.0 MB (118046090 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:569505cbc9e1bcad1fbbdd7edca170e5a914864bcad2f53e1fc5d5816ecc8aa5`  
		Last Modified: Wed, 20 Jul 2022 12:54:13 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14fd3e92eedf4bc2834ae3e44899ea1698f456b7591dc19c399d19a68ff3ada4`  
		Last Modified: Tue, 02 Aug 2022 18:47:59 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9745c3a8adab54303092679ef49c97bde9e9ad04c08fee5b2d1203b1d9482a`  
		Last Modified: Tue, 02 Aug 2022 18:47:57 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a125c33ef1114518479f7c1d5a1f95de50ce96ed0f294308b91a1c38ad16ca`  
		Last Modified: Tue, 02 Aug 2022 18:47:57 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30040349e243bc3ceb667c3d654a0f0e72f9db56b7215583f47fb34e00b4624`  
		Last Modified: Tue, 02 Aug 2022 18:47:55 GMT  
		Size: 87.6 KB (87604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840e33236958960e13729532b5e1ac19cd505a878bb5c3f0a437efdc5c75b717`  
		Last Modified: Tue, 02 Aug 2022 18:47:55 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9514c0d4d5dd04977a02661f6740e598a53bc675b9a42605f0a3de4a74b1a8df`  
		Last Modified: Tue, 02 Aug 2022 18:48:14 GMT  
		Size: 186.5 MB (186540060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48a7a570da8ddef4c350c84b6e22ba6ab6b39603d339883781f5b6f659086f5`  
		Last Modified: Tue, 02 Aug 2022 18:47:55 GMT  
		Size: 87.1 KB (87125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7249f3732dab8b7e87e9c018896c07938656910eff41353e139c6538183b755b`  
		Last Modified: Tue, 02 Aug 2022 18:47:55 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
