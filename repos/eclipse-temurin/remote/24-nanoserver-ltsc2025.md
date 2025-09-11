## `eclipse-temurin:24-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:a6de9ed2fcef188632efda27a770ebbcd2d7c4da3639754060f08b92f79498ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `eclipse-temurin:24-nanoserver-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull eclipse-temurin@sha256:8cb8b7d5329983c10160563faa50a3daa5722eb970691749050298f6ef5b4119
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.1 MB (331100258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ab267ce8ca9cb6fa42f33b240859850e622179ac4f0ee64d1d6c212ff265bb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Sep 2025 02:12:39 GMT
RUN Apply image 10.0.26100.6584
# Wed, 10 Sep 2025 22:19:45 GMT
SHELL [cmd /s /c]
# Wed, 10 Sep 2025 22:19:45 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Wed, 10 Sep 2025 22:19:46 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 10 Sep 2025 22:19:46 GMT
USER ContainerAdministrator
# Wed, 10 Sep 2025 22:19:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Sep 2025 22:19:52 GMT
USER ContainerUser
# Wed, 10 Sep 2025 22:20:04 GMT
COPY dir:f33586a1c43306f0f604ab16c8e427c967fb5f3c79695cbcabca361a95405189 in C:\openjdk-24 
# Wed, 10 Sep 2025 22:20:08 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Sep 2025 22:20:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a75a4ab04983f989d9a1442633d6c3952b863719a00dd77cf160f7055beaded9`  
		Last Modified: Tue, 09 Sep 2025 22:28:08 GMT  
		Size: 193.6 MB (193550846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52195b4a79779991d2790689d8603aef2a79616c7488122bce55cfe589c8c4a9`  
		Last Modified: Wed, 10 Sep 2025 22:20:56 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6106abb06350b900cb8060599e2d67f7a26d7735b47e562824fc31f12131d1cf`  
		Last Modified: Wed, 10 Sep 2025 22:20:56 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0ca1b4ac0aec88e27bf9239769db35a3e9d44dd9c8f0a49dfe6d3a7c02faf9`  
		Last Modified: Wed, 10 Sep 2025 22:20:57 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ec2193ed1a404b077e4c10c07b65fd430bec3775641289fa4e11ce5b25e1b1`  
		Last Modified: Wed, 10 Sep 2025 22:20:57 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918de4f7d5d763c459eab1c191611f0260c52186efadd319db4c84c71853ac95`  
		Last Modified: Wed, 10 Sep 2025 22:20:57 GMT  
		Size: 75.8 KB (75825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c79b5c97d255d62044526f69b534d60144671a6984a86a5b2963ee14262df68`  
		Last Modified: Wed, 10 Sep 2025 22:20:57 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb82324e1b62687b4233147193c0ed66c8101e9a9c2ff0bb91386f3fcd1ecd0`  
		Last Modified: Thu, 11 Sep 2025 00:18:26 GMT  
		Size: 137.4 MB (137383558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec0a6684ed3cc5cba8dbaeef379d38a89a36ad0981571704ea9abe57ce4f222`  
		Last Modified: Wed, 10 Sep 2025 22:20:57 GMT  
		Size: 83.6 KB (83636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b161e1a67eafc8564aa955b4831888b6bb9d11dd45ef48730d3e6af88d082bb`  
		Last Modified: Wed, 10 Sep 2025 22:20:57 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
