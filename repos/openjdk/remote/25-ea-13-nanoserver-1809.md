## `openjdk:25-ea-13-nanoserver-1809`

```console
$ docker pull openjdk@sha256:293a4b604f7ce6b4c37dbf1eb21fd10a0f843ead75d672a7ff432147a2c84a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `openjdk:25-ea-13-nanoserver-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull openjdk@sha256:b595e03b9e781eae4ab348da92d2827b4e7bbda1587e6897e96e1c01e1d11a20
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.8 MB (318812528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732d2791758dc65843c233a16db14df992fcaf696a037382e623664af3c4269d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Wed, 12 Mar 2025 19:18:03 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:18:05 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 12 Mar 2025 19:18:06 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:18:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 12 Mar 2025 19:18:10 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:18:10 GMT
ENV JAVA_VERSION=25-ea+13
# Wed, 12 Mar 2025 19:18:17 GMT
COPY dir:41adcea28f6e8239eac0b74c19049c5daef67ad138ba9db7bdf8df0acc8b0b9b in C:\openjdk-25 
# Wed, 12 Mar 2025 19:18:24 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 12 Mar 2025 19:18:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a3a60d876a6532ca19dde160af76ce891f2b9481df62c486a62a9f9ed03650`  
		Last Modified: Wed, 12 Mar 2025 19:18:32 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645f14e8f64c5cf823605e69d297a392bdf3c84450a326f5d7bd9b9123899ae7`  
		Last Modified: Wed, 12 Mar 2025 19:18:31 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f32d04711ac06a732e03419a288c5e265849261f0e97bc8d6f2822c9e1decf2`  
		Last Modified: Wed, 12 Mar 2025 19:18:31 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2e3e4032d2f2c615bf835ca2fbb224e63146299ab65fe1c507189cefcb9b72`  
		Last Modified: Wed, 12 Mar 2025 19:18:31 GMT  
		Size: 69.0 KB (68971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78a6d1516da2a30023bf06767f26de0ed886bb47b78ce83541b8ce177934d70`  
		Last Modified: Wed, 12 Mar 2025 19:18:29 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9dbd1b50e4a192f59304e3a7773b2d03cd6aaafa2a9c07203299faa43293113`  
		Last Modified: Wed, 12 Mar 2025 19:18:29 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a30e8f11fc3997c1c55599ebc652d663f64a867bd26b94352cc768284b5c1a`  
		Last Modified: Wed, 12 Mar 2025 19:18:40 GMT  
		Size: 207.4 MB (207399325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3c140474df4351300bf44644e8edb1bb16be1912f5e52c9a6666fba9cb1135`  
		Last Modified: Wed, 12 Mar 2025 19:18:30 GMT  
		Size: 4.4 MB (4430325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c5581ba06d056095beeaf4635a96c0068fa4c5f715d0c091ad8e0ad5bb2b48`  
		Last Modified: Wed, 12 Mar 2025 19:18:29 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
