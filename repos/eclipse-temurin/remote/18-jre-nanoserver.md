## `eclipse-temurin:18-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:eca100065ab55206487d83ce8e7066ad1ec016b223deec2374da8980647390b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.825; amd64
	-	windows version 10.0.17763.3165; amd64

### `eclipse-temurin:18-jre-nanoserver` - windows version 10.0.20348.825; amd64

```console
$ docker pull eclipse-temurin@sha256:4f59ce087e5dde52ee689be76f29bb39fc7cbccf9640dab1aa3a669b5f07fd4a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.4 MB (161350769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e3785ae11a8f164f33378709e39ca815661e00ebfa1244ec30f01eb534fa40`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Tue, 02 Aug 2022 18:39:06 GMT
COPY dir:cb1a0a94a679a671d2c9a1c60ff27dfac7a1768220183b4bef29235250155a74 in C:\openjdk-18 
# Tue, 02 Aug 2022 18:39:22 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:45c7ac7eb4c64c7c8ff83693b8fee20309eb96ed362fcfb3126ecb647d8329d2`  
		Last Modified: Tue, 02 Aug 2022 18:48:35 GMT  
		Size: 43.2 MB (43152996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456a3909f9c58534f0751cec165a2a6cac3959ed38b30d795acd7f3c4e1389b5`  
		Last Modified: Tue, 02 Aug 2022 18:48:27 GMT  
		Size: 58.4 KB (58368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:18-jre-nanoserver` - windows version 10.0.17763.3165; amd64

```console
$ docker pull eclipse-temurin@sha256:fb8a332915b8a5b6f9c6d5d2743090e0393b604fe0cae9d24ff882beda9c2e42
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.3 MB (149328954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffc2d6510ed058593058751df2c25ac99f921f60a7a17d39b831b4fd00364ac`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 06 Jul 2022 22:15:10 GMT
RUN Apply image 10.0.17763.3165
# Wed, 13 Jul 2022 14:50:41 GMT
SHELL [cmd /s /c]
# Tue, 02 Aug 2022 18:31:15 GMT
ENV JAVA_VERSION=jdk-18.0.2+9
# Tue, 02 Aug 2022 18:31:16 GMT
ENV JAVA_HOME=C:\openjdk-18
# Tue, 02 Aug 2022 18:31:17 GMT
USER ContainerAdministrator
# Tue, 02 Aug 2022 18:31:24 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 02 Aug 2022 18:31:25 GMT
USER ContainerUser
# Tue, 02 Aug 2022 18:35:55 GMT
COPY dir:cb1a0a94a679a671d2c9a1c60ff27dfac7a1768220183b4bef29235250155a74 in C:\openjdk-18 
# Tue, 02 Aug 2022 18:36:11 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:5d24e1a2f5c566b0afb1e46fc24e5cec821c8ebf44220276a95a2b91f44a2f2a`  
		Size: 103.2 MB (103155009 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3b09c07c6aeead64423fdefc240fe2e1b6330c96732fd2705113030da84416be`  
		Last Modified: Mon, 18 Jul 2022 21:22:33 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c6cd1224aed638f34d45a2530b69b7ae437447bf4803c266bda64f1170a5b7`  
		Last Modified: Tue, 02 Aug 2022 18:45:42 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d4c3e4829bdbc66d515e3daa3e0f48c044b164356469472365349567c982dd`  
		Last Modified: Tue, 02 Aug 2022 18:45:42 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f258ddf5e5681c6683143098201111c0fbe98cf60f13415b9e892692e8ec36b`  
		Last Modified: Tue, 02 Aug 2022 18:45:42 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf25e71a675bf8e5ea332993e70f6fdfa0e54de9df5a1e601fa4baacaa88a170`  
		Last Modified: Tue, 02 Aug 2022 18:45:39 GMT  
		Size: 68.3 KB (68337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8af2269cf951340b30ec707908a31c297b0c7189a8bda61baf5c0389a1b772`  
		Last Modified: Tue, 02 Aug 2022 18:45:39 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7af9c8e430c8ea2c78a0c1aeeaabf8745dd9efc808addb67dcbd2d78f1c1cf0`  
		Last Modified: Tue, 02 Aug 2022 18:46:59 GMT  
		Size: 43.1 MB (43148285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4368398b88371475e3e58ad7dd6886fcbcfe42e111f5d80f9966390d137cf56`  
		Last Modified: Tue, 02 Aug 2022 18:46:51 GMT  
		Size: 3.0 MB (2951540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
