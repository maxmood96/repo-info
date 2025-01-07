## `eclipse-temurin:11-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:a836a3f7b92016b54070e0f4bba1e7f88704e8b85dde2a2cf6f473e4c86f766e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.20348.2966; amd64

```console
$ docker pull eclipse-temurin@sha256:9d8c5e6622970d398473aad3b27847b1c23d8de2312f7a95b1253c5ba2be5d8c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316463595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39540fa9da638f924128a2c1884e249b5ae66b47c8a4c1a425670a6ad6700e9b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Dec 2024 01:18:54 GMT
RUN Apply image 10.0.20348.2966
# Wed, 11 Dec 2024 21:49:03 GMT
SHELL [cmd /s /c]
# Wed, 11 Dec 2024 21:49:04 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 11 Dec 2024 21:49:05 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 11 Dec 2024 21:49:05 GMT
USER ContainerAdministrator
# Wed, 11 Dec 2024 21:49:08 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Dec 2024 21:49:08 GMT
USER ContainerUser
# Wed, 11 Dec 2024 21:49:15 GMT
COPY dir:92a047b71eec51fdc82b01f518237bef64c78b39e065fcc3e9561b3909a60868 in C:\openjdk-11 
# Wed, 11 Dec 2024 21:49:21 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 11 Dec 2024 21:49:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f9d5d5ca3244fc2c429a892cbe6066394790f649f32d59acfdf012e490896378`  
		Last Modified: Tue, 10 Dec 2024 18:34:17 GMT  
		Size: 120.6 MB (120601318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71271aedcf4f313aa803008ea5725c2e889c77c05b57066d2bf60c27f3bfb2d`  
		Last Modified: Wed, 11 Dec 2024 21:49:24 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b421306d5738c690cd0009f30c5e2df80cdf42a8b7149b3ea2f1a23a9abb6e4d`  
		Last Modified: Wed, 11 Dec 2024 21:49:24 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b13d7334c255bbd9dafdcce4ee0b691b36c3a01306a13875367a04fa576f726`  
		Last Modified: Wed, 11 Dec 2024 21:49:24 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a25fd80991542a47e3f88ec3b52206c3ddff3d9ccb2d802261af9c7addccfd`  
		Last Modified: Wed, 11 Dec 2024 21:49:24 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620df7fff05fa68365a0bed09a94f03cb1eaa2b4ace64cebea52ef50514f975d`  
		Last Modified: Wed, 11 Dec 2024 21:49:23 GMT  
		Size: 77.2 KB (77211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6977a85ea30d1cb0ec33d9cf813eff556e1f10d75e534954ea798fd182fe9fd2`  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eba6a698862ba8dd7ed0b3a27b14487b1a90fc45994e2030b6c23b33ffe0284`  
		Last Modified: Wed, 11 Dec 2024 21:49:33 GMT  
		Size: 195.7 MB (195671821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec378d60eabb62b956e7ee02e5c8fbc23aa7c9192770631118c1f6ea86f49f7`  
		Last Modified: Wed, 11 Dec 2024 21:49:23 GMT  
		Size: 107.1 KB (107061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba65b1d0f2357b190f3adb7131db2e38db540a8d6549f31bbcb0e76a2f61952`  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.17763.6659; amd64

```console
$ docker pull eclipse-temurin@sha256:5028f385ee5fbc158b876123c6602e2ffe5907152b7d581f927f11063b801911
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.1 MB (351105803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e129034e159ca61700d396d4177831e305331a7f3b5cc418d369695d789821a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Wed, 11 Dec 2024 21:47:33 GMT
SHELL [cmd /s /c]
# Wed, 11 Dec 2024 21:47:34 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 11 Dec 2024 21:47:35 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 11 Dec 2024 21:47:35 GMT
USER ContainerAdministrator
# Wed, 11 Dec 2024 21:47:37 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Dec 2024 21:47:38 GMT
USER ContainerUser
# Wed, 11 Dec 2024 21:47:45 GMT
COPY dir:92a047b71eec51fdc82b01f518237bef64c78b39e065fcc3e9561b3909a60868 in C:\openjdk-11 
# Wed, 11 Dec 2024 21:47:50 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 11 Dec 2024 21:47:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Tue, 10 Dec 2024 21:03:34 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32514715eb23509216981b3c7e47c29a7d65d30b56169de58a686b52d49a99a`  
		Last Modified: Wed, 11 Dec 2024 21:47:54 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8108a0af0d948a494513cb79dd924dd41cf84dc9f5753ac0ce6632d001b5329`  
		Last Modified: Wed, 11 Dec 2024 21:47:54 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0074b2f6487c6ec3c654d7d161b4d53fea90b263d702f0e7a01a6bb7a8fa1f80`  
		Last Modified: Wed, 11 Dec 2024 21:47:54 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31238fe0f9b606a3991f4ece4c203add1bdf35068ff8c932148ec817eee3bc27`  
		Last Modified: Wed, 11 Dec 2024 21:47:54 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a85026d9d92b44582ba928d3f341ec4dfb355bcdb757e469527f87d71c956b31`  
		Last Modified: Wed, 11 Dec 2024 21:47:53 GMT  
		Size: 74.5 KB (74463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d271883ea23bebfbc5e3a3d2d235936a41a9aa8e0fc23b77662c94be0f16a154`  
		Last Modified: Wed, 11 Dec 2024 21:47:53 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cc1aa99f5ce5d3092b9a8dc1400d6b111e012dfea9a7310b1991808464c4c7`  
		Last Modified: Wed, 11 Dec 2024 21:48:03 GMT  
		Size: 195.7 MB (195672619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b4fd1e519c4acacb2cbdc41da11e7f742367fa79bec49207536443e30a9a00`  
		Last Modified: Wed, 11 Dec 2024 21:47:53 GMT  
		Size: 120.9 KB (120871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824b2f62c2965b901024846c4543340a7b1a4994d41fad266516c36b59176474`  
		Last Modified: Wed, 11 Dec 2024 21:47:53 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
