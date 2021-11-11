## `openjdk:18-nanoserver-1809`

```console
$ docker pull openjdk@sha256:6fb352605241063a7689cf99b1bc78fd5efaeab751e3a71c6f7d3012216b7f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `openjdk:18-nanoserver-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull openjdk@sha256:ec025d27caa59ea3603b6ff8e089dd88c2f7a26a69856dfc62c082c78b3c4969
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290017954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43881b592fbb5488ef2a1826031065b0507eaec5c09a746850b1813bc23ea083`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:13:20 GMT
SHELL [cmd /s /c]
# Wed, 10 Nov 2021 20:31:55 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 10 Nov 2021 20:31:55 GMT
USER ContainerAdministrator
# Wed, 10 Nov 2021 20:32:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 Nov 2021 20:32:07 GMT
USER ContainerUser
# Thu, 11 Nov 2021 02:26:55 GMT
ENV JAVA_VERSION=18-ea+22
# Thu, 11 Nov 2021 02:27:10 GMT
COPY dir:8d6a03ecb43a50e96e1ea8050215c3463f1cd25f09c6c66b339295cfb108fd47 in C:\openjdk-18 
# Thu, 11 Nov 2021 02:27:24 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 11 Nov 2021 02:27:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b9dc943b4e8df8f472d444248152fa0920172ec630a60ada316e1603600dd1c7`  
		Size: 102.8 MB (102782944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e60ec86b90e1492e0e0ed2cbebcf624990a34862e24207343fd85b84b3544c8e`  
		Last Modified: Wed, 10 Nov 2021 18:01:59 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d97d878bac5dd9dcbe1bb5f45ade2111fc77e8d4a5a348163bd9c3ddddbaf0`  
		Last Modified: Wed, 10 Nov 2021 21:11:37 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5a46fd95d3a8e8b5949c49cc0d70b858bddbe38c8c33e0a6a3e0f157d7795a`  
		Last Modified: Wed, 10 Nov 2021 21:11:37 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88539ad3f1fb0ea6957da9a7298c1f6546afbb52b2deb7199763195fca993d98`  
		Last Modified: Wed, 10 Nov 2021 21:11:37 GMT  
		Size: 74.2 KB (74205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d133fe2173015750539b2d0a8fb86dbdbe0c6b44c8d75ddeb714a82814f98e00`  
		Last Modified: Wed, 10 Nov 2021 21:11:33 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f70cd085588ca56ede8ce99b00cd84e76e989217138f8d5d545c068b4b03aa`  
		Last Modified: Thu, 11 Nov 2021 02:39:59 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a789c500a3d522aa9e0f7a275070ae5fda6f2c4a6aa83fda57c1c3f433f19cc`  
		Last Modified: Thu, 11 Nov 2021 02:40:20 GMT  
		Size: 183.6 MB (183609790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26200be72d5e7969ea70fcb1e295e3833109ddf22ef6008b07d81e5d5ee8b2db`  
		Last Modified: Thu, 11 Nov 2021 02:40:03 GMT  
		Size: 3.5 MB (3544102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ba4ebf7124214086dba305e9d9525a45618109821d8d9ef384507222eb24ec`  
		Last Modified: Thu, 11 Nov 2021 02:39:59 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
