## `openjdk:18-ea-7-nanoserver`

```console
$ docker pull openjdk@sha256:07965c83c7c225e66428d8bd1f4b443150df01a3809b9e6dcd8ba51d369b31bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `openjdk:18-ea-7-nanoserver` - windows version 10.0.17763.2061; amd64

```console
$ docker pull openjdk@sha256:4ea9bf09001219011111a98b9a8937028c8a380a888c7e3e72ee547563ff7e4c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289080620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b0a8f82600326ec18405c86a8293a2f1dca07b7ed0a9c92bfc99ea009209f18`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 06 Jul 2021 20:06:39 GMT
RUN Apply image 1809-amd64
# Wed, 14 Jul 2021 02:53:30 GMT
SHELL [cmd /s /c]
# Wed, 14 Jul 2021 02:53:36 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 14 Jul 2021 02:53:44 GMT
USER ContainerAdministrator
# Wed, 14 Jul 2021 02:54:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 14 Jul 2021 02:54:08 GMT
USER ContainerUser
# Fri, 23 Jul 2021 21:19:02 GMT
ENV JAVA_VERSION=18-ea+7
# Fri, 23 Jul 2021 21:19:20 GMT
COPY dir:4316257d011fe407011d703e5fcf4e0ae83997a4b6263c8b5dee96527845f784 in C:\openjdk-18 
# Fri, 23 Jul 2021 21:19:50 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 23 Jul 2021 21:19:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:29d43e56445c5279a6386c4dfe4d1ada3c7124ade9cb7b0f2757e58ffc7cd10b`  
		Size: 102.7 MB (102725622 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:78d8754fb12dd351c91bed29d92c703cddb135a78d8f056b6a3bf13a251c1d2d`  
		Last Modified: Wed, 14 Jul 2021 03:42:27 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89509de1f10eea36c6e14a8f32bc735a7e52e07235bb588c9dff480855c851c0`  
		Last Modified: Wed, 14 Jul 2021 03:42:25 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a172401c9271ad5ee8356c8f36a409f68259854e9de596e04069a2a176db3c6`  
		Last Modified: Wed, 14 Jul 2021 03:42:25 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3247de649752bd08242527a227d09c6398c2676025c2527f3b65c5c8cd032886`  
		Last Modified: Wed, 14 Jul 2021 03:42:24 GMT  
		Size: 69.9 KB (69948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1baf3b57ea2d376291b5174f1db66c9b8d971170b6ec871bdbd1fc496e82d65`  
		Last Modified: Wed, 14 Jul 2021 03:42:22 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88cfd4d793a830f0393aa244ddabbafa8542b6de2937faf3a0f1d19bc136f1f5`  
		Last Modified: Fri, 23 Jul 2021 21:25:44 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6e03e64bc545367a37c9b1ade631e0287926e8dfa00234c29cb96483e13b13`  
		Last Modified: Fri, 23 Jul 2021 21:29:18 GMT  
		Size: 182.7 MB (182656692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2c7b88ecdc9fc093771dfce49eacdd167d191e5707711312fac02a5ef2c90c`  
		Last Modified: Fri, 23 Jul 2021 21:25:49 GMT  
		Size: 3.6 MB (3621499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4836cd22f5f3144f1a622b3775f208b4faacf9e07b8ff5c72664b3ec1399c066`  
		Last Modified: Fri, 23 Jul 2021 21:25:45 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
