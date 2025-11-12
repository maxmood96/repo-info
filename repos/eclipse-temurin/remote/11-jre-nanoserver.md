## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:beba60b3ae23ad223754bedf551e42973ddfbfd10fff739306b71050c493df16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.26100.7171; amd64

```console
$ docker pull eclipse-temurin@sha256:76576bc73b3d175c8c84b76dda7cfd0a5d21c73147046d0fae2049b28c7c936a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241813810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634dfdb7724420c2a2fb3b7ab060a1c9c35cadfe9bb033029e3908e3267a5442`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 09 Nov 2025 10:04:50 GMT
RUN Apply image 10.0.26100.7171
# Tue, 11 Nov 2025 20:10:42 GMT
SHELL [cmd /s /c]
# Tue, 11 Nov 2025 20:12:07 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Tue, 11 Nov 2025 20:12:08 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 11 Nov 2025 20:12:08 GMT
USER ContainerAdministrator
# Tue, 11 Nov 2025 20:12:10 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 11 Nov 2025 20:12:10 GMT
USER ContainerUser
# Tue, 11 Nov 2025 20:12:17 GMT
COPY dir:4835e564d5b678d207d3850b6f40a90e0afa12e9d665c48e7909a88923b1a7a8 in C:\openjdk-11 
# Tue, 11 Nov 2025 20:12:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:87c91227213eb6e7c8cfe33b6bd0429350e524756878f37f3860b013f804bf59`  
		Last Modified: Tue, 11 Nov 2025 20:41:49 GMT  
		Size: 197.9 MB (197936447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82420529eec49d9844e6bcea0ba1c55c2202b9d70f948ba02c97b7dbbec9579`  
		Last Modified: Tue, 11 Nov 2025 20:11:47 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb63dd995f880b04e5ae69e960bd619455aeec512b64a2adab220dc8e3bda0e`  
		Last Modified: Tue, 11 Nov 2025 20:12:34 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9899b20bbf33d275d6ab95d92ded90c35ac6b2c4f2fe6b1b42c4be9f82b668b3`  
		Last Modified: Tue, 11 Nov 2025 20:12:34 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270ea1e8a5922afd62275d54d84d4a5834f70510db97ff6f8d9a834424cb633d`  
		Last Modified: Tue, 11 Nov 2025 20:12:34 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69a8668dbfdc09e66856b3b1abd6b5bde64cdee1a7b993a5eac8901ddd647ac`  
		Last Modified: Tue, 11 Nov 2025 20:12:34 GMT  
		Size: 72.3 KB (72309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e86c721c7ccff8bf3c6ff475d2ee3a21da1c785b05925a8d3760eedfc5b7fb8`  
		Last Modified: Tue, 11 Nov 2025 20:12:34 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe0ff9992e202f832ff36bae6303a873083628a20c938c65bd355ad7a8f0044`  
		Last Modified: Tue, 11 Nov 2025 20:12:38 GMT  
		Size: 43.7 MB (43695005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e218cc82f0eaa2c7c2d03b017e2bd72ac22ded20ecfc4a17101987e6d38a7cf8`  
		Last Modified: Tue, 11 Nov 2025 20:12:34 GMT  
		Size: 104.7 KB (104696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.20348.4405; amd64

```console
$ docker pull eclipse-temurin@sha256:87b6c76e95919be13cde54e5c9c002ad230aefedabc48e28c935bcc05f303a2e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.2 MB (170210655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf76bb4cc8fcdcc5e85b1bc774b2d0aa135cfcc37b6dc5a432aea1befbdffa12`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 11 Nov 2025 20:10:44 GMT
SHELL [cmd /s /c]
# Tue, 11 Nov 2025 20:10:45 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Tue, 11 Nov 2025 20:10:45 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 11 Nov 2025 20:10:45 GMT
USER ContainerAdministrator
# Tue, 11 Nov 2025 20:10:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 11 Nov 2025 20:10:49 GMT
USER ContainerUser
# Tue, 11 Nov 2025 20:10:58 GMT
COPY dir:4835e564d5b678d207d3850b6f40a90e0afa12e9d665c48e7909a88923b1a7a8 in C:\openjdk-11 
# Tue, 11 Nov 2025 20:11:01 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98d596b44731ccc546a8f48a8a6e760b6816cd774426ad0bf327076f1a5d218`  
		Last Modified: Tue, 11 Nov 2025 20:11:33 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419351bcc6f6ca5375f0795fff4d3069d28d3c710f0aa9ab8f9aa43f2d58ec69`  
		Last Modified: Tue, 11 Nov 2025 20:11:33 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b76fdc7c392950bfd77354bb05f990591dc67ad198443ea2b415b3b61a20a4`  
		Last Modified: Tue, 11 Nov 2025 20:11:33 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138ec515987f64999b7b58643d6a91c887f916f228e0ce464e5e391a9f5d2298`  
		Last Modified: Tue, 11 Nov 2025 20:11:33 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815a695d66179f5f44bf47d19f50e8b5da8bef6fe90c095dbecf72f0f3dc6344`  
		Last Modified: Tue, 11 Nov 2025 20:11:33 GMT  
		Size: 71.8 KB (71759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe47ae43221729c01a6376d845e6ac81d0f719923b5a13fcd45d46f538e97b4`  
		Last Modified: Tue, 11 Nov 2025 20:11:33 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eebd31dc55d09d546942539277c1fa41be8a58e81b9df8c7bfa16b337f5a52e`  
		Last Modified: Tue, 11 Nov 2025 20:11:36 GMT  
		Size: 43.7 MB (43694979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d01306a33544be522ae9730be4358bb1956cf4a4d54de82935c04687ac717671`  
		Last Modified: Tue, 11 Nov 2025 20:11:33 GMT  
		Size: 89.6 KB (89580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
