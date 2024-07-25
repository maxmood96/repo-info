## `eclipse-temurin:8u422-b05-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:25e63a1448737794a58f4c19e9b75fdbd7ae5d94bda35d94b76c3509be6d0a49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:8u422-b05-jdk-nanoserver-1809` - windows version 10.0.17763.6054; amd64

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
