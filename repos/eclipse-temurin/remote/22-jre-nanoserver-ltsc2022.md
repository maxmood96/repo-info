## `eclipse-temurin:22-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:072d559d14b68f69b766978aefb671a48848e2dbbc1fdaba84d5e5b2f5995fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `eclipse-temurin:22-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull eclipse-temurin@sha256:79e9d15c844891ad23a2f9f3105d999325bc5eae30548db1ae020857f95dea10
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169110074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb4abd432d07c02e0cc42c669e496208970729dfb459f6aed168fe30ed469121`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 09:30:07 GMT
RUN Apply image 10.0.20348.2582
# Wed, 10 Jul 2024 17:17:20 GMT
SHELL [cmd /s /c]
# Wed, 10 Jul 2024 17:21:50 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Wed, 10 Jul 2024 17:21:51 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 10 Jul 2024 17:21:51 GMT
USER ContainerAdministrator
# Wed, 10 Jul 2024 17:21:58 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jul 2024 17:21:59 GMT
USER ContainerUser
# Wed, 10 Jul 2024 17:22:34 GMT
COPY dir:b356dfbfb05ab2ab46133b6b7ad4e4cb6a7442df8599937d6806166f02780fa5 in C:\openjdk-22 
# Wed, 10 Jul 2024 17:22:43 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:652774a5d82a114642848f8b0b8d486ec1b4995f9dda56e36fe4ac7563429990`  
		Last Modified: Tue, 09 Jul 2024 20:33:26 GMT  
		Size: 120.5 MB (120490378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1dbb650483c31087741ccfe7cfef17abfd7465711d0851e35d39eabc775bdae`  
		Last Modified: Wed, 10 Jul 2024 17:38:52 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08ebf20fbe904b84fea17e450108b04546896985e66db0d560ed3313a33ebb2`  
		Last Modified: Wed, 10 Jul 2024 17:41:33 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:416088ac1d697c0b4e658ce2dc30fdb21af64e3c84979f927e4c93ec98aa3e58`  
		Last Modified: Wed, 10 Jul 2024 17:41:33 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d141c04cb4411ecd998a1e5987f3efcbc8f04e8edc0d86ce30687782ba331f2f`  
		Last Modified: Wed, 10 Jul 2024 17:41:33 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347c73ff61d51debebd0828530e77ae4ff83fbfeea37af628df6e09098f8f534`  
		Last Modified: Wed, 10 Jul 2024 17:41:31 GMT  
		Size: 78.1 KB (78123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d9ca92578119f567c5c41ba7fd0597e7306029a54a67fadb807eb7469e9b6b`  
		Last Modified: Wed, 10 Jul 2024 17:41:31 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c87ba8b2d1cedd9f2da01978e4b0141b14ef81681b8b0422fa536bb4176d08`  
		Last Modified: Wed, 10 Jul 2024 17:42:06 GMT  
		Size: 48.5 MB (48482588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad505602000ef9814645575b0b1403360e117859b9cbb88ed59243c5317dcc60`  
		Last Modified: Wed, 10 Jul 2024 17:41:59 GMT  
		Size: 53.3 KB (53283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
