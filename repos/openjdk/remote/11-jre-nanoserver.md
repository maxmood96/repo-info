## `openjdk:11-jre-nanoserver`

```console
$ docker pull openjdk@sha256:aa1c1ae1bef44f1d08956d7eff574eba52979f6e7d1948ad7556bc0e4ec50962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `openjdk:11-jre-nanoserver` - windows version 10.0.17763.1697; amd64

```console
$ docker pull openjdk@sha256:02544ea792bb1436e72d1eedeb5c90a9db4127d25a3728e757ae7c283b1150fe
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.8 MB (140796471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2e7028671e5d0e51837c57fc6d2d96dfaedf2732b6fc2417e6e1c61b2990a5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 Jan 2021 16:14:35 GMT
RUN Apply image 1809-amd64
# Wed, 13 Jan 2021 19:56:48 GMT
SHELL [cmd /s /c]
# Wed, 13 Jan 2021 20:51:03 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 13 Jan 2021 20:51:04 GMT
USER ContainerAdministrator
# Wed, 13 Jan 2021 20:51:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 13 Jan 2021 20:51:15 GMT
USER ContainerUser
# Wed, 13 Jan 2021 20:51:16 GMT
ENV JAVA_VERSION=11.0.9.1
# Wed, 13 Jan 2021 20:55:37 GMT
COPY dir:eaef7c5ff292e1f8a6aa3c608a2a96aef7062e71406091a23afb53db379465e6 in C:\openjdk-11 
# Wed, 13 Jan 2021 20:55:54 GMT
RUN echo Verifying install ... 	&& echo   java --version && java --version
```

-	Layers:
	-	`sha256:62239e9aa1a352a20b0d4969c2b508b8a18d10e799d4db72e6f24ccbb2c724d9`  
		Size: 101.3 MB (101340070 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c2b6c001c337f812bceb3b03d15a70d1d9905540658e751e42f20f7cc0ddc819`  
		Last Modified: Wed, 13 Jan 2021 21:16:47 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b553c864f409e5717f62dc4d8f0c98ab040fde61a56bb67bc5f69369c4c3d678`  
		Last Modified: Wed, 13 Jan 2021 21:32:12 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee853c00bc1a5dfd384a03054775a857e8f9d6d91fac0b7ac6954b21e10a53f4`  
		Last Modified: Wed, 13 Jan 2021 21:32:13 GMT  
		Size: 872.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0268c0ff0fa23b9da72152c78ba36a3d101419ba8fc1e45858a7da706e7702`  
		Last Modified: Wed, 13 Jan 2021 21:32:13 GMT  
		Size: 64.8 KB (64850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4adfef67520b16c85296f1f172dfac38cf1b91a899815bb2e96457730969a2`  
		Last Modified: Wed, 13 Jan 2021 21:32:09 GMT  
		Size: 911.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fb16baaf68052e026c6204df6bcaaf7f38bc2318f25511cdb0052d28e02b91`  
		Last Modified: Wed, 13 Jan 2021 21:32:07 GMT  
		Size: 873.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3c4ced3ede35bc1491e0c4eefa4ddbff7d2ff6e9a47cbe3201e84f735daa04`  
		Last Modified: Wed, 13 Jan 2021 21:37:24 GMT  
		Size: 39.3 MB (39306740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584cb7ccae782ba2079ceae72edbec080b42d1c91ce6dfb93f80e052d865b54a`  
		Last Modified: Wed, 13 Jan 2021 21:37:16 GMT  
		Size: 80.4 KB (80391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
