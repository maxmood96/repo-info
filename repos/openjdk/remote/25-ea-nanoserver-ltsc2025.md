## `openjdk:25-ea-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:656be7788aec571c95dfe167232460a3525247595170247e492234a97755b3d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `openjdk:25-ea-nanoserver-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull openjdk@sha256:a4556cfd1b93c318494ebba6acce0f8baa6397752c1df53157edf4b2ae22710d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.4 MB (414402085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39645497e134d10982af22ec85535594606c082424a625d4827f930800dd33c0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Thu, 27 Mar 2025 21:12:51 GMT
SHELL [cmd /s /c]
# Thu, 27 Mar 2025 21:12:52 GMT
ENV JAVA_HOME=C:\openjdk-25
# Thu, 27 Mar 2025 21:12:53 GMT
USER ContainerAdministrator
# Thu, 27 Mar 2025 21:12:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 27 Mar 2025 21:12:56 GMT
USER ContainerUser
# Thu, 27 Mar 2025 21:12:57 GMT
ENV JAVA_VERSION=25-ea+16
# Thu, 27 Mar 2025 21:13:05 GMT
COPY dir:19cd448448f63399f0cc00bb4ac8df0759f681650f72cc2b82002a92d2bbe677 in C:\openjdk-25 
# Thu, 27 Mar 2025 21:13:12 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 27 Mar 2025 21:13:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651258816319f8583025f1126a43a32c925fc488840490f9955160b8db9e2e79`  
		Last Modified: Thu, 27 Mar 2025 21:13:17 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4340e62aef4b69c46cb7da4165a62944688c741bf83adab4765f25b6a0fecbad`  
		Last Modified: Thu, 27 Mar 2025 21:13:17 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6b6b8caaddefdce854e9694fe716cdcd44c39e79aeb3da62ee3c377fcf6f04`  
		Last Modified: Thu, 27 Mar 2025 21:13:17 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c0f87d2173b3f8dc7aba930e7f55d1caa1ce8b3fd6de40fd97613c22d66940`  
		Last Modified: Thu, 27 Mar 2025 21:13:17 GMT  
		Size: 77.3 KB (77317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649008fd93c04016d8d6b1126044141dba408beb6d261644066540d42169520f`  
		Last Modified: Thu, 27 Mar 2025 21:13:16 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf5a1e26314899fa0d533da3d3f438da508a4be596be30dd46484b625f65cc3`  
		Last Modified: Thu, 27 Mar 2025 21:13:16 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a89ae1696d95e24c28ddf867966341149fa34d184ac9ac40f70c8b948a6b5ca`  
		Last Modified: Thu, 27 Mar 2025 21:13:27 GMT  
		Size: 207.9 MB (207900707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f04053ea1c19d8b835f4bab6fe6ba001011b2cb44132a37af531c3952f3766b`  
		Last Modified: Thu, 27 Mar 2025 21:13:15 GMT  
		Size: 115.5 KB (115452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7216c98f8d954a9ea74b745ec532e67f77086a87616cda42904bef2317d39b4`  
		Last Modified: Thu, 27 Mar 2025 21:13:15 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
