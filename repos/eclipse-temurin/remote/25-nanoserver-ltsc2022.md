## `eclipse-temurin:25-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:41db410d29ae749ad9846703c08c11fd6e16581dad657c1067fe5f0bbe0864cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `eclipse-temurin:25-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull eclipse-temurin@sha256:f70bd64bfdac23bb65e6e7a45d255a76f0c582b3ea4cf043efc9e5451301b5fb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264769013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c7e0cbe45dfc32af6403f97370faef016c809e31be540d38826e8a102e5d56`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Tue, 10 Feb 2026 23:30:39 GMT
SHELL [cmd /s /c]
# Tue, 10 Feb 2026 23:31:14 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 10 Feb 2026 23:31:14 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 10 Feb 2026 23:31:14 GMT
USER ContainerAdministrator
# Tue, 10 Feb 2026 23:31:16 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Feb 2026 23:31:16 GMT
USER ContainerUser
# Tue, 10 Feb 2026 23:31:29 GMT
COPY dir:ebca1fed269853ebca056470dac79e7ebf8f2b759d9752408e0c7f2313fb3842 in C:\openjdk-25 
# Tue, 10 Feb 2026 23:31:32 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 10 Feb 2026 23:31:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1235c15873321f97d8dc938470b404e01c464ec623aaf3d82988ecc939f3ae`  
		Last Modified: Tue, 10 Feb 2026 23:30:54 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4976d70b5f18222b950c4d390873a124d4595a26028ce0104da22237988e39ba`  
		Last Modified: Tue, 10 Feb 2026 23:31:38 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d2a5cffce586ad11cc0608bbb0dad068beda5a45ad5545b7d0fd79b1979acb1`  
		Last Modified: Tue, 10 Feb 2026 23:31:38 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7fbe716efc27cb173938085a6c8ae39a6eb9b1ab8a12e090e64bd2a0c2cccd`  
		Last Modified: Tue, 10 Feb 2026 23:31:38 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5e137da6146ae3f4583fae4c546702350e8e10d7fef9c7f7fe191a5fa01880`  
		Last Modified: Tue, 10 Feb 2026 23:31:37 GMT  
		Size: 77.3 KB (77304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9380f525bcf3a29c738b70add0e0ed6c1e481b29c40ca710e5dcdd2901c6d2b3`  
		Last Modified: Tue, 10 Feb 2026 23:31:37 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83fdda8889ceed6922b02370ea7d2f2389d866eb38b0a0c6e9863ae877a2d738`  
		Last Modified: Tue, 10 Feb 2026 23:31:48 GMT  
		Size: 137.9 MB (137932201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c198dc46393c970df66b61b1bb15f9111602b2ba78d36386f9b34393185938e`  
		Last Modified: Tue, 10 Feb 2026 23:31:37 GMT  
		Size: 107.3 KB (107334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8631ad4f19e96f83d1808f77000e87030bded3c0cb06496ddd710ddc677be982`  
		Last Modified: Tue, 10 Feb 2026 23:31:37 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
