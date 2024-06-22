## `eclipse-temurin:17-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:2616126cf433b1c9d888635a8748c82332c7735f05a76d9a3a23f738fb8f8166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2529; amd64
	-	windows version 10.0.17763.5936; amd64

### `eclipse-temurin:17-nanoserver` - windows version 10.0.20348.2529; amd64

```console
$ docker pull eclipse-temurin@sha256:0f8c319ab26de1842d2c78c0b0cb97234ce94fb749be46f40c590fb2a8a90ec7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.5 MB (307488571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9900b967adca2a6320065d998bfe4901003f1128d1d5d2b4c252aafa67b2611c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 19 Jun 2024 19:27:30 GMT
RUN Apply image 10.0.20348.2529
# Sat, 22 Jun 2024 00:50:29 GMT
SHELL [cmd /s /c]
# Sat, 22 Jun 2024 00:53:04 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Sat, 22 Jun 2024 00:53:05 GMT
ENV JAVA_HOME=C:\openjdk-17
# Sat, 22 Jun 2024 00:53:06 GMT
USER ContainerAdministrator
# Sat, 22 Jun 2024 00:53:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 22 Jun 2024 00:53:16 GMT
USER ContainerUser
# Sat, 22 Jun 2024 00:53:31 GMT
COPY dir:58180deb8c422e61d331dbc12d9d7d83d7afe3e9097adb59bd0860aff4211c36 in C:\openjdk-17 
# Sat, 22 Jun 2024 00:53:45 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 22 Jun 2024 00:53:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a8c295c425a912de308ded279124ae45fec44d55a451843fe5877155417f453c`  
		Last Modified: Fri, 21 Jun 2024 02:24:34 GMT  
		Size: 120.5 MB (120499549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c04e6fe7f33e5ed7b73641c362d031eb0404b55967c9af2b8fa6f2269d9f92`  
		Last Modified: Sat, 22 Jun 2024 01:06:26 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9803dbc941f205828a0d8bc61e5dc9da41077da5e02114f4902bbbbc156ecc7b`  
		Last Modified: Sat, 22 Jun 2024 01:07:58 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5739c49a35688d6f38646859512fb3830f981dda2c790af7ccb4565dc33c39`  
		Last Modified: Sat, 22 Jun 2024 01:07:58 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406a1038bc5a44c9617393f7df8f7f50605ad1fbc13ec30241c95aeceb276188`  
		Last Modified: Sat, 22 Jun 2024 01:07:58 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d3aa002337d4eaa521b373b4706827a1de9f68f132b657b37396fd96b13642`  
		Last Modified: Sat, 22 Jun 2024 01:07:56 GMT  
		Size: 85.7 KB (85652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299ddcec7bd2eda31e50cbf79a3641cee7d67a859279f54204fdf1d1a845becb`  
		Last Modified: Sat, 22 Jun 2024 01:07:56 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401d9b39db2bbbbd135721ee09efe261f0f5fbb97dab47eb5d4fa907b6827dbf`  
		Last Modified: Sat, 22 Jun 2024 01:08:14 GMT  
		Size: 186.8 MB (186837820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960589807b1fd14f61140b039d02cee0845fdf831d339238c1c2de22bdb89c07`  
		Last Modified: Sat, 22 Jun 2024 01:07:56 GMT  
		Size: 58.6 KB (58559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444c71a6de1bddc2e7a78281587a4a5d1022871be8c5504f3fcb862a61e43b55`  
		Last Modified: Sat, 22 Jun 2024 01:07:56 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull eclipse-temurin@sha256:1bc49f2ba2fedfb58066f1f87e2e120f2fd23e8bef4237a2416cd7a0676ce011
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.6 MB (345558830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd6a01d39502413f2c2b1d705467d462fac8736f74df0c1f666a805af44ce88`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 17:41:08 GMT
SHELL [cmd /s /c]
# Wed, 12 Jun 2024 18:01:17 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Wed, 12 Jun 2024 18:01:17 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 12 Jun 2024 18:01:18 GMT
USER ContainerAdministrator
# Wed, 12 Jun 2024 18:01:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Jun 2024 18:01:27 GMT
USER ContainerUser
# Wed, 12 Jun 2024 18:01:41 GMT
COPY dir:58180deb8c422e61d331dbc12d9d7d83d7afe3e9097adb59bd0860aff4211c36 in C:\openjdk-17 
# Wed, 12 Jun 2024 18:01:53 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Jun 2024 18:01:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce076c01ab33a997d8fa4a6a49752f31455fef6df331991ad3b3736b3567321`  
		Last Modified: Wed, 12 Jun 2024 18:40:43 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef4283eaec67ab82eb2eaf1394d348ef4b8095aae26938603564e9753ed3dd7`  
		Last Modified: Wed, 12 Jun 2024 18:46:00 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0971dcb75451d4945808f751c16bd6b1107708957392106f500273c3cf43c75`  
		Last Modified: Wed, 12 Jun 2024 18:45:59 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3fca7aa45609ebcb6f1aa65ba03489b6c380371840a7fc5a632bcd0ac82392`  
		Last Modified: Wed, 12 Jun 2024 18:45:59 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba8307dff66a644bbf0fc5a0ff9fade24aa29f5e1cb3bffbacb7750b6cad920`  
		Last Modified: Wed, 12 Jun 2024 18:45:57 GMT  
		Size: 69.0 KB (69006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc382ff7ccb019cad431b62ae9298ebe9978a095189f90effbaad82ad26c18b`  
		Last Modified: Wed, 12 Jun 2024 18:45:57 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee897e1a071b3afd6ae08b496852edc6ba1d0f4435ad9a4d0b5db4d1eec72ede`  
		Last Modified: Wed, 12 Jun 2024 18:46:15 GMT  
		Size: 186.8 MB (186837675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0155fe02bdeed1b382320fc46f20130f5d5f31384969519752fa2e8465b7b92`  
		Last Modified: Wed, 12 Jun 2024 18:45:58 GMT  
		Size: 3.6 MB (3611978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2899c8a81b879525f1137bccf3723ac4149b3d00d893a8088e7152a4fc25c6f9`  
		Last Modified: Wed, 12 Jun 2024 18:45:57 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
