## `openjdk:28-ea-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:bd71f4ec4821fdb41079db599c3e2b5d2be4e8eb1de30bf430cbb43eda351f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `openjdk:28-ea-nanoserver-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull openjdk@sha256:ddb764e335bbf9a77a53ada5bb492d57d80b5a9916279bcbe632c858b0216f8f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.7 MB (347712195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56d373f3117cc7f85b78d8e3000c9bf4cbb12da498162a0f6845ad12ba2663d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Wed, 17 Jun 2026 00:09:00 GMT
SHELL [cmd /s /c]
# Wed, 17 Jun 2026 00:09:01 GMT
ENV JAVA_HOME=C:\openjdk-28
# Wed, 17 Jun 2026 00:09:01 GMT
USER ContainerAdministrator
# Wed, 17 Jun 2026 00:09:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 17 Jun 2026 00:09:08 GMT
USER ContainerUser
# Wed, 17 Jun 2026 00:09:08 GMT
ENV JAVA_VERSION=28-ea+2
# Wed, 17 Jun 2026 00:10:16 GMT
COPY dir:7a688c2845332d8c78625013fb7ea6948a575814777db81fbce8268792efb42f in C:\openjdk-28 
# Wed, 17 Jun 2026 00:10:21 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 17 Jun 2026 00:10:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de52ab6f0e221eac4e1abafbec1f68338a9808610258ab1e6e431e69fafa10c`  
		Last Modified: Wed, 17 Jun 2026 00:10:36 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302dadb9e7ef94ce348919c42c603fda54b2e80c3c10f7d0e9bd14107ce6d4c0`  
		Last Modified: Wed, 17 Jun 2026 00:10:36 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b60c92665861d170653a4e8ec25482a238176fafef13374ee27ff7d5dbf75fc`  
		Last Modified: Wed, 17 Jun 2026 00:10:36 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb20b392a3fd0cdbb215bd54c8dd7da0ab9336f18016a7a8dd7709c6798916c`  
		Last Modified: Wed, 17 Jun 2026 00:10:36 GMT  
		Size: 71.1 KB (71107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6ffb76840896de26bff9bba9647aac85530b9b1d3601fb23bb811d1adae3f6`  
		Last Modified: Wed, 17 Jun 2026 00:10:34 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95e685be809a94b88666879b9bd908610eeb70597c3812acfbd8e7f53cb9a91`  
		Last Modified: Wed, 17 Jun 2026 00:10:34 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c886ce20a58ca115b9acad0732f3dd049f19616ca34fe581f38ce82209aa6d`  
		Last Modified: Wed, 17 Jun 2026 00:10:50 GMT  
		Size: 223.5 MB (223540094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bab90ba1d53ebb57d0e7b1f78f920ca1427ddd06452ca834755ee4e87c0bf4`  
		Last Modified: Wed, 17 Jun 2026 00:10:34 GMT  
		Size: 97.1 KB (97089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3897877382c39c0cdb39af8846ffbdb41caaf925d30fd87a4c949cbba6818b24`  
		Last Modified: Wed, 17 Jun 2026 00:10:34 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
