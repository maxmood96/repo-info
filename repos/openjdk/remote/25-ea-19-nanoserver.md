## `openjdk:25-ea-19-nanoserver`

```console
$ docker pull openjdk@sha256:0e252d10a8544b48bdacfb116680fda75380197938b1b0708f9fe6183d1b9e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `openjdk:25-ea-19-nanoserver` - windows version 10.0.26100.3781; amd64

```console
$ docker pull openjdk@sha256:f0089bc2f2b91a22d1657db551416c061952a35506ca1785a6e6fa8c15883d7b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.0 MB (398001132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8786dc0fb9925275c620843df5dc1ba9331be1e01886a7a80560e149588084`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Fri, 18 Apr 2025 19:13:25 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 19:13:26 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 18 Apr 2025 19:13:27 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 19:13:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 18 Apr 2025 19:13:30 GMT
USER ContainerUser
# Fri, 18 Apr 2025 19:13:31 GMT
ENV JAVA_VERSION=25-ea+19
# Fri, 18 Apr 2025 19:13:38 GMT
COPY dir:595a9046aeb360afc9a03339cfcb9f80b8fb3559c4a1bfb194a0956d7f6a1899 in C:\openjdk-25 
# Fri, 18 Apr 2025 19:13:46 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 18 Apr 2025 19:13:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 17 Apr 2025 02:52:17 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70cdbebaf49974106aaa6e14ba64219df10aee92d654984eca4bf6d04f54efa4`  
		Last Modified: Fri, 18 Apr 2025 19:13:53 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c4c1f089a47bca587005c935224357921ae601133738cc21d5dfef0f9cbfa5`  
		Last Modified: Fri, 18 Apr 2025 19:13:53 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18dad97aa81a7d82750b8d80df969378391dab1e7089f221abf2d794d803a37d`  
		Last Modified: Fri, 18 Apr 2025 19:13:53 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e163f320d21f2965653dc9eeb17790c53e55f96aea69f57cf02db83268c41e`  
		Last Modified: Fri, 18 Apr 2025 19:13:53 GMT  
		Size: 76.0 KB (76000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af57c8572c1a819cac1c451452122ea68c9f9db9dfa48a130fe79ecc94eed078`  
		Last Modified: Fri, 18 Apr 2025 19:13:51 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8326b399b507eaa182218a8e1237e5dccf75e1f277e1bb45f2513185d77fe64`  
		Last Modified: Fri, 18 Apr 2025 19:13:51 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9c849df021f526105a78f3ba71f4345906561fd3b42d2fe00b48832dcf5c9e`  
		Last Modified: Fri, 18 Apr 2025 19:14:03 GMT  
		Size: 207.7 MB (207662320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a500e7bbb31d65e970330c7ca1a9a87fe8a71ebc78d3ad7d5e6662468f4fde88`  
		Last Modified: Fri, 18 Apr 2025 19:13:51 GMT  
		Size: 114.5 KB (114486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9aae5121233c52e1a92b70b48a8c3eb5be0cb367c23350829b03f9a5df1492`  
		Last Modified: Fri, 18 Apr 2025 19:13:51 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-19-nanoserver` - windows version 10.0.20348.3566; amd64

```console
$ docker pull openjdk@sha256:cc2194d087e8d45cac684d470abc1c135b2af56fe43bf45eadde33c5fa5a82ad
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330392505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dabdc2b508c77be52c2f9a0cb62982d88471cfbc9145e2f194bb96111df1171`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Fri, 18 Apr 2025 19:15:39 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 19:15:40 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 18 Apr 2025 19:15:40 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 19:15:43 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 18 Apr 2025 19:15:43 GMT
USER ContainerUser
# Fri, 18 Apr 2025 19:15:44 GMT
ENV JAVA_VERSION=25-ea+19
# Fri, 18 Apr 2025 19:15:49 GMT
COPY dir:595a9046aeb360afc9a03339cfcb9f80b8fb3559c4a1bfb194a0956d7f6a1899 in C:\openjdk-25 
# Fri, 18 Apr 2025 19:15:56 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 18 Apr 2025 19:15:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Wed, 16 Apr 2025 23:30:29 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cdbef5435a340fb1d050ba5b0a3356c1518f343469934feac1c9d02da59771b`  
		Last Modified: Fri, 18 Apr 2025 19:16:01 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff61de1813c64920e820ae5460a370233054b727d5802a26fb9929e79305a838`  
		Last Modified: Fri, 18 Apr 2025 19:16:01 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ebf1dfca46f7e4517f42c261921bda04589effb49a65542ff0e77cd97940607`  
		Last Modified: Fri, 18 Apr 2025 19:16:01 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc7cc45c0126996a3e9b8d1d4f603b15ba3601142d12746bea8e9418f9127c9`  
		Last Modified: Fri, 18 Apr 2025 19:16:01 GMT  
		Size: 76.5 KB (76488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f3971570ac6d76a804f3248153fff257a562a6508c4fdb499d64a299366620`  
		Last Modified: Fri, 18 Apr 2025 19:15:59 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a399bee3edf4573bd6efef28192266f5e235d365cea713ae9d7f0f8ae99d33`  
		Last Modified: Fri, 18 Apr 2025 19:15:59 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214611d07602322b9b16c90671e9704ec48532a8230429c9a54a29e1d9e17ea5`  
		Last Modified: Fri, 18 Apr 2025 19:16:11 GMT  
		Size: 207.7 MB (207663846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70e2ef10acc6d0e0c27450cefc183234f4a3c37418d490ce371cabcf598cc9ee`  
		Last Modified: Fri, 18 Apr 2025 19:15:59 GMT  
		Size: 106.8 KB (106826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e67aae121f2ba10f6cc9250a0e29081984c92462433fb455b9e90ce7d59298e`  
		Last Modified: Fri, 18 Apr 2025 19:15:59 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-19-nanoserver` - windows version 10.0.17763.7249; amd64

```console
$ docker pull openjdk@sha256:29b24bcaeb181abcae645729afd80c23e1f646af8523e4978f20066b5375d733
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320869409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c55beb3840133bd7c57d213d6740ef5d43f5fb93cc73f2aa9bf7fbceb1c750b3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 19:17:51 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 19:17:54 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 18 Apr 2025 19:17:54 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 19:17:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 18 Apr 2025 19:17:57 GMT
USER ContainerUser
# Fri, 18 Apr 2025 19:17:58 GMT
ENV JAVA_VERSION=25-ea+19
# Fri, 18 Apr 2025 19:18:06 GMT
COPY dir:595a9046aeb360afc9a03339cfcb9f80b8fb3559c4a1bfb194a0956d7f6a1899 in C:\openjdk-25 
# Fri, 18 Apr 2025 19:18:11 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 18 Apr 2025 19:18:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2194e047ba19706a2edb4aa09f4bceefb6eb182e136c01eacb0218fc9b3e8431`  
		Last Modified: Fri, 18 Apr 2025 19:18:16 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea9286d32283cfdf9986cd94760448a280dfa03b66fbd6acabeacbb6803ad8f`  
		Last Modified: Fri, 18 Apr 2025 19:18:15 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238449a32813860e4417cded4e60b4e63a3888ace81bb64615180cfea0dbc876`  
		Last Modified: Fri, 18 Apr 2025 19:18:15 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71cb2a88ab624ca06f7ab21037d3c4efb0576580bd35cb5f02938163a005cfd7`  
		Last Modified: Fri, 18 Apr 2025 19:18:15 GMT  
		Size: 71.9 KB (71882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18be9c78d2197e03323d34272b4f5fe19144fc81c91b95a376764c72f6fa6dc7`  
		Last Modified: Fri, 18 Apr 2025 19:18:14 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a7686a23a37c4a39d6a580dd70f2483e4f65571419599d78bf6b1f09e38998`  
		Last Modified: Fri, 18 Apr 2025 19:18:14 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6021216e0333fb93b9c52831b8adbcf088d49d66b1fd1d511683096144d6c8`  
		Last Modified: Fri, 18 Apr 2025 19:18:25 GMT  
		Size: 207.7 MB (207663978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df93ab5b0769004c97508527dddd89c7757d892e76c640c3430672cb614b52e0`  
		Last Modified: Fri, 18 Apr 2025 19:18:15 GMT  
		Size: 4.4 MB (4375065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36640fe87809fa6f14d331dd2af82143811576c6382dcc757fca09ab66429665`  
		Last Modified: Fri, 18 Apr 2025 19:18:14 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
