## `openjdk:22-ea-33-nanoserver`

```console
$ docker pull openjdk@sha256:de6bf86e54a4660d39bb96d601ba30ea12fce255b41bd125d7be16bd369fc3da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `openjdk:22-ea-33-nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull openjdk@sha256:c80da07b753ca77ff71a364cc1ce0fbb389563fc0a1c31bc982eb2c7f23beaf1
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305866502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44fa1df77f3360b1eac7d4753fcbb496ebe0bdabc2d3f2af4900df70b50c34a2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Sat, 27 Jan 2024 00:53:43 GMT
SHELL [cmd /s /c]
# Sat, 27 Jan 2024 00:53:45 GMT
ENV JAVA_HOME=C:\openjdk-22
# Sat, 27 Jan 2024 00:53:47 GMT
USER ContainerAdministrator
# Sat, 27 Jan 2024 00:53:59 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 27 Jan 2024 00:54:00 GMT
USER ContainerUser
# Sat, 27 Jan 2024 00:54:01 GMT
ENV JAVA_VERSION=22-ea+33
# Sat, 27 Jan 2024 00:54:10 GMT
COPY dir:9f169993d8076343e1f77f6919bdd755ca6027bae3cc6b69bb406faa7b314b96 in C:\openjdk-22 
# Sat, 27 Jan 2024 00:54:16 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 27 Jan 2024 00:54:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0eaf9a16d5accb96d5724d6e13256c723e41146c7d6db8853dc9348abca714f`  
		Last Modified: Sat, 27 Jan 2024 00:54:26 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ea195b5fb0df9155453228d51790aeba49e78bd92ebb954b92d7105635a81b`  
		Last Modified: Sat, 27 Jan 2024 00:54:24 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f448940fddcc853704c8ee640c982b8b745d849eee3f4d368a41a39df949386`  
		Last Modified: Sat, 27 Jan 2024 00:54:24 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66b9bb2597a34b0382af1b077d6bcb5fb4d3296e551e035d08828f79d078ce0`  
		Last Modified: Sat, 27 Jan 2024 00:54:24 GMT  
		Size: 68.1 KB (68101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d19d9bc4abab6ab8ffbca82cf35dd711b0cb65fdd035ef8a518c6f1f7ceb492`  
		Last Modified: Sat, 27 Jan 2024 00:54:21 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55398cc7c59328f794938df8d2a95dfd39c3b0c702881259f6f7562fd6f0b88d`  
		Last Modified: Sat, 27 Jan 2024 00:54:21 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6662e193c92ae688ddf37270f75853485c020ca4a07dd88bd81b354e1694c4c3`  
		Last Modified: Sat, 27 Jan 2024 00:54:32 GMT  
		Size: 197.4 MB (197370470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87461f633a68a0090b846ccd0003444a85cf8a168f4eec746a3b21abcf5b7f59`  
		Last Modified: Sat, 27 Jan 2024 00:54:22 GMT  
		Size: 3.8 MB (3830471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa46738d2fc9e774f19d74697f27d129151f5a15aa9a1ea58ff1bd2c0e15454`  
		Last Modified: Sat, 27 Jan 2024 00:54:21 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
