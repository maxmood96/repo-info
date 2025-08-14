## `eclipse-temurin:24-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:bf0d52c6a75e94552e4b2c3732ffe33df2b649a756baff33af3c4e9941aef286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `eclipse-temurin:24-nanoserver` - windows version 10.0.26100.4946; amd64

```console
$ docker pull eclipse-temurin@sha256:f939aeed5bf4da8a9112a9b1b21288a3d4eddb512df91132c3473611fbc80e80
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.0 MB (331048566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3f0b97136cff02491180497bccece3cb47b5a1f32062445e783d90d7364912`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 Aug 2025 02:44:20 GMT
RUN Apply image 10.0.26100.4946
# Tue, 12 Aug 2025 20:50:19 GMT
SHELL [cmd /s /c]
# Tue, 12 Aug 2025 20:50:20 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Tue, 12 Aug 2025 20:50:20 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 12 Aug 2025 20:50:20 GMT
USER ContainerAdministrator
# Tue, 12 Aug 2025 20:50:22 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 12 Aug 2025 20:50:22 GMT
USER ContainerUser
# Tue, 12 Aug 2025 20:50:27 GMT
COPY dir:ec500d2496c53c21f9648717e875ebfb68429c449060cda7ccbee1a2a7024b32 in C:\openjdk-24 
# Tue, 12 Aug 2025 20:50:30 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 12 Aug 2025 20:50:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6d63d98dae9e3419e8c965c24a11d30e40947cf35ee17c204c5d8b7bae7ff2ef`  
		Last Modified: Tue, 12 Aug 2025 21:13:38 GMT  
		Size: 193.5 MB (193469373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f4156f61d40cef197e31f740e66d0e3081af1987295c65b59d9b2be5251659e`  
		Last Modified: Tue, 12 Aug 2025 21:14:08 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ca0a37e7880781ff2177e50d39ddd4795f3b1a2b0c9a32646f3899d67c5cc4`  
		Last Modified: Tue, 12 Aug 2025 21:14:11 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176c77338220af5118df3bb5b0ecfea18681064ed1449a9cde477b2683e69c6e`  
		Last Modified: Tue, 12 Aug 2025 21:14:14 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987f047efcd3289dd1f6e8f09d99f280576886aee434dcb1917e5876d683105d`  
		Last Modified: Tue, 12 Aug 2025 21:14:17 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9adb190daaa0f8b66de6638425cd16f7c634188cb9255141ef8c8d5f78b438a`  
		Last Modified: Tue, 12 Aug 2025 21:14:20 GMT  
		Size: 75.7 KB (75733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4b419871c6016643df859b6d320a25a222c0babc10d1a51a340aac5368e8fb`  
		Last Modified: Tue, 12 Aug 2025 21:14:23 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6840bed2bb3671469d4d4ee1b4fcc7a3c782309df288b09563b912aff000b916`  
		Last Modified: Tue, 12 Aug 2025 21:18:17 GMT  
		Size: 137.4 MB (137384068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2691028226de1b5f4fed7ab949d1ac9f24442248c1d185877897dd578b477619`  
		Last Modified: Tue, 12 Aug 2025 21:14:26 GMT  
		Size: 113.0 KB (113023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423d8d87b940276c1c26c0b1fd558a564b67078f89ffbd93ced2d0da1174a168`  
		Last Modified: Tue, 12 Aug 2025 21:14:31 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:24-nanoserver` - windows version 10.0.20348.4052; amd64

```console
$ docker pull eclipse-temurin@sha256:287dc956f89dac4e358d42991e2fd9d87a26cd3fee308ebf0af425db4fea159d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.2 MB (260235199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38628a9f6a4af9b84da4976330b64b21180bd30c2c91bcf8216c3ed4efd84fad`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:49:48 GMT
SHELL [cmd /s /c]
# Tue, 12 Aug 2025 20:49:49 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Tue, 12 Aug 2025 20:49:50 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 12 Aug 2025 20:49:52 GMT
USER ContainerAdministrator
# Tue, 12 Aug 2025 20:49:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 12 Aug 2025 20:49:56 GMT
USER ContainerUser
# Tue, 12 Aug 2025 20:50:02 GMT
COPY dir:ec500d2496c53c21f9648717e875ebfb68429c449060cda7ccbee1a2a7024b32 in C:\openjdk-24 
# Tue, 12 Aug 2025 20:50:08 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 12 Aug 2025 20:50:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7be4d7b5935ffef675e775fac8076e31506eaea93aeeb2dd5449ebf4f84ac2`  
		Last Modified: Tue, 12 Aug 2025 20:51:03 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58fd218f33422d3bcd87bf97a836855fffcd671eb9bdd5ee52035920fd382082`  
		Last Modified: Tue, 12 Aug 2025 20:51:04 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0dc32e49af24e65633659500cc183d4c4d0d73a5fedcbefe41baa15f32257d`  
		Last Modified: Tue, 12 Aug 2025 20:51:07 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87138a02d62666878291163b9864fa1bdb156e4f62a7a50b9433b7902ab02eca`  
		Last Modified: Tue, 12 Aug 2025 20:51:05 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9bb83c9df9d080d72bb58c9b60ac8d3bef9b339260d94076a4541ccd9e9260`  
		Last Modified: Tue, 12 Aug 2025 20:51:07 GMT  
		Size: 78.4 KB (78365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5679a44f06a7cb4cf9e5dd8e6102ac14b7c8aec943ea1aa88bcc689fee1022`  
		Last Modified: Tue, 12 Aug 2025 20:51:07 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f40b2992ea042cf03897586888040b0da1256932666ba72aec935a6240ecde`  
		Last Modified: Tue, 12 Aug 2025 21:18:13 GMT  
		Size: 137.4 MB (137382824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e847400e549e7997ecc6c37b08252a67b32d67096d9760448a31cfcf1b78aa`  
		Last Modified: Tue, 12 Aug 2025 20:51:09 GMT  
		Size: 107.5 KB (107497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e357c8c1d12b101d8a13457ed31b9165f0a06442af3ae1b05b363d2b12aa0d92`  
		Last Modified: Tue, 12 Aug 2025 20:51:08 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
