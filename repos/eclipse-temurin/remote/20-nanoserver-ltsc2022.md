## `eclipse-temurin:20-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:bcf5ac4a67592d47e0ac15ea6601301d406e7b9f710b2d9161cc9db071f83e96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1970; amd64

### `eclipse-temurin:20-nanoserver-ltsc2022` - windows version 10.0.20348.1970; amd64

```console
$ docker pull eclipse-temurin@sha256:32b6f8aba7577a7641b75b782add59c85385945aa01608a1a58c382ecf695e66
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.2 MB (316181682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e836c836a6772d3201defe95273fb94668c0015a599f648aec4dbd3e387c3f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 01 Sep 2023 00:20:14 GMT
RUN Apply image 10.0.20348.1970
# Wed, 13 Sep 2023 03:28:54 GMT
SHELL [cmd /s /c]
# Wed, 13 Sep 2023 03:32:14 GMT
ENV JAVA_VERSION=jdk-20.0.2+9
# Wed, 13 Sep 2023 03:32:14 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 13 Sep 2023 03:32:15 GMT
USER ContainerAdministrator
# Wed, 13 Sep 2023 03:32:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Sep 2023 03:32:22 GMT
USER ContainerUser
# Wed, 13 Sep 2023 03:32:37 GMT
COPY dir:4ed074865171ba014f3c2f68f57ad2bb21a4dd6e4cf7ff9654ee6c4c6e5176c0 in C:\openjdk-20 
# Wed, 13 Sep 2023 03:32:46 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 Sep 2023 03:32:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8f8cef0759210af9d01a2fb45d79956a2db738bbd3734b7244b17e14ad945cab`  
		Last Modified: Tue, 12 Sep 2023 18:47:39 GMT  
		Size: 120.6 MB (120567584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d67aef4c483590cefd40495efc212f13e4c62993e8036c20bb4e19bc8620508`  
		Last Modified: Wed, 13 Sep 2023 03:47:03 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4634269db964b0398e0eee8857f6f9e741e0d77d9756b734e52fcd50cb90b109`  
		Last Modified: Wed, 13 Sep 2023 03:49:26 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9523788cf112297aadea5c11363b6dd4dcb812dfcd605fd7e1ceaefa16a2ff6f`  
		Last Modified: Wed, 13 Sep 2023 03:49:26 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a66cd8fbc017b1506f1c2ee6beb4e7138aa38afbb0714e051472ea5231e300`  
		Last Modified: Wed, 13 Sep 2023 03:49:26 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca8dcce37e91e33e93bbe27a72bc9a9ccbafc84566f773a38beb132df9d2d9c`  
		Last Modified: Wed, 13 Sep 2023 03:49:24 GMT  
		Size: 84.7 KB (84679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7648837fcd42ac620828b08d39b107704a68af2bbb97daa5752870a62a719690`  
		Last Modified: Wed, 13 Sep 2023 03:49:24 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1378a37cf8de2e2acdf36d8d834b04ed80a22e3874a44fd56891b3508aca837`  
		Last Modified: Wed, 13 Sep 2023 03:49:46 GMT  
		Size: 195.5 MB (195461190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966d03e58b4c2be28db99b0bb909be366ae7f167e052bf69ce947cb84a2acda7`  
		Last Modified: Wed, 13 Sep 2023 03:49:24 GMT  
		Size: 61.9 KB (61949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77328afcdd017fcd96ec5dc219a3d576d5f4de1f6dbf577d18bed405aaa43dbb`  
		Last Modified: Wed, 13 Sep 2023 03:49:24 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
