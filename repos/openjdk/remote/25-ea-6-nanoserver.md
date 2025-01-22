## `openjdk:25-ea-6-nanoserver`

```console
$ docker pull openjdk@sha256:a7ff91dc67d19f58d7289e691d66bb81758c15fde40a3abf394fb199eea41899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `openjdk:25-ea-6-nanoserver` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:17dd0a32b83a724262f4373311dbc24c225b569470d6a45a2b9615f25bb5ffc8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.6 MB (406611738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c7de41f0bf9502a0397385e2c0145ba54b55d0acc53b9b16b92eef7e628391b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Wed, 22 Jan 2025 21:16:04 GMT
SHELL [cmd /s /c]
# Wed, 22 Jan 2025 21:16:05 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 22 Jan 2025 21:16:06 GMT
USER ContainerAdministrator
# Wed, 22 Jan 2025 21:16:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 22 Jan 2025 21:16:09 GMT
USER ContainerUser
# Wed, 22 Jan 2025 21:16:11 GMT
ENV JAVA_VERSION=25-ea+6
# Wed, 22 Jan 2025 21:16:17 GMT
COPY dir:f68a0a203262648eaad23f672eb21e06d231a686a9fcf56b24be2d2d46cfaae7 in C:\openjdk-25 
# Wed, 22 Jan 2025 21:16:24 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 22 Jan 2025 21:16:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303973f8fcab885da13334982934b6ca4e0619160524ec79d3bc8891b10231ce`  
		Last Modified: Wed, 22 Jan 2025 21:16:29 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f2fd8d1250b64b74238d0dc821ac217b4de5683a2c4076843ec5e0df78f90c`  
		Last Modified: Wed, 22 Jan 2025 21:16:29 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da07ddead9c467542de8075e9cbbcd5ecba2234e8456ef4dc9fddfada7a7beff`  
		Last Modified: Wed, 22 Jan 2025 21:16:29 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05faaa59235673c6e768cd2ffa206410feca9ba3b41f694c9a62d87afe1fa9b9`  
		Last Modified: Wed, 22 Jan 2025 21:16:29 GMT  
		Size: 76.6 KB (76553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3f233bc91a2b83dfb467aa5f80b25ebc9ec2942435c5eec9748ddd1f25632d`  
		Last Modified: Wed, 22 Jan 2025 21:16:28 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b3802163a4526513a38e0b2c97f6a1c1f926bcc167f53d403725e5549b321e`  
		Last Modified: Wed, 22 Jan 2025 21:16:28 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d634cb95715dd8088e7a9b02fafd93bdf705424857c9e6c95980333c5bcdd705`  
		Last Modified: Wed, 22 Jan 2025 21:16:39 GMT  
		Size: 207.4 MB (207370344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f52ed464df0ce5940d1395eebe83f9456eda847b692db035b399697b6ef8867`  
		Last Modified: Wed, 22 Jan 2025 21:16:28 GMT  
		Size: 104.1 KB (104127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112461794b1d0eae54bfad158d2bc7f7471e897e5be8dee305485f066c3df075`  
		Last Modified: Wed, 22 Jan 2025 21:16:28 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-6-nanoserver` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:45f58d1c84e26081cd4f71cf5cc441f5f400967ddfb0e569b03bae1db847e4a0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.2 MB (328222285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a740c8022ac4a2552fb3e44a37a29c739d75c973ba762be34c03eba08cb0491`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Wed, 22 Jan 2025 20:42:20 GMT
SHELL [cmd /s /c]
# Wed, 22 Jan 2025 20:42:21 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 22 Jan 2025 20:42:22 GMT
USER ContainerAdministrator
# Wed, 22 Jan 2025 20:42:24 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 22 Jan 2025 20:42:24 GMT
USER ContainerUser
# Wed, 22 Jan 2025 20:42:25 GMT
ENV JAVA_VERSION=25-ea+6
# Wed, 22 Jan 2025 20:42:32 GMT
COPY dir:f68a0a203262648eaad23f672eb21e06d231a686a9fcf56b24be2d2d46cfaae7 in C:\openjdk-25 
# Wed, 22 Jan 2025 20:42:38 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 22 Jan 2025 20:42:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5f876bd8a40865f3cc1f4967bceedd5e640dd7d99702609b05a1cc4edda97a`  
		Last Modified: Wed, 22 Jan 2025 20:42:45 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e789547d9f527fef787d89a7770370750451cd74f9345c9aed25b1d4b52f519`  
		Last Modified: Wed, 22 Jan 2025 20:42:44 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff384d45483ee1d9655631355b7797f8ad0c70895db634f92fdf5282506d2c0`  
		Last Modified: Wed, 22 Jan 2025 20:42:44 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e493838bd4e01c12dbe319512b8c770599084043513708f407c6f9bc736d47fd`  
		Last Modified: Wed, 22 Jan 2025 20:42:44 GMT  
		Size: 77.1 KB (77066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7f168ec1438cb46bb802ada4743bc90f0e2fb2fb320cc3d38d3d3413e96954`  
		Last Modified: Wed, 22 Jan 2025 20:42:42 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aec607aa499d782433512a2a984b62832206059005054a819ffb27a948741e`  
		Last Modified: Wed, 22 Jan 2025 20:42:42 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a118e1e12c5298497693fe99d942d9d099df91c08499e50521c3224ae0eeed1`  
		Last Modified: Wed, 22 Jan 2025 20:42:55 GMT  
		Size: 207.4 MB (207370104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:355d9693b817a66f4fd56aa3e638bd03eb94308367d5339417811ad0fd5c220e`  
		Last Modified: Wed, 22 Jan 2025 20:42:42 GMT  
		Size: 107.3 KB (107276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9131c67d3e2e17d7c5e95a4fd0b86d860f320da9004bede83f94fd51e10f8ad`  
		Last Modified: Wed, 22 Jan 2025 20:42:42 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-6-nanoserver` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:fc26d496e68bbea3d355543fea70fc425621309fdb18b602d2cce81ee59518bc
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.1 MB (367146450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623d21dbbd1e4856bd0ccb753c511b50606a40cbd015b9403ccdd9f96dbe1e85`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 22 Jan 2025 03:14:24 GMT
SHELL [cmd /s /c]
# Wed, 22 Jan 2025 03:14:25 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 22 Jan 2025 03:14:26 GMT
USER ContainerAdministrator
# Wed, 22 Jan 2025 03:14:28 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 22 Jan 2025 03:14:29 GMT
USER ContainerUser
# Wed, 22 Jan 2025 03:14:29 GMT
ENV JAVA_VERSION=25-ea+6
# Wed, 22 Jan 2025 03:14:37 GMT
COPY dir:f68a0a203262648eaad23f672eb21e06d231a686a9fcf56b24be2d2d46cfaae7 in C:\openjdk-25 
# Wed, 22 Jan 2025 03:14:42 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 22 Jan 2025 03:14:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0566d7b527e35b1fa8378f7c24b9f793edd5ac3da07896ee302358c44b263cf4`  
		Last Modified: Wed, 22 Jan 2025 03:14:48 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103ad165191df9a5c70055736022cf52cf2d78413b2ccbcad0d6186297880837`  
		Last Modified: Wed, 22 Jan 2025 03:14:47 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:422b7000764e810b4c0369601cb62e961e4f1dafe23fca59a6fc057474b5be9e`  
		Last Modified: Wed, 22 Jan 2025 03:14:47 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63ef1357477993bc9b94edc84e12b010ae66c79457fe2e6a8ec606659131d22`  
		Last Modified: Wed, 22 Jan 2025 03:14:47 GMT  
		Size: 76.1 KB (76124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9870cbfb6545d5c645772257535c30265f6bfec8810f77e9710df31d3ea7191d`  
		Last Modified: Wed, 22 Jan 2025 03:14:46 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e9689b3eb9f4d977a6883905b30466c435f0a472c693932f54434a702d04321`  
		Last Modified: Wed, 22 Jan 2025 03:14:46 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9078d28d1d9b4aa29d822d816e4de12ff293fc7e7365c2ffcd4e313241f873`  
		Last Modified: Wed, 22 Jan 2025 03:14:58 GMT  
		Size: 207.4 MB (207370320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4568b465a42fa362ce5b3a350346628306bd64e1be5b50db598f75e9f3f86da`  
		Last Modified: Wed, 22 Jan 2025 03:14:47 GMT  
		Size: 4.4 MB (4425888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aef8b17e3b39a61910c17414c04c2d8ff46b59891278fe0bd591154126bfb452`  
		Last Modified: Wed, 22 Jan 2025 03:14:46 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
