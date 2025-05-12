## `openjdk:25-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:e2411ac419788156726d5e77388ee96fd4f470e4e1db30c50d0daa0ae77d9237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `openjdk:25-jdk-nanoserver` - windows version 10.0.26100.3781; amd64

```console
$ docker pull openjdk@sha256:eb7c8215b3894a2eef99b9d29861a0a86fa5838310e9a6f1e449c838a8939fc5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.7 MB (398715878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce15741a25571dba8a487204f981ffea9ab6810d02a85e84703a09a73c7fe486`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Mon, 12 May 2025 20:14:24 GMT
SHELL [cmd /s /c]
# Mon, 12 May 2025 20:14:25 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 12 May 2025 20:14:26 GMT
USER ContainerAdministrator
# Mon, 12 May 2025 20:14:31 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 12 May 2025 20:14:32 GMT
USER ContainerUser
# Mon, 12 May 2025 20:14:33 GMT
ENV JAVA_VERSION=25-ea+22
# Mon, 12 May 2025 20:14:41 GMT
COPY dir:d2aeeab016ce5cfb722c90fbb6527341de5d03dac18528814b93fc4084ba77f8 in C:\openjdk-25 
# Mon, 12 May 2025 20:14:49 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 12 May 2025 20:14:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 17 Apr 2025 02:52:17 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa69cba76f2e76e6ea2f7fbc14d5c8749db1a4068cb2e0083d9e2eb3a2c6c402`  
		Last Modified: Mon, 12 May 2025 20:14:55 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2719773166b5d19a1173bfa522a49f34f7c294c866818cd18426082d9531e74b`  
		Last Modified: Mon, 12 May 2025 20:14:54 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f2d04c58919510454a32b0dcc98993ff1a5282a54bc6aaa12fbe5e21792e12`  
		Last Modified: Mon, 12 May 2025 20:14:54 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace9caea87efcc581055a12de97feb83f18915b83f4492f8f629219dcf4fcc15`  
		Last Modified: Mon, 12 May 2025 20:14:54 GMT  
		Size: 76.3 KB (76337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc4a509e8eb01590bb463ccccce8b9e9abc4424942b44686385832b26e245d7`  
		Last Modified: Mon, 12 May 2025 20:14:53 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e792ee4e77170efadbb84ceccd4fef37edd0f8389dc6343d855127a70eec115f`  
		Last Modified: Mon, 12 May 2025 20:14:53 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2cd6bbffb3dc880dd8b18be6945c3a133de647f4725a27ec4753dc10390a6ab`  
		Last Modified: Mon, 12 May 2025 20:15:05 GMT  
		Size: 208.4 MB (208366883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926b1301fdec750c43a61c4d012feea550182a0e468e5e81c99651e40e5a4b5c`  
		Last Modified: Mon, 12 May 2025 20:14:53 GMT  
		Size: 124.1 KB (124103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c54e8fda92be470437bf75b8fa283296cf4c314b101e19f3044d5a09bc1e33a`  
		Last Modified: Mon, 12 May 2025 20:14:54 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-jdk-nanoserver` - windows version 10.0.20348.3566; amd64

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

### `openjdk:25-jdk-nanoserver` - windows version 10.0.17763.7249; amd64

```console
$ docker pull openjdk@sha256:926b9585fca615eb2013e3a20e263744ad615f6839758abec130f47f33b3b983
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.6 MB (321587645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85fff3f245a29de2565ec20898a04125cb060e1af4dc093b7ceb7c23c9649b3c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Mon, 12 May 2025 20:08:47 GMT
SHELL [cmd /s /c]
# Mon, 12 May 2025 20:08:48 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 12 May 2025 20:08:49 GMT
USER ContainerAdministrator
# Mon, 12 May 2025 20:09:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 12 May 2025 20:09:08 GMT
USER ContainerUser
# Mon, 12 May 2025 20:09:08 GMT
ENV JAVA_VERSION=25-ea+22
# Mon, 12 May 2025 20:09:22 GMT
COPY dir:d2aeeab016ce5cfb722c90fbb6527341de5d03dac18528814b93fc4084ba77f8 in C:\openjdk-25 
# Mon, 12 May 2025 20:09:28 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 12 May 2025 20:09:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e964c72fb5be77163e031462fb094de88283b07d7b694a1e06e08577ef266c1a`  
		Last Modified: Mon, 12 May 2025 20:09:33 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e626c765b94ec57ed5f50b939f21ee2d0be3aa1adc540b1567ec3cd1024726f`  
		Last Modified: Mon, 12 May 2025 20:09:33 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17472dd1e6f52a08563f2cf262b3d6ed3c49f036cdb601b141e4842ae8db9fc`  
		Last Modified: Mon, 12 May 2025 20:09:33 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e142497424f839ea9c8c174c1e875d275ec0adea7aeca018df4891cdd7b87cf`  
		Last Modified: Mon, 12 May 2025 20:09:32 GMT  
		Size: 66.1 KB (66134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb0aa579060a21967ee8e77e0c4a7c1e5f70829cda8bd1d521dc943d9c8d56d`  
		Last Modified: Mon, 12 May 2025 20:09:31 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e32f2b0fc35797a070ccbbc6a305869237591334964315ce4294d1e87f83259a`  
		Last Modified: Mon, 12 May 2025 20:09:32 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73206b21d37a9fa0e78b3ca856735ce020bd60662a324497e253030731c2a0e7`  
		Last Modified: Mon, 12 May 2025 20:09:42 GMT  
		Size: 208.4 MB (208365658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730101272a379512d83bf33c8fe9f96ade95bcf3bcf196b1a499d79d200536f9`  
		Last Modified: Mon, 12 May 2025 20:09:32 GMT  
		Size: 4.4 MB (4397389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78165f53b601b351eeacb4d3416ac1eb64a0e5f61b39f0a10e7add1dcab737a4`  
		Last Modified: Mon, 12 May 2025 20:09:31 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
