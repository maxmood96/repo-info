## `openjdk:26-ea-23-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:ba83cb254be4d22ad8b5ac88088c67a7693f80d99013e9c461286e530102959e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `openjdk:26-ea-23-jdk-nanoserver` - windows version 10.0.26100.7171; amd64

```console
$ docker pull openjdk@sha256:2b87a4a9b0740511ff4ab06b819e1ab06e0970bd6f9f840eff3860a60e2de311
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.4 MB (419445249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ebeec2fec1a4ed9d2cd66d73980443734f056e328400789c7604d7beaab2f9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 09 Nov 2025 10:04:50 GMT
RUN Apply image 10.0.26100.7171
# Tue, 11 Nov 2025 20:11:08 GMT
SHELL [cmd /s /c]
# Tue, 11 Nov 2025 20:14:59 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 11 Nov 2025 20:14:59 GMT
USER ContainerAdministrator
# Tue, 11 Nov 2025 20:15:01 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 11 Nov 2025 20:15:01 GMT
USER ContainerUser
# Tue, 11 Nov 2025 20:15:02 GMT
ENV JAVA_VERSION=26-ea+23
# Tue, 11 Nov 2025 20:15:16 GMT
COPY dir:caac7c3daf5c418f731b855ae37dd48a49eef4e9ccf593b019be40c369c65420 in C:\openjdk-26 
# Tue, 11 Nov 2025 20:15:21 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 11 Nov 2025 20:15:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:87c91227213eb6e7c8cfe33b6bd0429350e524756878f37f3860b013f804bf59`  
		Last Modified: Tue, 11 Nov 2025 20:41:49 GMT  
		Size: 197.9 MB (197936447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6194cd77702c569004d9457e0c06be0662b8256bcd8f00c1d770f01827ff09e`  
		Last Modified: Tue, 11 Nov 2025 20:12:01 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1257b25cf52c5ede2032b927bc5f1342c450c20be32bbbc4d6aefe8357bc514`  
		Last Modified: Tue, 11 Nov 2025 20:15:51 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45440e2d56525b8b61f06079e41237c5d32db826dc6a5b6ec80ffd49e669ff3`  
		Last Modified: Tue, 11 Nov 2025 20:15:51 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca352de405283e15ac0a8e2b4f56ce7ab10396e432d99adfb942705c8d4756b`  
		Last Modified: Tue, 11 Nov 2025 20:15:51 GMT  
		Size: 72.0 KB (71961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e64c7b80e1865bd7b4331e807018e3fef5c04ad5c3454011782881336a03e1`  
		Last Modified: Tue, 11 Nov 2025 20:15:51 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b858af93df5546ff052de0b25fdeba592d6bca73f7d39db7806f5422fb6010`  
		Last Modified: Tue, 11 Nov 2025 20:15:51 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044bf286e691844ac398f4a9b2d0b5d56447b20e230d63c32acf1c89ba8ad296`  
		Last Modified: Tue, 11 Nov 2025 22:23:52 GMT  
		Size: 221.3 MB (221318054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1f597aa25978e3b820691a4cdb262e4db4b17f890f72a75047037e4d1eedbe`  
		Last Modified: Tue, 11 Nov 2025 20:15:51 GMT  
		Size: 112.4 KB (112396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837124e314b72377ab5ceb7f9b21a5258292afca60fd0b35244d945eeb6753df`  
		Last Modified: Tue, 11 Nov 2025 20:15:53 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-ea-23-jdk-nanoserver` - windows version 10.0.20348.4405; amd64

```console
$ docker pull openjdk@sha256:9dc8a9b79043b854fb956fff11117cb9f14b25297df88b4c97b796ac6950a3f4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.9 MB (347857439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6e0003322fa2d28bf5e707ce5399d524673df642243d4cd80eaf7cb4f9b63d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 11 Nov 2025 20:10:27 GMT
SHELL [cmd /s /c]
# Tue, 11 Nov 2025 20:16:31 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 11 Nov 2025 20:16:32 GMT
USER ContainerAdministrator
# Tue, 11 Nov 2025 20:16:34 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 11 Nov 2025 20:16:34 GMT
USER ContainerUser
# Tue, 11 Nov 2025 20:16:35 GMT
ENV JAVA_VERSION=26-ea+23
# Tue, 11 Nov 2025 20:16:53 GMT
COPY dir:caac7c3daf5c418f731b855ae37dd48a49eef4e9ccf593b019be40c369c65420 in C:\openjdk-26 
# Tue, 11 Nov 2025 20:16:57 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 11 Nov 2025 20:16:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc704c4257ca5dc0c86f854eff2df55a480551d342ee212cc3a99fcdb9018db`  
		Last Modified: Tue, 11 Nov 2025 20:11:34 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659a768b0bc21c400b19bafd60868e714c532293918c983e91d0b5f1a161db7c`  
		Last Modified: Tue, 11 Nov 2025 20:17:25 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b02e3e57c1aaec4a84c08f44716e90d106f75ae10d1367c872c42b4090e7964`  
		Last Modified: Tue, 11 Nov 2025 20:17:26 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02ee4773bd7f113829caef16499facd12e8b9ca4182991d69fc60cb58f7e75f`  
		Last Modified: Tue, 11 Nov 2025 20:17:26 GMT  
		Size: 76.8 KB (76788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d056b537798b4732d45b1dd069f0520b0541f42c100a0a9759fca8d64c6cdc`  
		Last Modified: Tue, 11 Nov 2025 20:17:26 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3dc8a3ea47de4bac2e636f57941d5e09630da75ace247ca3f0f50d8ed6a2295`  
		Last Modified: Tue, 11 Nov 2025 20:17:26 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4114449f094bc36981d84b462964164d49d130a362d91e05b0f1508ee129f3d5`  
		Last Modified: Tue, 11 Nov 2025 22:24:56 GMT  
		Size: 221.3 MB (221317877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e680281ab9e74e8a833a1cb9237b91c2e901f2ad8ffb0e42f253ac2b1b3c57`  
		Last Modified: Tue, 11 Nov 2025 20:17:26 GMT  
		Size: 107.4 KB (107358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f484804aac7493f57fc81bfe26ab282c71f5601383507cdf24cb4c5adb28755`  
		Last Modified: Tue, 11 Nov 2025 20:17:25 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
