## `openjdk:14-nanoserver-1809`

```console
$ docker pull openjdk@sha256:760cd242a8e23da3c02d8ec55cf0acd72e9c71e8a9011fc4bda595f04c5e96f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64

### `openjdk:14-nanoserver-1809` - windows version 10.0.17763.914; amd64

```console
$ docker pull openjdk@sha256:f043ce3c7792dad933e421caf26b1553503ec9a0249ca3312186051a6a349bd3
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298481014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70a83e6776c8426ba3438f4980cd45e4bf840a9d97c65da3c2ba6bd9beb4edb0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 28 Nov 2019 13:16:41 GMT
RUN Apply image 1809-amd64
# Wed, 11 Dec 2019 18:49:48 GMT
SHELL [cmd /s /c]
# Wed, 11 Dec 2019 18:49:50 GMT
ENV JAVA_HOME=C:\openjdk-14
# Wed, 11 Dec 2019 18:49:51 GMT
USER ContainerAdministrator
# Wed, 11 Dec 2019 18:50:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 11 Dec 2019 18:50:07 GMT
USER ContainerUser
# Tue, 31 Dec 2019 00:06:58 GMT
ENV JAVA_VERSION=14-ea+29
# Tue, 31 Dec 2019 00:07:55 GMT
COPY dir:155a431ef2c5461a111dda1d337e9b5e0269b66d9e46fe244b93e290968f2568 in C:\openjdk-14 
# Tue, 31 Dec 2019 00:08:17 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Tue, 31 Dec 2019 00:08:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1951f408509ba9ddcf240ef5d838c72c5596f97a05b063446508f2ba15d510f2`  
		Size: 101.1 MB (101106116 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:163d55b77f49371136083ba8066ddbec4afad6e1f4fbba77fa4ffebc99a8098a`  
		Last Modified: Wed, 11 Dec 2019 20:01:21 GMT  
		Size: 945.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9326e4caa8f459874d77c281820948a0fa2e558568f484250684f714e368c0bc`  
		Last Modified: Wed, 11 Dec 2019 20:01:19 GMT  
		Size: 953.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07bbc07ec7d9f59279b56946327222e61b8d576bc34eb8b70be4aa88b484d87`  
		Last Modified: Wed, 11 Dec 2019 20:01:19 GMT  
		Size: 944.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c25567424a9bb0685aa9d0cc78a53b800a3447fff914466146890e6bf40dcdd`  
		Last Modified: Wed, 11 Dec 2019 20:01:19 GMT  
		Size: 63.9 KB (63920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6607ef629cd6ba3de9b2b3f57cdc6172ca483c4f285428321d4b04ce9b321db8`  
		Last Modified: Wed, 11 Dec 2019 20:01:16 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815c388844f0cdc9aef754e1992e17e83395cd3f45b2715c9a38e574aeb8aa21`  
		Last Modified: Tue, 31 Dec 2019 00:25:36 GMT  
		Size: 918.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84095cd9af889104c13c17b95339cdbb987955ae5e4b364bad988a4fc5246ae`  
		Last Modified: Tue, 31 Dec 2019 00:25:57 GMT  
		Size: 193.8 MB (193828866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fc4f66701973dda9b580eec9c9e3484f6394ed437ffc45f0a99cb1caa937e12`  
		Last Modified: Tue, 31 Dec 2019 00:25:37 GMT  
		Size: 3.5 MB (3476482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232afc30c7e520d3a2d4b1ad558147e2b8ebbb47651016faf8bf7f94d39a9127`  
		Last Modified: Tue, 31 Dec 2019 00:25:36 GMT  
		Size: 921.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
