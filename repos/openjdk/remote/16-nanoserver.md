## `openjdk:16-nanoserver`

```console
$ docker pull openjdk@sha256:a6c2026bf3cb88ac929e93513d843f7ccf5c5d844d0cb9b831408378917d96e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `openjdk:16-nanoserver` - windows version 10.0.17763.1637; amd64

```console
$ docker pull openjdk@sha256:495fa93c85710ff3e63d4cfc07d78ed760e906d5308ddf223a006042455aa7af
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 MB (285021119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:387e6f461f90798b9c47f39e0ef3d61d5eaa521aa8d0c5bdae9eaba4664c6a0b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 03 Dec 2020 08:05:47 GMT
RUN Apply image 1809-amd64
# Wed, 09 Dec 2020 18:58:23 GMT
SHELL [cmd /s /c]
# Wed, 09 Dec 2020 18:58:23 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 09 Dec 2020 18:58:24 GMT
USER ContainerAdministrator
# Wed, 09 Dec 2020 18:58:40 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 09 Dec 2020 18:58:40 GMT
USER ContainerUser
# Wed, 09 Dec 2020 18:58:41 GMT
ENV JAVA_VERSION=16-ea+27
# Wed, 09 Dec 2020 18:59:17 GMT
COPY dir:99f811290cbed9d3a18665555a2b1dd859a8c3fc4fc549c64898d26e30c1b13a in C:\openjdk-16 
# Wed, 09 Dec 2020 18:59:40 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Wed, 09 Dec 2020 18:59:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:21be49aa856f07be4e0a677b988e43c04bd595a3c858e58b6c364477bbbf7222`  
		Size: 101.3 MB (101264827 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fe9a51a0164bd1c063cbda08c4e22dc4f5d04a8047a3951d7441f37fb93c57f2`  
		Last Modified: Wed, 09 Dec 2020 19:34:04 GMT  
		Size: 863.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8993beeae33a05d68775319a4b9f9df44ac08ccfc62cb15113a36b06ad62d1f`  
		Last Modified: Wed, 09 Dec 2020 19:34:02 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340da9582f81cba4147b5da6d500dacd9f3ffdd520c3211dfb20153cd4ae71fc`  
		Last Modified: Wed, 09 Dec 2020 19:34:02 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f848f35781549a8c193011c95049cd95311b558af39d0f8057a5b460a459488`  
		Last Modified: Wed, 09 Dec 2020 19:34:02 GMT  
		Size: 64.6 KB (64579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636f94045101715dca150f5013879c45929dec9e849eac5b53631727e42bb8a6`  
		Last Modified: Wed, 09 Dec 2020 19:33:59 GMT  
		Size: 873.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687b00df1d44709aa897758746c19fb74a09807d58601c455186fd61bc5bbd67`  
		Last Modified: Wed, 09 Dec 2020 19:33:59 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6910e8b5fe7cd04a5fb73f751bd3147afe7314e17af60862471a1fcbd97ea77b`  
		Last Modified: Wed, 09 Dec 2020 19:34:17 GMT  
		Size: 180.0 MB (180017283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71236cd2e38138ef8b1e4ada3cc10bb6c5dd06b21987eb082eca51307a552a0`  
		Last Modified: Wed, 09 Dec 2020 19:34:00 GMT  
		Size: 3.7 MB (3669220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18069f2280bfc5c30de3b48ed1dbe78cf856599e15fde536c206dbb19ca98836`  
		Last Modified: Wed, 09 Dec 2020 19:33:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
