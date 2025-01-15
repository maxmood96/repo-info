## `openjdk:25-nanoserver`

```console
$ docker pull openjdk@sha256:1d960f9975e6f0fe46fa72ae79bfc3e49e5baa71019afadfffbcd549cb604467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `openjdk:25-nanoserver` - windows version 10.0.17763.6659; amd64

```console
$ docker pull openjdk@sha256:2d15a39ff01a2f986edeed4c344600904799e34ce37dff0614e60a6068a55204
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.3 MB (368299004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad5ae8121fc02964aea77a50fa1149ac10e082b127ff6fd3a61d8950e0110bf`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Sat, 11 Jan 2025 03:08:51 GMT
SHELL [cmd /s /c]
# Sat, 11 Jan 2025 03:08:52 GMT
ENV JAVA_HOME=C:\openjdk-25
# Sat, 11 Jan 2025 03:08:53 GMT
USER ContainerAdministrator
# Sat, 11 Jan 2025 03:09:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 11 Jan 2025 03:09:05 GMT
USER ContainerUser
# Sat, 11 Jan 2025 03:09:05 GMT
ENV JAVA_VERSION=25-ea+5
# Sat, 11 Jan 2025 03:09:17 GMT
COPY dir:63c8c2c9000bce70ab79161ee8d862be4b6eb9e24d02b8adc700a46d4799aaa8 in C:\openjdk-25 
# Sat, 11 Jan 2025 03:09:22 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 11 Jan 2025 03:09:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Tue, 10 Dec 2024 21:03:34 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3741c08885924f5c7f8d019773ae8d08eeec435039f49fec7e57ce03bc767cad`  
		Last Modified: Sat, 11 Jan 2025 03:09:26 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b854e800f84ce17a53561f1405d688848d2f2631b1d19e3902e9f45c9c036c`  
		Last Modified: Sat, 11 Jan 2025 03:09:25 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9429e3e46063772df8e8a8a392c5a8178551d65eeb55950dd68720688bae8fd3`  
		Last Modified: Sat, 11 Jan 2025 03:09:25 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b236879475fed3affc4745f0988538cc11e861439dfe8504e60f6ab24aca64`  
		Last Modified: Sat, 11 Jan 2025 03:09:25 GMT  
		Size: 68.4 KB (68374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d750ca340c266ad7b9574fdc2f031a402796c8f6b3f88611541b1b7f55da0a73`  
		Last Modified: Sat, 11 Jan 2025 03:09:24 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108d177d7590fd3d88031294da8944a7e4792b49207afaadd0968f2c25c5cfce`  
		Last Modified: Sat, 11 Jan 2025 03:09:24 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2dceaf3ec130aed0eea3992c23ebc688ce721169a2cf264bd6636786fdcf84`  
		Last Modified: Sat, 11 Jan 2025 03:09:36 GMT  
		Size: 208.6 MB (208625754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a53ac2027d240c9b7463bdb17404dbbb9524c9cd34867a8535abe4504394557`  
		Last Modified: Sat, 11 Jan 2025 03:09:25 GMT  
		Size: 4.4 MB (4366925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6016adc31fc78c65445e3fcd5fe5a90714c1eac09467d49d75733d4c4f419f00`  
		Last Modified: Sat, 11 Jan 2025 03:09:24 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
