## `openjdk:18-nanoserver-1809`

```console
$ docker pull openjdk@sha256:19e6c6d075bd006f901d55132ea3792bb26c897cce94533d45cd7ab55cf46e1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `openjdk:18-nanoserver-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull openjdk@sha256:1089322ae09dfa70b08dfad3804e77800bcea403117ff753e1a8dab0db1d9005
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288903077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3519f25eae6ef87242a96a089761c8a5bf267b0a36b834324641be26f27525`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Aug 2021 19:15:20 GMT
RUN Apply image 1809-amd64
# Wed, 25 Aug 2021 16:34:07 GMT
SHELL [cmd /s /c]
# Wed, 25 Aug 2021 17:06:45 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 25 Aug 2021 17:06:46 GMT
USER ContainerAdministrator
# Wed, 25 Aug 2021 17:06:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 25 Aug 2021 17:06:55 GMT
USER ContainerUser
# Fri, 03 Sep 2021 18:18:33 GMT
ENV JAVA_VERSION=18-ea+13
# Fri, 03 Sep 2021 18:18:48 GMT
COPY dir:24fd2fc17f2cab08628ee5da2d33401ab9901709ae2f1a8bc6e264f8ed5493b2 in C:\openjdk-18 
# Fri, 03 Sep 2021 18:19:04 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 03 Sep 2021 18:19:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bc8517709e9cfff223cb034ff5be8fcbfa5409de286cdac9ae1b8878ebea6b84`  
		Size: 102.7 MB (102741177 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9191bd6656c8ea186f621f667fb09a30387fae304b3e7817fd7e8258c022d185`  
		Last Modified: Wed, 25 Aug 2021 23:21:14 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529f54617b19374dc6ae56b7cbadea820f6613c38ef8eb5b3780625f824e7f70`  
		Last Modified: Thu, 26 Aug 2021 00:39:57 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17928612bd587dae3533403ae499232eb58f410a5e0875cca4930241ef47caa3`  
		Last Modified: Thu, 26 Aug 2021 00:39:56 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6b2868a6eab69d3ff3c1ab6e50f537ef7b5671cd3a888b7fa6fcc521e63759`  
		Last Modified: Thu, 26 Aug 2021 00:39:56 GMT  
		Size: 71.1 KB (71120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1f7631bcd8fcfd1b84d19c43b45e42f54be2bafdb008157e4d2e8d7a64430a`  
		Last Modified: Thu, 26 Aug 2021 00:39:53 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e02295b1cc3c87f145486215dc6bd79d8a1d496c73996a9efff4de5559c099`  
		Last Modified: Fri, 03 Sep 2021 18:27:22 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d9d607e0f95224567298f3396cdae09c9bdca7500cd9a15e60ec27597814686`  
		Last Modified: Fri, 03 Sep 2021 18:27:38 GMT  
		Size: 182.5 MB (182538723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5154651c4e23791e14ed23e0fb86a72f531146ec9213b15d9a9857276e6ccd50`  
		Last Modified: Fri, 03 Sep 2021 18:27:22 GMT  
		Size: 3.5 MB (3545228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef623a4deacdd2d7549bfd9cda3e8292f4788591237229daed47a54c9aa6ed2`  
		Last Modified: Fri, 03 Sep 2021 18:27:21 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
