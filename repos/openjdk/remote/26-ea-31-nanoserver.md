## `openjdk:26-ea-31-nanoserver`

```console
$ docker pull openjdk@sha256:236f5f174f8c318d8849b4c5a455eb2ba01a50f04f1d04e6c83281e1eb6f08a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `openjdk:26-ea-31-nanoserver` - windows version 10.0.26100.32230; amd64

```console
$ docker pull openjdk@sha256:6b179ae96ff08062698928b95c8b8c1cddd8eeeecaecedbc8127e8764caf36c0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.1 MB (423127250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0eb37cb7a7b4f0171e2e8ca8c5b7f4a773732677b2e699179246a6d7c28beb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Tue, 20 Jan 2026 19:10:09 GMT
SHELL [cmd /s /c]
# Tue, 20 Jan 2026 19:10:09 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 20 Jan 2026 19:10:10 GMT
USER ContainerAdministrator
# Tue, 20 Jan 2026 19:10:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 20 Jan 2026 19:10:20 GMT
USER ContainerUser
# Tue, 20 Jan 2026 19:10:20 GMT
ENV JAVA_VERSION=26-ea+31
# Tue, 20 Jan 2026 19:11:18 GMT
COPY dir:ec9bb409beef74e950058b5eef791a367e3ef6d6363328b2aa35d44ef81db5a9 in C:\openjdk-26 
# Tue, 20 Jan 2026 19:11:26 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 20 Jan 2026 19:11:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:10 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1e52cb3772a1ddfe29ce7740cf66ed5a11aa3227a97f57ee0521f3b8a4a418`  
		Last Modified: Tue, 20 Jan 2026 19:11:53 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015f9431d5ff5a8f6a766e5838a7911bce896db9f1642433559f369c9a2d2079`  
		Last Modified: Tue, 20 Jan 2026 19:11:53 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc105019ee96c88047fa0be65dbb041b3fb0561f81d9591763d2fbb51eaddb7`  
		Last Modified: Tue, 20 Jan 2026 19:11:33 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652cbe701fdbf710ea310c084d93af9faf26480260c184c0accbcd77b162aa7e`  
		Last Modified: Tue, 20 Jan 2026 19:11:33 GMT  
		Size: 70.5 KB (70533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e7bdb8acb7c81ab56c51211f77cb240be20d11b6ae630aaacb10a21b270047`  
		Last Modified: Tue, 20 Jan 2026 19:11:53 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db07e39962c241519503e898bdf1c72b225eb919e0123be80036e139405db5ae`  
		Last Modified: Tue, 20 Jan 2026 19:11:32 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc6c9ecdbf10eec4dc687f31a5e6c767c0a7c227d302e4af1ec086eca437d0e6`  
		Last Modified: Wed, 21 Jan 2026 00:00:03 GMT  
		Size: 223.8 MB (223849860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d33d9b6e238d8e75c7bbe92af4da16d8b8b707266207d84d6492b3bc2b0ee54`  
		Last Modified: Tue, 20 Jan 2026 19:11:53 GMT  
		Size: 123.8 KB (123841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b04cf74b9b363ed1a98e13cae8ff8cdede7e1803a2d2f5b3592266c81795bf`  
		Last Modified: Tue, 20 Jan 2026 19:11:32 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-ea-31-nanoserver` - windows version 10.0.20348.4648; amd64

```console
$ docker pull openjdk@sha256:88d4afa674a1b027645cd6a5e9ad7c486ce262f829f7b27dfa41826457880361
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.7 MB (350742461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35e36d0e6eb960bfdcc48fd563e83a6149f4ba7753567d56e20d4c90be0ea61`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Tue, 20 Jan 2026 19:10:14 GMT
SHELL [cmd /s /c]
# Tue, 20 Jan 2026 19:10:15 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 20 Jan 2026 19:10:15 GMT
USER ContainerAdministrator
# Tue, 20 Jan 2026 19:10:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 20 Jan 2026 19:10:26 GMT
USER ContainerUser
# Tue, 20 Jan 2026 19:10:27 GMT
ENV JAVA_VERSION=26-ea+31
# Tue, 20 Jan 2026 19:11:40 GMT
COPY dir:ec9bb409beef74e950058b5eef791a367e3ef6d6363328b2aa35d44ef81db5a9 in C:\openjdk-26 
# Tue, 20 Jan 2026 19:11:46 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 20 Jan 2026 19:11:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:547b256fb86179fa79eb0eed000a9b67f14b23ea94615d95a8c13eb1d607121c`  
		Last Modified: Tue, 20 Jan 2026 19:11:53 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db989393655e4591aeab368e85574614f61c8547c6efae330f6c016e98266cca`  
		Last Modified: Tue, 20 Jan 2026 19:11:53 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e3ca11c732d615ec6a9cc379898e73bd06570709e487d259bd26798f44e010`  
		Last Modified: Tue, 20 Jan 2026 23:06:01 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32df0a4b5efda3121cda5b2d585d531a5414ef71bab3fd571564375070ef9cca`  
		Last Modified: Tue, 20 Jan 2026 19:11:53 GMT  
		Size: 71.3 KB (71346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce57849c3da5f59796a718dd6da95ff3778115481991193998d77ec3c01e2419`  
		Last Modified: Tue, 20 Jan 2026 19:12:14 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c884b6da964ff3c09e9c930968ce3bc18ce193fe39dd00a7a7c947b34df90adf`  
		Last Modified: Tue, 20 Jan 2026 19:11:52 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb626ec572d1c22f45b516d22d9384f369b53e1ff5cf7279d61fdaaa9490ff7`  
		Last Modified: Tue, 20 Jan 2026 19:37:26 GMT  
		Size: 223.9 MB (223850007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51e6bf4e5ca36770345090e129c34f0dc248ea5198333c5f10503672518e6f7`  
		Last Modified: Wed, 21 Jan 2026 05:27:44 GMT  
		Size: 117.9 KB (117896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b5ca7e198b0aa03f89df560091d4fc690362d96b860a0ee3f161107631823e`  
		Last Modified: Tue, 20 Jan 2026 19:12:14 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
