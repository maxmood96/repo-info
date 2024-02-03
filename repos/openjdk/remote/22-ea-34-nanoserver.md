## `openjdk:22-ea-34-nanoserver`

```console
$ docker pull openjdk@sha256:99c218b4f3e54585cb553c59d270a5c09f4bbc7be8e877f3344684462e51d064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `openjdk:22-ea-34-nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull openjdk@sha256:049e8d81dfed6cd9b3f12bb6a418f3d462bf95df8a641fbf0d3adee5b338010e
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305886011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e46401f5c3b7c21661fd0713c9c03dbeab9d6cebf9a7b130fbbd02c75e1e4a5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Fri, 02 Feb 2024 23:53:22 GMT
SHELL [cmd /s /c]
# Fri, 02 Feb 2024 23:53:24 GMT
ENV JAVA_HOME=C:\openjdk-22
# Fri, 02 Feb 2024 23:53:25 GMT
USER ContainerAdministrator
# Fri, 02 Feb 2024 23:53:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 02 Feb 2024 23:53:38 GMT
USER ContainerUser
# Fri, 02 Feb 2024 23:53:39 GMT
ENV JAVA_VERSION=22-ea+34
# Fri, 02 Feb 2024 23:53:47 GMT
COPY dir:7507700644c1de9ac912a15fc7989f655e799d7c1c035cf562aa0a88ab0dfd5b in C:\openjdk-22 
# Fri, 02 Feb 2024 23:53:54 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 02 Feb 2024 23:53:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a7feb9ef9af9b1b75ad00e91ed41e651860a1fff146e539b81e6cb9f10d2ce`  
		Last Modified: Fri, 02 Feb 2024 23:54:03 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c4d7d5687b1bd9e213475534a32c87acd18c13258a2a730c424800b87e3e7a`  
		Last Modified: Fri, 02 Feb 2024 23:54:02 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b82ad65ec0d8e32707e5ab5c88f2a638a1f024b6f763a8a8db977e108a01b03`  
		Last Modified: Fri, 02 Feb 2024 23:54:01 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672cde345e6181c800226da830ed76fd6385f6b80ec36070821f62911cdf6394`  
		Last Modified: Fri, 02 Feb 2024 23:54:01 GMT  
		Size: 67.7 KB (67728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d231787a562bbd73492ba458f8d3728c5b6e9446b04d0a774a59271ac59da45f`  
		Last Modified: Fri, 02 Feb 2024 23:53:59 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a0c35bcaa49f8e35062b6aa106e17891a7a1126fcfbd1823bd5376f8fa28ce`  
		Last Modified: Fri, 02 Feb 2024 23:53:59 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76e8aab56a3b17054a3f0413c00d112dda56f8ec20bbbb2678965f443bb7a07`  
		Last Modified: Fri, 02 Feb 2024 23:54:11 GMT  
		Size: 197.4 MB (197367554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545df351a6cd4e7b899440fca953cd1b739eda1436a9d3e3eaf91fb77fa4fdfb`  
		Last Modified: Fri, 02 Feb 2024 23:54:00 GMT  
		Size: 3.9 MB (3853268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c53553639ff1de516568d3619bd480e218945a7316b969cc394ad2d6bd99a0`  
		Last Modified: Fri, 02 Feb 2024 23:53:59 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
