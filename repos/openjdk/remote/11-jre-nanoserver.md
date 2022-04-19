## `openjdk:11-jre-nanoserver`

```console
$ docker pull openjdk@sha256:c4697c447aafc02e7265f46348cfe7097d80c46b5774e1b8cf720c29c6c9c605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `openjdk:11-jre-nanoserver` - windows version 10.0.17763.2803; amd64

```console
$ docker pull openjdk@sha256:72a87af34c462e8ac31528e0df1b3a352f98f7344e9d8cbab886f8b885b62623
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141894925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d2fae7f1e1fce3857427f36588beb52c14b0b492aafadad3524e6f955583a6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Apr 2022 10:52:49 GMT
RUN Apply image 1809-amd64
# Wed, 13 Apr 2022 15:16:11 GMT
SHELL [cmd /s /c]
# Wed, 13 Apr 2022 17:14:56 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 13 Apr 2022 17:14:57 GMT
USER ContainerAdministrator
# Wed, 13 Apr 2022 17:15:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 13 Apr 2022 17:15:03 GMT
USER ContainerUser
# Wed, 13 Apr 2022 17:15:03 GMT
ENV JAVA_VERSION=11.0.14.1
# Wed, 13 Apr 2022 17:17:44 GMT
COPY dir:aa02bf9b1385f5b048b84d2f1c20be3dc386940ae37d92f3d7df0885a1bea73b in C:\openjdk-11 
# Wed, 13 Apr 2022 17:17:51 GMT
RUN echo Verifying install ... 	&& echo   java --version && java --version 	&& echo Complete.
```

-	Layers:
	-	`sha256:6fc97003d8b7f593fe071cf3ea64f3ce760cc060f3402bb6b1b849c040e222d5`  
		Size: 103.1 MB (103096169 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ea4009814dceb50337c66614a6008cfc2fb73ce53e62162bce071ef6ea1adf2d`  
		Last Modified: Wed, 13 Apr 2022 15:58:06 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849f82959ffa51b7fc97fc8d879a85b8b443d32aa27a8507f2200e370c4022f6`  
		Last Modified: Tue, 19 Apr 2022 01:11:33 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302ab25e933bb29e0963abb16a53cff6a3f17aaa4d0de148077b06ab85fbb123`  
		Last Modified: Tue, 19 Apr 2022 01:11:33 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5f0ad271138cceb8261825016c3345ae53a44e0d7eb7df18a792fa61d5e5b6`  
		Last Modified: Tue, 19 Apr 2022 01:11:33 GMT  
		Size: 69.7 KB (69695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e23c499a1f064ee45af7c5b2696ec11f98304ec5ae5b878e24508df3ff0551c`  
		Last Modified: Tue, 19 Apr 2022 01:11:31 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5833ae37d200a018ec402c10249b4d59ce181cde4e609cd568f6b9d43a489a92`  
		Last Modified: Tue, 19 Apr 2022 01:11:31 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97cef5798312a8f8415fdadcf1af5069fcfe099597c97a43740202bb2362baa0`  
		Last Modified: Tue, 19 Apr 2022 01:16:40 GMT  
		Size: 38.6 MB (38640109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a92e9505ae57780d73feaa1b91954f35f4639952ec3b97b04a098759efd55b`  
		Last Modified: Tue, 19 Apr 2022 01:16:33 GMT  
		Size: 83.8 KB (83793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
