## `openjdk:15-nanoserver`

```console
$ docker pull openjdk@sha256:3a4767c99f16326cf2d37894c26c3ae3fe44a9ac57d3afd62015692ce988f822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `openjdk:15-nanoserver` - windows version 10.0.17763.1282; amd64

```console
$ docker pull openjdk@sha256:00f1f422501b7bb8a3dfb19d02ac249a1e4e3e9d0ff1e5a52d4543638d3b44b7
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295519987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd597da0efb8e58accbc306c3e71c28028ad9f4f810f5d9c8300cebda07b2c46`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jun 2020 11:12:32 GMT
RUN Apply image 1809-amd64
# Tue, 09 Jun 2020 22:42:44 GMT
SHELL [cmd /s /c]
# Tue, 09 Jun 2020 22:42:45 GMT
ENV JAVA_HOME=C:\openjdk-15
# Tue, 09 Jun 2020 22:42:45 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2020 22:43:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Tue, 09 Jun 2020 22:43:01 GMT
USER ContainerUser
# Tue, 09 Jun 2020 22:43:01 GMT
ENV JAVA_VERSION=15-ea+26
# Tue, 09 Jun 2020 22:43:49 GMT
COPY dir:7c4913b923f352234b1ecc7d6b37d6e281b0262e8101e7664a5bc785e9b435a4 in C:\openjdk-15 
# Tue, 09 Jun 2020 22:44:09 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Tue, 09 Jun 2020 22:44:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c7d6d47ff7dfb2aa4d4e819641b93ec971e8541978dff0ffc24c193babeb8c07`  
		Size: 101.0 MB (101043386 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5b390ee94e41353252b153770fa99d748992b90bdaf9abf7c785d93be52ee02c`  
		Last Modified: Tue, 09 Jun 2020 23:19:14 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a124a49383ae5eb05208979bcfbadf68055d2672da7f78201fe9a45e8d0bbb`  
		Last Modified: Tue, 09 Jun 2020 23:19:14 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb0c11b8fc0c6457077b02c8314626c0346af177c44a8615448f933e94b909c`  
		Last Modified: Tue, 09 Jun 2020 23:19:13 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29f17e75290909d8f60805f97895317f25ce6c2dc53b1b25e8d6dfe142e6f53`  
		Last Modified: Tue, 09 Jun 2020 23:19:13 GMT  
		Size: 63.5 KB (63500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fe65db6982f49c866229851adc1c64f6e6354b9e0a49d506241693ac2e660f`  
		Last Modified: Tue, 09 Jun 2020 23:19:11 GMT  
		Size: 814.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6141cd5477ae12c163672e467cb0c0b346fa71d3c595b5a925df608a8cd6193`  
		Last Modified: Tue, 09 Jun 2020 23:19:11 GMT  
		Size: 816.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff79848951701221686869d27320e1fcda16fe647aa0a6d7d3baa4f38a4bb2e0`  
		Last Modified: Tue, 09 Jun 2020 23:22:40 GMT  
		Size: 190.9 MB (190900094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a1766db33520f660bb872be99bff8bab2983c316e4f04eabddc86b17fb8fae`  
		Last Modified: Tue, 09 Jun 2020 23:19:12 GMT  
		Size: 3.5 MB (3508005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84e412e6532ebaee3ed84f72d2803dbd3f2e9a749b0912f4cfd68b89778f2d9a`  
		Last Modified: Tue, 09 Jun 2020 23:19:10 GMT  
		Size: 834.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
