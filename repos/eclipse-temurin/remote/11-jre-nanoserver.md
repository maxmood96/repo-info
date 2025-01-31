## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:d1eb56ef9e118bc22d45669193a7ab769e98f88751db5b68e48d68f3a43c1133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:dd5f0e230731a1d5f01937c9393419410983c171093f4d49dd0b2b850870e96f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242884269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0539acd422b64abfcf19859e10260fdfb99bc5166dad36d88e898fc157b7fb6c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Fri, 31 Jan 2025 03:15:53 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 03:15:54 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Fri, 31 Jan 2025 03:15:54 GMT
ENV JAVA_HOME=C:\openjdk-11
# Fri, 31 Jan 2025 03:15:54 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 03:15:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 03:15:57 GMT
USER ContainerUser
# Fri, 31 Jan 2025 03:16:00 GMT
COPY dir:e7319a06d2b9171c954fc18de0614fa7d0eb408950b795be61492806db04a6ea in C:\openjdk-11 
# Fri, 31 Jan 2025 03:16:04 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4e5cb6b429eec1ac314ebe4feb94168cac5fe85dc99c971623ee544f5927c7`  
		Last Modified: Fri, 31 Jan 2025 03:16:09 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35060226ea0443c8a9f213d5186ed8ce5a3aa1517c10a0b1af130d52089d1d7`  
		Last Modified: Fri, 31 Jan 2025 03:16:09 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18944dac6ee5c7303ade1b2ef0d655cf32400e3089add8bfeb36764f8ea2b6a`  
		Last Modified: Fri, 31 Jan 2025 03:16:09 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3ccdaaed8f40f78544e8b57eb58196a58f8743f7db3a567b255308eeac2a96`  
		Last Modified: Fri, 31 Jan 2025 03:16:07 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b711d5ce5eb2b7bc8c602eed0cf3e390d5c8e0e2a1e1c3a4ee17d07bd728547`  
		Last Modified: Fri, 31 Jan 2025 03:16:07 GMT  
		Size: 75.6 KB (75596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cea3631de827abfd51fd3d133f9adfa7b48f2eae6115c72b24d820fbcf5e87`  
		Last Modified: Fri, 31 Jan 2025 03:16:07 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa2470daedba768ff0f42903ae97a872aa7edca572ba4f57183e274e2f5f062`  
		Last Modified: Fri, 31 Jan 2025 03:16:12 GMT  
		Size: 43.7 MB (43656616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe061423720634ad28c5e038ee6da4ac418e64c0ad18bdeaca3bdcd7ed75385d`  
		Last Modified: Fri, 31 Jan 2025 03:16:07 GMT  
		Size: 92.6 KB (92552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:bbeb4b16b2e5030fee82ccd1aa18c531ac5a4a24e6abe4d79851fd075b3c1f87
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.5 MB (164505794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6c45b217c54b3f4621993babfad1083de5070d71266224547bf7518bdf5c02`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Fri, 31 Jan 2025 02:11:27 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 02:11:27 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Fri, 31 Jan 2025 02:11:28 GMT
ENV JAVA_HOME=C:\openjdk-11
# Fri, 31 Jan 2025 02:11:28 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 02:11:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 02:11:48 GMT
USER ContainerUser
# Fri, 31 Jan 2025 02:11:52 GMT
COPY dir:e7319a06d2b9171c954fc18de0614fa7d0eb408950b795be61492806db04a6ea in C:\openjdk-11 
# Fri, 31 Jan 2025 02:11:57 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18740068f2dd25ad338d37afdf7ecf4b89f9e0c57941a3d9fa2adff9831377c6`  
		Last Modified: Fri, 31 Jan 2025 02:12:00 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695acdfe86a31d9f59f55c038a808e87a5f039991e086ac683fb86242ccce4a7`  
		Last Modified: Fri, 31 Jan 2025 02:12:00 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7655994ce5ca894acbc945990b19895665df2f717b7df9ad2bed5dd77f3abaa7`  
		Last Modified: Fri, 31 Jan 2025 02:12:00 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a19d4dd4c6ce426d5c32f1a5af1d5659b738ded8e4f4adf9c4de5437a2ad58e`  
		Last Modified: Fri, 31 Jan 2025 02:11:59 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7134024a8b126c7d382b9e29dea0b0ca18cff360e8d423e9b0b572bc88608a6f`  
		Last Modified: Fri, 31 Jan 2025 02:11:59 GMT  
		Size: 87.8 KB (87793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c1925a5bbf9e11a9fe4c5b76425799c3eb9f582f5f81bfe11a602b8f3d860d`  
		Last Modified: Fri, 31 Jan 2025 02:11:59 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5711b3bab6634d8ec58dc48df4a20cbf86683110f444fd7f0ac69d25403f45a8`  
		Last Modified: Fri, 31 Jan 2025 02:12:03 GMT  
		Size: 43.7 MB (43654567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1697c5e6bc1d709ba2dde5c4f9da01b1e59a74e6331bd54711944b998b18aa5`  
		Last Modified: Fri, 31 Jan 2025 02:11:59 GMT  
		Size: 96.7 KB (96732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:aa0e56b632fa8bbeaf39acbfdd549e0f656dd9306c69f4a055124f5207bb7510
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199066743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f0f3818a91a8221d01180db72866dcaae02a6b37aeb6808a623ba97193c54f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Fri, 31 Jan 2025 03:11:50 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 03:11:51 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Fri, 31 Jan 2025 03:11:51 GMT
ENV JAVA_HOME=C:\openjdk-11
# Fri, 31 Jan 2025 03:11:52 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 03:11:58 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 03:11:58 GMT
USER ContainerUser
# Fri, 31 Jan 2025 03:12:03 GMT
COPY dir:e7319a06d2b9171c954fc18de0614fa7d0eb408950b795be61492806db04a6ea in C:\openjdk-11 
# Fri, 31 Jan 2025 03:12:06 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca7086926f493ad2a6ede9e3319b925ec28b99d058d68a4081b62c96ac13138`  
		Last Modified: Fri, 31 Jan 2025 03:12:12 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28197d935e34282bed8a0d1b5a0e82033931980697a186696abfab36853842d0`  
		Last Modified: Fri, 31 Jan 2025 03:12:12 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f593f1be8e1799dccc0a794177ed739e2ab5aaa7d4b497c19be7e5a08e17ee`  
		Last Modified: Fri, 31 Jan 2025 03:12:12 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76afdfaa508b86bcb2c0a9797badf093381bbd1e156bced1c87c1a112ba2060f`  
		Last Modified: Fri, 31 Jan 2025 03:12:10 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2810864b89b5f5c2354c07eb9824355075b3c0be475b0e5f06acc941edf528e`  
		Last Modified: Fri, 31 Jan 2025 03:12:10 GMT  
		Size: 68.0 KB (68027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84178d01dd8413e9a7b495c7544e274d918013a6a3f1a959db6f7852c1bbf375`  
		Last Modified: Fri, 31 Jan 2025 03:12:10 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3e4799f58112b1f496e941d62072cd76d2461b8975b4d249b4fa2315f16d23`  
		Last Modified: Fri, 31 Jan 2025 03:12:15 GMT  
		Size: 43.7 MB (43656864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49563bdb3d17f5cd27ccb84ec1ab2c3e6fe6130d157b498024f89ca9b663c03`  
		Last Modified: Fri, 31 Jan 2025 03:12:10 GMT  
		Size: 68.8 KB (68773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
