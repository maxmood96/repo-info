## `openjdk:27-ea-nanoserver`

```console
$ docker pull openjdk@sha256:cd10516e2334770af579e877b708c9588a4d8ab3769b135661e78efe3c85170c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `openjdk:27-ea-nanoserver` - windows version 10.0.26100.32522; amd64

```console
$ docker pull openjdk@sha256:ebbb22ade2e24bcd26c550eee995d9c056dd40864ac4e1efb3c469585ada9f83
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.0 MB (423964478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbdae8f1b16a302f1ae3a361da023f179903e2e68280d144e76cc3946eef567`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Mar 2026 01:45:55 GMT
RUN Apply image 10.0.26100.32522
# Mon, 23 Mar 2026 19:10:30 GMT
SHELL [cmd /s /c]
# Mon, 23 Mar 2026 19:10:33 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 23 Mar 2026 19:10:33 GMT
USER ContainerAdministrator
# Mon, 23 Mar 2026 19:10:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 23 Mar 2026 19:10:48 GMT
USER ContainerUser
# Mon, 23 Mar 2026 19:10:49 GMT
ENV JAVA_VERSION=27-ea+14
# Mon, 23 Mar 2026 19:12:03 GMT
COPY dir:1e03a1eeb0a7b9a5151c618212b4c0b4b3701f1a28f72fad799e2bd29790a005 in C:\openjdk-27 
# Mon, 23 Mar 2026 19:12:11 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 23 Mar 2026 19:12:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:06fab7822816d5f43d6835d07ac8db280fdf81384187f36d8dc43bbb7064a76d`  
		Last Modified: Tue, 10 Mar 2026 20:41:46 GMT  
		Size: 199.4 MB (199409325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9bf29e80d1fd75992fc0fce18981ebd29c465839433846c536be8b695161b62`  
		Last Modified: Mon, 23 Mar 2026 19:12:17 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ac65a694b879efbf5c890f284fa695aa69cdcdaac9e042e5b08a15bf63a62b`  
		Last Modified: Mon, 23 Mar 2026 19:12:17 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da882868ce717a01980946ee73a02dfd548bb7b244f5d0a6b4577f93ad64395c`  
		Last Modified: Mon, 23 Mar 2026 19:12:17 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c4a5811acd879c92bd3389c8343b9a7c467e4dad1077383f98971e0f81a1c3`  
		Last Modified: Mon, 23 Mar 2026 19:12:17 GMT  
		Size: 70.1 KB (70097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23cf3993b0be600f74dcd497b8baf1d3e8bec8a8612b4fd58b488ee0989e93b6`  
		Last Modified: Mon, 23 Mar 2026 19:12:15 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01daa444604adb1d61737ceeb1c721a6ab4b9262622cd4d8e0eafef58fe78912`  
		Last Modified: Mon, 23 Mar 2026 19:12:15 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba87180a861100fbbdd2b82be02c9466d3598ac519a850ed27283f65c8f7d24`  
		Last Modified: Mon, 23 Mar 2026 19:12:30 GMT  
		Size: 224.4 MB (224386376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71bb75fe01a5136b372ed91d586db967bff60e82419607f694631c0586ca537`  
		Last Modified: Mon, 23 Mar 2026 19:12:15 GMT  
		Size: 92.3 KB (92287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e367242775bb904a66b560d2abe9d6c79cd083c2119ad61134a7413810daefa2`  
		Last Modified: Mon, 23 Mar 2026 19:12:15 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-nanoserver` - windows version 10.0.20348.4893; amd64

```console
$ docker pull openjdk@sha256:bc8850003c0e14187bdfc0944b4a47956e3d85d62605280a01af9dd2d7378ce3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.3 MB (351273269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e5677db67264b274fa6e5e1de04c61056b5d062290d2fbbc2f42a408113771`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Mon, 23 Mar 2026 19:13:00 GMT
SHELL [cmd /s /c]
# Mon, 23 Mar 2026 19:13:01 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 23 Mar 2026 19:13:01 GMT
USER ContainerAdministrator
# Mon, 23 Mar 2026 19:13:03 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 23 Mar 2026 19:13:03 GMT
USER ContainerUser
# Mon, 23 Mar 2026 19:13:04 GMT
ENV JAVA_VERSION=27-ea+14
# Mon, 23 Mar 2026 19:14:50 GMT
COPY dir:1e03a1eeb0a7b9a5151c618212b4c0b4b3701f1a28f72fad799e2bd29790a005 in C:\openjdk-27 
# Mon, 23 Mar 2026 19:15:01 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 23 Mar 2026 19:15:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9ec82d1173531df98af54b6ffc8842a8d9d02c18f4306bbb7f5a6697391bce`  
		Last Modified: Mon, 23 Mar 2026 19:15:08 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1137eada5f23a8390783535e9b77e2997eb929a64ae065ab06bf90b31dab40`  
		Last Modified: Mon, 23 Mar 2026 19:15:08 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c35a8ec2fa2d2fea4f7302e4b16b37ed122272133523edccc01357eb2db342`  
		Last Modified: Mon, 23 Mar 2026 19:15:08 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fedcd7712b25e05f40327eb4508b6d870c854fd995d7b00391b9b467d376c6a`  
		Last Modified: Mon, 23 Mar 2026 19:15:08 GMT  
		Size: 77.0 KB (77049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d8bd01f1550e7a780e3c645c334a6e7292fba3fa620e23c1c5a818c87914ea`  
		Last Modified: Mon, 23 Mar 2026 19:15:06 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb766dcadba977adad4f0a23d987318ec6fbcaaa5abb0913041dd1fb3c5c036`  
		Last Modified: Mon, 23 Mar 2026 19:15:06 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e8e09277dd965c9ac5b9462fc267c53026b094bd01df3a40e1e9c6ff25f2f27`  
		Last Modified: Mon, 23 Mar 2026 19:15:21 GMT  
		Size: 224.4 MB (224386459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4caa734ac7f2f369297da801c5f60561f71086b813605deb4bb3865fd39bd6f`  
		Last Modified: Mon, 23 Mar 2026 19:15:06 GMT  
		Size: 152.9 KB (152882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7437e2ebfbac0ea67e25101823547c0874fdc71d41679cb73301f2a89a420a8d`  
		Last Modified: Mon, 23 Mar 2026 19:15:06 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
