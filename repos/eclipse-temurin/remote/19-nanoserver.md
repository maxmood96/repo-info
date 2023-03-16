## `eclipse-temurin:19-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:72b009fa10a30e3259b46a9c9de015280ddc41a1d43fc1c6d3634f61b60db83c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1607; amd64
	-	windows version 10.0.17763.4131; amd64

### `eclipse-temurin:19-nanoserver` - windows version 10.0.20348.1607; amd64

```console
$ docker pull eclipse-temurin@sha256:7c77b51585242a1a63d183fc557a18dc09c87216112d9cc542e0ba7cbe8f14e1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.6 MB (315592053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c009fe308e53bbcd5f26cf811c2250b6e985f6fa0ff4c75770a90455e75445b2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 10 Mar 2023 06:31:34 GMT
RUN Apply image 10.0.20348.1607
# Thu, 16 Mar 2023 01:29:33 GMT
SHELL [cmd /s /c]
# Thu, 16 Mar 2023 01:35:36 GMT
ENV JAVA_VERSION=jdk-19.0.2+7
# Thu, 16 Mar 2023 01:35:37 GMT
ENV JAVA_HOME=C:\openjdk-19
# Thu, 16 Mar 2023 01:35:38 GMT
USER ContainerAdministrator
# Thu, 16 Mar 2023 01:35:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 16 Mar 2023 01:35:51 GMT
USER ContainerUser
# Thu, 16 Mar 2023 01:36:08 GMT
COPY dir:09b3ada3bc8ac44822b97a9a56d697461744d2194cdcb6ab15233b0b9b376e38 in C:\openjdk-19 
# Thu, 16 Mar 2023 01:36:33 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 01:36:34 GMT
CMD ["jshell"]
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
	-	`sha256:5b8368ab26766b1ef7119f27b772d8ca295abc4f1ae402c1abc5344eeb2c40e7`  
		Last Modified: Thu, 16 Mar 2023 01:56:37 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2af9e20da7f3492d119eacd3a37388367f7429187dc13c8b3d4bf08fff30d2`  
		Last Modified: Thu, 16 Mar 2023 01:56:37 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e403e4e4258e98ee4fc68c4c4869158919b12cbe60414d72bcd2aabb3aab9cda`  
		Last Modified: Thu, 16 Mar 2023 01:56:37 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd4649ce4adc2d497c5f3a2e3dfc4f926f5216a16dcf2cae2b8c49c30b83daf`  
		Last Modified: Thu, 16 Mar 2023 01:56:35 GMT  
		Size: 83.5 KB (83490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb0f61c24a4bfc9fb00ed911061dede47133ef40e6e8ba90a45b71e3381dd2e`  
		Last Modified: Thu, 16 Mar 2023 01:56:35 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:315c8da99a1ef096248b8f7e33f0d39899d241e3859d0dbaf803fce29c72ae2a`  
		Last Modified: Thu, 16 Mar 2023 01:56:57 GMT  
		Size: 193.3 MB (193266775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9ebc50084cd7b2634e0acc3f03c6c8f7958be76b4bc15034625003085f7cfc`  
		Last Modified: Thu, 16 Mar 2023 01:56:35 GMT  
		Size: 63.1 KB (63065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52036e46a4b7cbb49b2867ef3d42410c712a28b0009024b63c486bb7df513534`  
		Last Modified: Thu, 16 Mar 2023 01:56:35 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:19-nanoserver` - windows version 10.0.17763.4131; amd64

```console
$ docker pull eclipse-temurin@sha256:6a02398702faf6af5cd722b5095fc8cf3aad600be766694979646b296bce299f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.7 MB (303742684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744a1d086ca19f0d1baad4001a498304074c5ab98923e84af92229084e8ebbb2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 11 Mar 2023 10:09:02 GMT
RUN Apply image 10.0.17763.4131
# Thu, 16 Mar 2023 00:45:50 GMT
SHELL [cmd /s /c]
# Thu, 16 Mar 2023 01:23:09 GMT
ENV JAVA_VERSION=jdk-19.0.2+7
# Thu, 16 Mar 2023 01:23:10 GMT
ENV JAVA_HOME=C:\openjdk-19
# Thu, 16 Mar 2023 01:23:11 GMT
USER ContainerAdministrator
# Thu, 16 Mar 2023 01:23:22 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 16 Mar 2023 01:23:23 GMT
USER ContainerUser
# Thu, 16 Mar 2023 01:23:39 GMT
COPY dir:09b3ada3bc8ac44822b97a9a56d697461744d2194cdcb6ab15233b0b9b376e38 in C:\openjdk-19 
# Thu, 16 Mar 2023 01:24:03 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 01:24:05 GMT
CMD ["jshell"]
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
	-	`sha256:ff0203cee4455804fb9efd8e5ab10476e33070a8381b133321b6040a7165dc13`  
		Last Modified: Thu, 16 Mar 2023 01:52:14 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b597da8738d9af3f7b678cb69221dd791517cffd43be0c5b8827d58396fc8f`  
		Last Modified: Thu, 16 Mar 2023 01:52:14 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b13b51bc5f7e086a7933dc25e93e541c6c5567835954dccda0b9acfa548c93`  
		Last Modified: Thu, 16 Mar 2023 01:52:14 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f93025d0762ff8183a41d12c546f8e1e228d843cd806b8517d9cb7a69d6416`  
		Last Modified: Thu, 16 Mar 2023 01:52:12 GMT  
		Size: 69.0 KB (69016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e445ed55caa35f1d5ff0e86202f3d3e09a051af742b5da6b3fefcd35016367`  
		Last Modified: Thu, 16 Mar 2023 01:52:12 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a6ff9c8dc682113b7153df0453a70bc5630bf741e13159ae12656cf1b777bc`  
		Last Modified: Thu, 16 Mar 2023 01:52:35 GMT  
		Size: 193.3 MB (193263057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a97ae539f1eb1900c5037b4de4dec702fae38e598cec5d621f08efc0634e23d`  
		Last Modified: Thu, 16 Mar 2023 01:52:13 GMT  
		Size: 3.7 MB (3719393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904469d8a93946c4060bc6eedc746ec185223a9d9c44392c1c7b0d1ca8483cb4`  
		Last Modified: Thu, 16 Mar 2023 01:52:12 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
