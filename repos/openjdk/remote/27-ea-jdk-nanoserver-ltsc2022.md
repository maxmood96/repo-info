## `openjdk:27-ea-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:c15d32f49de299b2bfa3c266e6a8122e29996c01ed6c23fa514f7514010fdb58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `openjdk:27-ea-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull openjdk@sha256:97f163d56a172b35b1716b7698b3b6245a9aa439f1752028dd0c72fcc981dcef
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.3 MB (351263976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6539b47d1184fd69abef36055c916620cdd1959b3a1e3e972460c86cbeaa939`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Mon, 30 Mar 2026 18:22:48 GMT
SHELL [cmd /s /c]
# Mon, 30 Mar 2026 18:22:48 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 30 Mar 2026 18:22:49 GMT
USER ContainerAdministrator
# Mon, 30 Mar 2026 18:22:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 30 Mar 2026 18:22:57 GMT
USER ContainerUser
# Mon, 30 Mar 2026 18:22:58 GMT
ENV JAVA_VERSION=27-ea+15
# Mon, 30 Mar 2026 18:23:44 GMT
COPY dir:a373531bc68615ea541aa6fcf8d3b8dbeba3f73235aedbbf62e1427c8271e4d6 in C:\openjdk-27 
# Mon, 30 Mar 2026 18:23:50 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 30 Mar 2026 18:23:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5bd548d2161817b5149f4ddff4e4687ceef7708007193536e9d84affd21895`  
		Last Modified: Mon, 30 Mar 2026 18:24:00 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aa82ef55dbd02595b5831e45137332e416b2d01b836b7c233affaa25c4c253`  
		Last Modified: Mon, 30 Mar 2026 18:24:00 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf9766280dcd90acc8d6136e68eece68266b8bee65c6b629d6a95d7d5a6cd12`  
		Last Modified: Mon, 30 Mar 2026 18:24:00 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a30d05a675a79c89057d26b13117f730224d23b97164bc24cba262c4b61d687`  
		Last Modified: Mon, 30 Mar 2026 18:24:00 GMT  
		Size: 85.7 KB (85720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84abe5ac15341c9ed1e883073e5b1a18ac0dfb9249dac520d5239d247e63b8b4`  
		Last Modified: Mon, 30 Mar 2026 18:23:58 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611a781536e55a4a0944ba80586ba18bf660a899959f26018f3183e7caad1dd8`  
		Last Modified: Mon, 30 Mar 2026 18:23:58 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c5ddc7deb635902dc222f02d87fadef97311d193d1289acca0098a47ad4b35`  
		Last Modified: Mon, 30 Mar 2026 18:24:12 GMT  
		Size: 224.4 MB (224435940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1684eaa1f4316341feca3318c0547d5fc6541b5ef0803b5129c8b862ce895bf`  
		Last Modified: Mon, 30 Mar 2026 18:23:58 GMT  
		Size: 85.3 KB (85327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57e7168cd466ad220716eaf50389be202488d57cb08fb0fdb49790ec34f24b5`  
		Last Modified: Mon, 30 Mar 2026 18:23:58 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
