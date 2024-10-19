## `eclipse-temurin:11-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:fbefe111deab7936180ad36948c0501ecf9be06ebb440c44f531dbf9160f706e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:11-nanoserver` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:7bc5729955f05e4abb72375b65760bf76cfb1c3457b099bcc6604ff1a95fa271
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314331288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffb933a9ce2292ae798ef7dcec9d11c19097eb6e44939a88243f6e6418b55e7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Sat, 19 Oct 2024 02:13:01 GMT
SHELL [cmd /s /c]
# Sat, 19 Oct 2024 02:13:02 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Sat, 19 Oct 2024 02:13:03 GMT
ENV JAVA_HOME=C:\openjdk-11
# Sat, 19 Oct 2024 02:13:03 GMT
USER ContainerAdministrator
# Sat, 19 Oct 2024 02:13:05 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 19 Oct 2024 02:13:06 GMT
USER ContainerUser
# Sat, 19 Oct 2024 02:13:13 GMT
COPY dir:9f246ebe37fca80f181c5fdb0fda2dac7a959f1509a5d6ecc970014a33d6198a in C:\openjdk-11 
# Sat, 19 Oct 2024 02:13:18 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 19 Oct 2024 02:13:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a5f35edd970f0dbf5fc624d4d2b28c5048b2f7530d2815c851719a6e042a5c`  
		Last Modified: Sat, 19 Oct 2024 02:13:24 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42059add2677af6fb832b14e31b52bc1a516ae0032e933a2d297835157e67929`  
		Last Modified: Sat, 19 Oct 2024 02:13:24 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d920254d6a2918a7ca1874e07524b703d704704f2b9013e483d6358a9982316`  
		Last Modified: Sat, 19 Oct 2024 02:13:24 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f530171a1053ecad0e5fb27311ea8c500dd5befbb7581e3d7bf0af96dccb4f`  
		Last Modified: Sat, 19 Oct 2024 02:13:24 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44aad60d4bf3914f454c55c7e9272af8f5e09ec4584f597a8c9e512e84e9d7dc`  
		Last Modified: Sat, 19 Oct 2024 02:13:22 GMT  
		Size: 76.3 KB (76292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5458f71070ccf22ea756344f9cf2f55fd0750c61bd2ec2a3d9af9f6f1f4d3e`  
		Last Modified: Sat, 19 Oct 2024 02:13:22 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e16adb69879f22c358c35230d6647211016c3b2aff2f4924257d3342a5dac8c`  
		Last Modified: Sat, 19 Oct 2024 02:13:32 GMT  
		Size: 193.6 MB (193630343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8fe06797654718bcb15908d201d4a55b59a99f8b9376caa8db3578389c19e4`  
		Last Modified: Sat, 19 Oct 2024 02:13:22 GMT  
		Size: 107.5 KB (107481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50575522ed08f42f049c35899a8b2b5b279625cb5df14f2bbfc1ad806c5aeb44`  
		Last Modified: Sat, 19 Oct 2024 02:13:22 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-nanoserver` - windows version 10.0.17763.6414; amd64

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
