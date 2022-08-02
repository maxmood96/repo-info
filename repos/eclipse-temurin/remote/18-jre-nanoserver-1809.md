## `eclipse-temurin:18-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:41b74ba7496e6dfb4c9c5b37fd34141a8a8eb23c2a030f808f1f87452264ab02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `eclipse-temurin:18-jre-nanoserver-1809` - windows version 10.0.17763.3165; amd64

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
