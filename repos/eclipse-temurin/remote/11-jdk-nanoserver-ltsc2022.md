## `eclipse-temurin:11-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:267b0c755ce92529b84e8cf6210c7f00e7a9182f405edfc8e3ec8a4675288110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `eclipse-temurin:11-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull eclipse-temurin@sha256:c2d382ec1c5ee3c088a8109500aea07abc050cf9339a104eecbddb3ff63bae80
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.1 MB (315116589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b2497a842c7866db2e65e851b3630ed32fed1712490e1f519b7b091ad3be77`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Apr 2024 08:53:11 GMT
RUN Apply image 10.0.20348.2402
# Wed, 10 Apr 2024 00:34:53 GMT
SHELL [cmd /s /c]
# Wed, 10 Apr 2024 00:36:12 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 10 Apr 2024 00:36:13 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 10 Apr 2024 00:36:13 GMT
USER ContainerAdministrator
# Wed, 10 Apr 2024 00:36:25 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Apr 2024 00:36:25 GMT
USER ContainerUser
# Wed, 10 Apr 2024 00:36:41 GMT
COPY dir:06bb700052ae5de12c7654c6d453b954bdaac52e59d87856592b85cdd3ce67e9 in C:\openjdk-11 
# Wed, 10 Apr 2024 00:36:56 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Apr 2024 00:36:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:755fc767289b8847bd0d0d8d75efc308c040140acf2a3426973ba9fbf022c4c0`  
		Last Modified: Tue, 09 Apr 2024 23:50:18 GMT  
		Size: 121.0 MB (120993754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70887eeae6a5d6d5fd81661024afc84fee637f674dee5e7127112cbfce90750`  
		Last Modified: Wed, 10 Apr 2024 01:00:01 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe62c8f081ea94a2840d89a47a30f866461fb652b13420a361d22749e8d09ff6`  
		Last Modified: Wed, 10 Apr 2024 01:00:51 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7362c835f62465014a8f53d706a07a1c7592958e8a8b3eb8d336811a94abd2`  
		Last Modified: Wed, 10 Apr 2024 01:00:51 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d72dee54d13dfb5a7c9be8a78d200fb7e1e432dfa934c19bd751f29eba4764`  
		Last Modified: Wed, 10 Apr 2024 01:00:51 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a2d872d1a8c8ca8f858ef0e089f456f747b9c89290beb05d79ea68b4c9852e`  
		Last Modified: Wed, 10 Apr 2024 01:00:49 GMT  
		Size: 76.3 KB (76314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfdfb98f977eea3476d922090d5b0fed8cd14c9beba7b6768c36b32d4e1b669`  
		Last Modified: Wed, 10 Apr 2024 01:00:49 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39133eba10fe88144cb8272c20ad00a0983dfd69bdec57db9b94b9cff1f6006`  
		Last Modified: Wed, 10 Apr 2024 01:01:09 GMT  
		Size: 194.0 MB (193980401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1834ef31acf2438805eb1d561b92cd838f2415f504c0e4c5655ecd9440f89ae`  
		Last Modified: Wed, 10 Apr 2024 01:00:49 GMT  
		Size: 59.7 KB (59739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877080e15a351ae3015fe03a0ffcc161f32639bc0dd161761863e0f6ae16a6c8`  
		Last Modified: Wed, 10 Apr 2024 01:00:49 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
