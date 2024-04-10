## `eclipse-temurin:21-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:79acbe4e403f81e25978705308996d91c6cf1b2974a9bca2626e433a7a89e4df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `eclipse-temurin:21-jdk-nanoserver-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull eclipse-temurin@sha256:6d00ce447bfc1043a17afb413c6780bb259975ea64e760d62b6ac40813151b4c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.9 MB (309907178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e9f5e45a815bb6cd01af2ec2cb5a8823b1b58cd8e8c69ef440efaae50131e0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Tue, 09 Apr 2024 23:42:55 GMT
SHELL [cmd /s /c]
# Wed, 10 Apr 2024 00:17:23 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Wed, 10 Apr 2024 00:17:24 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 10 Apr 2024 00:17:25 GMT
USER ContainerAdministrator
# Wed, 10 Apr 2024 00:17:34 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Apr 2024 00:17:35 GMT
USER ContainerUser
# Wed, 10 Apr 2024 00:17:51 GMT
COPY dir:ef01cec12ba2d7ca328dd166c68dc318e8666a1382b059655285e6e080af62b8 in C:\openjdk-21 
# Wed, 10 Apr 2024 00:18:04 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Apr 2024 00:18:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b591b5f81c02344da39dc8a9084b5791cbf552c1eb85e79db1f38dfc715a681`  
		Last Modified: Wed, 10 Apr 2024 00:47:46 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ddf43d90d7015588c216ecb111faa62bf819c9a5b33036e42dbe52c611c33e`  
		Last Modified: Wed, 10 Apr 2024 00:55:47 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a082822ba6554f06b386d63402e14825e3efa82d395ee2ee265265a70a0234`  
		Last Modified: Wed, 10 Apr 2024 00:55:47 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c549ce38ec12395456a22d08ebb489fa4860023b0e462d21db3dcc34cb71ee3`  
		Last Modified: Wed, 10 Apr 2024 00:55:47 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9303a6a441578fe2c75bda55d5d4fe4fd8805b8c109173001f36b837356fde6f`  
		Last Modified: Wed, 10 Apr 2024 00:55:45 GMT  
		Size: 66.0 KB (66006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553884b6b95fb4c21a90cdb2cd929c28e8b59d021b59dfeb34d63cb1745ce3e4`  
		Last Modified: Wed, 10 Apr 2024 00:55:45 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618666b92f484271f812b942303892f2b2bbd84af4e28958c873f4166492feb3`  
		Last Modified: Wed, 10 Apr 2024 00:56:05 GMT  
		Size: 201.1 MB (201124872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f3340ea0817e5ad7ee70e934ea311f09be9cdd84f95b15f9a3f47e16ae2b7d`  
		Last Modified: Wed, 10 Apr 2024 00:55:46 GMT  
		Size: 3.8 MB (3820489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7508cae19619dce6dd02b2b0d94feeb268eae8da01e6555c5956aa4adb04c8`  
		Last Modified: Wed, 10 Apr 2024 00:55:45 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
