## `openjdk:25-ea-7-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:af3584dd1489cab039752945a8a194cffbe1bb5537e2b907061f0de055381449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `openjdk:25-ea-7-jdk-nanoserver` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:1b6e76e6e20aecf631e50f45b21926916ba09dd544b0e323a6b1e682d156c8c1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.6 MB (406633523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37181759e4d11bc176478fcb66d077ce26ffe4bd565d2e0bd299d5cffdf62c2f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Wed, 29 Jan 2025 00:31:25 GMT
SHELL [cmd /s /c]
# Wed, 29 Jan 2025 00:31:25 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 29 Jan 2025 00:31:26 GMT
USER ContainerAdministrator
# Wed, 29 Jan 2025 00:31:28 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 29 Jan 2025 00:31:29 GMT
USER ContainerUser
# Wed, 29 Jan 2025 00:31:30 GMT
ENV JAVA_VERSION=25-ea+7
# Wed, 29 Jan 2025 00:31:38 GMT
COPY dir:8eaf4d943fad5808ffdf3732eba720fc3864b955a0e8f89e481534183a904eb4 in C:\openjdk-25 
# Wed, 29 Jan 2025 00:31:45 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 29 Jan 2025 00:31:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c3ff2b1af8808ff84d19e034d7db3b7ecfd654d4b319b30c22a7ec68d15be1`  
		Last Modified: Wed, 29 Jan 2025 00:31:49 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693ba15766975b8a6ce824da321e420249dc3df005a37d3f6acf1b0372daec9d`  
		Last Modified: Wed, 29 Jan 2025 00:31:49 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c75b6640ac8fd009cfbb6b6995b70f76f08baf0fa173d890b3c31d93af9ba17`  
		Last Modified: Wed, 29 Jan 2025 00:31:48 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768ee2cb955d5e240fefd10bb1e6becfcc53afd1fad9b86e26195d523e85b7a2`  
		Last Modified: Wed, 29 Jan 2025 00:31:48 GMT  
		Size: 76.2 KB (76176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86a2e7893e0a27a8a3b22a056a0d8ee9248dafcbc85687386a3c5facb02f4f1`  
		Last Modified: Wed, 29 Jan 2025 00:31:48 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496a1cc66e1347f235cfede57eb741fecad2370e5f12974e91f72b4bc39b74bb`  
		Last Modified: Wed, 29 Jan 2025 00:31:48 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a77cad5bccc562b4c9b14583f51d76bf15462b6e52bcd17838f6e29f33120c0`  
		Last Modified: Wed, 29 Jan 2025 00:31:59 GMT  
		Size: 207.4 MB (207392624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfcfee32c3f0a5507357797e3d514ea208fc802a2eed9654e8d21317deada3e3`  
		Last Modified: Wed, 29 Jan 2025 00:31:48 GMT  
		Size: 104.2 KB (104154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49d743e5ff9ea2649aa4952fea0316fb333b139cf0abf8d6f38dfe6a330e332`  
		Last Modified: Wed, 29 Jan 2025 00:31:48 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-7-jdk-nanoserver` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:60f841409f81055954ccfc7c00ab2c8091a55ad7e74167749d6cce9210eb08f4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.2 MB (328245693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d881cfb17878dd9c8af4e28d334eccfa9aa6384ea7f916e3af22b53466fbff3d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Wed, 29 Jan 2025 00:27:39 GMT
SHELL [cmd /s /c]
# Wed, 29 Jan 2025 00:27:39 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 29 Jan 2025 00:27:40 GMT
USER ContainerAdministrator
# Wed, 29 Jan 2025 00:27:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 29 Jan 2025 00:27:58 GMT
USER ContainerUser
# Wed, 29 Jan 2025 00:27:59 GMT
ENV JAVA_VERSION=25-ea+7
# Wed, 29 Jan 2025 00:28:07 GMT
COPY dir:8eaf4d943fad5808ffdf3732eba720fc3864b955a0e8f89e481534183a904eb4 in C:\openjdk-25 
# Wed, 29 Jan 2025 00:28:12 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 29 Jan 2025 00:28:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d0cbd2f5c45b30ab534c67fa51d78fbdb1f9b2224fc39e14b1a3b179fc6fe1`  
		Last Modified: Wed, 29 Jan 2025 00:28:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2e88535d8fc3649cda90510f7d175dfa1ef7afec987e4d5c1aec913c2c74af`  
		Last Modified: Wed, 29 Jan 2025 00:28:16 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e16bf76154bdf25696cd33f6d25edb75d192e226e6b1a3ab426284364bb10e`  
		Last Modified: Wed, 29 Jan 2025 00:28:16 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9077432da026e834e5031e44b312b5962552b66eb0be4878cb3403f7bf35bab`  
		Last Modified: Wed, 29 Jan 2025 00:28:16 GMT  
		Size: 88.2 KB (88153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5715ed4e44985ad222ed284344204f573a3fd08d81ecc93d7e043db8a4737bc9`  
		Last Modified: Wed, 29 Jan 2025 00:28:15 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47560958a79222fe077868af453176cfb888c2e0152c9cf224cc461ec26ad6e`  
		Last Modified: Wed, 29 Jan 2025 00:28:15 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59d06e42d5bf81b13ec6c5051949bd862d0d91a1acf941790d7f86713e3966c`  
		Last Modified: Wed, 29 Jan 2025 00:28:26 GMT  
		Size: 207.4 MB (207391839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097fd667c97dac8579cce6c5c20a8ba44721246d2d36e48127ad15c81b71285f`  
		Last Modified: Wed, 29 Jan 2025 00:28:15 GMT  
		Size: 97.8 KB (97752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d151f1a0d1732ea10050eccc668504f0405517a30cee02b2022a9d1025277e`  
		Last Modified: Wed, 29 Jan 2025 00:28:15 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-7-jdk-nanoserver` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:8a2d9deb7058b9d74730ccdd8ecbc172aab786a419a797472155ba8ccb59a24a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.1 MB (367100234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d686867f0d25554729fff7b2bd3f4a1a2ff580d30a43ffc041b3c88f65878e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 29 Jan 2025 01:27:24 GMT
SHELL [cmd /s /c]
# Wed, 29 Jan 2025 01:27:25 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 29 Jan 2025 01:27:26 GMT
USER ContainerAdministrator
# Wed, 29 Jan 2025 01:27:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 29 Jan 2025 01:27:39 GMT
USER ContainerUser
# Wed, 29 Jan 2025 01:27:39 GMT
ENV JAVA_VERSION=25-ea+7
# Wed, 29 Jan 2025 01:27:49 GMT
COPY dir:8eaf4d943fad5808ffdf3732eba720fc3864b955a0e8f89e481534183a904eb4 in C:\openjdk-25 
# Wed, 29 Jan 2025 01:27:56 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 29 Jan 2025 01:27:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea67f5cdc1f2758c05b742b3e18a51efe2bb84d95020f59547470834df302c2`  
		Last Modified: Wed, 29 Jan 2025 01:28:03 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5937f73c9dd7e7eb0aa74ae847a39230006b8697b79a0f09a78698cdede31f7`  
		Last Modified: Wed, 29 Jan 2025 01:28:02 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f8853451649bf457a5f4f9043c782fdd7978834cf0d58090be6e5dac8fce11`  
		Last Modified: Wed, 29 Jan 2025 01:28:02 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45bc0e37a6c5e649bb725fb45bd7ecd7a9ab5a414b9970c174aef2b6683543c`  
		Last Modified: Wed, 29 Jan 2025 01:28:02 GMT  
		Size: 66.5 KB (66519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de981d3231be646cbb4cd007372432f5534c9c5a5948cecada4e1f088cffac3`  
		Last Modified: Wed, 29 Jan 2025 01:28:00 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0436519f0d5ec3a6f647f52718f47ed632aecbc02aa3c293b32463edea63f0c`  
		Last Modified: Wed, 29 Jan 2025 01:28:00 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ecae1a982edbfcd9cee7c3887b2ce1f678d08fb4132fb25e7bb49863bee5f4`  
		Last Modified: Wed, 29 Jan 2025 01:28:12 GMT  
		Size: 207.4 MB (207391618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022c92a76b53052181e80c34182885f10d9221b588ae1f624f89deb302dd8fdc`  
		Last Modified: Wed, 29 Jan 2025 01:28:01 GMT  
		Size: 4.4 MB (4368034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d63d72b7a2d42347486dbe865135ecde74dfba96ed50333208cfaa18e695fa`  
		Last Modified: Wed, 29 Jan 2025 01:28:00 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
