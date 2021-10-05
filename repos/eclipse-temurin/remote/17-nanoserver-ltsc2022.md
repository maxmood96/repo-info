## `eclipse-temurin:17-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:820cd020fbf9fb0480e00410318d06fdbc077d14c056602de9e7d61d85e9813a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.230; amd64

### `eclipse-temurin:17-nanoserver-ltsc2022` - windows version 10.0.20348.230; amd64

```console
$ docker pull eclipse-temurin@sha256:29a9d810206a48888992ef1f33423a8215360d3fa3dcff4812d22686d5d4a841
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (301971046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa9a0be8a3c38f0f28a0a8774c13abe859081274a642b9a3b8dea391fbda73c3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Sep 2021 06:44:45 GMT
RUN Apply image ltsc2022-amd64
# Tue, 05 Oct 2021 22:17:48 GMT
SHELL [cmd /s /c]
# Tue, 05 Oct 2021 22:20:57 GMT
ENV JAVA_VERSION=jdk-17+35
# Tue, 05 Oct 2021 22:20:58 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 05 Oct 2021 22:20:58 GMT
USER ContainerAdministrator
# Tue, 05 Oct 2021 22:21:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 05 Oct 2021 22:21:10 GMT
USER ContainerUser
# Tue, 05 Oct 2021 22:21:27 GMT
COPY dir:ba92fda3ecc57988e3fdb5e98847d06c9e695148297ce16b53bb487a02cbd557 in C:\openjdk-17 
# Tue, 05 Oct 2021 22:21:47 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 05 Oct 2021 22:21:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:521b4ff1716af921a5cfbf2119d97dc479e9b1eb487d17d0f576ff856ab68e61`  
		Size: 116.9 MB (116897071 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:51c1c5356f69c33525116c868524e16b83d783420a64f7a7793348f61595daf2`  
		Last Modified: Tue, 05 Oct 2021 22:35:06 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b0ca96902d4102e4dcd5f578098cb2e9c378cd8c60f3362bc64f3696147c49`  
		Last Modified: Tue, 05 Oct 2021 22:37:08 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14707eff378b753ff0e2e5776bfa5c669e60006c8ec81fc4faefdecc1247b590`  
		Last Modified: Tue, 05 Oct 2021 22:37:09 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af0886857f520e7be9a477d51057efcbbd1a574811a016f2e5a02adcd8e1566`  
		Last Modified: Tue, 05 Oct 2021 22:37:08 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d97719079cce508873de08f904761d13cf929e707381e2fdbd56b5702de9214`  
		Last Modified: Tue, 05 Oct 2021 22:37:06 GMT  
		Size: 79.7 KB (79725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c96726a4fdc3d8db62ce8f5c10a4c8e01e16294b8bfd4402f8bf558ca3dddc5`  
		Last Modified: Tue, 05 Oct 2021 22:37:06 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a3fc80cfaa779dc402873249b96720731a06b8596f354fe539eec8c64c348a`  
		Last Modified: Tue, 05 Oct 2021 22:37:26 GMT  
		Size: 184.9 MB (184926394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a02e656dc4784162b9c65bc9f90e7d858c57ee5802572789fc939bcd458459`  
		Last Modified: Tue, 05 Oct 2021 22:37:06 GMT  
		Size: 60.9 KB (60925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab8e510c4454c0f89077e52792b42c22c9a775649837d0d4974806fd209aa05`  
		Last Modified: Tue, 05 Oct 2021 22:37:06 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
