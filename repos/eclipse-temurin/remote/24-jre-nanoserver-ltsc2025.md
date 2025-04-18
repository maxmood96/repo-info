## `eclipse-temurin:24-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:8ce28f517e1329ea0facb906bbfc2f97cf35ae1d693bc5c6a92a3e84cf60ddf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `eclipse-temurin:24-jre-nanoserver-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull eclipse-temurin@sha256:895c5b46fe6b6fabe814fb3752c7f0adbfbabe20ff5ed5c844177c9526ddc093
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.0 MB (248028806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af56c8e428a07361eca3e112733e87fef152d5ac37a804a3d450e9c903e79fb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Fri, 18 Apr 2025 04:14:31 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:14:33 GMT
ENV JAVA_VERSION=jdk-24+36
# Fri, 18 Apr 2025 04:14:35 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 18 Apr 2025 04:14:36 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:14:41 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:14:43 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:14:49 GMT
COPY dir:90c9828944ffcd2978afe702f80884cbf787022d7dcd7becc7c91cd2ab6f7dd5 in C:\openjdk-24 
# Fri, 18 Apr 2025 04:14:55 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 17 Apr 2025 02:52:17 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830db1f296ef76578cd03f67ea5ec749bd3034f6c1f38b0526181c9d816e2254`  
		Last Modified: Fri, 18 Apr 2025 04:15:01 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa0f7a3138c7ba1057e22a05faaf1a9c3fb6ad620918f1058cd53a0926a06af`  
		Last Modified: Fri, 18 Apr 2025 04:15:01 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd5d4252bc1cccbdb139376b965f49370d6ea4744631faee88c18a48d42b403`  
		Last Modified: Fri, 18 Apr 2025 04:15:01 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d2503b18180c028e4117124e2127e2de154358c9267961cdc3c437cbd37688`  
		Last Modified: Fri, 18 Apr 2025 04:14:59 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74fba3fb334c499a5a0d4c59c36a146d841532915aab902203af977a4ff7d36`  
		Last Modified: Fri, 18 Apr 2025 04:14:59 GMT  
		Size: 76.7 KB (76710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d27ec6faba382301c2ae6a6ae556b1f1d04f68a927271b7e65d6be7710b448e`  
		Last Modified: Fri, 18 Apr 2025 04:14:59 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba4365ad8e3222958a020f9ffdf5201c75816bc4ec0bf14d568069f56d7619f`  
		Last Modified: Fri, 18 Apr 2025 04:15:06 GMT  
		Size: 57.7 MB (57702446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea2a7897ec674360791db8509804f888d3a7d134b75adf3927255196b5704b9`  
		Last Modified: Fri, 18 Apr 2025 04:14:59 GMT  
		Size: 102.4 KB (102359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
