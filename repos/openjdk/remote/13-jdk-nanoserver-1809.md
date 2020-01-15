## `openjdk:13-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:1f426aa6af0fe874ef32aae75d30f0033fd4871fc64309b4c5d67873c692971b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `openjdk:13-jdk-nanoserver-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull openjdk@sha256:a9e878496bff7e9b5c11e5a768fd3965f365d516062fb7bef2978701e8a4d91d
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295704496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6651b0fc936215b5be964fec20903943a589baa5d9f0d788f77c5e2c4e35d41`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 04 Jan 2020 07:17:17 GMT
RUN Apply image 1809-amd64
# Tue, 14 Jan 2020 23:56:11 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2020 01:15:34 GMT
ENV JAVA_HOME=C:\openjdk-13
# Wed, 15 Jan 2020 01:15:36 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2020 01:15:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 15 Jan 2020 01:15:49 GMT
USER ContainerUser
# Wed, 15 Jan 2020 01:15:51 GMT
ENV JAVA_VERSION=13.0.2
# Wed, 15 Jan 2020 01:16:55 GMT
COPY dir:9a8e1dcd5a25212e98d91ff411fe0ca991e6e2e35d98496f930933354e28449f in C:\openjdk-13 
# Wed, 15 Jan 2020 01:17:17 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Wed, 15 Jan 2020 01:17:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ee446884f7bef76f8275c2f16add1c4fb598bea2ba861e72bce8fb4aac9b55ef`  
		Size: 101.1 MB (101054324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:764e25aa4e95684bd69a4d130dc1c729bfaef95293d9c76c4d2a12ced9e3a9ac`  
		Last Modified: Wed, 15 Jan 2020 01:51:06 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc296e8c7ca0d9b11883dfbe815810a776089384271bf92cf1fd028f18043b58`  
		Last Modified: Wed, 15 Jan 2020 02:03:13 GMT  
		Size: 944.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a789ef3b67a3f7dd732ee95cd0096e2664ce129ee757d5876e2a1eed2e5be07`  
		Last Modified: Wed, 15 Jan 2020 02:03:11 GMT  
		Size: 918.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e483e85a2fe2a4d5924f31eb345c70c1840108e06c7736fca641a444d2d356`  
		Last Modified: Wed, 15 Jan 2020 02:03:12 GMT  
		Size: 67.4 KB (67416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9272a55b8bd00fa14d4926a2f910ef9de5f53f98c1971acbc01d7d6b5b5483ee`  
		Last Modified: Wed, 15 Jan 2020 02:03:09 GMT  
		Size: 943.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34190fabf0320144247d506bc99405147076f59d0b3ece5bb0a87353a215dcfd`  
		Last Modified: Wed, 15 Jan 2020 02:03:09 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d0a66e6556d24f095dddc7b322eed7ef31ebcca9c7019c3d3be3617692fcd3`  
		Last Modified: Wed, 15 Jan 2020 02:03:31 GMT  
		Size: 191.2 MB (191181861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1aa22956264b470b2dec7cdf09c363c8d8a5d29f12a722460ca34ce82a301c0`  
		Last Modified: Wed, 15 Jan 2020 02:03:10 GMT  
		Size: 3.4 MB (3395367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a728fcea61c22bf850f874bc9dbecf76bf6334d10fedfdcbef2f712bbebb4404`  
		Last Modified: Wed, 15 Jan 2020 02:03:09 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
