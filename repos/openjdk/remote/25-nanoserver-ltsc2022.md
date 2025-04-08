## `openjdk:25-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:770e414918825e89bc283f4269a1400e7f58fd99a16a6ad281f15aa52154b1d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `openjdk:25-nanoserver-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull openjdk@sha256:dd71ceb8b5487836df61fdbe5a84b59c4cdb3869ed35ddbb69371bda862e57ee
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.8 MB (328838463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c869babe348e53a5f396f46340f26a097243201129d1b6151bcb63476e0129e8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Mon, 07 Apr 2025 23:08:36 GMT
SHELL [cmd /s /c]
# Mon, 07 Apr 2025 23:08:38 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 07 Apr 2025 23:08:39 GMT
USER ContainerAdministrator
# Mon, 07 Apr 2025 23:09:03 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 07 Apr 2025 23:09:04 GMT
USER ContainerUser
# Mon, 07 Apr 2025 23:09:05 GMT
ENV JAVA_VERSION=25-ea+17
# Mon, 07 Apr 2025 23:09:13 GMT
COPY dir:31d4a08dd20e935927d81b33c56eb56ceaeead96529382a0c30c5f89fc836ee7 in C:\openjdk-25 
# Mon, 07 Apr 2025 23:09:20 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 07 Apr 2025 23:09:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3adbaf979377b73e57263e4d7d7d043747229f2c660dbf1fe4a9195d55275e5`  
		Last Modified: Mon, 07 Apr 2025 23:09:25 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faab8d63e2abdb03b2416da6b024d2e95de95ec200aebfeb74664687291bb841`  
		Last Modified: Mon, 07 Apr 2025 23:09:25 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2eee29df16a1094c6740eb398ec9c93c006d1aac0a694c9fe9e62cbc3eddd7`  
		Last Modified: Mon, 07 Apr 2025 23:09:24 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e07608d484196bde6b105555c7f2d14700ea95678f31e0dae8a990357be11bd`  
		Last Modified: Mon, 07 Apr 2025 23:09:25 GMT  
		Size: 89.0 KB (88987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c902cb1dd92da13661f92160e6a3593d28b835fe1d3030518f325ed041d98d3`  
		Last Modified: Mon, 07 Apr 2025 23:09:23 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7792b329ce603fdd5018083b487afea475cd1c85dfbbac4ad1661622d1b187b3`  
		Last Modified: Mon, 07 Apr 2025 23:09:24 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1342c9718f1fc7c6580c57fa6776ef39c8f0e41d846bf1befaba3fc7c95c3f`  
		Last Modified: Mon, 07 Apr 2025 23:09:34 GMT  
		Size: 208.0 MB (207954960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f750f0dc8e6cb688e9483d2939e06411f0a6ddea92ca37ad543f01c20a9e8f1`  
		Last Modified: Mon, 07 Apr 2025 23:09:24 GMT  
		Size: 92.8 KB (92775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6380fd72ad226b5425f4b5c3eb515d88afd132e2e4ddfa9c7b684508156daac2`  
		Last Modified: Mon, 07 Apr 2025 23:09:24 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
