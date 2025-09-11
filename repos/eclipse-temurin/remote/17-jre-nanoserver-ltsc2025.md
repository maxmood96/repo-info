## `eclipse-temurin:17-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:792554d401feefdfb736101ec4486f9363594906fa26e1c1ba10f6d47fb39c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull eclipse-temurin@sha256:a283a7d2e1c1d12667e297d6e2cf378bc034e5e2b848ae3a62dde7bba9e8f16a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237461497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac30b94eeef4ed95becd8d78e7ba5b8d66898500b82a05ca532ff57ea22a2f0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Sep 2025 02:12:39 GMT
RUN Apply image 10.0.26100.6584
# Wed, 10 Sep 2025 22:19:29 GMT
SHELL [cmd /s /c]
# Wed, 10 Sep 2025 22:19:30 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Wed, 10 Sep 2025 22:19:30 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 10 Sep 2025 22:19:31 GMT
USER ContainerAdministrator
# Wed, 10 Sep 2025 22:19:35 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Sep 2025 22:19:35 GMT
USER ContainerUser
# Wed, 10 Sep 2025 22:19:41 GMT
COPY dir:f06eb607ed2664f134ec9f1021e1b4f935a771c666407ab724ddde53439bca46 in C:\openjdk-17 
# Wed, 10 Sep 2025 22:19:44 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:a75a4ab04983f989d9a1442633d6c3952b863719a00dd77cf160f7055beaded9`  
		Last Modified: Tue, 09 Sep 2025 22:28:08 GMT  
		Size: 193.6 MB (193550846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:405e4f0a195de15bbe1dd36da41bdd9fe1bbc1c1080c2dcabfc4f6e553e3ba2c`  
		Last Modified: Wed, 10 Sep 2025 23:08:32 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abfd3b7e8531a3f7349312f2854862e45512f2887ddcbbc7c844761aedfeb6d0`  
		Last Modified: Wed, 10 Sep 2025 23:19:15 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e041afaff4d02967d21ca890caabfb7e86418a30bf783f9645b592967ec8aac9`  
		Last Modified: Wed, 10 Sep 2025 23:19:22 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59cca41d84a18e966999dff95bdcef0f5674398e7b17ee40070e8d4ef5a88201`  
		Last Modified: Wed, 10 Sep 2025 23:19:15 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d13c0a17f87f377cebd101baeb535c321d31a791fe498e70c69105e3e63e4cb`  
		Last Modified: Wed, 10 Sep 2025 23:19:16 GMT  
		Size: 72.1 KB (72097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ae5276b0d1da169a0778ec7a7f83b6ee58bb2f9387ee49987c63d442b612ac`  
		Last Modified: Wed, 10 Sep 2025 23:19:15 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97afac89374838130e3d03e5735ad188758f703d8c0f7cca715892d2e422531b`  
		Last Modified: Thu, 11 Sep 2025 00:15:09 GMT  
		Size: 43.7 MB (43748323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70cba9c78b157617a44420f16a037cc2eb21cc758b162a0ce6dcfcb83f73064`  
		Last Modified: Wed, 10 Sep 2025 23:19:14 GMT  
		Size: 84.8 KB (84769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
