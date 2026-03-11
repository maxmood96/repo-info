## `eclipse-temurin:11-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:5771a9449f0045e428edb71d5fbbfe08a4cb23e4aeca60917958f9494fea77ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `eclipse-temurin:11-nanoserver` - windows version 10.0.26100.32522; amd64

```console
$ docker pull eclipse-temurin@sha256:27eb47d178ab631029adafef8e8e22d81d14a564da3e7243f1ec738d650c8d59
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.3 MB (394301972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2448965e0983efd3d9a62352e6b987471740e2a525d5e9217e7cc92c99ad890a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Mar 2026 01:45:55 GMT
RUN Apply image 10.0.26100.32522
# Tue, 10 Mar 2026 22:43:00 GMT
SHELL [cmd /s /c]
# Tue, 10 Mar 2026 22:43:01 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 10 Mar 2026 22:43:01 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 10 Mar 2026 22:43:01 GMT
USER ContainerAdministrator
# Tue, 10 Mar 2026 22:43:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Mar 2026 22:43:07 GMT
USER ContainerUser
# Tue, 10 Mar 2026 22:43:18 GMT
COPY dir:7dbbb550790b7446baaa5767cc14c2e1895a96b2462584273935c311b414f284 in C:\openjdk-11 
# Tue, 10 Mar 2026 22:43:23 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 10 Mar 2026 22:43:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:06fab7822816d5f43d6835d07ac8db280fdf81384187f36d8dc43bbb7064a76d`  
		Last Modified: Tue, 10 Mar 2026 20:41:46 GMT  
		Size: 199.4 MB (199409325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f7869993458abe7da3875a434f95cf18f3fba5016f632bb0bc2664816a15ad`  
		Last Modified: Tue, 10 Mar 2026 22:43:29 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842191b0bcfd599eb0febb971cc25625d4d9ce2b98c55d1e2398130d7448000f`  
		Last Modified: Tue, 10 Mar 2026 22:43:29 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351393a3a3a0556c67831e361c2a1f152320be3fb48c2ec386921d4009c2aab`  
		Last Modified: Tue, 10 Mar 2026 22:43:29 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938a94a46f1fe53810ebbc962a4ac91a18c124b2f623e5169d18e7a930a88345`  
		Last Modified: Tue, 10 Mar 2026 22:43:29 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3086bcd4552e1fd6343037d4443143ea82161a187f06474f553dad7d61ecdb8`  
		Last Modified: Tue, 10 Mar 2026 22:43:27 GMT  
		Size: 70.1 KB (70065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c111b3caca8c855d8c1ff3d9bbe2f4ddba2a4e59f542160ea17064ae6e949e06`  
		Last Modified: Tue, 10 Mar 2026 22:43:27 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e368038ff98c24b808281ca18c21ec3af5f0967579a749a41ce62a2997062b`  
		Last Modified: Tue, 10 Mar 2026 22:43:39 GMT  
		Size: 194.7 MB (194722184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe4e7e98bd6894071160e0adc0bdd4acaa4c6e84a129046e9549a53d4dc350a`  
		Last Modified: Tue, 10 Mar 2026 22:43:27 GMT  
		Size: 93.9 KB (93935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4216bb452d890fb27e29735d17add13f5d3fbd467b8dfe91649fd3fcadcba081`  
		Last Modified: Tue, 10 Mar 2026 22:43:27 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-nanoserver` - windows version 10.0.20348.4893; amd64

```console
$ docker pull eclipse-temurin@sha256:3710d88c8b80a5e761630ba97a4874fa832fcebe8ab6bd047b038d243675a6de
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.5 MB (321549236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee599d7e8bc51c4f541a78dca66055ac5d740ff6a3335e47e139b661dbb443b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 10 Mar 2026 22:36:36 GMT
SHELL [cmd /s /c]
# Tue, 10 Mar 2026 22:36:36 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 10 Mar 2026 22:36:36 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 10 Mar 2026 22:36:36 GMT
USER ContainerAdministrator
# Tue, 10 Mar 2026 22:36:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Mar 2026 22:36:39 GMT
USER ContainerUser
# Tue, 10 Mar 2026 22:36:48 GMT
COPY dir:7dbbb550790b7446baaa5767cc14c2e1895a96b2462584273935c311b414f284 in C:\openjdk-11 
# Tue, 10 Mar 2026 22:36:52 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 10 Mar 2026 22:36:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807d2824c917294d6edf619f31fd4bf4797460117c9bf4a2a6c56070bbad5671`  
		Last Modified: Tue, 10 Mar 2026 22:36:58 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b606389192e14991a5534478afe7ef4e1fa322a48b2c216a67fec0782b04c27`  
		Last Modified: Tue, 10 Mar 2026 22:36:58 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a63de925c34262ddf9ecb4b3279884475aaaceefaa0d5b2ec7d6e0bd8ebd3c4`  
		Last Modified: Tue, 10 Mar 2026 22:36:58 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f354cf52ad25b19197e81e3f330c2179b0dc3e8bb43224ea65f5e606d5f33e6`  
		Last Modified: Tue, 10 Mar 2026 22:36:58 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f4080af4b8c4994342374ccdbb442a61b03d204fdd2500318b970c814f82f2`  
		Last Modified: Tue, 10 Mar 2026 22:36:57 GMT  
		Size: 72.2 KB (72192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b09c8f18c26357e82945519f23c4e47de1f3c6bc4a6d8387b09e7dd0edde2c`  
		Last Modified: Tue, 10 Mar 2026 22:36:56 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b34c7f002478f341e80459e7d324ad7d99a9ec1aeb4a4a935203224ca8a5c3`  
		Last Modified: Tue, 10 Mar 2026 22:37:09 GMT  
		Size: 194.7 MB (194722386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a98f2ba162a4d9a69f76683ff5c79d7501b18893ed94e45e06bd1a77f40cec5`  
		Last Modified: Tue, 10 Mar 2026 22:36:56 GMT  
		Size: 97.7 KB (97748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63da0d90a4ed6e91db7a5ef3b72f1aba19188b9afa1aec1e6f694d15bba1a3a9`  
		Last Modified: Tue, 10 Mar 2026 22:36:56 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
