## `eclipse-temurin:8u442-b06-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:fec195d7130aafeb33e4a68664680b2cf49b4e0ca7626c320fdb739d76937621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `eclipse-temurin:8u442-b06-jre-nanoserver-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull eclipse-temurin@sha256:52774750386a6406c98c7b22e2d51297d67d0ceab49750b3a720b794f99e072e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.5 MB (149483805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4834ff5193ed43f310b26f1389d79066ff49f5df85760e3d889d1ed2401830bb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 04:15:05 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:15:07 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Fri, 18 Apr 2025 04:15:07 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 18 Apr 2025 04:15:08 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:15:11 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:15:11 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:15:14 GMT
COPY dir:5687adced9ba5f2555526fe07fa3e848c7771941703db13fa4b29a0f81d58070 in C:\openjdk-8 
# Fri, 18 Apr 2025 04:15:18 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b37b0eced1360f181fac38b2f2f0c4a981da7db22eb9d796506a19bc53093b`  
		Last Modified: Fri, 18 Apr 2025 04:15:23 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30aced64f1fd02e0d422985800ad389b49805ef857fb4d924af650d127417a52`  
		Last Modified: Fri, 18 Apr 2025 04:15:23 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b29175cff2d29bedf4f23ab8467bfc69bc3dbe3b24b57e10a72cb510b4e0c2e`  
		Last Modified: Fri, 18 Apr 2025 04:15:23 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5dce7ad54b3da46e4369cf49da7c40df178469f87bfc2a2d15c2813a518d53f`  
		Last Modified: Fri, 18 Apr 2025 04:15:22 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ccb50adb37cf49af155f7524bb3f22dd7f63e4afd925690b9332f9f95faf02`  
		Last Modified: Fri, 18 Apr 2025 04:15:22 GMT  
		Size: 73.5 KB (73459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40acafb373b60f153cab01e55eeb3a93b33becf347a8fe7e65bd7f5ce27d82e1`  
		Last Modified: Fri, 18 Apr 2025 04:15:22 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8704a29f332693a188821acf3b59f071a4ea94cf4a1aa6732504e6da661254`  
		Last Modified: Fri, 18 Apr 2025 04:15:25 GMT  
		Size: 40.6 MB (40552354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305677797e3285ef74df871e66816a815c224e5902d63085d9bd3a909656438d`  
		Last Modified: Fri, 18 Apr 2025 04:15:22 GMT  
		Size: 100.6 KB (100569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
