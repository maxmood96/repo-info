## `openjdk:25-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:ab4cfa124cc881aa08e238feaf065bdd1197913fc14280d1568243843826ca09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `openjdk:25-ea-jdk-nanoserver` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:752e40e0e9df0eda0913ece08efe1b6e61061415e7e6168c1fbce6752c4a9cc6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406721025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48f25b3d30f91109a203c991569e60a7527e157b92472b9e04e1b9f2a41013d7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Tue, 11 Feb 2025 01:31:41 GMT
SHELL [cmd /s /c]
# Tue, 11 Feb 2025 01:31:41 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 11 Feb 2025 01:31:42 GMT
USER ContainerAdministrator
# Tue, 11 Feb 2025 01:31:44 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 11 Feb 2025 01:31:45 GMT
USER ContainerUser
# Tue, 11 Feb 2025 01:31:45 GMT
ENV JAVA_VERSION=25-ea+9
# Tue, 11 Feb 2025 01:31:52 GMT
COPY dir:d7acfa7ae78317b124adc15f4373b266207aef9ee64c7b37ba0d0b39bb9389f0 in C:\openjdk-25 
# Tue, 11 Feb 2025 01:31:58 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 11 Feb 2025 01:31:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Wed, 22 Jan 2025 08:02:27 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140e01ee1c13ca37b35e581776495593f51e7a6c29eb4e65c935b423854548e0`  
		Last Modified: Wed, 12 Feb 2025 21:50:50 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893b118f97c0dd29192d5157cd21eeb0e7425a1822414c62f52df9c772e33434`  
		Last Modified: Wed, 12 Feb 2025 21:50:51 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88b3541f10dd70bdb925a68c463698e497a4100094a19071b3fa735fef1f9ef`  
		Last Modified: Wed, 12 Feb 2025 21:50:52 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686d895ffc360568bd1ca652853ebfc0740f2c68411fa22aea870a758f93ab86`  
		Last Modified: Wed, 12 Feb 2025 21:50:52 GMT  
		Size: 75.7 KB (75706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da557ece925761d9dd9b9a55b0c0869ee07f55ab894886c678e7fbf594d2da1`  
		Last Modified: Wed, 12 Feb 2025 21:50:54 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb254d90661960d93bb4389fadd62504c23aa9b057499c72767795e53c56917`  
		Last Modified: Wed, 12 Feb 2025 21:50:55 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029cdb3cc24f6d6c4f82d78fa2d56a1e630550c26df478a5724bf27b1b150a9d`  
		Last Modified: Tue, 11 Feb 2025 01:32:14 GMT  
		Size: 207.5 MB (207492194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5460dd801f2e3569b985d6c87605a6c98c480f579f63d910e3463348a3edb37d`  
		Last Modified: Wed, 12 Feb 2025 21:51:43 GMT  
		Size: 92.5 KB (92461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2cb44344e4b0b8d7a6497fb04ffaf43476061e7b935924af9ff8a1131c1bd03`  
		Last Modified: Wed, 12 Feb 2025 21:51:44 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-jdk-nanoserver` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:1c75c1e7228498a3bc6080b8e9973fa56ffa4db97d214d8f85836a4d3a138259
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.3 MB (328344781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf0c3a808089af6da4757775f8e4e4dd2134f818eb1565d229e6c6d0a5104524`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Tue, 11 Feb 2025 01:27:43 GMT
SHELL [cmd /s /c]
# Tue, 11 Feb 2025 01:27:44 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 11 Feb 2025 01:27:45 GMT
USER ContainerAdministrator
# Tue, 11 Feb 2025 01:27:58 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 11 Feb 2025 01:27:58 GMT
USER ContainerUser
# Tue, 11 Feb 2025 01:27:59 GMT
ENV JAVA_VERSION=25-ea+9
# Tue, 11 Feb 2025 01:28:07 GMT
COPY dir:d7acfa7ae78317b124adc15f4373b266207aef9ee64c7b37ba0d0b39bb9389f0 in C:\openjdk-25 
# Tue, 11 Feb 2025 01:28:12 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 11 Feb 2025 01:28:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Wed, 15 Jan 2025 01:24:28 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec4371e05de61188dabfd1db464cc871528a821b7d40045cfed1ca5c3a430f1`  
		Last Modified: Tue, 11 Feb 2025 08:57:24 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff43f898360944bcfdb11818b3618b14f46cc58622baa0fea9c3750f28e2dd90`  
		Last Modified: Tue, 11 Feb 2025 08:57:25 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e3a6052982087b5f719d9ae3883c9184c56671ab65e2ee785d73b1eba9dcac`  
		Last Modified: Wed, 12 Feb 2025 09:01:26 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e872eeb66e49bc35e189095ee3f3933a1347eff32ccac52e0e734cb7fe5c8d72`  
		Last Modified: Tue, 11 Feb 2025 08:57:25 GMT  
		Size: 87.5 KB (87482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7605987bd8df853473ecba10f8d87d47016f8680e6812b943e11ff68e9abaa6c`  
		Last Modified: Tue, 11 Feb 2025 15:03:22 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239fd1e1005860f8dec30d25e6f2bbca280f2d218324f450f30298d132b7b898`  
		Last Modified: Tue, 11 Feb 2025 15:03:22 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34be423673a6d1a81a4518a8baa173a896239f9056d1e8d10eb63dcbb19ec78`  
		Last Modified: Tue, 11 Feb 2025 08:57:41 GMT  
		Size: 207.5 MB (207491655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f363b8de8562e6f63f635374654bb2ae5a02c56796ed8f65f4264a5669db6224`  
		Last Modified: Tue, 11 Feb 2025 08:57:44 GMT  
		Size: 97.8 KB (97824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06019fcc1ca6ae7c43a9f301f61651e061efdb65c255b48f4381bbe7514e2c63`  
		Last Modified: Tue, 11 Feb 2025 15:03:23 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-jdk-nanoserver` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:5efed6438831a1a670f4a4cc6d4960501696bf0ad108eb736476b13ec87eae17
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.2 MB (367224289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5b6931cebb69171b3aa12326eb423b2ef9e2842e95b94fb930d047f8fcd075`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Tue, 11 Feb 2025 01:28:06 GMT
SHELL [cmd /s /c]
# Tue, 11 Feb 2025 01:28:07 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 11 Feb 2025 01:28:08 GMT
USER ContainerAdministrator
# Tue, 11 Feb 2025 01:28:28 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 11 Feb 2025 01:28:29 GMT
USER ContainerUser
# Tue, 11 Feb 2025 01:28:29 GMT
ENV JAVA_VERSION=25-ea+9
# Tue, 11 Feb 2025 01:28:41 GMT
COPY dir:d7acfa7ae78317b124adc15f4373b266207aef9ee64c7b37ba0d0b39bb9389f0 in C:\openjdk-25 
# Tue, 11 Feb 2025 01:28:47 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 11 Feb 2025 01:28:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Wed, 15 Jan 2025 07:23:16 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0e98901daf448d7b7108791c075e7bd537617e8aa81f78703d15c858edfc9f`  
		Last Modified: Wed, 12 Feb 2025 21:50:25 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14889923c476e830c372226162661ce115791175644cfa35951e721e5c744d2`  
		Last Modified: Wed, 12 Feb 2025 21:50:26 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1591cbf85d73773982923a2a341761d819e926cfe48908e20556145960b3c6b9`  
		Last Modified: Wed, 12 Feb 2025 21:50:27 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a476cae9e0671f0de4517848c7a2520bfd704ecb583625436829bf2630378bab`  
		Last Modified: Wed, 12 Feb 2025 21:50:28 GMT  
		Size: 74.8 KB (74794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59628c56a214178e0380378505a642f218f241c8db0d9feac4fec44a659fc1a6`  
		Last Modified: Wed, 12 Feb 2025 21:50:30 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8278cf74fdbe48f0776671e711ca04c2a34a8ba2041cfa7d73b60ff6d63c4bc3`  
		Last Modified: Wed, 12 Feb 2025 21:50:30 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528a5f86ba034bb954587cb793ba29f63217644a5a47b95c8f590585b5ff5609`  
		Last Modified: Tue, 11 Feb 2025 01:29:02 GMT  
		Size: 207.5 MB (207492295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c69a57d05662ccf2bb4f9f154ab8a3ca9e1c8725c11a688d1495ff51abf627`  
		Last Modified: Wed, 12 Feb 2025 21:51:06 GMT  
		Size: 4.4 MB (4383244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594f46864ebf14deb7600287c9f7c1a9d43e724097679f8713f2f400c11b9f2f`  
		Last Modified: Wed, 12 Feb 2025 21:51:08 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
