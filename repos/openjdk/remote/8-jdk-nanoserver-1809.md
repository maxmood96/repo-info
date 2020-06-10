## `openjdk:8-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:13e7b19d3928ce5b7cc36ed007bec570b1620f61c8dc5bf1a542f380373269b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `openjdk:8-jdk-nanoserver-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull openjdk@sha256:7c3a92b35ab06efcf8a0bc10565fd34e4737acd04c1c57eca2d575ec91f33a6a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.9 MB (200919095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c67cdbd7b55eac812589489325b76a5a6bcc396e38479152b4eecc97f1cd4ac`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jun 2020 11:12:32 GMT
RUN Apply image 1809-amd64
# Tue, 09 Jun 2020 22:42:44 GMT
SHELL [cmd /s /c]
# Tue, 09 Jun 2020 23:10:49 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 09 Jun 2020 23:10:50 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2020 23:11:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Tue, 09 Jun 2020 23:11:03 GMT
USER ContainerUser
# Tue, 09 Jun 2020 23:11:03 GMT
ENV JAVA_VERSION=8u252
# Tue, 09 Jun 2020 23:11:35 GMT
COPY dir:ab479e12b22d2d8e4d7a7f2a7c1ce2c9a985b2211941ab66c77b1be78e3ec440 in C:\openjdk-8 
# Tue, 09 Jun 2020 23:11:54 GMT
RUN echo Verifying install ... 	&& echo   javac -version && javac -version 	&& echo   java -version && java -version
```

-	Layers:
	-	`sha256:c7d6d47ff7dfb2aa4d4e819641b93ec971e8541978dff0ffc24c193babeb8c07`  
		Size: 101.0 MB (101043386 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5b390ee94e41353252b153770fa99d748992b90bdaf9abf7c785d93be52ee02c`  
		Last Modified: Tue, 09 Jun 2020 23:19:14 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ceaf36f52880d38e22fe7b7f8fb469078f6c3cbd8878cb0cb6622f84331a55`  
		Last Modified: Tue, 09 Jun 2020 23:33:31 GMT  
		Size: 867.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495ef2c347d7f8951f93f5b11447092502dbf5148e0afc42bd6a93cdfac22e43`  
		Last Modified: Tue, 09 Jun 2020 23:33:31 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c5b466a2d08cf215a8f231507f418d6f8f0937fd9ea6be0f9eba83d332301b`  
		Last Modified: Tue, 09 Jun 2020 23:33:29 GMT  
		Size: 69.0 KB (69041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73c238f787394408ba51a1bb4103d83b74626d53a8c138fcd934fe665c57589`  
		Last Modified: Tue, 09 Jun 2020 23:33:29 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8c25bbf35b268fa8cdd03b4ded93b7063f5895c399f1c52dccaf183abc295e`  
		Last Modified: Tue, 09 Jun 2020 23:33:28 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4495f1c11d33d4e1db9728904acf099bf8066d74d35ec5346bcabd27cfc7b25`  
		Last Modified: Tue, 09 Jun 2020 23:33:40 GMT  
		Size: 99.7 MB (99747968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326078912a8e839baf135e085318796660a7af9ce0f2cf45f1867c5172f67094`  
		Last Modified: Tue, 09 Jun 2020 23:33:29 GMT  
		Size: 54.3 KB (54340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
