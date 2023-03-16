## `eclipse-temurin:17-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:d03b3451ed6fc846283fa7f5c44d4e8f5a53977e397c80c7118881c9a06e784f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1607; amd64
	-	windows version 10.0.17763.4131; amd64

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.20348.1607; amd64

```console
$ docker pull eclipse-temurin@sha256:74d8be038436e3dbff802c4f662a2597a2726a7596a7bf4e7536d969cf8b834a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165633665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e067f4b9c4a6a756486ac54aa842e4ae8ed950ed5ac835a98fec76d1cda4a6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 10 Mar 2023 06:31:34 GMT
RUN Apply image 10.0.20348.1607
# Thu, 16 Mar 2023 01:29:33 GMT
SHELL [cmd /s /c]
# Thu, 16 Mar 2023 01:33:25 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 01:33:26 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 16 Mar 2023 01:33:27 GMT
USER ContainerAdministrator
# Thu, 16 Mar 2023 01:33:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 16 Mar 2023 01:33:39 GMT
USER ContainerUser
# Thu, 16 Mar 2023 01:35:03 GMT
COPY dir:bfcbd3aaadac52e2fbf5597edb59a69874950e88ce16232f7581c0ac600a935c in C:\openjdk-17 
# Thu, 16 Mar 2023 01:35:24 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:7abf0a70d48bf65f3d985f5780d4bdaece36f1f4bb8be10d5a6aacce33dacc75`  
		Last Modified: Thu, 16 Mar 2023 01:54:24 GMT  
		Size: 122.2 MB (122171731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a611a20686e9374e3a55a49399506f83c041ae711ed47018c2267c341156dd97`  
		Last Modified: Thu, 16 Mar 2023 01:53:50 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9653c7841fe2911686bb05797100e5d3aac112a6c5a31fd109fdf273c3c7d81`  
		Last Modified: Thu, 16 Mar 2023 01:55:45 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d961af1d066326c8e1186fbc6876a3d4dbe91d3d6872218505bec61dd725a21f`  
		Last Modified: Thu, 16 Mar 2023 01:55:45 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69ba0af288067e9cca1f23c1de2ead5658b53ed2546ea3de73c6f4e1b897504`  
		Last Modified: Thu, 16 Mar 2023 01:55:45 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1548f7ad98467d9f81b01049dc8293c2e89075b47855b6bbd4ec968122d401d`  
		Last Modified: Thu, 16 Mar 2023 01:55:43 GMT  
		Size: 80.0 KB (80016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24269970d76158337295eb022f62b2023eea8965be236222ea57b4f5ccbc6159`  
		Last Modified: Thu, 16 Mar 2023 01:55:43 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cbc4a7b5427450a6e5d523262fb3273cd8034130f6f1407e20654816e9a0b10`  
		Last Modified: Thu, 16 Mar 2023 01:56:26 GMT  
		Size: 43.3 MB (43302944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8851ba0bafe905a3205ec495e147ee16420736f1c2abc661f4cc5df7debc7136`  
		Last Modified: Thu, 16 Mar 2023 01:56:16 GMT  
		Size: 73.1 KB (73146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.17763.4131; amd64

```console
$ docker pull eclipse-temurin@sha256:1afb94125f9db70efc1fb8543ffef0e43f30cc4847c47956c3bec60e1da033f5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153085347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b776e99e186bf59d9270ff5412853630d1741213ff4879a82a73e5d12ca0a1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 11 Mar 2023 10:09:02 GMT
RUN Apply image 10.0.17763.4131
# Thu, 16 Mar 2023 00:45:50 GMT
SHELL [cmd /s /c]
# Thu, 16 Mar 2023 01:10:40 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 01:10:41 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 16 Mar 2023 01:10:42 GMT
USER ContainerAdministrator
# Thu, 16 Mar 2023 01:10:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 16 Mar 2023 01:10:54 GMT
USER ContainerUser
# Thu, 16 Mar 2023 01:16:29 GMT
COPY dir:bfcbd3aaadac52e2fbf5597edb59a69874950e88ce16232f7581c0ac600a935c in C:\openjdk-17 
# Thu, 16 Mar 2023 01:16:47 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:95eb2f0f3287f5ec687287cc244924aafc74c7ada3121d43f54223487f3f2d8d`  
		Last Modified: Thu, 16 Mar 2023 01:43:14 GMT  
		Size: 106.7 MB (106684240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5837fe68a36caddf38b0aaa99f4ef20ca36d8dfe2825fa6ffbcf0d38b9d59a`  
		Last Modified: Thu, 16 Mar 2023 01:42:43 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cef6b623b0498bbc748423c89b5ead7b9c77269a3ff759cdbeb3067625df172`  
		Last Modified: Thu, 16 Mar 2023 01:49:08 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4c24f4b371e2c05b725b983ca3515f3a9e357c1be997893795a766ef67f631`  
		Last Modified: Thu, 16 Mar 2023 01:49:07 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d088c9439a9a0516cb592c4a77f5cc4e3a76015e3ea92d78de5a491305b667`  
		Last Modified: Thu, 16 Mar 2023 01:49:07 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1acbd9403c07bd275e88a3a4f87c12423f8e635b4be1bb490e565397fe2d64de`  
		Last Modified: Thu, 16 Mar 2023 01:49:05 GMT  
		Size: 71.6 KB (71593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a3b89d22970421cb0ce96cf04bef4d162f237ff90934963e4f6d0df4049d78`  
		Last Modified: Thu, 16 Mar 2023 01:49:05 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae2b48dd8e0a9fe886bbb7ffd2727b08b0d7815ae4c3a11bba4c9bd16fba698`  
		Last Modified: Thu, 16 Mar 2023 01:50:32 GMT  
		Size: 43.3 MB (43287776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:631ef4a88895bdaefcf26304b20be5f3ac693218c8495c2ed55e57c53088951b`  
		Last Modified: Thu, 16 Mar 2023 01:50:23 GMT  
		Size: 3.0 MB (3035890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
