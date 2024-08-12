## `openjdk:23-rc-nanoserver-1809`

```console
$ docker pull openjdk@sha256:81bf1dfb4854d81a8d4ef4825c58dae0f30d089f6f3124dbc32cfa5a34b8a984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `openjdk:23-rc-nanoserver-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull openjdk@sha256:98c8bd6b0d799cd28f45281b7634c4de1ddd6bdc7eb45ac21737d221cd9a88b3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.3 MB (365285997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae23c19e97b15b5b75f7a9ffefe95f6e4b6d6a09c2e7d36a66477a2b708a120`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Mon, 12 Aug 2024 18:54:18 GMT
SHELL [cmd /s /c]
# Mon, 12 Aug 2024 18:54:20 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 12 Aug 2024 18:54:20 GMT
USER ContainerAdministrator
# Mon, 12 Aug 2024 18:54:33 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 12 Aug 2024 18:54:34 GMT
USER ContainerUser
# Mon, 12 Aug 2024 18:54:34 GMT
ENV JAVA_VERSION=23
# Mon, 12 Aug 2024 18:54:43 GMT
COPY dir:7f285cee4711ed5c5f7c87b2783489a3640a2db87c0fcb661fcbc1197c78fec4 in C:\openjdk-23 
# Mon, 12 Aug 2024 18:54:49 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 12 Aug 2024 18:54:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168894d37c616218debc59e47f474c1f74a649f9facb57f0082e8e928b1ca330`  
		Last Modified: Mon, 12 Aug 2024 18:54:53 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bb7a6e8988e6fec4b93b1aab9295f4f0f487a31973c3a888fdc96907796d55`  
		Last Modified: Mon, 12 Aug 2024 18:54:53 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e759e2e3983eb714833261893a5188659316a4cf29882c0dbb93222900f83213`  
		Last Modified: Mon, 12 Aug 2024 18:54:53 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a49f7854a4df23c075cf458d9e9ed6483c042dc3eb888161279783a333ca6a`  
		Last Modified: Mon, 12 Aug 2024 18:54:52 GMT  
		Size: 66.3 KB (66265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f675949421c261fae49ff6e8954c5a49a9e8ad6bb591fa08cfc07fe5db82f5`  
		Last Modified: Mon, 12 Aug 2024 18:54:52 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef440a19df02c10869993081275c7270470f5108d6cba548f1f2cac36983309f`  
		Last Modified: Mon, 12 Aug 2024 18:54:52 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05674eca64f234fb7f9ca3cf5587cd59a53994eb93ca255695b940a717b2d0d`  
		Last Modified: Mon, 12 Aug 2024 18:55:07 GMT  
		Size: 206.0 MB (206042445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5217a5460f294375a31d260ca1056fda0fe8d2856807a8176fa6c48b4be6dbbc`  
		Last Modified: Mon, 12 Aug 2024 18:54:52 GMT  
		Size: 4.1 MB (4089602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72cd08b98c8b4f910dd72e95c808072fbb1b53467da8d3a2fce8927ee87399d2`  
		Last Modified: Mon, 12 Aug 2024 18:54:52 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
