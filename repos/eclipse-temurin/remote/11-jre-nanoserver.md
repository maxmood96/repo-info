## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:dc6285ce18c2caf9c835fb9a38b5dfeef7103348ec60e30a7804d401635ba444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.26100.32860; amd64

```console
$ docker pull eclipse-temurin@sha256:17945f1b05475a307df5ad95ecd2e98f8176e1a6770ad7808b95f07c49b2a926
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243658485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c120d3f938688797a346af403fc6052d99ff3627d6a5ceaa1520d85cdd5149`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 May 2026 09:46:02 GMT
RUN Apply image 10.0.26100.32860
# Wed, 13 May 2026 00:28:41 GMT
SHELL [cmd /s /c]
# Wed, 13 May 2026 00:28:41 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 13 May 2026 00:28:42 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 13 May 2026 00:28:42 GMT
USER ContainerAdministrator
# Wed, 13 May 2026 00:28:46 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 May 2026 00:28:46 GMT
USER ContainerUser
# Wed, 13 May 2026 00:28:50 GMT
COPY dir:b48d35a79d584b4e6e30bd64a65514a5a8dd37c415c758cd9c300ebbad014bb0 in C:\openjdk-11 
# Wed, 13 May 2026 00:28:53 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:34ab6476d71f2d23d05a00ac439000ba4c19d17e5c66f15efbe329ed79bba2bf`  
		Last Modified: Tue, 12 May 2026 22:29:47 GMT  
		Size: 199.7 MB (199739001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c6a8908648c0dfbf8d32abc71669debdbb0d446292f14c2e6abe1a34f4ed93`  
		Last Modified: Wed, 13 May 2026 00:28:59 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03295729d442c23f9190c7115a7846bff631033d21f4e4b19e638179cebe8af`  
		Last Modified: Wed, 13 May 2026 00:28:59 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51c219fb882b9a88a1852e16fc6201401244d39dd50f5480716a9f4936b52cd`  
		Last Modified: Wed, 13 May 2026 00:28:59 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b22cc15121738b9a78649d79ee5424f7875758d20a265bd1091fcbd84ae9905`  
		Last Modified: Wed, 13 May 2026 00:28:57 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed9d2627e6e6c06feab12d4d3c2ae1dc4248311c03f2c2e71d90b07e89dbc370`  
		Last Modified: Wed, 13 May 2026 00:28:57 GMT  
		Size: 77.5 KB (77452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726273f6037799bdb616aff8bfc549f78983ca964d20f294ad7c207952b37bd6`  
		Last Modified: Wed, 13 May 2026 00:28:57 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d361052aed9984bd43f130663677bf4b2ed2b69187a3b0564be2587ca60edd50`  
		Last Modified: Wed, 13 May 2026 00:29:03 GMT  
		Size: 43.7 MB (43738796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb88e4484a625f665c0eeb0226ebf7bee622785cebbe60cf09730f13642fef5`  
		Last Modified: Wed, 13 May 2026 00:28:57 GMT  
		Size: 97.8 KB (97797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.20348.5139; amd64

```console
$ docker pull eclipse-temurin@sha256:e0d597ed05df1c0afb65d384cfff20f8147762b6d5dab4664e69e9de17e674d8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (170971908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e0956d4ebe268afdcc68771d14d27ae7d5bc9dfdcc7d23e6355347c219a2f6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:23:40 GMT
SHELL [cmd /s /c]
# Wed, 13 May 2026 00:23:40 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 13 May 2026 00:23:40 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 13 May 2026 00:23:41 GMT
USER ContainerAdministrator
# Wed, 13 May 2026 00:23:42 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 May 2026 00:23:43 GMT
USER ContainerUser
# Wed, 13 May 2026 00:23:46 GMT
COPY dir:b48d35a79d584b4e6e30bd64a65514a5a8dd37c415c758cd9c300ebbad014bb0 in C:\openjdk-11 
# Wed, 13 May 2026 00:23:49 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a173affe297b5dba2b646cd33ee31e0563e200d7d0a2914833024551a6d90dda`  
		Last Modified: Wed, 13 May 2026 00:23:55 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e688e805d8f1ba896137bd6c10bbd0a89458d49c9342f2325d38722e36d52a08`  
		Last Modified: Wed, 13 May 2026 00:23:55 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d007931264f9f2eeb449c6de2d59365a989a06ded992aae2f07baf0bc0def39a`  
		Last Modified: Wed, 13 May 2026 00:23:54 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d954097f8994ab4a8d39278fd0ea1bbc5b110e58e68d09862b50cce1735f7eaa`  
		Last Modified: Wed, 13 May 2026 00:23:53 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4899a25969aec522f5a33982dd749fcf656509d527b0b770e783e1f15c64cc94`  
		Last Modified: Wed, 13 May 2026 00:23:53 GMT  
		Size: 77.2 KB (77249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b221d079a7657109fac51cb451c28924db183184931727fd3032424adca7832c`  
		Last Modified: Wed, 13 May 2026 00:23:53 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f2c3f20d574932f0bd1dbe6ffbf97f5a3f494ced843e74311fb8da4dfbb15f`  
		Last Modified: Wed, 13 May 2026 00:23:58 GMT  
		Size: 43.7 MB (43739015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1f4a30a032095cbdd0cb6b36d8b84584a3918bfd4c823e253c8b054c158b83`  
		Last Modified: Wed, 13 May 2026 00:23:53 GMT  
		Size: 111.5 KB (111514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
