## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:5b3c9ccba0290ed98b2178cd2cb1e8dbe0e443afa44fc7b293fe873671f78c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.26100.3781; amd64

```console
$ docker pull eclipse-temurin@sha256:082d5ef9aefd5b88faf992a05703f0525fa22e7a889ea2d0feedc0e2f955b96c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (233973560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ccd8f1b9acd46d97b112c7681aa1c8aff52b761a1068c84b2683e559e0ba759`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Fri, 18 Apr 2025 04:14:13 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:14:14 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Fri, 18 Apr 2025 04:14:15 GMT
ENV JAVA_HOME=C:\openjdk-11
# Fri, 18 Apr 2025 04:14:16 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:14:19 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:14:19 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:14:23 GMT
COPY dir:e7319a06d2b9171c954fc18de0614fa7d0eb408950b795be61492806db04a6ea in C:\openjdk-11 
# Fri, 18 Apr 2025 04:14:28 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 17 Apr 2025 02:52:17 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c42e86f25544cf39f37b20d6e872db116627603fbc234002a57d1a33e874ae`  
		Last Modified: Fri, 18 Apr 2025 04:14:31 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7ecb3cb5836c78960932c546d23cbd0ecb566a08876b68509c00334df4db01`  
		Last Modified: Fri, 18 Apr 2025 04:14:31 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb47b5557b371e826a72b05842d616d50cefb387dad15d9dc055d83408396c19`  
		Last Modified: Fri, 18 Apr 2025 04:14:31 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb593eb5500e8d4eb4adf487203f8eb694291ff2041f3f55eadecc192570fe8`  
		Last Modified: Fri, 18 Apr 2025 04:14:30 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029335f998edc1f8b8ed4b848d79d9fd7cce00026996d1a8e2397d4af68fa94b`  
		Last Modified: Fri, 18 Apr 2025 04:14:30 GMT  
		Size: 76.6 KB (76556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4942af0f44111b4de3b7b168e69c87afbbceb883eb8c91aca58e609285cd05`  
		Last Modified: Fri, 18 Apr 2025 04:14:30 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f717611de3532e7be81ee1a6acdfee0c51515468205973f715d6a47a819d5e`  
		Last Modified: Fri, 18 Apr 2025 04:14:34 GMT  
		Size: 43.7 MB (43656872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d1d76f0f2148d469f111a42bb2d71f385531805a11956b8d1adf1417a22e35`  
		Last Modified: Fri, 18 Apr 2025 04:14:30 GMT  
		Size: 92.8 KB (92835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.20348.3566; amd64

```console
$ docker pull eclipse-temurin@sha256:4455dbca4d519a28fdcc05609dc8a25fd0ef2508ad5ec90601c08b586efb2443
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166374586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d5de39a8ef5657af31429280bf4f62a433a551dd68feb96fe20d9109e89a64d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Fri, 18 Apr 2025 04:20:12 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:20:13 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Fri, 18 Apr 2025 04:20:14 GMT
ENV JAVA_HOME=C:\openjdk-11
# Fri, 18 Apr 2025 04:20:14 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:20:17 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:20:17 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:20:21 GMT
COPY dir:e7319a06d2b9171c954fc18de0614fa7d0eb408950b795be61492806db04a6ea in C:\openjdk-11 
# Fri, 18 Apr 2025 04:20:25 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Wed, 16 Apr 2025 23:30:29 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18425fa4b4138baef16dbfa2ba224baa455931e6bc23a6577a2afd55b0ac4f76`  
		Last Modified: Fri, 18 Apr 2025 04:20:28 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc193d11d27cb1d78986266f6c77db731f569c37157e808b315fccf7ce1e0320`  
		Last Modified: Fri, 18 Apr 2025 04:20:28 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7664834bb6593b5498108723271abe57e3c3182345c052630b8a2190648d020`  
		Last Modified: Fri, 18 Apr 2025 04:20:28 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acb401f560326762ed6006c55f7a66f31ad686e923ddb66f5ab9a2de7c4d3df`  
		Last Modified: Fri, 18 Apr 2025 04:20:27 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f9bdb64dd9cd86f292faea02e30acb53b3305df0e7ee5caaf0186f94da2fe7`  
		Last Modified: Fri, 18 Apr 2025 04:20:27 GMT  
		Size: 77.0 KB (76985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b233014ed0dd472a65d72c90390d4babc419522049c0b3258fc116f01c23806`  
		Last Modified: Fri, 18 Apr 2025 04:20:27 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f1bad29584c11c1d1622979b2f33eea8f5159b55f47d8982ebffbbeed2209a`  
		Last Modified: Fri, 18 Apr 2025 04:20:32 GMT  
		Size: 43.7 MB (43655534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce515fca57f14b4fe4f1166c3431bfd58f7a6fd89ea753182c9bdd059442b9c`  
		Last Modified: Fri, 18 Apr 2025 04:20:27 GMT  
		Size: 97.8 KB (97834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.17763.7249; amd64

```console
$ docker pull eclipse-temurin@sha256:7f06646c6a80c4f346635f3506e5b832003812877f78c739fe5e67be53c6b951
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152579007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae4ec7ab43069e584b3f30722836a7366d483b6355ea5a086b264bf4f1a25d3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 04:20:07 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:20:09 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Fri, 18 Apr 2025 04:20:10 GMT
ENV JAVA_HOME=C:\openjdk-11
# Fri, 18 Apr 2025 04:20:10 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:20:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:20:13 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:20:18 GMT
COPY dir:e7319a06d2b9171c954fc18de0614fa7d0eb408950b795be61492806db04a6ea in C:\openjdk-11 
# Fri, 18 Apr 2025 04:20:21 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e6b9a580e293bba2cf4d11519c25b84d41186b703ef9bf090eaf0e7df1f5ed`  
		Last Modified: Fri, 18 Apr 2025 04:20:24 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a23d273bd203263f4494e0ca7f226bc5b12085f77030fd3438a3694f94b6c9`  
		Last Modified: Fri, 18 Apr 2025 04:20:24 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63711701320903e16b4a084cbe81f049ab9687157cc8286b7dc78c72461d6fd9`  
		Last Modified: Fri, 18 Apr 2025 04:20:24 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9ec982bb5638f6107d8880119b7d630063429f5ffaf42ed0a5b73d616efc30`  
		Last Modified: Fri, 18 Apr 2025 04:20:23 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6945a8ead60f2e0d5bfe772accf0cd35860746b282c382d0a56e8b5158329fba`  
		Last Modified: Fri, 18 Apr 2025 04:20:23 GMT  
		Size: 69.0 KB (69033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75467b559af8d31e0cd50d0346cc4afd147d550e7acd290f8ce32cc2ca61fd3d`  
		Last Modified: Fri, 18 Apr 2025 04:20:23 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87b9f3696b87ea07978cbdf2406d17abc180bc6e3becb923a94c709a87fb06c`  
		Last Modified: Fri, 18 Apr 2025 04:20:27 GMT  
		Size: 43.7 MB (43655421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2281144aae56f475d5b0f16f493d13d0dadfbf90dab5496a85cc013b223015`  
		Last Modified: Fri, 18 Apr 2025 04:20:23 GMT  
		Size: 97.1 KB (97078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
