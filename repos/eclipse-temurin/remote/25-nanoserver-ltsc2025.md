## `eclipse-temurin:25-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:f634c852d63162ac39212c2fa54f625f09a79ff77a7fdd4429d3dee7ca694563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `eclipse-temurin:25-nanoserver-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull eclipse-temurin@sha256:4c6a356bddaa505e3ba066a0a8c8356a08bf0f9a55ae6dd040db863f1c7d3ab8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.5 MB (337521771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33e8630024efbd0d8392b363c7dc0b107abf11caa8d4bd92e0ea38c9d441f16`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Mar 2026 01:45:55 GMT
RUN Apply image 10.0.26100.32522
# Tue, 10 Mar 2026 22:44:02 GMT
SHELL [cmd /s /c]
# Tue, 10 Mar 2026 22:44:02 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 10 Mar 2026 22:44:03 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 10 Mar 2026 22:44:03 GMT
USER ContainerAdministrator
# Tue, 10 Mar 2026 22:44:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Mar 2026 22:44:10 GMT
USER ContainerUser
# Tue, 10 Mar 2026 22:44:23 GMT
COPY dir:ebca1fed269853ebca056470dac79e7ebf8f2b759d9752408e0c7f2313fb3842 in C:\openjdk-25 
# Tue, 10 Mar 2026 22:44:30 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 10 Mar 2026 22:44:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:06fab7822816d5f43d6835d07ac8db280fdf81384187f36d8dc43bbb7064a76d`  
		Last Modified: Tue, 10 Mar 2026 20:41:46 GMT  
		Size: 199.4 MB (199409325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e61f5348397c570d7aecf06deb2ba50cb439efc28796c03eb9f795b6eeff59e`  
		Last Modified: Tue, 10 Mar 2026 22:44:36 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e795ce995bd1cf7b0cc7f9e6709ca98ee1124a889524c55807c6c98017e233`  
		Last Modified: Tue, 10 Mar 2026 22:44:36 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a1b63778efca2015c6e0fa76db779784bba3e28463ddf11c658c977b4217e1`  
		Last Modified: Tue, 10 Mar 2026 22:44:36 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab5a097615209dec52a7a213175c7b1c5a1210c570da731948bc79aa230370a`  
		Last Modified: Tue, 10 Mar 2026 22:44:36 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca8c42b91ab4a50196a56c61281d1fe903cfb52b87ff5de087b5c744deb93e5`  
		Last Modified: Tue, 10 Mar 2026 22:44:34 GMT  
		Size: 70.1 KB (70077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:422bafbc83ae717ad1779aced661f4380f6d62880d2b20b01a67dcdeb66803f1`  
		Last Modified: Tue, 10 Mar 2026 22:44:34 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e318251a8f05dddb4c6d7a11d1d2330f1aad10dc0f583e61460c9d4122c1dd`  
		Last Modified: Tue, 10 Mar 2026 22:44:47 GMT  
		Size: 137.9 MB (137932772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2555bf4180e018dfcb9f720283100111569886445ce7e9e99ea51b040e8c7a2`  
		Last Modified: Tue, 10 Mar 2026 22:44:34 GMT  
		Size: 103.2 KB (103188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9425ca258a3ac4071bf78c43bfb90715fc50d06ec4626166d0cb72fe082ec303`  
		Last Modified: Tue, 10 Mar 2026 22:44:34 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
