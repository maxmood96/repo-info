## `openjdk:11-jre-nanoserver`

```console
$ docker pull openjdk@sha256:4fa018cf4c6e6b385fd7a7cc4689a1e67252cdf9bdbe4517d7a7f561df27bf32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `openjdk:11-jre-nanoserver` - windows version 10.0.17763.2300; amd64

```console
$ docker pull openjdk@sha256:a46ecc6dc1cb0a1c1c740312b6124a361d08fab3f0a7ae025d5185dc27e8b4ec
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142324567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48eab004958b6e413672cdb926b3cbf2a5dd0c6db9b18c93fc7becaa1f459b7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:13:20 GMT
SHELL [cmd /s /c]
# Wed, 10 Nov 2021 20:46:15 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 10 Nov 2021 20:46:16 GMT
USER ContainerAdministrator
# Wed, 10 Nov 2021 20:46:23 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 Nov 2021 20:46:24 GMT
USER ContainerUser
# Wed, 10 Nov 2021 20:46:25 GMT
ENV JAVA_VERSION=11.0.13
# Wed, 10 Nov 2021 20:50:19 GMT
COPY dir:63916d6bee2220e36f2a9872b4f6dbefd913ce14199f5f87aa18e7a5987717fa in C:\openjdk-11 
# Wed, 10 Nov 2021 20:50:31 GMT
RUN echo Verifying install ... 	&& echo   java --version && java --version 	&& echo Complete.
```

-	Layers:
	-	`sha256:b9dc943b4e8df8f472d444248152fa0920172ec630a60ada316e1603600dd1c7`  
		Size: 102.8 MB (102782944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e60ec86b90e1492e0e0ed2cbebcf624990a34862e24207343fd85b84b3544c8e`  
		Last Modified: Wed, 10 Nov 2021 18:01:59 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0258b006591e3ca818e6cbd67031e5cd910c8bbb5ddc2e2f8b105abdb91e059`  
		Last Modified: Wed, 10 Nov 2021 21:26:13 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f788350c94df9811eba0cdf89656b7aabb171110642c8bb7ef37f649dd94c412`  
		Last Modified: Wed, 10 Nov 2021 21:26:12 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e0bee83cf42384d1e701316291c2ef834fab8a44d6170338c42051fbeb5129`  
		Last Modified: Wed, 10 Nov 2021 21:26:12 GMT  
		Size: 73.5 KB (73496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b6565fe586092981ff06465bf3d3164be60e8875cc5a80fa47ffe2e25adde6`  
		Last Modified: Wed, 10 Nov 2021 21:26:10 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ce91426a365ddf1d65111c01172ef97384f119148d4e1326cfb0d587469ffc`  
		Last Modified: Wed, 10 Nov 2021 21:26:11 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4663a9edca55da45e3e4b1b30d54e28b3df88179bcfed8cf69a96ff812a23248`  
		Last Modified: Wed, 10 Nov 2021 21:30:52 GMT  
		Size: 39.4 MB (39419298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c7220a84fc2e2fef2102a4bc970b707ae1cf8336e9bf11bf943c73537e3dde`  
		Last Modified: Wed, 10 Nov 2021 21:30:45 GMT  
		Size: 43.5 KB (43455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
