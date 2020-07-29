## `openjdk:11-jre-nanoserver-1809`

```console
$ docker pull openjdk@sha256:3fb98df0da20e8b846a3311ed6a9ad09b33e1e189e5d47f148f7607bbbea7e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `openjdk:11-jre-nanoserver-1809` - windows version 10.0.17763.1339; amd64

```console
$ docker pull openjdk@sha256:03bc7e53f65b28796377e20a394ee37bb1f44c04a4b6f2a072c5977172ea298d
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.2 MB (140174333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea2d1e489ae433a646cf7f70dda442edebac44c31e2fa43c144fbcece3d91f32`
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
# Wed, 29 Jul 2020 01:28:53 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 29 Jul 2020 01:28:54 GMT
USER ContainerUser
# Wed, 29 Jul 2020 01:28:55 GMT
ENV JAVA_VERSION=11.0.8
# Wed, 29 Jul 2020 01:33:19 GMT
COPY dir:9d2dfaa400645982ad32c3b7350b19d788f232ed927c1fa52c11be3c2de3579a in C:\openjdk-11 
# Wed, 29 Jul 2020 01:33:36 GMT
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
	-	`sha256:0a7d3375a14db90366958677208727982a9905bdd0945a459ccc5e124fd16810`  
		Last Modified: Wed, 29 Jul 2020 01:53:12 GMT  
		Size: 67.6 KB (67602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db12785a88bc4a13edd12ed8d3ad5be8adb875de38e2eec7c636050661af2195`  
		Last Modified: Wed, 29 Jul 2020 01:53:08 GMT  
		Size: 810.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7805373b840156272bd6f8e7bd8010ff6777ee97b6e471e9b42b2c2823e010a3`  
		Last Modified: Wed, 29 Jul 2020 01:53:09 GMT  
		Size: 836.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ea7da4120f0979859c2cf440e6dd18f019a91ae6d3f56c04ccf4d3fed0f242`  
		Last Modified: Wed, 29 Jul 2020 01:54:40 GMT  
		Size: 39.1 MB (39127965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d12f731fda0e9203ed04102f3389153a604d5cfbfdf2502b6925307b4f61353`  
		Last Modified: Wed, 29 Jul 2020 01:54:32 GMT  
		Size: 78.8 KB (78820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
