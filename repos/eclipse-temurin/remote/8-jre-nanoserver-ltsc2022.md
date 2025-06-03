## `eclipse-temurin:8-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:fd24da65f27555e1096a1d54b1568a68d51392ba67000239111247be73d2a098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull eclipse-temurin@sha256:930484efb6e2b3ee9f42584da90672f55c73d88ded79df6b3f1566a4c9440f30
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163308493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f2da037dbde7e96982dc056f396e6f67593ca8d695e87faf2d7ec2b9bc7f5d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Wed, 14 May 2025 21:12:13 GMT
SHELL [cmd /s /c]
# Wed, 14 May 2025 21:12:14 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Wed, 14 May 2025 21:12:14 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 14 May 2025 21:12:15 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 21:12:18 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 May 2025 21:12:18 GMT
USER ContainerUser
# Wed, 14 May 2025 21:12:21 GMT
COPY dir:88632ffe03bdff97c0f2931283e9e8742ceaeaec8904ee54b87f8b4347f84ae7 in C:\openjdk-8 
# Wed, 14 May 2025 21:12:25 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ae651cc91f06b415e55640e4dc7b07bd999822210663d662a0ec9043c5d391`  
		Last Modified: Sun, 18 May 2025 21:01:44 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66a7765f157e34c443a8af0df411f21f6904b3e22ae841446215727bbba8892`  
		Last Modified: Sun, 18 May 2025 21:01:44 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6476bb55afc8227cfc5081d2573d12d55fa4ffadb183de589b119911e9926c9c`  
		Last Modified: Sun, 18 May 2025 21:01:44 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aecdc18d31f3aa91dc7a0905eeb4d4cde31da2ecc611d1f9b4cbda821a3c5e9`  
		Last Modified: Sun, 18 May 2025 21:01:44 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719f2cc2f8ebfddc68ecab79ad4799c4b9090cc087ab8cbcacafd7c480019eff`  
		Last Modified: Sun, 18 May 2025 21:01:45 GMT  
		Size: 76.4 KB (76352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28906281c141570e3a0e85ccadd76d1e62a0b750bf269443a9f2fa768a366e3`  
		Last Modified: Sun, 18 May 2025 21:01:45 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f98cc9ff146c88853184973352bd0cf68cc9d0bbb3d622dfbaba7857317fba5`  
		Last Modified: Sun, 18 May 2025 21:01:49 GMT  
		Size: 40.6 MB (40552739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1df2202a7285227d2bbaadf1bc9292346e7ea53ac024b33da68bb505914def`  
		Last Modified: Sun, 18 May 2025 21:01:46 GMT  
		Size: 97.6 KB (97627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
