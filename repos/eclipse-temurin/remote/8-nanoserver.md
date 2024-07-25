## `eclipse-temurin:8-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:51e912c63814aa6812aee9de41e25d921d83ac5ad2b9d77b11e4367e1aad9749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:8-nanoserver` - windows version 10.0.20348.2582; amd64

```console
$ docker pull eclipse-temurin@sha256:a76f6ed5f20bf5aed9498991310f34680d07fd5ea4d2ed2b0df580bb8fffea38
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.2 MB (222184220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b13cb11169e08db7d90ffa0e925a2b6c22fbaf9a0cb49393800bfa28f03e07`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 09:30:07 GMT
RUN Apply image 10.0.20348.2582
# Wed, 10 Jul 2024 17:17:20 GMT
SHELL [cmd /s /c]
# Thu, 25 Jul 2024 17:25:11 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 25 Jul 2024 17:25:12 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 25 Jul 2024 17:25:13 GMT
USER ContainerAdministrator
# Thu, 25 Jul 2024 17:25:22 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 25 Jul 2024 17:25:22 GMT
USER ContainerUser
# Thu, 25 Jul 2024 17:25:32 GMT
COPY dir:cf98fec7e439356342f3bf03fb67b0dac0e213296a20d5e427a9ebba9080193e in C:\openjdk-8 
# Thu, 25 Jul 2024 17:25:51 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:652774a5d82a114642848f8b0b8d486ec1b4995f9dda56e36fe4ac7563429990`  
		Last Modified: Tue, 09 Jul 2024 20:33:26 GMT  
		Size: 120.5 MB (120490378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1dbb650483c31087741ccfe7cfef17abfd7465711d0851e35d39eabc775bdae`  
		Last Modified: Wed, 10 Jul 2024 17:38:52 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd0adf4702d813bb7fa724c9bf2343c201391c6d70a7a35135b18cc53499721`  
		Last Modified: Thu, 25 Jul 2024 17:31:42 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94884a864d317b3caa2f721285e95de08018c4d1388ebfcc7b74d0b3371564c`  
		Last Modified: Thu, 25 Jul 2024 17:31:41 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4085421efae24344eed5fb063a3fed76207a5fa6434c58e5060c180b76b7821`  
		Last Modified: Thu, 25 Jul 2024 17:31:40 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82df57eb258bb9e82243a6cda569545565c89aa9f4d19b7a9d443746926e680`  
		Last Modified: Thu, 25 Jul 2024 17:31:40 GMT  
		Size: 80.4 KB (80387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183f1e530fbf61205e4a140565535007984ca4ba7ad524ccc77eca5b3a7d54d9`  
		Last Modified: Thu, 25 Jul 2024 17:31:40 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cdac0f4413cb012aac3babb0a1abd8f892241861c762955ba0c61f67517c1c`  
		Last Modified: Thu, 25 Jul 2024 17:31:50 GMT  
		Size: 101.5 MB (101546680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2de5554842da9307d189264477fdcca898988edbf8443c1cc3fa011787f551`  
		Last Modified: Thu, 25 Jul 2024 17:31:40 GMT  
		Size: 61.0 KB (60996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-nanoserver` - windows version 10.0.17763.6054; amd64

```console
$ docker pull eclipse-temurin@sha256:09732ef666e3dfc1ac50d7fcc28cbc949b641aebda0cefcb78792ee1637efdde
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 MB (256780243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932e0f2bccaf5ff85a292d08b3714c2740bd9a6895ad05feaf9ce34eeae81052`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 16:38:43 GMT
SHELL [cmd /s /c]
# Thu, 25 Jul 2024 17:18:48 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 25 Jul 2024 17:18:48 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 25 Jul 2024 17:18:49 GMT
USER ContainerAdministrator
# Thu, 25 Jul 2024 17:18:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 25 Jul 2024 17:18:56 GMT
USER ContainerUser
# Thu, 25 Jul 2024 17:19:04 GMT
COPY dir:cf98fec7e439356342f3bf03fb67b0dac0e213296a20d5e427a9ebba9080193e in C:\openjdk-8 
# Thu, 25 Jul 2024 17:19:13 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00a79547db1bc3ab4a5550f2ec9ba165e302f4a4984af3c1bfbbbe1726a3bf6`  
		Last Modified: Wed, 10 Jul 2024 17:28:00 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848e7677215baaa1434649f02f2e139006fe6a40682b242095f66c53026b6c45`  
		Last Modified: Thu, 25 Jul 2024 17:30:20 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49149340728b0e7f5b7f7808d620efa8d5915f34b567ccdfea2e5660c32bd101`  
		Last Modified: Thu, 25 Jul 2024 17:30:19 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1578cbd6d39d4b23817f2fa5cb7e6271d3186bd15660e9534c1b74d53ac0db4`  
		Last Modified: Thu, 25 Jul 2024 17:30:17 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb2abf155b203af9595a7cadd2a3a3e6ff6134100de207677d10db7ef3b0ccd`  
		Last Modified: Thu, 25 Jul 2024 17:30:17 GMT  
		Size: 69.0 KB (68980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f76482775d497e229394b5d2b7349baeeb1a2c81c9a8eab72a3e42fe6505d9`  
		Last Modified: Thu, 25 Jul 2024 17:30:17 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8cb1442827022999a4f0d81cfb742266c6b6deb229b8c2e97ef84ac343d695`  
		Last Modified: Thu, 25 Jul 2024 17:30:27 GMT  
		Size: 101.5 MB (101544044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370b181feb077245de58e10019444e9016ea3671a1da7d922082d09506893af7`  
		Last Modified: Thu, 25 Jul 2024 17:30:17 GMT  
		Size: 80.1 KB (80142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
