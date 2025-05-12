## `openjdk:25-ea-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:6a1a2e5a5da2a0e1fa44fa92b4114bab5a9d534587a46a8100bfaf7cc1ea79dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `openjdk:25-ea-nanoserver-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull openjdk@sha256:b7d1593d040bdfea68536e012007c806000a677b7635a08c1cf5d461683c5663
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.1 MB (331094901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6afaf7ce75691bad6c5da3b27fb4fa6973512e6810f3adca35f0563f3bc055f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Mon, 12 May 2025 20:08:22 GMT
SHELL [cmd /s /c]
# Mon, 12 May 2025 20:08:23 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 12 May 2025 20:08:23 GMT
USER ContainerAdministrator
# Mon, 12 May 2025 20:08:40 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 12 May 2025 20:08:41 GMT
USER ContainerUser
# Mon, 12 May 2025 20:08:42 GMT
ENV JAVA_VERSION=25-ea+22
# Mon, 12 May 2025 20:08:53 GMT
COPY dir:d2aeeab016ce5cfb722c90fbb6527341de5d03dac18528814b93fc4084ba77f8 in C:\openjdk-25 
# Mon, 12 May 2025 20:08:58 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 12 May 2025 20:08:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Wed, 16 Apr 2025 23:30:29 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f2ab7e0b309d88827d7650e70e0a8e7d92cd53c3ddd8fa364e56c3bef1798d`  
		Last Modified: Mon, 12 May 2025 20:09:03 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87efe19cb99ceaed4a3fdff0d85a152dbe852d7a4fdcb622346bb41adc6b107`  
		Last Modified: Mon, 12 May 2025 20:09:03 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb173b316581ece714ff103541762a68d5cbd9997001bbc755afcd740fed375`  
		Last Modified: Mon, 12 May 2025 20:09:03 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebe43d3bd4d592bb28ff40859934995ea2158f87379d60dc79199b3757f3f01`  
		Last Modified: Mon, 12 May 2025 20:09:03 GMT  
		Size: 89.3 KB (89287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df1e1def0a516cae490f15447121d12df8a9557a34f3a8f90778979c35a9dfe`  
		Last Modified: Mon, 12 May 2025 20:09:02 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897a7ee4738176fc3de7207663be0cb1f8d708caefaa1ac6c6692e324be53e7f`  
		Last Modified: Mon, 12 May 2025 20:09:02 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1449133672ac0798e44bf0afa0bedb77584d6fbba269c512fa474ab3b88483c2`  
		Last Modified: Mon, 12 May 2025 20:09:13 GMT  
		Size: 208.4 MB (208366913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835b7106ade0d5ef37f3247108e5f33f2aa0d56830eedd6600bbe4d12b2346cd`  
		Last Modified: Mon, 12 May 2025 20:09:02 GMT  
		Size: 93.4 KB (93362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cff8973c7d772630ea562c43bd4f303f798427617d353df61cafdc861f84f1d`  
		Last Modified: Mon, 12 May 2025 20:09:02 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
