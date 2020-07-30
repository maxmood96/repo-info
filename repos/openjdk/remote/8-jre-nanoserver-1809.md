## `openjdk:8-jre-nanoserver-1809`

```console
$ docker pull openjdk@sha256:e185b39c0e50702d1538d00b41b3ff23fa624150d078ff7a369b283fb8393eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `openjdk:8-jre-nanoserver-1809` - windows version 10.0.17763.1339; amd64

```console
$ docker pull openjdk@sha256:20a036e7fa720ddb8387b90857285677c96be9b2fd4d482e0d15707ca690048f
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138438252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eece79155d8a4b5a3fe6779b934943bb60ded4536e8bd3d0d1258d50113fa972`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 07 Jul 2020 13:50:07 GMT
RUN Apply image 1809-amd64
# Wed, 15 Jul 2020 01:54:43 GMT
SHELL [cmd /s /c]
# Wed, 15 Jul 2020 02:34:08 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 15 Jul 2020 02:34:09 GMT
USER ContainerAdministrator
# Wed, 29 Jul 2020 01:38:31 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 29 Jul 2020 01:38:32 GMT
USER ContainerUser
# Thu, 30 Jul 2020 22:19:51 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:23:47 GMT
COPY dir:f9cdcac6b6965117d0bbadf86b5d0b55237954c067839a8e6ad0130705a48c8f in C:\openjdk-8 
# Thu, 30 Jul 2020 22:24:02 GMT
RUN echo Verifying install ... 	&& echo   java -version && java -version
```

-	Layers:
	-	`sha256:dc95608099543221ef539391bfece5c1ce37b97af9da457f5990349cab028a12`  
		Size: 100.9 MB (100895619 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9f6486e4debac36806ed3527d9b1baea75c1a807e26baccdd0a2f521c814273f`  
		Last Modified: Wed, 15 Jul 2020 02:43:55 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635f616413e2ffeb2b698529474f16b802473016d0380fd29b21f12527e7006d`  
		Last Modified: Wed, 15 Jul 2020 02:54:29 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a9bf2169040f2fa44109296c3dc79cd3e81ec224a0a19ae4d74f3866e4bac3`  
		Last Modified: Wed, 15 Jul 2020 02:54:29 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12919e4a3f7690ed0c169e50a54145f9ad295248806072f541b2753c617e25c7`  
		Last Modified: Wed, 29 Jul 2020 01:55:54 GMT  
		Size: 66.4 KB (66363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a3ba49404160f0c5b7fe7e56cc630dc53340e9e3ce7327144589c193f51427`  
		Last Modified: Wed, 29 Jul 2020 01:55:53 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c8250f9dab00bfef751c16f2eed1d51cbfcc3be032a34e9cd464b0c26eaa39`  
		Last Modified: Thu, 30 Jul 2020 22:28:15 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5851b6b213ed8471b8781a40e2ce2bf905967338e9a2810bb849a39f7bf90d31`  
		Last Modified: Thu, 30 Jul 2020 22:29:25 GMT  
		Size: 37.4 MB (37425936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574944577a0d1c847de9f60022827d4c1eeebf6b29775cd0db9b49ac2991f50b`  
		Last Modified: Thu, 30 Jul 2020 22:29:19 GMT  
		Size: 45.9 KB (45910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
