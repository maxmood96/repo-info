## `openjdk:23-ea-14-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:1a2695dc8f3efa341d97eed39620a4abfff053350fca3dbde639ec6ac5eea8b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `openjdk:23-ea-14-jdk-nanoserver` - windows version 10.0.17763.5576; amd64

```console
$ docker pull openjdk@sha256:460ba11945834c36465d78492d3beeb56e7ee7d59b7e4bb7ff6170d695e4483e
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.1 MB (306097140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6664635618e6f282f9e58f05b7b7f3bb3264fca44ba841ce81c7d6457fa9e1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Sat, 16 Mar 2024 01:04:08 GMT
SHELL [cmd /s /c]
# Sat, 16 Mar 2024 01:04:09 GMT
ENV JAVA_HOME=C:\openjdk-23
# Sat, 16 Mar 2024 01:04:10 GMT
USER ContainerAdministrator
# Sat, 16 Mar 2024 01:04:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 16 Mar 2024 01:04:12 GMT
USER ContainerUser
# Sat, 16 Mar 2024 01:04:12 GMT
ENV JAVA_VERSION=23-ea+14
# Sat, 16 Mar 2024 01:04:21 GMT
COPY dir:6277dee7c8eccce4052ef356647b124beb3a135473f3b8caa08bc0e830332ccd in C:\openjdk-23 
# Sat, 16 Mar 2024 01:04:25 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 16 Mar 2024 01:04:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8185d11164404abee9610d39d4233eece1a540631982b5f02b35e38676b40b2`  
		Last Modified: Sat, 16 Mar 2024 01:04:32 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d52202d696f6fdb055015bad6a94b29fc43bb9ded4c5c995bff66b75ac7c31`  
		Last Modified: Sat, 16 Mar 2024 01:04:31 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a251ef9f5a454db1abe1e6b4c5f46ac8e8bcfb2e1fa3c69f1c454f0f0357402`  
		Last Modified: Sat, 16 Mar 2024 01:04:31 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc9dc341e1f4106def29e7700430c2bb507792f370b313b5522cefa77fc67e6`  
		Last Modified: Sat, 16 Mar 2024 01:04:31 GMT  
		Size: 72.4 KB (72405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c48138317f36890dc5c1e3e891e3c8d382d0fc58ee4b11e43c30f87f8d022`  
		Last Modified: Sat, 16 Mar 2024 01:04:29 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f108e22b7d35fc54c1104877e2a2e8e678d42b67e52129d220f701af717f3a2`  
		Last Modified: Sat, 16 Mar 2024 01:04:29 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e3650e776f8328b514567a71dc20abc85d0d8123a1e5e7acc27e2b0e4512bb`  
		Last Modified: Sat, 16 Mar 2024 01:04:41 GMT  
		Size: 197.2 MB (197174596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3542a70064ef15660a0d67e45085241d4bf5afa5a9cc183ca7a4e7e95b1ce96b`  
		Last Modified: Sat, 16 Mar 2024 01:04:30 GMT  
		Size: 4.2 MB (4223445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43943e99c172e5cfeafae262e38abdc45f8d86d5305a7d02770d4d903c9c5eb0`  
		Last Modified: Sat, 16 Mar 2024 01:04:29 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
