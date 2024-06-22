## `eclipse-temurin:21-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:c0936250a8d6801ca626c47b75db69c7ba6427a0ecdb839d370cd3bfb96aa6b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2529; amd64

### `eclipse-temurin:21-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.2529; amd64

```console
$ docker pull eclipse-temurin@sha256:0c341aaab50d55d90db890c9fee140eea58325a9c6992271b866b879dac12ce2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.8 MB (321796609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f781cf881da5d674a0393a0db4878a403b58d8ed57b64e305480d79862946e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 19 Jun 2024 19:27:30 GMT
RUN Apply image 10.0.20348.2529
# Sat, 22 Jun 2024 00:50:29 GMT
SHELL [cmd /s /c]
# Sat, 22 Jun 2024 00:54:28 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Sat, 22 Jun 2024 00:54:29 GMT
ENV JAVA_HOME=C:\openjdk-21
# Sat, 22 Jun 2024 00:54:30 GMT
USER ContainerAdministrator
# Sat, 22 Jun 2024 00:54:41 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 22 Jun 2024 00:54:41 GMT
USER ContainerUser
# Sat, 22 Jun 2024 00:54:57 GMT
COPY dir:23b4ead9c2036754f644b00182bded9da6af0a8e5b9adaf18f46a103fb435a07 in C:\openjdk-21 
# Sat, 22 Jun 2024 00:55:14 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 22 Jun 2024 00:55:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a8c295c425a912de308ded279124ae45fec44d55a451843fe5877155417f453c`  
		Last Modified: Fri, 21 Jun 2024 02:24:34 GMT  
		Size: 120.5 MB (120499549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c04e6fe7f33e5ed7b73641c362d031eb0404b55967c9af2b8fa6f2269d9f92`  
		Last Modified: Sat, 22 Jun 2024 01:06:26 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6af0cf5ec3755a82f9105b718400505d6d7eab97c51f13c91f9513f7342508`  
		Last Modified: Sat, 22 Jun 2024 01:08:42 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64609b1bc056b95efa8c49578838c02d7d20ea5be6270ea3d9e7458ec401593e`  
		Last Modified: Sat, 22 Jun 2024 01:08:42 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a901f61c54a3824838ed528441558914f3a9696e44ed905c93660504981bedb`  
		Last Modified: Sat, 22 Jun 2024 01:08:42 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0085856e28f21c2c6d7df076a3abcc246870a47201ad4c62802b2b8f024d1f1a`  
		Last Modified: Sat, 22 Jun 2024 01:08:40 GMT  
		Size: 79.2 KB (79234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32227cd9509b4e41814a209e6ef0b2ce548cea18e72cf6e7e657da983288e0b2`  
		Last Modified: Sat, 22 Jun 2024 01:08:41 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47b9dcb0162e130c0a35ec5aa3bab0949c0f01bfbcb72bd3a51f8cb736f52f8`  
		Last Modified: Sat, 22 Jun 2024 01:09:00 GMT  
		Size: 201.1 MB (201148738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90855fb6d802934994e1088f2a78501fc1fb46811675893a563dfb222c925eaa`  
		Last Modified: Sat, 22 Jun 2024 01:08:41 GMT  
		Size: 62.1 KB (62105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7456e8cf3d59e16530b42dd0f36d991f6d3235269a2dd4268136049d5caca593`  
		Last Modified: Sat, 22 Jun 2024 01:08:40 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
