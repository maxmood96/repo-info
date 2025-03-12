## `eclipse-temurin:8-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:9c7c66e300928570a4095cee47ddc66f736783ea7f3ea156029d4b0e1418f881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `eclipse-temurin:8-jdk-nanoserver` - windows version 10.0.26100.3476; amd64

```console
$ docker pull eclipse-temurin@sha256:2d6d63e3d11fe4559983c3b1a9cbcaaa70c402f9bee5315923277d6c0d3487df
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.9 MB (308943632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5ae0a70102c7a5f4155fd486edcd15c7d94d2c403cd42c464f98aaee0f6cdf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Wed, 12 Mar 2025 19:15:58 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:15:59 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Wed, 12 Mar 2025 19:16:00 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 12 Mar 2025 19:16:00 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:16:03 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:16:04 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:16:09 GMT
COPY dir:bdaea23e3e57be9dfb95abf135786259c631aa0db2125cb7a86f299ac37b3921 in C:\openjdk-8 
# Wed, 12 Mar 2025 19:16:15 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a96ee8de066214a90d726dbf3318f38966a00b7cbb68db3ecf9dc2005ba219`  
		Last Modified: Wed, 12 Mar 2025 19:16:21 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5a628fb7d91aded698969d1043521992e0c010450740447986500322a8cedd`  
		Last Modified: Wed, 12 Mar 2025 19:16:20 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5c09f828b46874359177943857b39271b5d8d21335f2515de2b3ac8d56bcff`  
		Last Modified: Wed, 12 Mar 2025 19:16:20 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e9e843e842d0b78bf8782a7f5d1130dda87e1489122a537d614503db314072`  
		Last Modified: Wed, 12 Mar 2025 19:16:19 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d51b829bdf4d1aa5cd293bae5180b030f87d9f5f9082e9fb34cf9c270e4732`  
		Last Modified: Wed, 12 Mar 2025 19:16:19 GMT  
		Size: 76.3 KB (76327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29095f0104bfcf1ecccc42367c5ec02aea3b53aa9038b51999618b2e2c2d1214`  
		Last Modified: Wed, 12 Mar 2025 19:16:18 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0893e0d750f3a447f51bb9c6fa3bacd6ab08d8a2242fcebe44b5d081e029153`  
		Last Modified: Wed, 12 Mar 2025 19:16:25 GMT  
		Size: 102.4 MB (102433887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8e86718474b43aab68d7f1c917283d1df5ef0ac991592553e67e3945cdb32a`  
		Last Modified: Wed, 12 Mar 2025 19:16:19 GMT  
		Size: 126.0 KB (125965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jdk-nanoserver` - windows version 10.0.20348.3328; amd64

```console
$ docker pull eclipse-temurin@sha256:9d7c78b13e53de38a1a3470a1145fc4739ad5736820312fa3873155fa18b75e2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223318394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6386cbef56e66fb82b7e0d67db870141d383f63ecc6c704acdd8776b5b805b30`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Wed, 12 Mar 2025 19:19:35 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:19:36 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Wed, 12 Mar 2025 19:19:37 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 12 Mar 2025 19:19:37 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:19:40 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:19:40 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:19:45 GMT
COPY dir:bdaea23e3e57be9dfb95abf135786259c631aa0db2125cb7a86f299ac37b3921 in C:\openjdk-8 
# Wed, 12 Mar 2025 19:19:50 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a7eb22c346b2739fb13ce46a21f5aba2d795f94dc4eacf060c05eff6f47788`  
		Last Modified: Wed, 12 Mar 2025 19:19:56 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca8dd253d5299e9552267033847d6fbea0864a654ec4a2f6e5b4cd8ff1d41ad`  
		Last Modified: Wed, 12 Mar 2025 19:19:56 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bce45b12140ad0afdb7c56552dfdb4eb3b458ad9ce740cdd7cffa23f73af560`  
		Last Modified: Wed, 12 Mar 2025 19:19:56 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d2976cec768d9d94b5421d6bca98814d5754c8d0ac475186fe5901ebd8a586`  
		Last Modified: Wed, 12 Mar 2025 19:19:54 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0ae1817290ada447a19e7116fb3cc598752d8cbdc904d4c457c73eb97fee8b`  
		Last Modified: Wed, 12 Mar 2025 19:19:54 GMT  
		Size: 78.5 KB (78548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e6217011485bb88798884a9bb588bab1d82bd60c750dfe80e28a83714ef9ef`  
		Last Modified: Wed, 12 Mar 2025 19:19:54 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79005d2aa9e6e54f96ae89f524b18a89d4e4360f7ba910e1822b7a3e9858c551`  
		Last Modified: Wed, 12 Mar 2025 19:20:00 GMT  
		Size: 102.4 MB (102432219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f5358eec207990a73202236341a537d204a17d62b543038da71fe04aa1a7ce`  
		Last Modified: Wed, 12 Mar 2025 19:19:54 GMT  
		Size: 106.9 KB (106924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jdk-nanoserver` - windows version 10.0.17763.7009; amd64

```console
$ docker pull eclipse-temurin@sha256:264fda757f19ab3e20d6e2f9ccd701b4503229b60dc85b25f4b1c4b5f54f90eb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.6 MB (209560215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83883432dbec3dcff8db1384bb68cbd90b3a66ead70c3d85838068314847464f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Wed, 12 Mar 2025 19:23:16 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:23:17 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Wed, 12 Mar 2025 19:23:18 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 12 Mar 2025 19:23:19 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:23:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:23:22 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:23:27 GMT
COPY dir:bdaea23e3e57be9dfb95abf135786259c631aa0db2125cb7a86f299ac37b3921 in C:\openjdk-8 
# Wed, 12 Mar 2025 19:23:31 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26be7caa7d084eb128cdb1d4c713985d00f0219f05ebd0eb33bedef42e0e1f8f`  
		Last Modified: Wed, 12 Mar 2025 19:23:34 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e108cca6bb2a6d85bb8aa9811b2a6b7236b78825c4efe17ff3201e6a3b84f7`  
		Last Modified: Wed, 12 Mar 2025 19:23:34 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73eeb4ec79f423e3437b83eecf4c9760da226becb1efcb6701ab46282a5cf28b`  
		Last Modified: Wed, 12 Mar 2025 19:23:34 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cafd92107c95a9cf3340e0b9c5ac2f8e753b4d15e1d8d047b3901f4576d5865`  
		Last Modified: Wed, 12 Mar 2025 19:23:33 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada021a79fcfc30c8a66ed88109162653272bbdcf0ef40852f846d74e9456756`  
		Last Modified: Wed, 12 Mar 2025 19:23:33 GMT  
		Size: 71.8 KB (71758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58311d408b069986ccf18340cea8370bf0a1dc52b30267b2885153491d33048`  
		Last Modified: Wed, 12 Mar 2025 19:23:33 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff4e2ecf0a02798fa8d6b080b43c7ed94b25ee90874f88f74eb99e5af95ca16`  
		Last Modified: Wed, 12 Mar 2025 19:23:39 GMT  
		Size: 102.4 MB (102431252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e14637cb1a72bd5cd54cd1a47a7d796f5f08450ff9aa9f969a46587ac283510c`  
		Last Modified: Wed, 12 Mar 2025 19:23:33 GMT  
		Size: 144.3 KB (144303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
