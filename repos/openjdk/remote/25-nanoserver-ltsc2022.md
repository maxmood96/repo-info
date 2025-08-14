## `openjdk:25-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:93656c44c6f0def20bf022cc50eed57270466be994df3c1927da521d4ac34cda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `openjdk:25-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull openjdk@sha256:58eb4b2ef2cda3b87a9b24c4891c39ffea5960f4c132fff9b70c0c309c06600b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.4 MB (341385540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7175fa2536a8dc40a17e3a36bcf40aaae4bfc4d371f9b0a803299e3749ceef3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:49:54 GMT
SHELL [cmd /s /c]
# Tue, 12 Aug 2025 20:49:55 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 12 Aug 2025 20:49:55 GMT
USER ContainerAdministrator
# Tue, 12 Aug 2025 20:49:58 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 12 Aug 2025 20:49:59 GMT
USER ContainerUser
# Tue, 12 Aug 2025 20:49:59 GMT
ENV JAVA_VERSION=25
# Tue, 12 Aug 2025 20:50:06 GMT
COPY dir:7f4ebec9bbadc904e8c904a47d94c73f09fb6efdec5d25e1d0c69bce87e6d7e9 in C:\openjdk-25 
# Tue, 12 Aug 2025 20:50:12 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 12 Aug 2025 20:50:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c380a20007ca2c3f1aa6d77d33c1ef86bd08bc0fa758741bc04af55ae90fd6`  
		Last Modified: Tue, 12 Aug 2025 21:23:56 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be67fa233a413938117e9727c431a30ede59927030a307cf2cfc603dde3b6e05`  
		Last Modified: Tue, 12 Aug 2025 21:23:56 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9bed6db482f20f246cec312836b4814149c9490c6b537ca365b42887859274a`  
		Last Modified: Tue, 12 Aug 2025 21:23:56 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b491e033edce438d245bfc53f79b9a6c12d34e6c737ff72fba36dff7a6f62a`  
		Last Modified: Tue, 12 Aug 2025 21:23:56 GMT  
		Size: 77.8 KB (77825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b474974a75ac99f825942338719168601565fe777a2a76b8148b4275b5109135`  
		Last Modified: Tue, 12 Aug 2025 21:23:57 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23e06962b3202dc5db2771b2b99139c38f226b63e175ad918a397fe0c5c465b`  
		Last Modified: Tue, 12 Aug 2025 21:23:57 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fafca0e97f82213b066a54b825cae3b9c3afb3a7ec5d54a05adb9482a83d0c3a`  
		Last Modified: Tue, 12 Aug 2025 21:24:39 GMT  
		Size: 218.5 MB (218534306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0329859c2e0ca40aad3ec5a34f4a066315e89872b635c2911492929d182da21b`  
		Last Modified: Tue, 12 Aug 2025 21:23:57 GMT  
		Size: 106.9 KB (106892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b14bf5f8dd23a40a9f5c2ed012d424a80ec699391c30bafec2de152234c8c00`  
		Last Modified: Tue, 12 Aug 2025 21:23:57 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
