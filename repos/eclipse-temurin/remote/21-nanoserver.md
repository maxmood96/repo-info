## `eclipse-temurin:21-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:3a7fb36b57b0f2bdda037e3ec2c212b9dc7ba20317410a025bf81946cfc8d752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `eclipse-temurin:21-nanoserver` - windows version 10.0.26100.4946; amd64

```console
$ docker pull eclipse-temurin@sha256:ed4520e95a55c8adcd3f2b880d300589d5c64916cf81d8756a3dd9fe498abf91
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.3 MB (395337711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5232893b6327cc65500f7b4efa5809fbb4bb5f26c5968fdac5547c87c2c4709`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 Aug 2025 02:44:20 GMT
RUN Apply image 10.0.26100.4946
# Tue, 12 Aug 2025 20:50:53 GMT
SHELL [cmd /s /c]
# Tue, 12 Aug 2025 20:50:54 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Tue, 12 Aug 2025 20:50:54 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 12 Aug 2025 20:50:54 GMT
USER ContainerAdministrator
# Tue, 12 Aug 2025 20:50:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 12 Aug 2025 20:50:56 GMT
USER ContainerUser
# Tue, 12 Aug 2025 20:51:02 GMT
COPY dir:a2bf4cf331367a1d9342464c0f96e9c7392f7330076b470131cd025fc6568609 in C:\openjdk-21 
# Tue, 12 Aug 2025 20:51:05 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 12 Aug 2025 20:51:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6d63d98dae9e3419e8c965c24a11d30e40947cf35ee17c204c5d8b7bae7ff2ef`  
		Last Modified: Tue, 12 Aug 2025 21:13:38 GMT  
		Size: 193.5 MB (193469373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf96a9fec737af3c6a17d19d90d2dc1e1aade122294b0d5c767778ddb223ea5`  
		Last Modified: Tue, 12 Aug 2025 20:52:03 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc838dade98430677c4663dce661f09b0be84211c159d370f408ba3a12044ea`  
		Last Modified: Tue, 12 Aug 2025 20:52:04 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f3f3059d2ef26e9c7195329bf38360f83dc7ac4b9a7288b612e35c2276004f3`  
		Last Modified: Tue, 12 Aug 2025 20:52:03 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437d63c22d54dc7f08af3beadd54694d146fd4febdf98c26112eb3aa6fba7969`  
		Last Modified: Tue, 12 Aug 2025 20:52:04 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f810c6168e925a971a39db5732cf8da4f965376acfc8abdec873c940395190`  
		Last Modified: Tue, 12 Aug 2025 20:52:05 GMT  
		Size: 75.5 KB (75499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107c9cb8cf1494f88368471e9a3d34d4d35e69680df113aca7b25e0b1e25c929`  
		Last Modified: Tue, 12 Aug 2025 20:52:05 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb6bd8ea45cc6eb2d2fa37cc581b86d592dabb4d18242ee73c36847c18bac5e`  
		Last Modified: Tue, 12 Aug 2025 21:16:32 GMT  
		Size: 201.7 MB (201672630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879444c7f4ac6ed540d373243411bed3c5a5b3001ef4265c94eb989dbcc96e29`  
		Last Modified: Tue, 12 Aug 2025 20:52:06 GMT  
		Size: 113.8 KB (113756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf79354d4bf7d098d316c4eb3e5d004bf24f11d6f2ec74490de11eda9788b58`  
		Last Modified: Tue, 12 Aug 2025 20:52:05 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-nanoserver` - windows version 10.0.20348.4052; amd64

```console
$ docker pull eclipse-temurin@sha256:206f6c700ac10cc1a45c68fefea07a7c29ac5dfc34a67909337c9170d19c3b32
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.5 MB (324523934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7548194e9af683cdbffd5de55d8368aca6d49dbf85b75b101c2e360491ad4892`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:49:30 GMT
SHELL [cmd /s /c]
# Tue, 12 Aug 2025 20:49:31 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Tue, 12 Aug 2025 20:49:32 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 12 Aug 2025 20:49:33 GMT
USER ContainerAdministrator
# Tue, 12 Aug 2025 20:49:36 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 12 Aug 2025 20:49:37 GMT
USER ContainerUser
# Tue, 12 Aug 2025 20:49:44 GMT
COPY dir:a2bf4cf331367a1d9342464c0f96e9c7392f7330076b470131cd025fc6568609 in C:\openjdk-21 
# Tue, 12 Aug 2025 20:49:50 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 12 Aug 2025 20:49:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d36552c31f0872e53ebd4e9f4aeff07e935120ead15616d2a096d61f73894b7`  
		Last Modified: Tue, 12 Aug 2025 20:50:38 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aae7eaab660824cc88d344f94152216d188e6d1dfdde3136c313f27195146f6`  
		Last Modified: Tue, 12 Aug 2025 20:50:37 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea258026a189c2612dba0e0b96a5b6dfd6b82ca540ee948b6e6560cb0741f56`  
		Last Modified: Tue, 12 Aug 2025 20:50:38 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1fa4a405ade80b762a9b7fe0a4faf7b08071ac4337f7cd3a80ad135ec36798`  
		Last Modified: Tue, 12 Aug 2025 20:50:37 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084638e7436d7cea740a83f75861922523c1215fff82b52b55be7d8df4c457f6`  
		Last Modified: Tue, 12 Aug 2025 20:50:38 GMT  
		Size: 77.1 KB (77083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0f5862bedf592a2194ebd6ef1d842ec5e2b951f1d5a0c1a26adab36df00954`  
		Last Modified: Tue, 12 Aug 2025 20:50:39 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c465eb7da834842c61a1066ae25f499de5fba01a02b9194b51c9f6b9ff76fe`  
		Last Modified: Tue, 12 Aug 2025 21:16:40 GMT  
		Size: 201.7 MB (201671957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8006a30afeda35f0bf450fae4e1c2fa1816da903d8833c8498c4d457bcada8`  
		Last Modified: Tue, 12 Aug 2025 20:50:40 GMT  
		Size: 108.4 KB (108400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0986f223315c5e3bd0ad8fe69e15b14319a7febfea39a3988e66515185923f03`  
		Last Modified: Tue, 12 Aug 2025 20:50:39 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
