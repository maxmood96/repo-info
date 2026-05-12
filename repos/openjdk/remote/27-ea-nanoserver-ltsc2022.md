## `openjdk:27-ea-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:a3f0c92ac1c1612db39e5927fb24fd50ab38cd244ae82867af3504d07eaee394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `openjdk:27-ea-nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull openjdk@sha256:0f15f8ca8656e00f90ea7dcdd00a9c38939949508b80b2808413ee4c898e3f40
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.9 MB (351920992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f50b0268cf78594b4bccdd0d225033f1c7db22f6d0f0a8adfa460b3a54a01f9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 12 May 2026 01:13:21 GMT
SHELL [cmd /s /c]
# Tue, 12 May 2026 01:13:23 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 12 May 2026 01:13:24 GMT
USER ContainerAdministrator
# Tue, 12 May 2026 01:13:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 12 May 2026 01:13:40 GMT
USER ContainerUser
# Tue, 12 May 2026 01:13:40 GMT
ENV JAVA_VERSION=27-ea+21
# Tue, 12 May 2026 01:14:39 GMT
COPY dir:21b86086b1737f2f7722d7588722f1390e0aa73709337ec2a22a64f142e83a09 in C:\openjdk-27 
# Tue, 12 May 2026 01:14:46 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 12 May 2026 01:14:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c0e7d1d787fd39b9f526ba057571470bbca5132d415d190f69cab3a17f34c81`  
		Last Modified: Tue, 12 May 2026 01:14:54 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202c171928413ef123eaf793429de5c40048a8729b300c9bee98a78bc8922425`  
		Last Modified: Tue, 12 May 2026 01:14:54 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9f4905a8dc2f331e4027a53cf319c8fdc114e3bcab56e6dd6b035e60aa04c1`  
		Last Modified: Tue, 12 May 2026 01:14:54 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659e0264621cb0960ce28e4a3e6460999c1b6f007755522dcfe5b4a3cfb944ac`  
		Last Modified: Tue, 12 May 2026 01:14:54 GMT  
		Size: 71.2 KB (71188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421ab21e165f4d0c5cfd8b33070c5e2a1d9586367404ba45dd7d7a16fbcfa914`  
		Last Modified: Tue, 12 May 2026 01:14:53 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402355f3f7d95766695847ba3c933a7ecdcbe18f75adccfa2eb8a740dcaffcbf`  
		Last Modified: Tue, 12 May 2026 01:14:53 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96203b234b1d2b8706ac00ab0acdadbc272a5246cebd2acb3bf4dbf1aa1947d`  
		Last Modified: Tue, 12 May 2026 01:15:07 GMT  
		Size: 224.8 MB (224768943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f20cb292ceb73362a06a0fdc6b1343ca94837c82a869a09effd77801103e306`  
		Last Modified: Tue, 12 May 2026 01:14:53 GMT  
		Size: 118.5 KB (118524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c02d4ed79bdc92173fa5292554456e1ad10a733050c1fcc677cbf9cba7d319`  
		Last Modified: Tue, 12 May 2026 01:14:53 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
