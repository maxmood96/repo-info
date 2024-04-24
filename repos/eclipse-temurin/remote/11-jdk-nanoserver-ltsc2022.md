## `eclipse-temurin:11-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:ff57dcefa793ed52915db26ec33cc8f8cf23380dad17305e3f69adcfa05aa811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `eclipse-temurin:11-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull eclipse-temurin@sha256:0089d380f18922116c76b44d70342672558f3afabdf97418759a6cf6663065ad
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.2 MB (315221562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2c5541bf2d59f739d2c128fe5b4f3fb7b886ac99a2c960d840c9e6bd638bf4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Apr 2024 08:53:11 GMT
RUN Apply image 10.0.20348.2402
# Wed, 10 Apr 2024 00:34:53 GMT
SHELL [cmd /s /c]
# Wed, 24 Apr 2024 19:23:58 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Wed, 24 Apr 2024 19:23:59 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 24 Apr 2024 19:23:59 GMT
USER ContainerAdministrator
# Wed, 24 Apr 2024 19:24:10 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Apr 2024 19:24:11 GMT
USER ContainerUser
# Wed, 24 Apr 2024 19:24:27 GMT
COPY dir:8aa740e08efd9dadfa2fb1fd54d653720c8e2097106a2d2f0f8f1f0b127bcc3e in C:\openjdk-11 
# Wed, 24 Apr 2024 19:24:44 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 24 Apr 2024 19:24:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:755fc767289b8847bd0d0d8d75efc308c040140acf2a3426973ba9fbf022c4c0`  
		Last Modified: Tue, 09 Apr 2024 23:50:18 GMT  
		Size: 121.0 MB (120993754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70887eeae6a5d6d5fd81661024afc84fee637f674dee5e7127112cbfce90750`  
		Last Modified: Wed, 10 Apr 2024 01:00:01 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2193f7233ee9ca7d1dda364e716073831621842dd832deb8f3c69021aa9d6334`  
		Last Modified: Wed, 24 Apr 2024 19:46:46 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1727b617a83ee4a6ad51740f7c297bf8f286e72a3aaad5a45fc7a5ff594d9f2`  
		Last Modified: Wed, 24 Apr 2024 19:46:46 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6589479c4d6064b58314b90fbe097b165dfe7c0bce69f14eb48a896cb9d2e0`  
		Last Modified: Wed, 24 Apr 2024 19:46:46 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc05e4667a98baef0dbcc6e71d46c018dc80e22b83a3e32435c2063c1ec507d`  
		Last Modified: Wed, 24 Apr 2024 19:46:44 GMT  
		Size: 76.8 KB (76791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c3360e9b88abe16f00f54eb59d334aedf61e54d3fa3776751aea8e2fb6a73b`  
		Last Modified: Wed, 24 Apr 2024 19:46:44 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b930dab2b7897785c835ff84cb9f42d45edfe677606da0452d0022195c6683`  
		Last Modified: Wed, 24 Apr 2024 19:47:02 GMT  
		Size: 194.1 MB (194083519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e422cb81c1d8c70dc848b8ae0bc1e0c2031e835ee125163b9dfac27e9ef7f8cd`  
		Last Modified: Wed, 24 Apr 2024 19:46:44 GMT  
		Size: 61.2 KB (61211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6331fe34cbb0422b7e33e9467b9a5d91245d68fa7a5c09fa4166d54c5d7d0b`  
		Last Modified: Wed, 24 Apr 2024 19:46:44 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
