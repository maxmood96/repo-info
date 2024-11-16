## `openjdk:24-ea-24-nanoserver-1809`

```console
$ docker pull openjdk@sha256:bb72c0c857671b7d0fc54bb4e32df98a5f6ab82327d059eb026db06db7581efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `openjdk:24-ea-24-nanoserver-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull openjdk@sha256:86863ada5cb2e972b584fc477ba5477a8426d09e41dc0d16259ac32a6e1824f2
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.4 MB (377351489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcce99d82b13de6f326397c2791c14ae80778735761acbb29147720457bec22f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Sat, 16 Nov 2024 00:04:16 GMT
SHELL [cmd /s /c]
# Sat, 16 Nov 2024 00:04:17 GMT
ENV JAVA_HOME=C:\openjdk-24
# Sat, 16 Nov 2024 00:04:18 GMT
USER ContainerAdministrator
# Sat, 16 Nov 2024 00:04:28 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 16 Nov 2024 00:04:29 GMT
USER ContainerUser
# Sat, 16 Nov 2024 00:04:29 GMT
ENV JAVA_VERSION=24-ea+24
# Sat, 16 Nov 2024 00:04:37 GMT
COPY dir:9ef0c32cf530fbfc56043e4de50ad443fb879b3d3204659d955b6d3bbab68fed in C:\openjdk-24 
# Sat, 16 Nov 2024 00:04:43 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 16 Nov 2024 00:04:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724dee79ab79a24321d215722579b0f3cede00ac2e71a8a30e596282e71eb075`  
		Last Modified: Sat, 16 Nov 2024 00:04:51 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3adea119c1788b85499eb740ac8b96dfaf06469bee9fce43de1bdece44b9c3a`  
		Last Modified: Sat, 16 Nov 2024 00:04:50 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86e9a75bd14a526b41c9323aad7d0fa03fdfbbfb573d0ac09646620a71fca75`  
		Last Modified: Sat, 16 Nov 2024 00:04:50 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8cedc4854a605899427aad4d71a5a0edb7b67080af603c63d6ed30482d3aa08`  
		Last Modified: Sat, 16 Nov 2024 00:04:50 GMT  
		Size: 66.5 KB (66506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815f8dbbf7f9ac0a5155a8942e1a0055c6d029d1d65891ecf3c940047e01994e`  
		Last Modified: Sat, 16 Nov 2024 00:04:48 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600e097c462c9af5d0ee1a10a02930df446a4caeef8b90fc3d7cb7d8fd01b696`  
		Last Modified: Sat, 16 Nov 2024 00:04:48 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39c0b723b870ccc1387b1383b79c13a6d2c7ae6ff004888cd53a6f03d5e6621`  
		Last Modified: Sat, 16 Nov 2024 00:05:01 GMT  
		Size: 217.6 MB (217626193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2a2cc1d59d995f99d3e8e4b97189906b3221e1662014097f41244db9b50ca5`  
		Last Modified: Sat, 16 Nov 2024 00:04:49 GMT  
		Size: 4.4 MB (4438294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e6f8134fafd149bd37c682764e4d84dcbc9869d205deffa42dcb0b7ebdbf08`  
		Last Modified: Sat, 16 Nov 2024 00:04:48 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
