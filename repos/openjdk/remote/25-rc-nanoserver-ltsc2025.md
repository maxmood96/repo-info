## `openjdk:25-rc-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:6e557407d6b1ffb44258e88f6882fa663b32df5f03446bf28611085a5f5580ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `openjdk:25-rc-nanoserver-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull openjdk@sha256:8d5e43ed143f130c58c16371a269a703a91fb8ed2ed0f804419407a136efade1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.2 MB (412200508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0589617d7391a66eb67498d1364ece32ee136d777b5ed8384b56c6840fb27c47`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 Aug 2025 02:44:20 GMT
RUN Apply image 10.0.26100.4946
# Tue, 12 Aug 2025 20:50:55 GMT
SHELL [cmd /s /c]
# Tue, 12 Aug 2025 20:50:56 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 12 Aug 2025 20:50:56 GMT
USER ContainerAdministrator
# Tue, 12 Aug 2025 20:50:58 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 12 Aug 2025 20:50:58 GMT
USER ContainerUser
# Tue, 12 Aug 2025 20:50:59 GMT
ENV JAVA_VERSION=25
# Tue, 12 Aug 2025 20:51:06 GMT
COPY dir:7f4ebec9bbadc904e8c904a47d94c73f09fb6efdec5d25e1d0c69bce87e6d7e9 in C:\openjdk-25 
# Tue, 12 Aug 2025 20:51:09 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 12 Aug 2025 20:51:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6d63d98dae9e3419e8c965c24a11d30e40947cf35ee17c204c5d8b7bae7ff2ef`  
		Last Modified: Tue, 12 Aug 2025 21:13:38 GMT  
		Size: 193.5 MB (193469373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e82c2b88e814db5c82473c61f5282b4cf994aead6020abaafd1b428f9895624`  
		Last Modified: Tue, 12 Aug 2025 20:52:08 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9f3c2edcd379535662f4a23a326168e6d9af5f40f40dad1f91440ee42e390d`  
		Last Modified: Tue, 12 Aug 2025 20:52:09 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b36d73cdc3fa17dffb0fefabf28ca8ddad6f180a158c8ccb70a1b4ba7550cd6`  
		Last Modified: Tue, 12 Aug 2025 20:52:08 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3749905918e68a616147bd7e8461a6ccec8bc3442a3ea027e737f48e21e8db60`  
		Last Modified: Tue, 12 Aug 2025 20:52:09 GMT  
		Size: 75.8 KB (75759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916aaefce3bc9eb8fcc4d798672ff5334b0eafcc25c3ef4a0a4956daf43d5695`  
		Last Modified: Tue, 12 Aug 2025 20:52:08 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdcb7b24d8bf304a594107742ee64826d763b9cf0b857b968e8ddb7b4a167015`  
		Last Modified: Tue, 12 Aug 2025 20:52:09 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf6b940f4059d232517cace1f473089474bd30d0b14b25093811fd2234c2ab7`  
		Last Modified: Tue, 12 Aug 2025 21:24:05 GMT  
		Size: 218.5 MB (218535508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b0eefa49abcac6a2afbe0eff08db59397b6243a211c61d373c5b2babbac737`  
		Last Modified: Tue, 12 Aug 2025 20:52:12 GMT  
		Size: 113.5 KB (113469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7eebe41ac05f1f50e15a03b7374224c0663db27599d318f54f6a69217162aa`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
