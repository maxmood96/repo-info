## `eclipse-temurin:11-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:5f65e6350fb43a8b6472bd2ee0a5a666507073f88b352921fb0cf0846c75ba3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:11-jdk-nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:1ed7908e3d5c1cd9e6325d19063bb08ea4c3ca5bcc4f4dee17a0447adc07020b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.9 MB (348864858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:449c96572a317f7e24efb0d526fe8fd33e3142ec39e6cedb7fc07357bd71984c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Sat, 19 Oct 2024 02:06:52 GMT
SHELL [cmd /s /c]
# Sat, 19 Oct 2024 02:06:54 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Sat, 19 Oct 2024 02:06:54 GMT
ENV JAVA_HOME=C:\openjdk-11
# Sat, 19 Oct 2024 02:06:55 GMT
USER ContainerAdministrator
# Sat, 19 Oct 2024 02:07:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 19 Oct 2024 02:07:06 GMT
USER ContainerUser
# Sat, 19 Oct 2024 02:07:12 GMT
COPY dir:9f246ebe37fca80f181c5fdb0fda2dac7a959f1509a5d6ecc970014a33d6198a in C:\openjdk-11 
# Sat, 19 Oct 2024 02:07:18 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 19 Oct 2024 02:07:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a295ca478293fa7363528dfaf41b88710154d9b2371595e354da44417a747b`  
		Last Modified: Sat, 19 Oct 2024 02:07:25 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df0d1a5413119788939ca654f817eb7777dcf4c0f5ebd0b858ae1f2e5915d6b`  
		Last Modified: Sat, 19 Oct 2024 02:07:25 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b93c78bb327c199bc7c12c1be84721aa1eccfbcf08147e92bb64b9abec310c`  
		Last Modified: Sat, 19 Oct 2024 02:07:25 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24db2babb063be2be2ca7a73f9d139e7d020ff751d668c9511f5647322844099`  
		Last Modified: Sat, 19 Oct 2024 02:07:25 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be7e099dd514421c814fde5321644f8bbebc4ab4ee11869e4dbea6d4a1835569`  
		Last Modified: Sat, 19 Oct 2024 02:07:23 GMT  
		Size: 66.4 KB (66420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f3b0b63ebd5499edeaccd4713cf127f9c27eb99a3a1a67dd47ebd5fba4238d`  
		Last Modified: Sat, 19 Oct 2024 02:07:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ea4e59a8a7d721c06ca7ed4bac27c2b093344c738640fc8657cf20905d0d39`  
		Last Modified: Sat, 19 Oct 2024 02:07:33 GMT  
		Size: 193.6 MB (193630593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5077931c2527ef6bd7d9cbb5e0e0527f2e28c1503189ccb37944af6ac5852f03`  
		Last Modified: Sat, 19 Oct 2024 02:07:23 GMT  
		Size: 68.1 KB (68087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609ec2a63ca0736a3580a92e7be1f3bc0f44bd43c883c93a0609fb53ee5f3a0b`  
		Last Modified: Sat, 19 Oct 2024 02:07:23 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
