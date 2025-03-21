## `openjdk:25-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:7cbf393fa8e4f39519fb1578ba160eada19f0765ea21b9d3573c09150fa6323f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `openjdk:25-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull openjdk@sha256:ff4944def2ee5d43b27c1e37a7899f3946e2961b4958ecde2abeff6c86b78f42
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328400125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75133fb1c55e75e9a7cd2d272df10ff2713ce46cca91426e2e972d54b625829`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Fri, 21 Mar 2025 18:18:34 GMT
SHELL [cmd /s /c]
# Fri, 21 Mar 2025 18:18:35 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 21 Mar 2025 18:18:35 GMT
USER ContainerAdministrator
# Fri, 21 Mar 2025 18:18:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 21 Mar 2025 18:18:39 GMT
USER ContainerUser
# Fri, 21 Mar 2025 18:18:39 GMT
ENV JAVA_VERSION=25-ea+15
# Fri, 21 Mar 2025 18:18:47 GMT
COPY dir:e950963f28ad2c857b90aa9d6a65c8fd16c501192e94c7e71046153717554da9 in C:\openjdk-25 
# Fri, 21 Mar 2025 18:18:53 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 21 Mar 2025 18:18:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd48fd9d29a2821090b3b8fec24b3a44f16632dce562889db3a62fcc9be22c1`  
		Last Modified: Fri, 21 Mar 2025 18:18:58 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49a59884fba413b1c6453578d4118c00fea0fc2f2153d5559a18985addd6724`  
		Last Modified: Fri, 21 Mar 2025 18:18:58 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9b1d6b29187dfab5d8ba95d8e5b9f45ec0680551cc4165d7f551ba5e50c4b5`  
		Last Modified: Fri, 21 Mar 2025 18:18:57 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd5f7be5ee047eec2eae6eebd83ff5895729072bed5cfb7e72fc0cc47240d23`  
		Last Modified: Fri, 21 Mar 2025 18:18:58 GMT  
		Size: 78.2 KB (78189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41d18d85f1d311929cfeb870ba2e67556367b3707f1a800427603894c4e558b`  
		Last Modified: Fri, 21 Mar 2025 18:18:56 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97be6a64590fb8144655cc36c403b0039ce73ae37449e00f6784069948e25874`  
		Last Modified: Fri, 21 Mar 2025 18:18:56 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb87e3c4f139c3a78228e81e2157047d58b70f8de3ba9534d4980262101a560`  
		Last Modified: Fri, 21 Mar 2025 18:19:10 GMT  
		Size: 207.5 MB (207501933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a703a2a77b97af90a0f32734a368d42fa4c7f64c3f5137d9ecd6142ff2c13114`  
		Last Modified: Fri, 21 Mar 2025 18:18:56 GMT  
		Size: 118.3 KB (118270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1f327d99f51246552e009ccc3b71f554c00af2e3742e0eaec1c75f91e5beec`  
		Last Modified: Fri, 21 Mar 2025 18:18:56 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
