## `eclipse-temurin:8-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:fcd392eb623bacb77dca34c24ff579d94294a64d8966fa7aba48a9547d613249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3194; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.26100.3194; amd64

```console
$ docker pull eclipse-temurin@sha256:0a9760279d9e4de578b510d865e20a1dcbad20dc993893f52fef0bc1454c4c17
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246622713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df3cfd2c1a44d7a05d575597272893395ee3ccd2933066477e52a98bcdb8573`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 08 Feb 2025 22:31:47 GMT
RUN Apply image 10.0.26100.3194
# Thu, 27 Feb 2025 19:14:02 GMT
SHELL [cmd /s /c]
# Thu, 27 Feb 2025 19:14:03 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 27 Feb 2025 19:14:04 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 27 Feb 2025 19:14:05 GMT
USER ContainerAdministrator
# Thu, 27 Feb 2025 19:14:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 27 Feb 2025 19:14:10 GMT
USER ContainerUser
# Thu, 27 Feb 2025 19:14:13 GMT
COPY dir:5687adced9ba5f2555526fe07fa3e848c7771941703db13fa4b29a0f81d58070 in C:\openjdk-8 
# Thu, 27 Feb 2025 19:14:17 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:e075dd07cbf907b7da8dbd8365b73a71ac92a834b78f520bd976cb97e0fcc0a1`  
		Last Modified: Wed, 12 Feb 2025 22:34:59 GMT  
		Size: 205.9 MB (205890263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf8c648f739270cc2cbaae9f0909358ad182d7408cfe5decacb0f3235216b50`  
		Last Modified: Thu, 27 Feb 2025 19:14:21 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767a636b0d34cb71d72fbb4ef0f8b16edb3e3ea1519a7111dfe0ecfc2e606851`  
		Last Modified: Thu, 27 Feb 2025 19:14:20 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6567eb05e3c9d20cd7aa03dddf65f55a004c71068dec72e04dd8395125aa32c3`  
		Last Modified: Thu, 27 Feb 2025 19:14:20 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe0d360ba227b9d5fce16fae65d0d49acdf76107ee70ed564bafbf3c8a200f3`  
		Last Modified: Thu, 27 Feb 2025 19:14:19 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e342002a38b4183fd1703890ecdd5730b7022fd70535dd61c7b7482834e91e01`  
		Last Modified: Thu, 27 Feb 2025 19:14:20 GMT  
		Size: 78.6 KB (78624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945173c9742068ea655314705d66877e52ea2edc577f3ffc859873ffcb7ff448`  
		Last Modified: Thu, 27 Feb 2025 19:14:19 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499abd2063611c8b13e6574ee0b4a6214ba83b523721453b34fc3dc5a223f110`  
		Last Modified: Thu, 27 Feb 2025 19:14:23 GMT  
		Size: 40.6 MB (40552486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d48bd5633f050a7157f7e0d7bb6efd5980d79c625153ce16a50991411d1d00`  
		Last Modified: Thu, 27 Feb 2025 19:14:19 GMT  
		Size: 96.1 KB (96083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.20348.3207; amd64

```console
$ docker pull eclipse-temurin@sha256:1600f08a5b565b8633b3398eb76e1ca76183d7afe2d382fbeb52c7a5f2aa1c6b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.4 MB (161408789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c63602f6d9b9aacac72c6f9a9a3d05dc8b88358b5ac78f1cf3ac1710b049d5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 20:45:43 GMT
RUN Apply image 10.0.20348.3207
# Thu, 13 Feb 2025 01:19:16 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:19:16 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 13 Feb 2025 01:19:17 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 13 Feb 2025 01:19:18 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:19:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Feb 2025 01:19:21 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:19:24 GMT
COPY dir:5687adced9ba5f2555526fe07fa3e848c7771941703db13fa4b29a0f81d58070 in C:\openjdk-8 
# Thu, 13 Feb 2025 01:19:28 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:938e4585b186fc3df3c1959d47ba7a634fea121cec7545db7923ceb191d99a33`  
		Last Modified: Tue, 11 Feb 2025 22:43:09 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ba70dbf3f40191b010fa33b1bd34f9d6f8d089219d77ba35d7c0c47ce22839`  
		Last Modified: Thu, 13 Feb 2025 01:19:32 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b0b4702ab0d37e437e1615b2294a4393d6d6edf8dcdc0908ea10d8c6f6fa92`  
		Last Modified: Thu, 13 Feb 2025 01:19:32 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e24a506ff8d7f646f1156acc8f33f0cb05ec18662f3dfd7f0b51b14e626470`  
		Last Modified: Thu, 13 Feb 2025 01:19:32 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c53fef263b73fbcbd35b639ac0e880af29a31e2558f9672035be8afdba1cca1`  
		Last Modified: Thu, 13 Feb 2025 01:19:31 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bfbade1fe44f7a88f34940ddf88b4b65f02ef84eb91e821c2ed2f8ed7f5b4c8`  
		Last Modified: Thu, 13 Feb 2025 01:19:31 GMT  
		Size: 77.8 KB (77766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5477b84876c85dedddf3eb09190837248be49feaa99bfc6422369535bf787a`  
		Last Modified: Thu, 13 Feb 2025 01:19:31 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba44beb4d6ef065bf8a185d11f5adc511ee3b5032ec4b92cdb39e5a5f68a796`  
		Last Modified: Thu, 13 Feb 2025 01:19:34 GMT  
		Size: 40.6 MB (40552285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0226aac1f12359a8767e8933a901f9f2fa5b5f51135035c18973ed860803d7fc`  
		Last Modified: Thu, 13 Feb 2025 01:19:31 GMT  
		Size: 107.0 KB (106980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.17763.6893; amd64

```console
$ docker pull eclipse-temurin@sha256:76268eeef1d01ea11e5880e5afa34614aa6591e4330fa246f527413b1fc4f974
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147666937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e2646b77ae9801e2f08c74b879e1a27acce9efdbfb43c6648a891e691cc76d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:16:09 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:16:10 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 13 Feb 2025 01:16:11 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 13 Feb 2025 01:16:11 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:16:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Feb 2025 01:16:14 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:16:16 GMT
COPY dir:5687adced9ba5f2555526fe07fa3e848c7771941703db13fa4b29a0f81d58070 in C:\openjdk-8 
# Thu, 13 Feb 2025 01:16:19 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6f21906c13536ac52a4e444ca1564bd9b24c89aea9d9365bf250496965acd4`  
		Last Modified: Thu, 13 Feb 2025 01:16:25 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26dd6cea81edf388c4c196f574c03fcbd30a08b54b4c164ce759f8e2ddb0654`  
		Last Modified: Thu, 13 Feb 2025 01:16:25 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209b95b49fb9a13664ca64d75cdd44c463e9385c3f0eec096c626bca01b000f5`  
		Last Modified: Thu, 13 Feb 2025 01:16:25 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb9247e29e3c3c135077ea418c67149ec791baa28c630ba77bd79265c641641`  
		Last Modified: Thu, 13 Feb 2025 01:16:23 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03b34f98a0d7bcc6dc472b522b7742e742198b3311b4eed06b461c9e5a73cee`  
		Last Modified: Thu, 13 Feb 2025 01:16:23 GMT  
		Size: 83.6 KB (83631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8704f2e956529882a556a4e33e026bdccb7f78437550e99522f11ce470b8c7b2`  
		Last Modified: Thu, 13 Feb 2025 01:16:23 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5c06d39ba5b395f5e6ed3cac9ddd3c22f7c539bf0b825678e86d1574638223`  
		Last Modified: Thu, 13 Feb 2025 01:16:26 GMT  
		Size: 40.6 MB (40552128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53dd063e1841b5a0fdbd64a02fea99c82dedee9de8d246e7faf66916d5fbdade`  
		Last Modified: Thu, 13 Feb 2025 01:16:23 GMT  
		Size: 110.5 KB (110517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
