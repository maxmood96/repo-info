## `openjdk:11-nanoserver`

```console
$ docker pull openjdk@sha256:ef150a5a029aff43ea0ab093cba0765d7c9f4d719b70df4976d37548506b4a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `openjdk:11-nanoserver` - windows version 10.0.17763.1339; amd64

```console
$ docker pull openjdk@sha256:f6f69db2f28375020df55b7bb4bf167161c48cf79e62115a84f3ebdb7e0938d2
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 MB (291081104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c002feded397af9852a16ff77d698b048bc9996828f1d7c92b1f5328ea1f58a5`
-	Default Command: `["jshell"]`
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
# Thu, 16 Jul 2020 23:33:26 GMT
COPY dir:ba8f3626996a51913ed5e7f3fbcaeadaf7aaae17e19e9afdd11f176c2572b854 in C:\openjdk-11 
# Thu, 16 Jul 2020 23:33:41 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Thu, 16 Jul 2020 23:33:42 GMT
CMD ["jshell"]
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
	-	`sha256:7a4420d252cf8ab7ae40dcc4020d46272094c1b70c712a426ee387254e81a8bc`  
		Last Modified: Fri, 17 Jul 2020 00:23:29 GMT  
		Size: 190.0 MB (190038854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39522f18e782b984ef9838db0eeeab08cca8e9f2fb148d1edafebaae4e5abb4`  
		Last Modified: Fri, 17 Jul 2020 00:23:11 GMT  
		Size: 77.1 KB (77063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d561c446d6bea2ec24d78dbd8a34b69939ba0347fb7f0a8af88fc864878c973`  
		Last Modified: Fri, 17 Jul 2020 00:23:11 GMT  
		Size: 914.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
