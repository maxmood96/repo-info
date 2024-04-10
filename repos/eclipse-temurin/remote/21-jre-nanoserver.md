## `eclipse-temurin:21-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:9dae2362eefd8a4fee723241b717c12adae1da16e2e0aa8331b12bac3a79ceb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.20348.2402; amd64

```console
$ docker pull eclipse-temurin@sha256:5f769c72eb42c1753dda3f2a5af4982677457602e1c721aa3f622bfe4c2b23a1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.9 MB (169887263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5cea6852cce2482f84506d4ec2c95a0e7855c71e8fc53b6939e500d07069baa`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Apr 2024 08:53:11 GMT
RUN Apply image 10.0.20348.2402
# Wed, 10 Apr 2024 00:34:53 GMT
SHELL [cmd /s /c]
# Wed, 10 Apr 2024 00:39:00 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Wed, 10 Apr 2024 00:39:00 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 10 Apr 2024 00:39:01 GMT
USER ContainerAdministrator
# Wed, 10 Apr 2024 00:39:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Apr 2024 00:39:12 GMT
USER ContainerUser
# Wed, 10 Apr 2024 00:40:01 GMT
COPY dir:a5c64f66204a1ce40e58093b44657f9abbd9eecac263988d919d778d3cf84131 in C:\openjdk-21 
# Wed, 10 Apr 2024 00:40:13 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:755fc767289b8847bd0d0d8d75efc308c040140acf2a3426973ba9fbf022c4c0`  
		Last Modified: Tue, 09 Apr 2024 23:50:18 GMT  
		Size: 121.0 MB (120993754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70887eeae6a5d6d5fd81661024afc84fee637f674dee5e7127112cbfce90750`  
		Last Modified: Wed, 10 Apr 2024 01:00:01 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:312eb5a78cfa6f13afd6c4776c5cfe493c689b5a6deb5cd39bf9ff9d00255a57`  
		Last Modified: Wed, 10 Apr 2024 01:02:29 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95df9bac0b145e33b324b9280ecbb66171abba5ddef38594eb47a4fc3a2ac33d`  
		Last Modified: Wed, 10 Apr 2024 01:02:28 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed5f44d83d3572628a0f0cb2769958a659b4a554f7357fe3b0c8547827358c6`  
		Last Modified: Wed, 10 Apr 2024 01:02:28 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7734f46f55d9928b5b440034a3c44fb06258d40177cc9daa3766c5c8e8bc857d`  
		Last Modified: Wed, 10 Apr 2024 01:02:27 GMT  
		Size: 83.9 KB (83899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5311424d09268f0b171cd86abf78d08316783448ff1587a1f93b33d9e33a57`  
		Last Modified: Wed, 10 Apr 2024 01:02:26 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113d4a25a77c8af8cf0dc86de9d5d75d632753ed2ecc37189e54613bf2ce5330`  
		Last Modified: Wed, 10 Apr 2024 01:03:09 GMT  
		Size: 48.7 MB (48749747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9226a9e8e58f770184f8c38fbf2deb62401ebf59304765a0c3ea8cd6b2e2697`  
		Last Modified: Wed, 10 Apr 2024 01:02:59 GMT  
		Size: 54.7 KB (54673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.17763.5696; amd64

```console
$ docker pull eclipse-temurin@sha256:5f86291412c16956f1dce59b657b4c28247266bab3cf1de6f1166a916efcafc6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157071327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b695b3bee4f8a6f22d074ce7810169c490ca41847988c66a154b4dc50e61f8bd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Tue, 09 Apr 2024 23:42:55 GMT
SHELL [cmd /s /c]
# Wed, 10 Apr 2024 00:17:23 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Wed, 10 Apr 2024 00:17:24 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 10 Apr 2024 00:17:25 GMT
USER ContainerAdministrator
# Wed, 10 Apr 2024 00:17:34 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Apr 2024 00:17:35 GMT
USER ContainerUser
# Wed, 10 Apr 2024 00:22:59 GMT
COPY dir:a5c64f66204a1ce40e58093b44657f9abbd9eecac263988d919d778d3cf84131 in C:\openjdk-21 
# Wed, 10 Apr 2024 00:23:10 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b591b5f81c02344da39dc8a9084b5791cbf552c1eb85e79db1f38dfc715a681`  
		Last Modified: Wed, 10 Apr 2024 00:47:46 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ddf43d90d7015588c216ecb111faa62bf819c9a5b33036e42dbe52c611c33e`  
		Last Modified: Wed, 10 Apr 2024 00:55:47 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a082822ba6554f06b386d63402e14825e3efa82d395ee2ee265265a70a0234`  
		Last Modified: Wed, 10 Apr 2024 00:55:47 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c549ce38ec12395456a22d08ebb489fa4860023b0e462d21db3dcc34cb71ee3`  
		Last Modified: Wed, 10 Apr 2024 00:55:47 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9303a6a441578fe2c75bda55d5d4fe4fd8805b8c109173001f36b837356fde6f`  
		Last Modified: Wed, 10 Apr 2024 00:55:45 GMT  
		Size: 66.0 KB (66006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553884b6b95fb4c21a90cdb2cd929c28e8b59d021b59dfeb34d63cb1745ce3e4`  
		Last Modified: Wed, 10 Apr 2024 00:55:45 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d269a07ae6ed719e93b1aa8c2eba37bfad9cfeb81a031d2efd67863b0011c186`  
		Last Modified: Wed, 10 Apr 2024 00:57:06 GMT  
		Size: 48.7 MB (48749834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0756a76f088d66f0ba37914274abde334a84a300a9a490a8d7314a7b06c39c`  
		Last Modified: Wed, 10 Apr 2024 00:56:57 GMT  
		Size: 3.4 MB (3360812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
