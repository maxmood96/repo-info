## `eclipse-temurin:21-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:4db35d24b164ad2ade2b6928912a0c0e200105b5dea0eccba338b43fec376fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `eclipse-temurin:21-jre-nanoserver-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull eclipse-temurin@sha256:b6ecc4a941ba48c9c67e252e300762d9a2cf26773d3b6c777e9f6044757c5e7c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.1 MB (207140667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c41aadaf2a1434062086207a23478d085155e4ff21111fa52c06bef80a03a534`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 19:42:01 GMT
SHELL [cmd /s /c]
# Wed, 15 May 2024 20:15:47 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Wed, 15 May 2024 20:15:47 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 15 May 2024 20:15:48 GMT
USER ContainerAdministrator
# Wed, 15 May 2024 20:15:59 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 May 2024 20:15:59 GMT
USER ContainerUser
# Wed, 15 May 2024 20:21:03 GMT
COPY dir:30866ffc44919960ba2d43fceab02c0cbcad12e73e3b28316799617dca9a13d0 in C:\openjdk-21 
# Wed, 15 May 2024 20:21:14 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6a511fea8e874efc08e5058ac5b12b6433c36ba6570862a619dd80cfb0e190`  
		Last Modified: Wed, 15 May 2024 20:45:52 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4841491247350a2cba22e1d7deecfc13e43a405a6bf7b96689d0b169bf4a4fe0`  
		Last Modified: Wed, 15 May 2024 20:53:51 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a6273893979eaf90f1cf0ba4b42c4c9369bf97d556f2e62ba9fa4eff08f910`  
		Last Modified: Wed, 15 May 2024 20:53:51 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c33ee8b266be6936b2f35575cf3a5a5383bee76bbe81975578e99f6651514d`  
		Last Modified: Wed, 15 May 2024 20:53:50 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d775a9c260301bb3c11962dba072c4a531ef28a1f85dc32dd705e3e05daad8e`  
		Last Modified: Wed, 15 May 2024 20:53:49 GMT  
		Size: 68.4 KB (68439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18782632469d51a768f172daa64d27fc8cca50a0276127a4c4f5ef26e28973fb`  
		Last Modified: Wed, 15 May 2024 20:53:49 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19d88d104d426267c25fa419d8e14b759a519af11d256438debe36c93a93209`  
		Last Modified: Wed, 15 May 2024 20:55:07 GMT  
		Size: 48.8 MB (48758824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c816df84db4e89a349e5371b6034c0ee23d86f3464a2df6430397a76bca7845`  
		Last Modified: Wed, 15 May 2024 20:54:59 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
