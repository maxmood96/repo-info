## `openjdk:25-ea-nanoserver`

```console
$ docker pull openjdk@sha256:24506f39586df7eca83f58a9598032bff7101df8d5bbea38f8289ce29b1ffe53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `openjdk:25-ea-nanoserver` - windows version 10.0.26100.2894; amd64

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

### `openjdk:25-ea-nanoserver` - windows version 10.0.20348.3207; amd64

```console
$ docker pull openjdk@sha256:d761616005afa03fab1617d7bb04a91f7507830a0c709fd66100bfe06923dbdc
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328361129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0f78c798792830aefd231790a286a634568426c26f5443d278530ac3e2d6ca`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 20:45:43 GMT
RUN Apply image 10.0.20348.3207
# Thu, 13 Feb 2025 01:18:20 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:18:21 GMT
ENV JAVA_HOME=C:\openjdk-25
# Thu, 13 Feb 2025 01:18:22 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:18:25 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 13 Feb 2025 01:18:25 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:18:26 GMT
ENV JAVA_VERSION=25-ea+9
# Thu, 13 Feb 2025 01:18:34 GMT
COPY dir:d7acfa7ae78317b124adc15f4373b266207aef9ee64c7b37ba0d0b39bb9389f0 in C:\openjdk-25 
# Thu, 13 Feb 2025 01:18:39 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 13 Feb 2025 01:18:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:938e4585b186fc3df3c1959d47ba7a634fea121cec7545db7923ceb191d99a33`  
		Last Modified: Tue, 11 Feb 2025 22:49:39 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ded16b24cbe888f5b94fb9cdee90efe89a6f8ba50ae3e689c97962a82b1fc35`  
		Last Modified: Thu, 13 Feb 2025 04:24:06 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0caf4cc603aab32900a2b432e17fd24a0d5263fdcead3fdfea1e767a06e0c3`  
		Last Modified: Thu, 13 Feb 2025 04:24:06 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc746471d97bbf8b341cb410fbb151ff426851c9b8e585305d5a9c0b1a94346`  
		Last Modified: Thu, 13 Feb 2025 04:24:06 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc7c607ba546ed30b6e366e2b1553aa18f9b95bd7d16ac4abaa2e47077304e4`  
		Last Modified: Thu, 13 Feb 2025 04:24:06 GMT  
		Size: 78.7 KB (78676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b1f4d25c5c3767495777d6c47104dc8a151d04d4ca0aa3776a306d07614399`  
		Last Modified: Thu, 13 Feb 2025 04:24:06 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee167e8f0b7b150cf8d97f1a2aecc73c1e12145b03803c9ef2423ede084e944`  
		Last Modified: Thu, 13 Feb 2025 04:24:07 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc29fde919b08a8213849d7d25191c2cbd1067311b1b0b52f495e2350af374b`  
		Last Modified: Thu, 13 Feb 2025 04:24:18 GMT  
		Size: 207.5 MB (207491611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3a4c0a49c05a84694f01e21fdfcc84b8e4ffae5c575afb4470025b89c3bd63`  
		Last Modified: Thu, 13 Feb 2025 04:24:07 GMT  
		Size: 118.0 KB (118042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95cbf379b2560231ff47db9be22a2a1750f549e7cc84ecd6ae0bb2a65721f29c`  
		Last Modified: Thu, 13 Feb 2025 04:24:07 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-nanoserver` - windows version 10.0.17763.6893; amd64

```console
$ docker pull openjdk@sha256:199e70742777497f982da71f50bb112a0a74f18dae94611f6ad5112302c279dd
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.9 MB (318910803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7476a504d2d8eb605c73897878da0c1fe5633a4925d2247e67b4ce0d2cee8e5b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:18:39 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:18:41 GMT
ENV JAVA_HOME=C:\openjdk-25
# Thu, 13 Feb 2025 01:18:42 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:18:44 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 13 Feb 2025 01:18:45 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:18:46 GMT
ENV JAVA_VERSION=25-ea+9
# Thu, 13 Feb 2025 01:18:53 GMT
COPY dir:d7acfa7ae78317b124adc15f4373b266207aef9ee64c7b37ba0d0b39bb9389f0 in C:\openjdk-25 
# Thu, 13 Feb 2025 01:18:59 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 13 Feb 2025 01:18:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Wed, 12 Feb 2025 21:38:54 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde751c4bc53b6c604b5c8a99be5897187126d9e793ae873e57ee25fbf7eb519`  
		Last Modified: Thu, 13 Feb 2025 04:24:10 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91205a8bdb894e0e58e1d0b036d4991b214aef422a3303ed05c70f8ce76d2497`  
		Last Modified: Thu, 13 Feb 2025 04:24:10 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e96511b9b02efbbae1dcbd361681213436e54fe19463647e53a29225319f68`  
		Last Modified: Thu, 13 Feb 2025 04:24:10 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc9724db27288929ffe00fba733a5efde62eb4a214e7e35df99cea26c958111`  
		Last Modified: Thu, 13 Feb 2025 04:24:10 GMT  
		Size: 80.0 KB (80036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ac56568fc42802a538facfd762a3ecc719d6d8d820299e81bba715c77a0b96`  
		Last Modified: Thu, 13 Feb 2025 04:24:10 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a561e6b74538464c5ec9b6f01cc375b65c00df3ef569d69fdddc44e17abc2bad`  
		Last Modified: Thu, 13 Feb 2025 04:24:10 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6145d4c146b68baf20bf50e2f84817c912e061e986b494d0fe4cfc5882055a`  
		Last Modified: Thu, 13 Feb 2025 04:24:28 GMT  
		Size: 207.5 MB (207491688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3efa93d1f6b21fddd6955ae38f3c18e1f7802bc7f136c51940e160342e7a98e5`  
		Last Modified: Thu, 13 Feb 2025 04:24:10 GMT  
		Size: 4.4 MB (4417374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a9587f6560d67a2a7d0c5aac0ddf81b03f86ee14e9f10b5e178be9148c7976`  
		Last Modified: Thu, 13 Feb 2025 04:24:10 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
