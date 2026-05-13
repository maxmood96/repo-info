## `openjdk:27-ea-21-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:c05192475252a5ff6ba56040cbf20e2d3452b9364ee5158facc42c27f04f8a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `openjdk:27-ea-21-jdk-nanoserver` - windows version 10.0.26100.32860; amd64

```console
$ docker pull openjdk@sha256:2724d1a8225826262454f450ad12f552e8de5d0fa59de169231a7062ad5c7e6d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.7 MB (424698725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:642e4e2a45bae37a227baa14ac02635189709c644d0dec4c6fbc51e2a988d004`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 May 2026 09:46:02 GMT
RUN Apply image 10.0.26100.32860
# Wed, 13 May 2026 00:29:14 GMT
SHELL [cmd /s /c]
# Wed, 13 May 2026 00:30:13 GMT
ENV JAVA_HOME=C:\openjdk-27
# Wed, 13 May 2026 00:30:14 GMT
USER ContainerAdministrator
# Wed, 13 May 2026 00:30:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 13 May 2026 00:30:15 GMT
USER ContainerUser
# Wed, 13 May 2026 00:30:16 GMT
ENV JAVA_VERSION=27-ea+21
# Wed, 13 May 2026 00:30:26 GMT
COPY dir:21b86086b1737f2f7722d7588722f1390e0aa73709337ec2a22a64f142e83a09 in C:\openjdk-27 
# Wed, 13 May 2026 00:30:31 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 13 May 2026 00:30:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:34ab6476d71f2d23d05a00ac439000ba4c19d17e5c66f15efbe329ed79bba2bf`  
		Last Modified: Tue, 12 May 2026 22:29:47 GMT  
		Size: 199.7 MB (199739001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353f839ae1b6bca354af0c348feb64f0df227628c75588ea69316206842af558`  
		Last Modified: Wed, 13 May 2026 00:29:35 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bd0aa37d50e0f03dc781b2194ad742edcaae0802a1bce045996f7e419d4c2a`  
		Last Modified: Wed, 13 May 2026 00:30:37 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5344ca3531ec80bc066902b2d54342f337292f7fa082888b565405c01ecd2bfc`  
		Last Modified: Wed, 13 May 2026 00:30:37 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da739850fb0a14c4137aeb9f6f96bb4520fd05629da41b81187b6fd8a1e0dc5`  
		Last Modified: Wed, 13 May 2026 00:30:37 GMT  
		Size: 71.9 KB (71912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbb9fbe55cc9a73e2155c67f1e1b8bf1308f3ae8228343c498bbfec1d9e1c2b`  
		Last Modified: Wed, 13 May 2026 00:30:35 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9b8a97b645f3a836114a4542cd2c63284761f18e5c55290bb3d596e2f33948`  
		Last Modified: Wed, 13 May 2026 00:30:35 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9837606f5b0b70c497c1ffe0ff6fa652c0248206596d8f9644bc14863a1a50b8`  
		Last Modified: Wed, 13 May 2026 00:30:50 GMT  
		Size: 224.8 MB (224768809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea71388f92257ec20a937ed2b42f62ca071dc0addc45d55407506ef86b07843`  
		Last Modified: Wed, 13 May 2026 00:30:35 GMT  
		Size: 112.6 KB (112612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:381e7ff7f6506b3af1e272559e7b5c90d08db71b771b2d0e00a40af7028fc717`  
		Last Modified: Wed, 13 May 2026 00:30:35 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-21-jdk-nanoserver` - windows version 10.0.20348.5139; amd64

```console
$ docker pull openjdk@sha256:a19b86532e8603f1720a052a1c852644e688a162fbd6284fc77a7d78be0a9d50
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.0 MB (351998712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79bda091b3ce5065c39bcb42cd60591053d81935a141fb9324b3f7c06b54877`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:23:53 GMT
SHELL [cmd /s /c]
# Wed, 13 May 2026 00:30:32 GMT
ENV JAVA_HOME=C:\openjdk-27
# Wed, 13 May 2026 00:30:32 GMT
USER ContainerAdministrator
# Wed, 13 May 2026 00:30:34 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 13 May 2026 00:30:35 GMT
USER ContainerUser
# Wed, 13 May 2026 00:30:35 GMT
ENV JAVA_VERSION=27-ea+21
# Wed, 13 May 2026 00:30:44 GMT
COPY dir:21b86086b1737f2f7722d7588722f1390e0aa73709337ec2a22a64f142e83a09 in C:\openjdk-27 
# Wed, 13 May 2026 00:30:49 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 13 May 2026 00:30:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268beb93bae0a3fcb4f27b79193145978fd732af03aac83a53212232ff073dca`  
		Last Modified: Wed, 13 May 2026 00:24:15 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b92309608d9d1e688e314b0d4f9d68c9df443f66a791849cf7f48e3f5458be`  
		Last Modified: Wed, 13 May 2026 00:30:56 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292877d0bbc364216404aa1c12ad34811583aa216c7240fac6936965c27bc487`  
		Last Modified: Wed, 13 May 2026 00:30:57 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6f7e06b5044bdea994d8146da6b2255edafe3228c2e184218275f59f3db6e8`  
		Last Modified: Wed, 13 May 2026 00:30:56 GMT  
		Size: 76.8 KB (76805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b461dca860a39ba5425980544bcd3d1d7300b54496da85ca1a4f26cd3a3815`  
		Last Modified: Wed, 13 May 2026 00:30:54 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2256d877ac5fa5c7222a83a895ab01cdef7d3db140955655ec3e2d90fabc5b`  
		Last Modified: Wed, 13 May 2026 00:30:54 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fde8b8fc1d5cb9fe289f765acf562683ca88ba5e1033e8b2fe9ce5afcd06a95`  
		Last Modified: Wed, 13 May 2026 00:31:10 GMT  
		Size: 224.8 MB (224768870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10dcd60b88f9d81c53528d8a9fe36d849e087b910e72ac838402556949b5465e`  
		Last Modified: Wed, 13 May 2026 00:30:54 GMT  
		Size: 107.8 KB (107842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72badbd8ac9e3e79800fd3a5b16f7cc1f16d48ac107e0e833652a1bd6cd0bfdc`  
		Last Modified: Wed, 13 May 2026 00:30:54 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
