## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:8ac220bc999fc752684fc240f8a907e58f89f38aba14129d5593c457aa6e6608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7136; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.26100.3775; amd64

```console
$ docker pull eclipse-temurin@sha256:a9226ae5afea9c54c36aee62bf7d5b74b59cccb49142f4446b74639f08ea2af5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (233955519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6845a0156d1bc3a4ed59ffa14e85c757f033f8a84e1c7e67edefed608e9d91`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Apr 2025 07:26:08 GMT
RUN Apply image 10.0.26100.3775
# Wed, 09 Apr 2025 01:17:33 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:17:34 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Wed, 09 Apr 2025 01:17:35 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 09 Apr 2025 01:17:36 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:17:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:17:40 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:17:44 GMT
COPY dir:e7319a06d2b9171c954fc18de0614fa7d0eb408950b795be61492806db04a6ea in C:\openjdk-11 
# Wed, 09 Apr 2025 01:17:48 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:79b2ed45f890e91d23d7d22491a8fb6909c9268c668dc6a0e3b40131da02ed74`  
		Last Modified: Wed, 09 Apr 2025 00:36:30 GMT  
		Size: 190.1 MB (190113206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f35326682400ca198f0714baa663029235da99784314e6e39e2cb0187f6b7a`  
		Last Modified: Wed, 09 Apr 2025 01:17:52 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b794edcdd112bad11544e07c17753e1a2e927537de6b9ee25138ea7956f016de`  
		Last Modified: Wed, 09 Apr 2025 01:17:53 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f627ddab4df96ed184a919cb7fbb7c0076e62edc7ba8bf6a5a88e98131ab63f`  
		Last Modified: Wed, 09 Apr 2025 01:17:52 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a2f156ad6a1de9dd571d77b7e1e192d53d1dd579a986d49b177d006e8054e5`  
		Last Modified: Wed, 09 Apr 2025 01:17:51 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39252553e0b52f574874ec549e7a030986c937e6b97ce8b5de6e1d40f2d64ec8`  
		Last Modified: Wed, 09 Apr 2025 01:17:51 GMT  
		Size: 75.9 KB (75915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48dd237c00d3cffe9072fca48094853c6793f6c75775a652409b8a19a46cc1c9`  
		Last Modified: Wed, 09 Apr 2025 01:17:51 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9427bac43e96a132321d5d56a3452f168fef8d450b6f56f4269415cfc6d733f7`  
		Last Modified: Wed, 09 Apr 2025 01:17:56 GMT  
		Size: 43.7 MB (43656841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5896538a01bb278000d7a5af1517b2a77df24a3534f9d7d398bab64242dc9c17`  
		Last Modified: Wed, 09 Apr 2025 01:17:51 GMT  
		Size: 104.3 KB (104305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.20348.3453; amd64

```console
$ docker pull eclipse-temurin@sha256:cc78670bb30370d849f31e826f1d479eb2fde05b2ca9f6608915b5231b623c98
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164584768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2ee55253aa03bba529247d7c1b9ca1e6788cff8a9797eae1a941816a1d9ce38`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Apr 2025 22:57:50 GMT
RUN Apply image 10.0.20348.3453
# Wed, 09 Apr 2025 01:20:38 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:20:39 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Wed, 09 Apr 2025 01:20:40 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 09 Apr 2025 01:20:41 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:20:44 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:20:45 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:20:49 GMT
COPY dir:e7319a06d2b9171c954fc18de0614fa7d0eb408950b795be61492806db04a6ea in C:\openjdk-11 
# Wed, 09 Apr 2025 01:20:54 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:5caa30147a287e99992660f7f85276c53fe3299503a06c47d476387410721453`  
		Last Modified: Wed, 09 Apr 2025 01:13:36 GMT  
		Size: 120.7 MB (120736312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a33cdbea6e791dc3f830388d2f1cf828d3d8714ef703798b26e27dda9c489ac`  
		Last Modified: Wed, 09 Apr 2025 01:21:01 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d1b936f97399f32997b0a18589d162b1ce5337d6393c1891635760eab9446f`  
		Last Modified: Wed, 09 Apr 2025 01:21:00 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39629e246afdf18a62d855e1194c2c4c3a9f68a4f819b961dd603eef600a2ebd`  
		Last Modified: Wed, 09 Apr 2025 01:21:00 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f03ce397c520a7322e1405920da0f677e4e113cfc1e657f0bd79699da3edbc`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4d23173c73b056b3e4cf8da67d8cac4b914431d018e513895ad6330f53817a`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 77.0 KB (77015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefe062dbc626c5bfc7f583839a592ec1ae4e757fe82ef3d93c652b44858d471`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab64173e5836ef45556affc5671e72cd3680c2e3015db5cf3daf3a8cecd0add`  
		Last Modified: Wed, 09 Apr 2025 01:21:04 GMT  
		Size: 43.7 MB (43656484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40681fc9723444240b4da9662c4f81a397778e046874639187ab0d6914586f7`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 109.7 KB (109744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.17763.7136; amd64

```console
$ docker pull eclipse-temurin@sha256:f8281afc2b8df82d7dc2bfb8550354b1374803572f2fd93f8ff84e19878a0f19
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.8 MB (150750512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6b7243fb1d07ccb4ddecd95b66aa6c2f4880c2fbeb3790125ae6603a2e92d1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Apr 2025 01:31:28 GMT
RUN Apply image 10.0.17763.7136
# Wed, 09 Apr 2025 01:18:50 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:18:52 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Wed, 09 Apr 2025 01:18:52 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 09 Apr 2025 01:18:53 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:18:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:18:55 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:18:59 GMT
COPY dir:e7319a06d2b9171c954fc18de0614fa7d0eb408950b795be61492806db04a6ea in C:\openjdk-11 
# Wed, 09 Apr 2025 01:19:04 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:a06e0965a0fa3715e629889bd9332aa22aadd75654cac5c9818b67c0264b3ee1`  
		Last Modified: Tue, 08 Apr 2025 20:16:02 GMT  
		Size: 106.9 MB (106922524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48285d8ae6d3f9bbbea337ab790eef98fbf84e1bcc7b37d00f156f10d56b6e8`  
		Last Modified: Wed, 09 Apr 2025 01:19:09 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354be8866d061f28d36f8d9be61020fa18db825b787a434e69becee9cb31e1ba`  
		Last Modified: Wed, 09 Apr 2025 01:19:09 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42eb226929039229dcea1ff249213910326bc95c4c238c4037abf858d3fab496`  
		Last Modified: Wed, 09 Apr 2025 01:19:09 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b175c2f43d785f4fcc0821cdbd37bdaff12fe0e731e1965708cff469d0ad08d5`  
		Last Modified: Wed, 09 Apr 2025 01:19:07 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9c70600754ee8358a4c26e9d148dd21f2c072a2ea3d7ccba62b72a6316a18f`  
		Last Modified: Wed, 09 Apr 2025 01:19:07 GMT  
		Size: 70.2 KB (70163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0642a4667b22186670fef37fbfe4ba9e3e411529bb2d57100128c78b03eeb23`  
		Last Modified: Wed, 09 Apr 2025 01:19:07 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbce22c8d51642006275130f4571af2fb2aba83cfe11d0f883de2fef3ac423db`  
		Last Modified: Wed, 09 Apr 2025 01:19:13 GMT  
		Size: 43.7 MB (43656154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f0ec2661a3d3d980bcdac5c1f7f335f3906a270e96fb464665feb819bee235`  
		Last Modified: Wed, 09 Apr 2025 01:19:07 GMT  
		Size: 96.4 KB (96411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
