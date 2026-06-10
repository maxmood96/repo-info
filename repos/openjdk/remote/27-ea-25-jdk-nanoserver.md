## `openjdk:27-ea-25-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:d1ebba35064478b4bcc145f104ef5f87d7159f9ff0f6a2e853e06a5c9c8227e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `openjdk:27-ea-25-jdk-nanoserver` - windows version 10.0.26100.32995; amd64

```console
$ docker pull openjdk@sha256:08e1aa0a37fd88656c31707cb193b4781513452747eb708a4108139cf9787f56
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.0 MB (419956848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15855624a2d3c7e1caeaef6d79b20a3d533a6cd5585c7e66d7ff05da4f0622f0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 07:06:15 GMT
RUN Apply image 10.0.26100.32995
# Tue, 09 Jun 2026 23:20:06 GMT
SHELL [cmd /s /c]
# Tue, 09 Jun 2026 23:22:00 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 09 Jun 2026 23:22:00 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2026 23:22:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 09 Jun 2026 23:22:03 GMT
USER ContainerUser
# Tue, 09 Jun 2026 23:22:03 GMT
ENV JAVA_VERSION=27-ea+25
# Tue, 09 Jun 2026 23:22:25 GMT
COPY dir:2d44b60de7278e1e5741976187b08fdfd7908345a04ec10edcdba62993c11b6a in C:\openjdk-27 
# Tue, 09 Jun 2026 23:22:30 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 09 Jun 2026 23:22:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:64f5cd94d3bcd0fae94830b1fad0f8b3dc33677f8d7dc15c5219b56fe2a6584e`  
		Last Modified: Tue, 09 Jun 2026 22:11:30 GMT  
		Size: 196.7 MB (196668131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a4212199a2492ffd90053401f0671a7aad235421e10c6dd150b4603e354a1d`  
		Last Modified: Tue, 09 Jun 2026 23:20:46 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f581a0a81c777d2fa0bc486bbeba304197c9ce0b0c58e29d5d728ce526b9f6f2`  
		Last Modified: Tue, 09 Jun 2026 23:22:36 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f00773cb9bfe86758b307ab7541964931554d3dc30787fb2994feb99225677`  
		Last Modified: Tue, 09 Jun 2026 23:22:36 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e9816e6c114f83fa5815b5c46ace4206709345241bb2d2fa726bd969d106a7`  
		Last Modified: Tue, 09 Jun 2026 23:22:36 GMT  
		Size: 75.2 KB (75171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c86a4d111866ed25938bb944916b2cfbdc4d5cd1bd8652fed018a43648a7177`  
		Last Modified: Tue, 09 Jun 2026 23:22:34 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9501f4c2615c8e9d3123458af4c53fa43e9e9a389542521972d3f161e62f35`  
		Last Modified: Tue, 09 Jun 2026 23:22:34 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc5b74d8c2809f2f511ccd28828ccffbf7647bde8c6577cdfc2966bd5b38d80`  
		Last Modified: Tue, 09 Jun 2026 23:22:50 GMT  
		Size: 223.1 MB (223094878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d280a45f4b31873df3fc984cb0d44627f31ceecea41d75c831b550b0e5d35239`  
		Last Modified: Tue, 09 Jun 2026 23:22:35 GMT  
		Size: 112.4 KB (112391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a37bdf92dd5e67d6b84e2ccc87cc832cc18c298c18a7504598bc234aa737ea`  
		Last Modified: Tue, 09 Jun 2026 23:22:34 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-25-jdk-nanoserver` - windows version 10.0.20348.5256; amd64

```console
$ docker pull openjdk@sha256:b4421b7570109879dc2a5f58ff2d22dd3c5f4e91490a3838a23145f24209ffa4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.3 MB (347327723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253cafc5a7b090a03779b4603c63ff0394e28c9815b67fb8f4b454daad8dce22`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Tue, 09 Jun 2026 23:21:56 GMT
SHELL [cmd /s /c]
# Tue, 09 Jun 2026 23:24:00 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 09 Jun 2026 23:24:01 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2026 23:24:03 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 09 Jun 2026 23:24:04 GMT
USER ContainerUser
# Tue, 09 Jun 2026 23:24:05 GMT
ENV JAVA_VERSION=27-ea+25
# Tue, 09 Jun 2026 23:24:58 GMT
COPY dir:2d44b60de7278e1e5741976187b08fdfd7908345a04ec10edcdba62993c11b6a in C:\openjdk-27 
# Tue, 09 Jun 2026 23:25:04 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 09 Jun 2026 23:25:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5beb5700dfb290eb9db754f3ee1692dfa9331c95cd3d0441290f84448e0ecfae`  
		Last Modified: Tue, 09 Jun 2026 23:22:26 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785236a2b35ed765c272e1c9f1b8608887dc359aa98e5a2b0c2efc4918fbaa2e`  
		Last Modified: Tue, 09 Jun 2026 23:25:11 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38db7ee6895acd871f222a31bae7b68546ae832a49ef817a4889d3fc6a43f519`  
		Last Modified: Tue, 09 Jun 2026 23:25:11 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f098d21588ad1525f7fac9542a163b53fd47c686f16e3e1fab3783c499a8535`  
		Last Modified: Tue, 09 Jun 2026 23:25:11 GMT  
		Size: 95.6 KB (95591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b7a39b1fc8e3bb6510f7b5ed1b493f40c8e2fa4c9afb0e47cffe4852c0679f`  
		Last Modified: Tue, 09 Jun 2026 23:25:09 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af28872d0a582943e4647f5de406cc84dcfe6e451ac49912d69a82956311db7`  
		Last Modified: Tue, 09 Jun 2026 23:25:09 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f715e0241eb1f418a765b24322721b3a1170ef47d01221c8562c4d8410ff1a51`  
		Last Modified: Tue, 09 Jun 2026 23:25:24 GMT  
		Size: 223.1 MB (223095110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81eef5be23ef926ae2ac7243cdc6599d814e55031a21ebc610b719c2a69ecbc3`  
		Last Modified: Tue, 09 Jun 2026 23:25:09 GMT  
		Size: 133.1 KB (133132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780fbaef8a805c69aadd86c2d20e0f6441b9220f45790455051272c0e95cf95f`  
		Last Modified: Tue, 09 Jun 2026 23:25:09 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
