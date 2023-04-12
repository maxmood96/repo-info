## `openjdk:21-nanoserver`

```console
$ docker pull openjdk@sha256:c39b137267bec31225fed3fa3e980be52ca02ea542601694254979edd28b93af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4252; amd64

### `openjdk:21-nanoserver` - windows version 10.0.17763.4252; amd64

```console
$ docker pull openjdk@sha256:7d4098b482dc8085d23208b19d317319d661f961a7534382f92b31b3c2d31f93
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.7 MB (306719027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60dd7ad7236326db046695c915145927d7badd133bb025df1fd4ddbafd84a14f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Apr 2023 00:14:49 GMT
RUN Apply image 10.0.17763.4252
# Tue, 11 Apr 2023 23:45:41 GMT
SHELL [cmd /s /c]
# Tue, 11 Apr 2023 23:45:42 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 11 Apr 2023 23:45:43 GMT
USER ContainerAdministrator
# Tue, 11 Apr 2023 23:45:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 11 Apr 2023 23:45:57 GMT
USER ContainerUser
# Tue, 11 Apr 2023 23:45:57 GMT
ENV JAVA_VERSION=21-ea+17
# Tue, 11 Apr 2023 23:46:13 GMT
COPY dir:1915dc6e126c4da4073053ea6e369dacaa1159532dc6a7a454571cf45ddbafb9 in C:\openjdk-21 
# Tue, 11 Apr 2023 23:46:37 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 11 Apr 2023 23:46:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:af799fb2ff133c89311c6a42d34b8cb6c9b11d775f52e04ab08389d05e64ed1c`  
		Last Modified: Wed, 12 Apr 2023 00:53:10 GMT  
		Size: 106.8 MB (106788951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1db438f20b81fe0c031e4e3eee58d278fba7258d01057ff18964cccf70d41c`  
		Last Modified: Wed, 12 Apr 2023 00:52:38 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959014ae4c354475658573dc2e10e98575d191deef98e1f23bf7cb9f4768408f`  
		Last Modified: Wed, 12 Apr 2023 00:52:37 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b662327c70093bac13b7d07354fdbcd6967cbc13aaac870ca2e077fafefceb8`  
		Last Modified: Wed, 12 Apr 2023 00:52:37 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9446ad09d009884e8a1db2085ef50cd6467dc3270eca7bac27fca70698013943`  
		Last Modified: Wed, 12 Apr 2023 00:52:37 GMT  
		Size: 68.0 KB (68014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1335b1a9f9197626e9424d9d24737142c9d98659cc7f5510ca10378488d00b51`  
		Last Modified: Wed, 12 Apr 2023 00:52:35 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9353fdbff1c4541ecdcb33cce2f5a0d06ed1de727a642d1af07b2f1ee11b08`  
		Last Modified: Wed, 12 Apr 2023 00:52:35 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f07a21d7e2813d85ced09757c7b7f966afe22372d73fbb620dfccaf239ea385`  
		Last Modified: Wed, 12 Apr 2023 00:53:03 GMT  
		Size: 196.1 MB (196082591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4353c3e5809796b4983b730f26067cd50ce5a0135c93bffa9c715efe225cb03d`  
		Last Modified: Wed, 12 Apr 2023 00:52:36 GMT  
		Size: 3.8 MB (3772562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac2a5875f2a3c29b35bbefb029d319e938a82aad5ac8c8a03d91fceb03cec4b`  
		Last Modified: Wed, 12 Apr 2023 00:52:34 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
