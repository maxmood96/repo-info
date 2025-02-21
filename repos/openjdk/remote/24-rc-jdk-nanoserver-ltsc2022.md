## `openjdk:24-rc-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:ab630c051c3308c87329b7897fcde7a6de929f10942e53e7f86a32cab6de3478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `openjdk:24-rc-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull openjdk@sha256:5d99fd40a56e2dc97df07817613073c7d8394315d89e14f725181c13eb7079ce
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.4 MB (329398030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffde4c639f0d9bddad0571c1d4c4e2e1eff1cf7ad7a7799db1fa685a799b503e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 20:45:43 GMT
RUN Apply image 10.0.20348.3207
# Thu, 13 Feb 2025 01:18:46 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:18:47 GMT
ENV JAVA_HOME=C:\openjdk-24
# Thu, 13 Feb 2025 01:18:48 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:18:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 13 Feb 2025 01:18:51 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:18:52 GMT
ENV JAVA_VERSION=24
# Thu, 13 Feb 2025 01:18:59 GMT
COPY dir:cf5ecdf170ed29d5224593d2b3a510464d2e7297517065c397a2229de8b2a139 in C:\openjdk-24 
# Thu, 13 Feb 2025 01:19:04 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 13 Feb 2025 01:19:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:938e4585b186fc3df3c1959d47ba7a634fea121cec7545db7923ceb191d99a33`  
		Last Modified: Tue, 11 Feb 2025 22:43:09 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca32c5ed90f22b0929449a457d80c4c4d488d229a00de61f4ad4c2ad992ab6e`  
		Last Modified: Thu, 13 Feb 2025 01:19:11 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ec97e98e193c39e1ba87bf34b37ab27327cb58abd4c444ae089417a4d397e6`  
		Last Modified: Thu, 13 Feb 2025 01:19:11 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea151a55ec5a5402d2ed66d67168550cebb72bdae88962cdf056147110d30be9`  
		Last Modified: Thu, 13 Feb 2025 01:19:11 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e40df6a94263acbe1e3457fdc53e1d0c32c3475686f1ce81ac7813cf4416ae1`  
		Last Modified: Thu, 13 Feb 2025 01:19:11 GMT  
		Size: 79.3 KB (79336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26011d2ade6cdbbed31766f3d18cbb3a2f2320e8516c6857d724cfe3b4671366`  
		Last Modified: Thu, 13 Feb 2025 01:19:09 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bbb293beea64d907a749bea6cf0b9ba20cd3d8ed46e88b46ef3ae1ab16b8833`  
		Last Modified: Thu, 13 Feb 2025 01:19:09 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046171047dce804264d3cea1587ddf75710e1a88d40de818a7185426f6dd27b3`  
		Last Modified: Thu, 13 Feb 2025 01:19:20 GMT  
		Size: 208.5 MB (208527578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f03e65ece69044afe2727d8b07a82891ad8efedfc7596ff820e5f1bf387992`  
		Last Modified: Thu, 13 Feb 2025 01:19:09 GMT  
		Size: 118.3 KB (118277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75301350ffd85a4c54218762a009c59e3a7d0afd1ba168dc281b51f2361f394`  
		Last Modified: Thu, 13 Feb 2025 01:19:09 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
