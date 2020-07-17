## `openjdk:11-jre-nanoserver-1809`

```console
$ docker pull openjdk@sha256:9c0a29532ecbc6e0408cd698370c3726344c6c7b6dbad56382ce6e8d089a8dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `openjdk:11-jre-nanoserver-1809` - windows version 10.0.17763.1339; amd64

```console
$ docker pull openjdk@sha256:0da19ae1574bd97e99e961e93aed79aea61d790f9cfcb39398a78eeed4e20b5c
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.2 MB (140168746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0744b0a5111449da61e0faae13eec00d53b8ee63c6ce0933b42e70c190828a0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 07 Jul 2020 13:50:07 GMT
RUN Apply image 1809-amd64
# Wed, 15 Jul 2020 01:54:43 GMT
SHELL [cmd /s /c]
# Wed, 15 Jul 2020 02:21:21 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 15 Jul 2020 02:21:22 GMT
USER ContainerAdministrator
# Wed, 15 Jul 2020 02:21:33 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 15 Jul 2020 02:21:34 GMT
USER ContainerUser
# Thu, 16 Jul 2020 23:32:31 GMT
ENV JAVA_VERSION=11.0.8
# Thu, 16 Jul 2020 23:47:44 GMT
COPY dir:9d2dfaa400645982ad32c3b7350b19d788f232ed927c1fa52c11be3c2de3579a in C:\openjdk-11 
# Thu, 16 Jul 2020 23:47:57 GMT
RUN echo Verifying install ... 	&& echo   java --version && java --version
```

-	Layers:
	-	`sha256:dc95608099543221ef539391bfece5c1ce37b97af9da457f5990349cab028a12`  
		Size: 100.9 MB (100895619 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9f6486e4debac36806ed3527d9b1baea75c1a807e26baccdd0a2f521c814273f`  
		Last Modified: Wed, 15 Jul 2020 02:43:55 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1edf2cf232929022745a17a752c11091206fd6804fbcd0deb0cf94f65d838e43`  
		Last Modified: Wed, 15 Jul 2020 02:51:37 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34289060bcecad92a4781d988ddd844d829452e51a1c73c3f2608a0a6085c77`  
		Last Modified: Wed, 15 Jul 2020 02:51:37 GMT  
		Size: 909.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78522c618af5554ffd3adf8623d7933e1792428e86ad573127cee6fdc3a590d`  
		Last Modified: Wed, 15 Jul 2020 02:51:37 GMT  
		Size: 64.2 KB (64206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5608ac22c3f2ef90c8c5bc20a0fe2c584d51c075fe6bf2a5b7509df4c32d755d`  
		Last Modified: Wed, 15 Jul 2020 02:51:35 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e39d6fa7bbce16b7f6757e366671ba696877e7e67f0313fd1c65da7b97ac503`  
		Last Modified: Fri, 17 Jul 2020 00:23:12 GMT  
		Size: 872.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02501e083eb067ff8428685a205ae6b07a6aa7e3d616d3588065a260bf4a12e6`  
		Last Modified: Fri, 17 Jul 2020 00:24:34 GMT  
		Size: 39.1 MB (39127965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d310bea2ecc4d65564fe83c81208ca112ba23172d27f90db8d61d9b7668df2`  
		Last Modified: Fri, 17 Jul 2020 00:24:13 GMT  
		Size: 76.5 KB (76508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
