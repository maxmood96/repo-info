## `eclipse-temurin:11-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:abff62786ebc444f88925cf39d0ba9f3771992cb01d95e028fe5c5627ee025fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `eclipse-temurin:11-nanoserver-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull eclipse-temurin@sha256:400952a872d49a6fffee7a7546fa2247a3459a2e0c3de76288bc44ee84fd1f2d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.9 MB (384878741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4f050a749d23d4d0b8a1648b2856c69bcf1bac560ce78052dd6d28b342d77d4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Apr 2025 07:26:08 GMT
RUN Apply image 10.0.26100.3775
# Wed, 09 Apr 2025 01:18:32 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:18:34 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Wed, 09 Apr 2025 01:18:35 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 09 Apr 2025 01:18:37 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:18:41 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:18:42 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:18:51 GMT
COPY dir:9a97e9a1ce762bb8542962ee0a2b0ca6fa379668e092b80acfc01b297b3b57a6 in C:\openjdk-11 
# Wed, 09 Apr 2025 01:18:59 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 09 Apr 2025 01:19:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:79b2ed45f890e91d23d7d22491a8fb6909c9268c668dc6a0e3b40131da02ed74`  
		Last Modified: Wed, 09 Apr 2025 00:36:30 GMT  
		Size: 190.1 MB (190113206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51dcbc248e2fe87185099346d851ee13f4b4cf01d5a1bc19965c5077f53a6ba7`  
		Last Modified: Wed, 09 Apr 2025 01:19:04 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab6014ac3080da2617258e6b355f19fb22beb231a26f8593309c6c9ef8b4dd52`  
		Last Modified: Wed, 09 Apr 2025 01:19:04 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f052e6ee89dedf32994ac0627ca7353e80c177d975ba2d3f2fd37d7d20eca2c`  
		Last Modified: Wed, 09 Apr 2025 01:19:04 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038ca4752a6776aff58311712fde24e2884eb2e5476b75b81233cff4bcb6ae15`  
		Last Modified: Wed, 09 Apr 2025 01:19:04 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47d40a0e8b97141cd32b122897cb409d23b64ca23a0734cb1a4abb700e6d925`  
		Last Modified: Wed, 09 Apr 2025 01:19:03 GMT  
		Size: 76.5 KB (76527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0716bd0bae9252c84f5af88998e8175726a0e4287b1155381d4b81e2e78e2bd9`  
		Last Modified: Wed, 09 Apr 2025 01:19:03 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f232d7ff09612987060b1f2d243b8ce1318e0670fcc78f8831c61222d32b8c`  
		Last Modified: Wed, 09 Apr 2025 01:19:13 GMT  
		Size: 194.6 MB (194557425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe2447486d86c56788eb90bfaf44025ef54f05b4c8e339e9d3b6e3f62e68021d`  
		Last Modified: Wed, 09 Apr 2025 01:19:03 GMT  
		Size: 125.4 KB (125378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102fb78643a5d0258004617e920007ef0b1cee8f154cefb79b54e49bd5f08ae3`  
		Last Modified: Wed, 09 Apr 2025 01:19:03 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
