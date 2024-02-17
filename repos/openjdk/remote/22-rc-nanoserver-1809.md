## `openjdk:22-rc-nanoserver-1809`

```console
$ docker pull openjdk@sha256:0facf4b80c4bd561ab728580ca2a09cc47979a36e3f6f6fc8313f43db994b9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `openjdk:22-rc-nanoserver-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull openjdk@sha256:38284a0fd98025c7346116b48781f221da042a2c8a110d733cbed01f92acc795
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305942160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:044d5240eca1197dad9e5f16da69ba76e667186085c694eeca086a03af71f6f9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Sat, 17 Feb 2024 02:00:40 GMT
SHELL [cmd /s /c]
# Sat, 17 Feb 2024 02:00:41 GMT
ENV JAVA_HOME=C:\openjdk-22
# Sat, 17 Feb 2024 02:00:42 GMT
USER ContainerAdministrator
# Sat, 17 Feb 2024 02:00:44 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 17 Feb 2024 02:00:45 GMT
USER ContainerUser
# Sat, 17 Feb 2024 02:00:46 GMT
ENV JAVA_VERSION=22
# Sat, 17 Feb 2024 02:00:55 GMT
COPY dir:0ef6a7becb679ad3edc5c96eb7b0f5b5893989ee8e0051f559b592b4b972c479 in C:\openjdk-22 
# Sat, 17 Feb 2024 02:00:59 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 17 Feb 2024 02:01:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d1f7984eaddccfe701f90712b1dca0abc497cea1ba0c4d045c045dce4d2b8f4`  
		Last Modified: Sat, 17 Feb 2024 02:01:07 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8504aaa9a8163d6ecbd2a344b44a87e3d558cbe1c487e5eb99042217398573a`  
		Last Modified: Sat, 17 Feb 2024 02:01:06 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd2a1521abb5362fef96ad0835da9acf90aae0a9a0e34c2fdd4073a89131cea`  
		Last Modified: Sat, 17 Feb 2024 02:01:06 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b929af2861b8c3c85dc9d83142d54e4a1bcbdcf244b979584dafc0539fcf8bc`  
		Last Modified: Sat, 17 Feb 2024 02:01:06 GMT  
		Size: 84.2 KB (84152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b47a8a992344b0d1f925b6bbde48cfc2de8444bfce461fb7bd8da33490e44ac`  
		Last Modified: Sat, 17 Feb 2024 02:01:04 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5876ad073064c044b124f6ae63cd2f26162a3ed762661d42e2f00d903720745c`  
		Last Modified: Sat, 17 Feb 2024 02:01:04 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049a8dcb53466fc1d9305a1410d83cfb9be17e9e8cb2f2cd56669f8637765c16`  
		Last Modified: Sat, 17 Feb 2024 02:01:16 GMT  
		Size: 197.4 MB (197367158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2092e85b810a01d5b19e0e21849397a3ec4aa13c614bac1b787dd0e400774a3`  
		Last Modified: Sat, 17 Feb 2024 02:01:05 GMT  
		Size: 3.9 MB (3863029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f824a9509015c5ef12257774be3a09f1e6b6ee8fc13d32e58208845d0579d26e`  
		Last Modified: Sat, 17 Feb 2024 02:01:04 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
