## `openjdk:13-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:7d3a31f7ba719149c07f4be5ccd7c196b16d97e823e9080cbff9c94e73979005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64

### `openjdk:13-jdk-nanoserver-1809` - windows version 10.0.17763.914; amd64

```console
$ docker pull openjdk@sha256:d1bcc1d03a7c9374464bf22819e3b49d628a59ca0afaac355c5048f2f51741ec
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295747634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266df759bbf5bf32255b98449f93768cb10d04175246cd03cb448774c7e12c81`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 28 Nov 2019 13:16:41 GMT
RUN Apply image 1809-amd64
# Wed, 11 Dec 2019 18:49:48 GMT
SHELL [cmd /s /c]
# Wed, 11 Dec 2019 18:59:01 GMT
ENV JAVA_HOME=C:\openjdk-13
# Wed, 11 Dec 2019 18:59:02 GMT
USER ContainerAdministrator
# Wed, 11 Dec 2019 18:59:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 11 Dec 2019 18:59:15 GMT
USER ContainerUser
# Wed, 11 Dec 2019 18:59:17 GMT
ENV JAVA_VERSION=13.0.1
# Wed, 11 Dec 2019 19:00:13 GMT
COPY dir:06ac5270bbe8c04999154de58a6424d5e06055ec1cc554443ad497420d28c2e4 in C:\openjdk-13 
# Wed, 11 Dec 2019 19:00:34 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Wed, 11 Dec 2019 19:00:36 GMT
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
	-	`sha256:74ede0760636291a2af717db34b4e63eab8bf7f51ce462de5b109d73b015c742`  
		Last Modified: Wed, 11 Dec 2019 20:05:59 GMT  
		Size: 917.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22a597f51b9c7412f7c3ccf84608abdcf940ab3cfdb33bc9ce8e23422616774`  
		Last Modified: Wed, 11 Dec 2019 20:05:58 GMT  
		Size: 943.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbadaafd74b5a51c53ab8f75d62fe937f824e39bce6c02374209018deacb933e`  
		Last Modified: Wed, 11 Dec 2019 20:05:58 GMT  
		Size: 66.1 KB (66072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25d6bb485cba9e7b1aac7fc748c8e5a1dec4092e5895757cc2085b06d7ab956`  
		Last Modified: Wed, 11 Dec 2019 20:05:56 GMT  
		Size: 952.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fcf65f28548d5841cb0abf4a1b62ea1a6b7e4dde55e213d32ec615f38ce188d`  
		Last Modified: Wed, 11 Dec 2019 20:05:55 GMT  
		Size: 919.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4feefabf96690e630564ab43796365b28579aaa24e0fc22ee5300af383d74dbb`  
		Last Modified: Wed, 11 Dec 2019 20:06:17 GMT  
		Size: 191.2 MB (191173241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bb4702291543da2e1d7066a18eed0cc5851c79571e363e3fee1834c44644b5`  
		Last Modified: Wed, 11 Dec 2019 20:05:56 GMT  
		Size: 3.4 MB (3396611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e426fd8f35778ab863479d436ec7b652b48f28b8212b1174859f90d952a95b9`  
		Last Modified: Wed, 11 Dec 2019 20:05:55 GMT  
		Size: 918.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
