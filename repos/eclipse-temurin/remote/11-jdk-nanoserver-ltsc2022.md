## `eclipse-temurin:11-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:433902ca4df8c527bbecd6564faa6df3f04db5279e18948aef719b526809e17f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:11-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull eclipse-temurin@sha256:53947c8661b140b9aa8194a618f657e3c408847f6d43dc334e996df0c2a0334d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.9 MB (321853871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a97afa094080f9963eb086a946a1d1591d07431f5aa3e623cf5ae230496c60`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 22:11:21 GMT
SHELL [cmd /s /c]
# Tue, 14 Apr 2026 22:11:22 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 14 Apr 2026 22:11:22 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 14 Apr 2026 22:11:24 GMT
USER ContainerAdministrator
# Tue, 14 Apr 2026 22:11:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Apr 2026 22:11:29 GMT
USER ContainerUser
# Tue, 14 Apr 2026 22:11:53 GMT
COPY dir:7dbbb550790b7446baaa5767cc14c2e1895a96b2462584273935c311b414f284 in C:\openjdk-11 
# Tue, 14 Apr 2026 22:11:57 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 14 Apr 2026 22:11:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfc801a8ca6a27b7b5a70e0d1ed65f8bb3a7c35240fe1b8451ac454ac800422`  
		Last Modified: Tue, 14 Apr 2026 22:12:04 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d995337c142783507f00492312bc2f5221589bde3914cb85218cb4bd1a730a17`  
		Last Modified: Tue, 14 Apr 2026 22:12:04 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c9f9ff04df89285aa771ff659108726fd35baf529621a6b8ca261edc304040`  
		Last Modified: Tue, 14 Apr 2026 22:12:04 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c52e52af0a5fd188ffc9720ecabda6c073be8a2b8c392cf83570672a76c38c`  
		Last Modified: Tue, 14 Apr 2026 22:12:04 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eeb7786f6cd4b3e49f99f22a9463c2dd033f7c7e3db0d171379dcd1ef1c81b1`  
		Last Modified: Tue, 14 Apr 2026 22:12:02 GMT  
		Size: 71.8 KB (71821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9815c107b112e93398da6c765ae5fd8fd65771a8714cd251bb1bbd36bd8304e1`  
		Last Modified: Tue, 14 Apr 2026 22:12:02 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761c14f9ea6d83d6e0092ae21fe59ad9ff800329fa7431cc76423adbc01bdbeb`  
		Last Modified: Tue, 14 Apr 2026 22:12:18 GMT  
		Size: 194.7 MB (194721888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae95a4088aa9a9a72cd0f0bf7433adf26334e4cfa4cae8746a139b7ea0488524`  
		Last Modified: Tue, 14 Apr 2026 22:12:02 GMT  
		Size: 97.8 KB (97842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc39bc97bf5eae6bef047c84b9feb86da416c47e41a3cb98d9591dcba763c2b`  
		Last Modified: Tue, 14 Apr 2026 22:12:02 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
