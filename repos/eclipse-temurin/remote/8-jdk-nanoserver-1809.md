## `eclipse-temurin:8-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:5f8ab7eb832bf61d39052aaea289befa6719abc8929c15aa851b9bf56b318b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `eclipse-temurin:8-jdk-nanoserver-1809` - windows version 10.0.17763.7009; amd64

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
