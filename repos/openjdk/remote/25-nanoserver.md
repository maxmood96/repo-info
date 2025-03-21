## `openjdk:25-nanoserver`

```console
$ docker pull openjdk@sha256:54160a3dbdfe4eec5e29de4a9565992f621db410e8148b5822a43a11e6906833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `openjdk:25-nanoserver` - windows version 10.0.26100.3476; amd64

```console
$ docker pull openjdk@sha256:519c8fb2b9438b93c5d924f276146eed307ee343161ecf7274187a4caa07a355
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.0 MB (414017991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f3866e2acef58a78f7cb0877767352f40d9c4f7b95b2deefde7c645cd02b793`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Fri, 21 Mar 2025 18:13:12 GMT
SHELL [cmd /s /c]
# Fri, 21 Mar 2025 18:13:13 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 21 Mar 2025 18:13:14 GMT
USER ContainerAdministrator
# Fri, 21 Mar 2025 18:13:17 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 21 Mar 2025 18:13:19 GMT
USER ContainerUser
# Fri, 21 Mar 2025 18:13:20 GMT
ENV JAVA_VERSION=25-ea+15
# Fri, 21 Mar 2025 18:13:27 GMT
COPY dir:e950963f28ad2c857b90aa9d6a65c8fd16c501192e94c7e71046153717554da9 in C:\openjdk-25 
# Fri, 21 Mar 2025 18:13:34 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 21 Mar 2025 18:13:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735775f52d6eaaa6628c87a3ef88b136a7c710c7efe206f53589f81cb05469c1`  
		Last Modified: Fri, 21 Mar 2025 18:13:41 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9111da4106e55db039829e713d5d3f4773afbee5a6fd369f3b3c1e74ff848f8`  
		Last Modified: Fri, 21 Mar 2025 18:13:41 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bb35d737f68628f448f7b0c1518661fcdff1aaf666970600421b042ef47292`  
		Last Modified: Fri, 21 Mar 2025 18:13:41 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711c349e58374c2e0699900395f3709c8c2449d81d031e6f10b63b87d1c9be93`  
		Last Modified: Fri, 21 Mar 2025 18:13:41 GMT  
		Size: 75.9 KB (75904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0a8476a77a928f4ce439d0c5efbe80204e4251e6d5cbbcd9083e88f12eb5fb`  
		Last Modified: Fri, 21 Mar 2025 18:13:39 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc974b6e37408dd189909ee6d445cb7227f272eb95b72466ca4dfca593272f48`  
		Last Modified: Fri, 21 Mar 2025 18:13:39 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e186b2735601841540165648cf5d4aeeaf68718f9df674e2c46b534bd704513`  
		Last Modified: Fri, 21 Mar 2025 18:13:51 GMT  
		Size: 207.5 MB (207501808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d029cf565449debf2a0cf9f0a972d8742685d7f18ba2d7c17f2a6633c38079`  
		Last Modified: Fri, 21 Mar 2025 18:13:39 GMT  
		Size: 131.8 KB (131751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ca1a2f60e1303d192ef4a2b44957c0ff3d1f4a3aa9d68498cd6cf1ce80e9f1`  
		Last Modified: Fri, 21 Mar 2025 18:13:39 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-nanoserver` - windows version 10.0.20348.3328; amd64

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

### `openjdk:25-nanoserver` - windows version 10.0.17763.7009; amd64

```console
$ docker pull openjdk@sha256:977e258f2f76e0e00f2af4aa2d9afcd6d4ca70e1385da1b545572778ab9c0ec5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.9 MB (318906744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcbed0d385c24dbe0b318f0ce521a16dc1b65f887a9de2c998668d8b43977f71`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Fri, 21 Mar 2025 18:15:20 GMT
SHELL [cmd /s /c]
# Fri, 21 Mar 2025 18:15:22 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 21 Mar 2025 18:15:22 GMT
USER ContainerAdministrator
# Fri, 21 Mar 2025 18:15:24 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 21 Mar 2025 18:15:25 GMT
USER ContainerUser
# Fri, 21 Mar 2025 18:15:25 GMT
ENV JAVA_VERSION=25-ea+15
# Fri, 21 Mar 2025 18:15:32 GMT
COPY dir:e950963f28ad2c857b90aa9d6a65c8fd16c501192e94c7e71046153717554da9 in C:\openjdk-25 
# Fri, 21 Mar 2025 18:15:38 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 21 Mar 2025 18:15:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc960cac91ac363a95bef98a38cc3fb38959fa72bc0cb7265db2189a3a2e235a`  
		Last Modified: Fri, 21 Mar 2025 18:15:44 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a79cc5df8e0c7c8e6c563687a0f78d9870101094935a115b6870b8a9492fad`  
		Last Modified: Fri, 21 Mar 2025 18:15:43 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3300230bafc1fabe41a5770baa1e47cdcc97ad21e23f5a50534401d8b14c14`  
		Last Modified: Fri, 21 Mar 2025 18:15:43 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b900f540f263cb8a381ed0994e9bf77a8d728dab20861e8b814619f0338aea`  
		Last Modified: Fri, 21 Mar 2025 18:15:43 GMT  
		Size: 69.0 KB (69007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c1547c89f815bb84fdd7658f9d9202b0e22836d7a24573fd1f925db9f1a475`  
		Last Modified: Fri, 21 Mar 2025 18:15:42 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985796622cb9631672c0810504b1c1b32008b7f14be35e0434ddf49b89f329`  
		Last Modified: Fri, 21 Mar 2025 18:15:42 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15788921873c8cacd33c7f356128579bb2e1692261e82123a3108d4e60fc505`  
		Last Modified: Fri, 21 Mar 2025 18:15:53 GMT  
		Size: 207.5 MB (207502652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba29098ea7f10232e0f69015f2095bff4d06221e8fb282e2e62203b5107e69f`  
		Last Modified: Fri, 21 Mar 2025 18:15:42 GMT  
		Size: 4.4 MB (4421007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd15deb15c083c0b0cc3b10c5f2512d0d55c61f196dd6dc470c7b0787c7940e3`  
		Last Modified: Fri, 21 Mar 2025 18:15:42 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
