## `openjdk:27-ea-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:82261ff72769860571d3f3c9f6e8110a3780f13044085a336a039e8db3c2b417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `openjdk:27-ea-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull openjdk@sha256:a258afede6967984bc06bbb4a11aeb5499aedeeb8b5679d0143d224167c3ad13
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.3 MB (347304956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b44bd1476bb5c15360eac799b9cff4b20b079fb484edb5a4eea463bac0203bd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Fri, 26 Jun 2026 23:08:47 GMT
SHELL [cmd /s /c]
# Fri, 26 Jun 2026 23:08:48 GMT
ENV JAVA_HOME=C:\openjdk-27
# Fri, 26 Jun 2026 23:08:48 GMT
USER ContainerAdministrator
# Fri, 26 Jun 2026 23:08:59 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 26 Jun 2026 23:09:00 GMT
USER ContainerUser
# Fri, 26 Jun 2026 23:09:00 GMT
ENV JAVA_VERSION=27-ea+28
# Fri, 26 Jun 2026 23:09:46 GMT
COPY dir:4ebef711240c45398e9b005c4af57e81a1e010a3220f8b29271464be340ccef0 in C:\openjdk-27 
# Fri, 26 Jun 2026 23:09:51 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 26 Jun 2026 23:09:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a2ca6b2d5fd7900fc47693f8cab450e375c6d368bd9a6898a43e91299bd0ef`  
		Last Modified: Fri, 26 Jun 2026 23:09:57 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff2539f7aa7d9747555f4ee4c3442e67078f1fffe36e16fce9075341b436eeb`  
		Last Modified: Fri, 26 Jun 2026 23:09:57 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88915cb5b040dec0557f8be84624208003c10a81fdac2011ed14b6ab23c44b5f`  
		Last Modified: Fri, 26 Jun 2026 23:09:57 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ba28b110265d4284bbc34f73ca79b93a68bb57fec14ee241cd9732870d0b9b`  
		Last Modified: Fri, 26 Jun 2026 23:09:57 GMT  
		Size: 77.2 KB (77168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f9ae0b0be6dbaa428b5001f909dab401c7f1ed4c61ea6349d565f633b3d40d`  
		Last Modified: Fri, 26 Jun 2026 23:09:55 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7fd2ae35b0579ae15c11e05b65238ab41204106638b0d5804ccde05820b4645`  
		Last Modified: Fri, 26 Jun 2026 23:09:55 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03963d000dd57856e377ba1c05c665ff190d29eb46894edab645f398ebbb0a44`  
		Last Modified: Fri, 26 Jun 2026 23:10:10 GMT  
		Size: 223.1 MB (223124874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5daf6c88b09389cd8c11839b393d452da80dc484b0b2d761b125fa04284977`  
		Last Modified: Fri, 26 Jun 2026 23:09:55 GMT  
		Size: 99.0 KB (98952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab04dfdd03ccba8550fc2e11b9eb500ab99b6b29b50d406688db1bbead9f69c`  
		Last Modified: Fri, 26 Jun 2026 23:09:55 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
