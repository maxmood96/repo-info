## `openjdk:26-ea-5-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:5de7d81d4c746dafe3d642c11781aaac6312521879ea57db716d4cd591f34456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3932; amd64

### `openjdk:26-ea-5-nanoserver-ltsc2022` - windows version 10.0.20348.3932; amd64

```console
$ docker pull openjdk@sha256:fcf10725bb26a741fb1257312922128fdcc93034374b6267bf8ed540f93bfc64
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.3 MB (341307015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a90ece93415f27eb5c5cfed87de8c23da56c01b1a2560b926fd3a35f7ff3d4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Jul 2025 05:15:23 GMT
RUN Apply image 10.0.20348.3932
# Wed, 09 Jul 2025 19:12:49 GMT
SHELL [cmd /s /c]
# Wed, 09 Jul 2025 19:12:49 GMT
ENV JAVA_HOME=C:\openjdk-26
# Wed, 09 Jul 2025 19:12:50 GMT
USER ContainerAdministrator
# Wed, 09 Jul 2025 19:12:53 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 09 Jul 2025 19:12:54 GMT
USER ContainerUser
# Wed, 09 Jul 2025 19:12:54 GMT
ENV JAVA_VERSION=26-ea+5
# Wed, 09 Jul 2025 19:13:01 GMT
COPY dir:a8af305eda69ca7e4a97e843a96509e487ef158cc8b5f27ab7de11cd1f4c0ba7 in C:\openjdk-26 
# Wed, 09 Jul 2025 19:13:07 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 09 Jul 2025 19:13:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b1cf2c299ff70c52cb8ecf52e66d64d5068519867510919d8807ed2c58a54ba2`  
		Last Modified: Tue, 08 Jul 2025 21:55:51 GMT  
		Size: 122.6 MB (122630906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97b84376619517fc0316a987983bf53b66a29cbbb195ca8ff914af80beaaf33`  
		Last Modified: Wed, 09 Jul 2025 19:13:35 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b591f532283fd30f009b2d3210c1f384c518591667bdb77b6824e84ed2793cbf`  
		Last Modified: Wed, 09 Jul 2025 19:13:35 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25073d4ecc4039f0509dfda5373a178870a0e7550c8447f00ad25106a0ce05e`  
		Last Modified: Wed, 09 Jul 2025 19:13:35 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a94f79f87c35ed3eaa4b8871eb2242ee3e808a768189f555d3608806b5e8a6`  
		Last Modified: Wed, 09 Jul 2025 19:13:36 GMT  
		Size: 77.5 KB (77505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:856a55b2a70c84159ca8db97ae320dc9c5632ab4b5ce6b4cfb41d8a9d134981d`  
		Last Modified: Wed, 09 Jul 2025 19:13:36 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78d7deb1f5d61dd9a19cbf5711a4cfee3c4473420e1d20f9df83e35cd05bb4c`  
		Last Modified: Wed, 09 Jul 2025 19:13:35 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc9b1d42e7937fb2a739cf63573d09a11651c54134193e37e90a65f7bccc4df`  
		Last Modified: Wed, 09 Jul 2025 21:25:40 GMT  
		Size: 218.5 MB (218485671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d88854ca1f92d1a225f3fb0a426f4b51a2cffaaf31101c8e6b1a633a56fa43`  
		Last Modified: Wed, 09 Jul 2025 19:13:36 GMT  
		Size: 106.8 KB (106752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26707ef861b8aede27a25e8e3b1be4cf03b32e04abbf1260f7dfb06174de661b`  
		Last Modified: Wed, 09 Jul 2025 19:13:35 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
