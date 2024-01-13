## `openjdk:22-ea-31-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:330aac773e4be9c60d54e337413962b916cc5320e8358a893d3917884c398c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `openjdk:22-ea-31-jdk-nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull openjdk@sha256:e8943f00acedef238c9189b4b9140cfc251441b1de6938b9286165dedb9d3fde
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305883176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc9579925b65efd57038a1961ac19409b43a4246ef133cd2c2f0f6453d62f50`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Sat, 13 Jan 2024 02:09:54 GMT
SHELL [cmd /s /c]
# Sat, 13 Jan 2024 02:09:55 GMT
ENV JAVA_HOME=C:\openjdk-22
# Sat, 13 Jan 2024 02:09:56 GMT
USER ContainerAdministrator
# Sat, 13 Jan 2024 02:09:58 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 13 Jan 2024 02:09:59 GMT
USER ContainerUser
# Sat, 13 Jan 2024 02:10:00 GMT
ENV JAVA_VERSION=22-ea+31
# Sat, 13 Jan 2024 02:10:08 GMT
COPY dir:bf7b65b9466a358fb4320384cc12a22b073ecefbeec14f0a5163389c6b25cb8c in C:\openjdk-22 
# Sat, 13 Jan 2024 02:10:13 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 13 Jan 2024 02:10:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160231c8f4ad7f053b7df425b7b4ddeb2e241dd33141a40afb23b968fbd97534`  
		Last Modified: Sat, 13 Jan 2024 02:10:18 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c775980f06da10233225694c6c27d562ffae7031be6d62188bbde38cf4fb0b`  
		Last Modified: Sat, 13 Jan 2024 02:10:18 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4bb5d0e54b5693dce4cb8d3bde8a5cb0bd20fc379d742e61bc3034f72a2c2eb`  
		Last Modified: Sat, 13 Jan 2024 02:10:17 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f6ee495f6a1046902c77f1993b3e3ab184784109e2c9dd183956c9c44eaef8`  
		Last Modified: Sat, 13 Jan 2024 02:10:17 GMT  
		Size: 73.0 KB (72986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb3117fa5a5a050730932a44ffd892a97023cb33fa42b94ac9741d73c85ee86`  
		Last Modified: Sat, 13 Jan 2024 02:10:16 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de444d27bd7b846764526ab8bcb4ef696bad5ecd3bf185226f4745355ae8870`  
		Last Modified: Sat, 13 Jan 2024 02:10:16 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3549f5642a4d1c774806f40acd419328747dfc299f13679c004060c48570ed`  
		Last Modified: Sat, 13 Jan 2024 02:10:28 GMT  
		Size: 197.4 MB (197354368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c70222e76f4754fc7cd34a5b0a38dfdc2cf544f0f94f4eae81d964cc411d1d`  
		Last Modified: Sat, 13 Jan 2024 02:10:17 GMT  
		Size: 3.9 MB (3858162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73a21a853510b72e275b8d921967118673467359372ed5c83f7260c755dc2bc`  
		Last Modified: Sat, 13 Jan 2024 02:10:17 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
