## `openjdk:25-nanoserver`

```console
$ docker pull openjdk@sha256:207bfb4bfa74523349e06ae94d8f5bbb26b446d8b5040919c49c879e18926778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `openjdk:25-nanoserver` - windows version 10.0.17763.6775; amd64

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
