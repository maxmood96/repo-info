## `openjdk:16-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:80b36d7901361841cdaf8386b99b5322154aa402cdc41eeab1f85cf73708134e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `openjdk:16-jdk-nanoserver` - windows version 10.0.17763.2114; amd64

```console
$ docker pull openjdk@sha256:089fcf0d927b32c103812c4772250c95f98fd42239211362229887fedb5b25f2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286597187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78280df1137487e5614d488f19f16522ed905522e6084a1e9d9b737ab72105dd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Aug 2021 19:15:20 GMT
RUN Apply image 1809-amd64
# Wed, 11 Aug 2021 17:30:38 GMT
SHELL [cmd /s /c]
# Wed, 11 Aug 2021 17:47:59 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 11 Aug 2021 17:48:02 GMT
USER ContainerAdministrator
# Wed, 11 Aug 2021 17:48:17 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 11 Aug 2021 17:48:20 GMT
USER ContainerUser
# Wed, 11 Aug 2021 17:48:23 GMT
ENV JAVA_VERSION=16.0.2
# Wed, 11 Aug 2021 17:48:42 GMT
COPY dir:cb0fff7e1eb7273b9cd408e88cd60c60a3923c3595eb85b84f5ecaf2afd41761 in C:\openjdk-16 
# Wed, 11 Aug 2021 17:49:03 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 11 Aug 2021 17:49:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bc8517709e9cfff223cb034ff5be8fcbfa5409de286cdac9ae1b8878ebea6b84`  
		Size: 102.7 MB (102741177 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ae0a5a946be2ad0e39a8260e454c0060a31a9f7e5be75d1f9038dc13730abc0a`  
		Last Modified: Wed, 11 Aug 2021 18:21:28 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529da2001ff49f33aeab3c8b2ced09726b9141c703af49c07356e9f5e8f47fb7`  
		Last Modified: Wed, 11 Aug 2021 18:28:23 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f5181f0ab84d4352412bcf51a8f43379cdff502696ff15042c0f1d74644d3f`  
		Last Modified: Wed, 11 Aug 2021 18:28:23 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb85b9299e2eae453eaff412de8bc5f069a97a03be3fba7b54f8c3b48bb08fff`  
		Last Modified: Wed, 11 Aug 2021 18:28:23 GMT  
		Size: 68.4 KB (68358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044f8b0d08d7c48b7190e6f25eebaa170113e9f4d458c6a0476dead13a59d02e`  
		Last Modified: Wed, 11 Aug 2021 18:28:20 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164afcc22581f344eb00934f810e82cbd694c1506eb45188b5b65843be40696`  
		Last Modified: Wed, 11 Aug 2021 18:28:20 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38f930edf90dc0ab4b4cc740f42a22b93f15c0ab68682ad7790c48d033ef85b0`  
		Last Modified: Wed, 11 Aug 2021 18:28:43 GMT  
		Size: 180.1 MB (180114476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc7f4dfdb44bd6edaaf2fa2bbff5d6b59478d8eab2e2ad64c52befa26927efb`  
		Last Modified: Wed, 11 Aug 2021 18:28:21 GMT  
		Size: 3.7 MB (3666148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d794311571b37390de0c1527441c30ec92d10e0f5da55dd7299b07d1062aa66`  
		Last Modified: Wed, 11 Aug 2021 18:28:20 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
