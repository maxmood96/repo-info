## `openjdk:11-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:c0062144463577f6593697d77771c26559b1ec663f78a6dca40f4a0184ccb373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64

### `openjdk:11-jdk-nanoserver` - windows version 10.0.17763.914; amd64

```console
$ docker pull openjdk@sha256:3f8305d1ec68251f3b2f22f6dfe00571c11e2d367e2de4c47524ebd654f3a4d7
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290893886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c9b0ced90247b0e0d29ffb16d0e16480cec7e34d3c360340f076373d8f1c38c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 28 Nov 2019 13:16:41 GMT
RUN Apply image 1809-amd64
# Wed, 11 Dec 2019 18:49:48 GMT
SHELL [cmd /s /c]
# Wed, 11 Dec 2019 19:09:14 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 11 Dec 2019 19:09:15 GMT
USER ContainerAdministrator
# Wed, 11 Dec 2019 19:09:27 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 11 Dec 2019 19:09:28 GMT
USER ContainerUser
# Wed, 11 Dec 2019 19:09:29 GMT
ENV JAVA_VERSION=11.0.5
# Wed, 11 Dec 2019 19:10:34 GMT
COPY dir:5db7c86b4aa60ed483c360e3f016d803ad91a566a85ce1f3831a8f82ff4c61c1 in C:\openjdk-11 
# Wed, 11 Dec 2019 19:10:52 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Wed, 11 Dec 2019 19:10:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1951f408509ba9ddcf240ef5d838c72c5596f97a05b063446508f2ba15d510f2`  
		Size: 101.1 MB (101106116 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:163d55b77f49371136083ba8066ddbec4afad6e1f4fbba77fa4ffebc99a8098a`  
		Last Modified: Wed, 11 Dec 2019 20:01:21 GMT  
		Size: 945.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c888c8cbd6188f8c91b3a33902c7effd7ebb9bb105c0a7044e23f919b078bb70`  
		Last Modified: Wed, 11 Dec 2019 20:10:13 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25e433628b6d53e86689094cd8d5693c4777775350065c451ed5fcd9195eb67`  
		Last Modified: Wed, 11 Dec 2019 20:10:13 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cdf60404a153e1b843d95fa2035c5a3cf74596f0b422c2bc3ea26c36fa57985`  
		Last Modified: Wed, 11 Dec 2019 20:10:13 GMT  
		Size: 67.0 KB (67034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea884077a3c82b9a836c99b4ba4604a358a7c0f4e79299aa03700b51aae91b0`  
		Last Modified: Wed, 11 Dec 2019 20:10:10 GMT  
		Size: 919.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370f7c37c71a1f020c66f281b7446fffbfda081ef5e1fc784707ba2fb7e51a93`  
		Last Modified: Wed, 11 Dec 2019 20:10:10 GMT  
		Size: 926.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a6db676733b62f2fa336fe89e08027bdddd24da50a7e84a7e1e6dcd9aa3b9d`  
		Last Modified: Wed, 11 Dec 2019 20:10:33 GMT  
		Size: 189.7 MB (189660836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfbb191b269e3165b8c5b8d0dae2e2bbe3123386b71a83fa9af45df9e0231f1`  
		Last Modified: Wed, 11 Dec 2019 20:10:10 GMT  
		Size: 54.3 KB (54328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f092a0c3bd9c2f42c69d0c815d35d5245ff372cc65052ed43c83f126ad18c6`  
		Last Modified: Wed, 11 Dec 2019 20:10:10 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
