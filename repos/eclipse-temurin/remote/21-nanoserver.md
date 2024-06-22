## `eclipse-temurin:21-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:4023bdbfd875f290e2672f37837fb535aba4d079d709c2494ed540415564a1df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2529; amd64
	-	windows version 10.0.17763.5936; amd64

### `eclipse-temurin:21-nanoserver` - windows version 10.0.20348.2529; amd64

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

### `eclipse-temurin:21-nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull eclipse-temurin@sha256:158466fe46fe58e32c184eb3fc1fd47b3173f00556f17a47bd14105869817e4a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.0 MB (360048781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f82e2683f318cfe7b78e323fdf86ab1b1860bc65b8de78992dfdc50cf0a483e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 17:41:08 GMT
SHELL [cmd /s /c]
# Wed, 12 Jun 2024 18:11:13 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Wed, 12 Jun 2024 18:11:14 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 12 Jun 2024 18:11:15 GMT
USER ContainerAdministrator
# Wed, 12 Jun 2024 18:11:23 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Jun 2024 18:11:24 GMT
USER ContainerUser
# Wed, 12 Jun 2024 18:11:39 GMT
COPY dir:23b4ead9c2036754f644b00182bded9da6af0a8e5b9adaf18f46a103fb435a07 in C:\openjdk-21 
# Wed, 12 Jun 2024 18:11:51 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Jun 2024 18:11:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce076c01ab33a997d8fa4a6a49752f31455fef6df331991ad3b3736b3567321`  
		Last Modified: Wed, 12 Jun 2024 18:40:43 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94d2c91363bfe5e9d08cb403aac28f5e6a9c7eb513331c4b32254f2a78d6e57`  
		Last Modified: Wed, 12 Jun 2024 18:48:41 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c42fbc76f14521951f86387cd95eac4ab4a327bb15279428acd40c4756eefaae`  
		Last Modified: Wed, 12 Jun 2024 18:48:40 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bbb023a716434c74e0fc6e28a4ca7504b2694a7f29494538e188c9f633398a`  
		Last Modified: Wed, 12 Jun 2024 18:48:40 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d78851526fef0a3dda198e35c498f99840f32e799958db9fca78e5c2c54451`  
		Last Modified: Wed, 12 Jun 2024 18:48:39 GMT  
		Size: 74.6 KB (74552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7f8d09079553b45d46af6f933ab9086bd44ac29d365222754d666cb5eefde2`  
		Last Modified: Wed, 12 Jun 2024 18:48:38 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3186d54e93da414ade02e44b617b14d7b48a087b29f7100636a3b440cabeee9`  
		Last Modified: Wed, 12 Jun 2024 18:48:58 GMT  
		Size: 201.1 MB (201148566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17b6949ba3aff997873c328ee230fa2e8f5281eb7be644f49f1a6b2e6b75d12`  
		Last Modified: Wed, 12 Jun 2024 18:48:40 GMT  
		Size: 3.8 MB (3785522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd815643ea7be50b1dc5bcb1dfbdde02b57c1667801ad6ec42475c8755bbb6dd`  
		Last Modified: Wed, 12 Jun 2024 18:48:38 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
