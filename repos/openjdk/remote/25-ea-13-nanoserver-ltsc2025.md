## `openjdk:25-ea-13-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:cbad3fb5db4ba601aaf53958b7c575ddcce5b910e5eb023a10a14c25b2455cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `openjdk:25-ea-13-nanoserver-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull openjdk@sha256:15dd6d18cca310e976f1194de7d28e0efbde24ff944fc24390eb40a0b590a18c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.9 MB (413898526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4ea0193c5aa52e5694fbf04ff9b7dd0685c82c40cc53738f7fb3f7031ba447`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Wed, 12 Mar 2025 19:17:32 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:17:33 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 12 Mar 2025 19:17:34 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:17:36 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 12 Mar 2025 19:17:37 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:17:37 GMT
ENV JAVA_VERSION=25-ea+13
# Wed, 12 Mar 2025 19:17:45 GMT
COPY dir:41adcea28f6e8239eac0b74c19049c5daef67ad138ba9db7bdf8df0acc8b0b9b in C:\openjdk-25 
# Wed, 12 Mar 2025 19:17:52 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 12 Mar 2025 19:17:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e613ab96b2ca62c89b368c48e5bbe28db973bd4201adca9d267cc2876ed9fd2d`  
		Last Modified: Wed, 12 Mar 2025 19:17:56 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edcef208ed4c4473ae0d055992d18ccde447bee0d0fa8b0c8efdd17e798647b1`  
		Last Modified: Wed, 12 Mar 2025 19:17:56 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e3a3b1ff09815997575fdf009d7ec4b044e03d4a91a7384bdd62a8f4d83cce`  
		Last Modified: Wed, 12 Mar 2025 19:17:56 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3f8326eaca13881197bdc2307a37a60b8f30b5fcc5e6cb0eae5139be2d11f4`  
		Last Modified: Wed, 12 Mar 2025 19:17:56 GMT  
		Size: 76.2 KB (76186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863590b5ca2eec1f0d3fa2f63963f064796eb0509eda9993c77b13580217e7eb`  
		Last Modified: Wed, 12 Mar 2025 19:17:55 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f4d8f45c2fe0ec276ce226ba6ce8be6edee8e88ed99821eba73f63be0f1ee6`  
		Last Modified: Wed, 12 Mar 2025 19:17:55 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ba0f62807efbee03152b49a1dcbbf9caab397334a8bae7fbe6aa894b38763a`  
		Last Modified: Wed, 12 Mar 2025 19:18:07 GMT  
		Size: 207.4 MB (207398796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1ff3bce5a2499fc81d755c17a820a93a199f3db7d676dfc9ac306d05c91c91`  
		Last Modified: Wed, 12 Mar 2025 19:17:55 GMT  
		Size: 114.9 KB (114901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed24ba2c25c4b63036c7f375ebdcd56143b211f40cd5bce1ce113ae3a2eaf2c`  
		Last Modified: Wed, 12 Mar 2025 19:17:55 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
