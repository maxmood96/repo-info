## `openjdk:16-ea-nanoserver-1809`

```console
$ docker pull openjdk@sha256:283a2dd9cfd6ae5c8892a574d115ea06c5728d05bc6c85d877ce64425c2f2075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `openjdk:16-ea-nanoserver-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull openjdk@sha256:2255197282f1c4e0e9f1336ce9f27d23f6f3eeb5adc4b7933d8eeb55d9cab3ef
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.0 MB (297046944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472d4c80c6ee5d472c2fec124906f2dff0373d25a443f64103e252550963421c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 30 Sep 2020 11:25:56 GMT
RUN Apply image 1809-amd64
# Wed, 14 Oct 2020 17:46:04 GMT
SHELL [cmd /s /c]
# Wed, 14 Oct 2020 17:46:05 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 14 Oct 2020 17:46:06 GMT
USER ContainerAdministrator
# Wed, 14 Oct 2020 17:46:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 14 Oct 2020 17:46:22 GMT
USER ContainerUser
# Wed, 14 Oct 2020 17:46:23 GMT
ENV JAVA_VERSION=16-ea+19
# Wed, 14 Oct 2020 17:47:04 GMT
COPY dir:bdf4e5ef39680bc6900a8942c0e86a2fa60a3a2a7434c43c49d0857baa5ba447 in C:\openjdk-16 
# Wed, 14 Oct 2020 17:47:26 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Wed, 14 Oct 2020 17:47:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:aab6118ce69c93410df7fa15842a6e3b3c7ff20b639c779b5d5f78e7653eaa07`  
		Size: 101.2 MB (101205155 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:40f59dc77cd194db29e444ce30cc9a91a3d555f7d4d7329fb6f46c13e559dc2f`  
		Last Modified: Wed, 14 Oct 2020 18:31:55 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2c5c7ff5b97e2384ad57c7cd4094b1a40907ea3634e923a539236764052c20`  
		Last Modified: Wed, 14 Oct 2020 18:31:53 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e535cf22ef1ca77aebd1948de6ab3937b1f63d64895ea717d71cff42d95815`  
		Last Modified: Wed, 14 Oct 2020 18:31:54 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a209bbfc514f45496baa96d8592838b00434aae4cd11fb8ffbcf643dfe386c`  
		Last Modified: Wed, 14 Oct 2020 18:31:52 GMT  
		Size: 72.2 KB (72249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc31a2a793752d0400745705f15ea0e51a67ed288dc5bc3c6eda4520ca139549`  
		Last Modified: Wed, 14 Oct 2020 18:31:50 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1fa135894bcb2928e20f62ee90e1c35a3309d4d26f2c14e5acadacdc78c70d`  
		Last Modified: Wed, 14 Oct 2020 18:31:50 GMT  
		Size: 863.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3810f5cd33a6e752a23f6013ddab6ebda1baa16e59dbcd33c46db07e6cccb677`  
		Last Modified: Wed, 14 Oct 2020 18:34:30 GMT  
		Size: 192.2 MB (192244901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af59c766ede91e9c59fbab0117c50e8878814b98a18e3fb07b7a77562c77200c`  
		Last Modified: Wed, 14 Oct 2020 18:31:51 GMT  
		Size: 3.5 MB (3519364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6493a4d6320f7e952c908d3cfef204efb59a362cdbf3e592de0369542d771f87`  
		Last Modified: Wed, 14 Oct 2020 18:31:49 GMT  
		Size: 839.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
