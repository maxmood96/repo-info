## `eclipse-temurin:11-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:87bb03c30e4790d34ef946cf2e604bd57969a8e95a4bf40251773fb80608f7cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1906; amd64

### `eclipse-temurin:11-nanoserver-ltsc2022` - windows version 10.0.20348.1906; amd64

```console
$ docker pull eclipse-temurin@sha256:73452151be802f8295e243e2cd59481b071d1e672b499190726440e9f5b301a5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.8 MB (313750505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8977d04b970aeb63ad3e0591a3e6d681af7fe66b3fd9f87dd01395aea9cdd12`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 03 Aug 2023 09:40:19 GMT
RUN Apply image 10.0.20348.1906
# Thu, 10 Aug 2023 00:11:36 GMT
SHELL [cmd /s /c]
# Thu, 10 Aug 2023 00:12:45 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Thu, 10 Aug 2023 00:12:46 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 10 Aug 2023 00:12:46 GMT
USER ContainerAdministrator
# Thu, 10 Aug 2023 00:12:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 10 Aug 2023 00:12:57 GMT
USER ContainerUser
# Thu, 10 Aug 2023 00:13:12 GMT
COPY dir:0494f0c3004dc0f4e40e3f6c0c6e0f2ac35120ffc9906421c49b5c62e99eee70 in C:\openjdk-11 
# Thu, 10 Aug 2023 00:13:25 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 10 Aug 2023 00:13:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ea9613880997b3ab2284a37c0c14a403553457b0c331b41c6bd6d1cc7838a222`  
		Last Modified: Tue, 08 Aug 2023 18:47:21 GMT  
		Size: 120.5 MB (120500677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3572ac06c9147f0946a40530f2197bb0101b82dd45b1defe04a8904a1c81a18`  
		Last Modified: Thu, 10 Aug 2023 00:30:45 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3585ee163e7811a248a038e7cbe6a30fddab3e7cff338299caf4fb3598c5d4ba`  
		Last Modified: Thu, 10 Aug 2023 00:31:36 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340e22b0be8b090c4dd8b95d88547278c9fcda10b561b2d80d752db7b7ffd69d`  
		Last Modified: Thu, 10 Aug 2023 00:31:36 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f709ab4c1d708fb1d441674b982b48b57c7d51b2773a9e053bb31fa1d65808`  
		Last Modified: Thu, 10 Aug 2023 00:31:36 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2bc452fdcb4a26a123e0a9fdb557b435ebde27ac6e6d79fafbeed127f1bd1ec`  
		Last Modified: Thu, 10 Aug 2023 00:31:34 GMT  
		Size: 80.1 KB (80129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c839e94c1a7864547fda043ac20045a3922094eb635d20971d93ef3d14fe82`  
		Last Modified: Thu, 10 Aug 2023 00:31:34 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a692b245354084d1477c768ac22495aab647f2c3cd73f5bcbda5e46bacfeaa05`  
		Last Modified: Thu, 10 Aug 2023 00:31:53 GMT  
		Size: 193.1 MB (193102472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cefd8934533257056607ea1d10c99ffb3a6445f9ab55ba9936b5c478aeb53c0`  
		Last Modified: Thu, 10 Aug 2023 00:31:34 GMT  
		Size: 61.0 KB (61009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7da8b455634a3288880259928ea7b7ad0401b56cf2c6037238190dceb96cee9`  
		Last Modified: Thu, 10 Aug 2023 00:31:34 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
