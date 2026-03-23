## `openjdk:27-ea-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:b4a0f5b302f2d98a186faef84154619b2665a71a8e934508b546352daec83aef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `openjdk:27-ea-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull openjdk@sha256:bc8850003c0e14187bdfc0944b4a47956e3d85d62605280a01af9dd2d7378ce3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.3 MB (351273269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e5677db67264b274fa6e5e1de04c61056b5d062290d2fbbc2f42a408113771`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Mon, 23 Mar 2026 19:13:00 GMT
SHELL [cmd /s /c]
# Mon, 23 Mar 2026 19:13:01 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 23 Mar 2026 19:13:01 GMT
USER ContainerAdministrator
# Mon, 23 Mar 2026 19:13:03 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 23 Mar 2026 19:13:03 GMT
USER ContainerUser
# Mon, 23 Mar 2026 19:13:04 GMT
ENV JAVA_VERSION=27-ea+14
# Mon, 23 Mar 2026 19:14:50 GMT
COPY dir:1e03a1eeb0a7b9a5151c618212b4c0b4b3701f1a28f72fad799e2bd29790a005 in C:\openjdk-27 
# Mon, 23 Mar 2026 19:15:01 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 23 Mar 2026 19:15:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9ec82d1173531df98af54b6ffc8842a8d9d02c18f4306bbb7f5a6697391bce`  
		Last Modified: Mon, 23 Mar 2026 19:15:08 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1137eada5f23a8390783535e9b77e2997eb929a64ae065ab06bf90b31dab40`  
		Last Modified: Mon, 23 Mar 2026 19:15:08 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c35a8ec2fa2d2fea4f7302e4b16b37ed122272133523edccc01357eb2db342`  
		Last Modified: Mon, 23 Mar 2026 19:15:08 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fedcd7712b25e05f40327eb4508b6d870c854fd995d7b00391b9b467d376c6a`  
		Last Modified: Mon, 23 Mar 2026 19:15:08 GMT  
		Size: 77.0 KB (77049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d8bd01f1550e7a780e3c645c334a6e7292fba3fa620e23c1c5a818c87914ea`  
		Last Modified: Mon, 23 Mar 2026 19:15:06 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb766dcadba977adad4f0a23d987318ec6fbcaaa5abb0913041dd1fb3c5c036`  
		Last Modified: Mon, 23 Mar 2026 19:15:06 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e8e09277dd965c9ac5b9462fc267c53026b094bd01df3a40e1e9c6ff25f2f27`  
		Last Modified: Mon, 23 Mar 2026 19:15:21 GMT  
		Size: 224.4 MB (224386459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4caa734ac7f2f369297da801c5f60561f71086b813605deb4bb3865fd39bd6f`  
		Last Modified: Mon, 23 Mar 2026 19:15:06 GMT  
		Size: 152.9 KB (152882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7437e2ebfbac0ea67e25101823547c0874fdc71d41679cb73301f2a89a420a8d`  
		Last Modified: Mon, 23 Mar 2026 19:15:06 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
