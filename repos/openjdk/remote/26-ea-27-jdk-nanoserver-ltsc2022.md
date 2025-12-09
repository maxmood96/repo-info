## `openjdk:26-ea-27-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:953bdd9cc85bdc28c536c02734d33473120bb473b9e1c82de846f18f1092afd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `openjdk:26-ea-27-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull openjdk@sha256:03e3e96ad22a3b4b036b9e37b0f79820401b20314cc2c7c453a8be9cf9299892
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.7 MB (351724897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c051f232654b53061e30eb83fb35e7b6d2a5bf0c56cc9764a5442deb4c37f3c6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 09 Dec 2025 21:12:49 GMT
SHELL [cmd /s /c]
# Tue, 09 Dec 2025 21:16:08 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 09 Dec 2025 21:16:08 GMT
USER ContainerAdministrator
# Tue, 09 Dec 2025 21:16:10 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 09 Dec 2025 21:16:10 GMT
USER ContainerUser
# Tue, 09 Dec 2025 21:16:11 GMT
ENV JAVA_VERSION=26-ea+27
# Tue, 09 Dec 2025 21:16:19 GMT
COPY dir:babad47417a0162dfe31675fb569b90c77d833ec4f406c1de246f79f46496cd3 in C:\openjdk-26 
# Tue, 09 Dec 2025 21:16:25 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 09 Dec 2025 21:16:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39379f4668f7979dc09bdc5a0a70c7fe2057bbe447911ca76de5488139977d7`  
		Last Modified: Tue, 09 Dec 2025 21:13:27 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a09159775d71e6775a1f779f343a43cdea2a1bfc39049fa2b0e93f145eea02d`  
		Last Modified: Tue, 09 Dec 2025 21:16:54 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ff223f5db7133c511d518ff0d369337579d35818cd341552520f30389c2ccf`  
		Last Modified: Tue, 09 Dec 2025 21:16:55 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a30f18dedbf874e32b28c75e8334d1a971ed77424ff7f3afd9cd5af9c99e72b`  
		Last Modified: Tue, 09 Dec 2025 21:16:54 GMT  
		Size: 77.3 KB (77279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013b6a61dea8dd142bf6c5c500d1f429780303dce44786ad0f698dbac187bb30`  
		Last Modified: Tue, 09 Dec 2025 21:16:54 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10f549c03b14a0b031e2b0a7d2bb329823990168da854fa6448bf16d1df79ae`  
		Last Modified: Tue, 09 Dec 2025 21:16:54 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7630155f7a210731091d1dbee20437f9c82d6c85856b3af43b6a3f74f726ec`  
		Last Modified: Tue, 09 Dec 2025 21:17:04 GMT  
		Size: 225.2 MB (225175683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3ccc94df4e6f900868b1ec513a85ed41e45da54accf67e2e18cd68a758c218`  
		Last Modified: Tue, 09 Dec 2025 21:16:54 GMT  
		Size: 107.3 KB (107292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a15de56d8491f00caa8bc069f42b34cd4068152a2caf09a4d234d0857dade9`  
		Last Modified: Tue, 09 Dec 2025 21:16:54 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
