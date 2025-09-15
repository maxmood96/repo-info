## `openjdk:26-ea-15-nanoserver`

```console
$ docker pull openjdk@sha256:870d2cee39d3ee1ac0cd16b5c6529cd921aacbdf134e773a8fbf98117389658a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `openjdk:26-ea-15-nanoserver` - windows version 10.0.26100.6584; amd64

```console
$ docker pull openjdk@sha256:20739a50200a68ba54d21e4b2946262335a12f3759b6a161d37fefdc390e325c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.6 MB (412612624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b4d67b2696b3522bdcc83784320824b00f02c693e885291e985ded33a6f32b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Sep 2025 02:12:39 GMT
RUN Apply image 10.0.26100.6584
# Mon, 15 Sep 2025 18:06:09 GMT
SHELL [cmd /s /c]
# Mon, 15 Sep 2025 18:06:11 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 15 Sep 2025 18:06:12 GMT
USER ContainerAdministrator
# Mon, 15 Sep 2025 18:06:25 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 15 Sep 2025 18:06:25 GMT
USER ContainerUser
# Mon, 15 Sep 2025 18:06:26 GMT
ENV JAVA_VERSION=26-ea+15
# Mon, 15 Sep 2025 18:06:47 GMT
COPY dir:609b8c1ea17fd4b2dc32204a5b54838c1e6ca5dcaab5222bbde3be71315dfdc8 in C:\openjdk-26 
# Mon, 15 Sep 2025 18:06:56 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 15 Sep 2025 18:06:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a75a4ab04983f989d9a1442633d6c3952b863719a00dd77cf160f7055beaded9`  
		Last Modified: Tue, 09 Sep 2025 22:28:08 GMT  
		Size: 193.6 MB (193550846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9d06a1ed4ffae5ba1ce15c2aa6c91291a5d916163ac52eb3e5868950dc83a3`  
		Last Modified: Mon, 15 Sep 2025 18:08:35 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9679db6a2b5f5379dfa67ca06bbe077eb074d712472024ffb3b95c8ef35e49`  
		Last Modified: Mon, 15 Sep 2025 18:08:35 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24e7d6c9e3058f6ee558bef694c9ff5ad3b0819c71f5895dc11b04492e08642`  
		Last Modified: Mon, 15 Sep 2025 18:08:35 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7269bd98ba160eb8c6cedbe8f9017e19c1ac271c8c13208e1bbde98b2adcea`  
		Last Modified: Mon, 15 Sep 2025 18:08:35 GMT  
		Size: 74.3 KB (74336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63abb48b2fe6ead8d1236203eb8c6f7031f948eea40bb34886ecbb1ac75c90f9`  
		Last Modified: Mon, 15 Sep 2025 18:08:35 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbacf99c4e2fdcc41c113036ad2ac9d1d087b0e908bdf0e7da1e017d528b498`  
		Last Modified: Mon, 15 Sep 2025 18:08:35 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd4df782d68f9aa055d67cb61745c3651c064e2ee4bb5bd2490b34aa9db2b89`  
		Last Modified: Mon, 15 Sep 2025 21:25:06 GMT  
		Size: 218.9 MB (218877977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1913f0b7a6c5fa5d242443db10a0e7edd990922b7796649a2510d058bc2646`  
		Last Modified: Mon, 15 Sep 2025 18:08:35 GMT  
		Size: 103.0 KB (102977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5dfb42e86567e79f66c35d891a00bcb63aef094a264c5fe37bcb9459e0843f4`  
		Last Modified: Mon, 15 Sep 2025 18:08:35 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-ea-15-nanoserver` - windows version 10.0.20348.4171; amd64

```console
$ docker pull openjdk@sha256:0d8cab7b7fe62f3caafea51ae3d0fe6c88c2946253abf43b4dcf73c649de6f99
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.8 MB (341783719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b22200f33c44a7c98b23b5eec676e4ea34d026bf8ca8df8b6c8eca926333d77d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Mon, 15 Sep 2025 18:02:10 GMT
SHELL [cmd /s /c]
# Mon, 15 Sep 2025 18:02:11 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 15 Sep 2025 18:02:12 GMT
USER ContainerAdministrator
# Mon, 15 Sep 2025 18:02:25 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 15 Sep 2025 18:02:25 GMT
USER ContainerUser
# Mon, 15 Sep 2025 18:02:26 GMT
ENV JAVA_VERSION=26-ea+15
# Mon, 15 Sep 2025 18:03:14 GMT
COPY dir:609b8c1ea17fd4b2dc32204a5b54838c1e6ca5dcaab5222bbde3be71315dfdc8 in C:\openjdk-26 
# Mon, 15 Sep 2025 18:03:20 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 15 Sep 2025 18:03:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa5cbea6b5da592c29269d73b7c5ebb48fdbb8bcc1220fcaeba9ec1d7acaa04`  
		Last Modified: Mon, 15 Sep 2025 18:04:45 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c5645e115e9a787dd134f5d30c8d9e43a9ab47e4bd87d671840019b2cda612`  
		Last Modified: Mon, 15 Sep 2025 18:04:45 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd6aabb27d0c953173dec2ce23ff8ebf1b226bfb60a6cffbfe051309c42cbb7`  
		Last Modified: Mon, 15 Sep 2025 18:04:45 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637872356acf9036310c3905af3b5231fa9cee7b21518d84ad421b039dcca3fc`  
		Last Modified: Mon, 15 Sep 2025 18:04:46 GMT  
		Size: 86.9 KB (86857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059b1119b9b759bbc810a95539c57d994952e45da7a19864195ddb0fb00b799b`  
		Last Modified: Mon, 15 Sep 2025 18:04:46 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd085646b18d6eb04a18006a6e888e6ad181cdc93e774c83894f8c7d8dc5992b`  
		Last Modified: Mon, 15 Sep 2025 18:04:46 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9512c187f8af8a90cc7767e620d7244a8946cafa53a17ad45a138c7008f03aef`  
		Last Modified: Mon, 15 Sep 2025 18:24:53 GMT  
		Size: 218.9 MB (218877863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5583d730efad93de66ef58dece7766d508ecd3af2322bbca9b5bdb9813914e`  
		Last Modified: Mon, 15 Sep 2025 18:04:46 GMT  
		Size: 92.7 KB (92658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b45e9e061de99ff504d25f81ccd5ad403206738095c8748685c444d3699c7a4`  
		Last Modified: Mon, 15 Sep 2025 18:04:46 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
