## `openjdk:14-ea-30-nanoserver-1809`

```console
$ docker pull openjdk@sha256:3227b4a34e4f723ddbb3a45f470cdbbd91cb0785e32cfda3df61f7fcb6b968ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `openjdk:14-ea-30-nanoserver-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull openjdk@sha256:5f63f9e31d34bd36e090147f6549a2d0ff4cb3baa7e7eaf1848b4e9bb13e8abe
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298403094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2093c6f5d76c628e87c5d3516dc353a21435f2da8d51cecdb24f3ff3e0059b02`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 04 Jan 2020 07:17:17 GMT
RUN Apply image 1809-amd64
# Tue, 14 Jan 2020 23:56:11 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2020 00:05:42 GMT
ENV JAVA_HOME=C:\openjdk-14
# Wed, 15 Jan 2020 00:05:43 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2020 00:05:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 15 Jan 2020 00:05:57 GMT
USER ContainerUser
# Wed, 15 Jan 2020 00:05:58 GMT
ENV JAVA_VERSION=14-ea+30
# Wed, 15 Jan 2020 00:07:00 GMT
COPY dir:4b0191a72f8e091ffdd613e34bd9beb628e72ed6906ece0f0d1de856f1353379 in C:\openjdk-14 
# Wed, 15 Jan 2020 00:07:22 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Wed, 15 Jan 2020 00:07:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ee446884f7bef76f8275c2f16add1c4fb598bea2ba861e72bce8fb4aac9b55ef`  
		Size: 101.1 MB (101054324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:764e25aa4e95684bd69a4d130dc1c729bfaef95293d9c76c4d2a12ced9e3a9ac`  
		Last Modified: Wed, 15 Jan 2020 01:51:06 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f3a5df9926db070e4016e42e49a7d9ce0131f528e644ae4388774831b6b46e`  
		Last Modified: Wed, 15 Jan 2020 01:58:21 GMT  
		Size: 951.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c21d67a14cad5558f706984eed7f97aaa2665e4b4cf1a7a1d21888c5e2c02a2`  
		Last Modified: Wed, 15 Jan 2020 01:58:20 GMT  
		Size: 943.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ffd38236cfc5913ab84e035b74a0bddf197bbfffdd8e9e8b151cc30bbf8adb`  
		Last Modified: Wed, 15 Jan 2020 01:58:20 GMT  
		Size: 66.5 KB (66486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8510d836b27dbac14cee7131c4209ebf2081c2ba957f75e05cbeff605e5320`  
		Last Modified: Wed, 15 Jan 2020 01:58:18 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35940d0423c701861eac295fdac5e5ef7754a951f48ed1311fbbfe8f4c97731a`  
		Last Modified: Wed, 15 Jan 2020 01:58:18 GMT  
		Size: 936.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203453509e843d313b0cf9b3156c17aa559dfe23e548e88aa7d2bfc4fc1903f7`  
		Last Modified: Wed, 15 Jan 2020 01:58:41 GMT  
		Size: 193.8 MB (193829748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f467eaf7f32bf5d3db8422dae456800b31066879f3762f93d83a29a31451b1f7`  
		Last Modified: Wed, 15 Jan 2020 01:58:19 GMT  
		Size: 3.4 MB (3446920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc5d6823511537290adcfb2e2ef841d3b5c2b2a3546cea6201640a93dfc581b`  
		Last Modified: Wed, 15 Jan 2020 01:58:18 GMT  
		Size: 921.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
