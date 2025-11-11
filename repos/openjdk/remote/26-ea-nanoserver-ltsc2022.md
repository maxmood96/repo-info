## `openjdk:26-ea-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:d560dd42da4a42ea43d089cd9b1b47d612d77e54d64a4d522ed5d42067baaa7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `openjdk:26-ea-nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull openjdk@sha256:fac1052655146df7f6affba40acf61a052e78094e2aa71e73246104a9b5fcd15
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.2 MB (344233686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15889fa9f785edc9da77fe88998ce3dd737de1515515ca7723ce902f6c2d332`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Mon, 10 Nov 2025 20:00:51 GMT
SHELL [cmd /s /c]
# Mon, 10 Nov 2025 20:00:52 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 10 Nov 2025 20:00:52 GMT
USER ContainerAdministrator
# Mon, 10 Nov 2025 20:00:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 10 Nov 2025 20:00:57 GMT
USER ContainerUser
# Mon, 10 Nov 2025 20:00:58 GMT
ENV JAVA_VERSION=26-ea+23
# Mon, 10 Nov 2025 20:01:39 GMT
COPY dir:caac7c3daf5c418f731b855ae37dd48a49eef4e9ccf593b019be40c369c65420 in C:\openjdk-26 
# Mon, 10 Nov 2025 20:01:44 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 10 Nov 2025 20:01:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d7b72c7ca7071ab88ddc43f73d9f99f0c9e7693b4e28cb84e76cb96bb8d877`  
		Last Modified: Mon, 10 Nov 2025 20:02:13 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6022505b4da15d63f55793f96b86297befe5d8483ac786c7b4f4fecd0aa93d8`  
		Last Modified: Mon, 10 Nov 2025 20:02:13 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53025c75ad8967cc43980ac5072f75fa8fb373bcf763369f7296699917b561f9`  
		Last Modified: Mon, 10 Nov 2025 20:02:14 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae09868ad588f593164166b2ab9f99517bb028a600bd4240151ffd16e804445`  
		Last Modified: Mon, 10 Nov 2025 20:02:14 GMT  
		Size: 70.5 KB (70501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86853ff5fdee5e1972b520287c1f494db5470d12c8381d7b22a588e6722bff9c`  
		Last Modified: Mon, 10 Nov 2025 20:02:14 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cff97f9a07bc1b13a83e42568c262e511290039ac53df6e166c71ca2fb1057c`  
		Last Modified: Mon, 10 Nov 2025 20:02:14 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9200dbf1e5937b00ef9b179714f17382a14692739c83775f439575ddf4c63569`  
		Last Modified: Mon, 10 Nov 2025 22:24:58 GMT  
		Size: 221.3 MB (221317947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e5d564efc823da9f53cbde0104ff7f39f01e4cbd9def4f39204f3ccec84fdb`  
		Last Modified: Mon, 10 Nov 2025 20:02:15 GMT  
		Size: 154.8 KB (154780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:919908cb172bb1cdee745f931b484fad42c07e8adab50fb08bf1a48c2be2e55e`  
		Last Modified: Mon, 10 Nov 2025 20:02:15 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
