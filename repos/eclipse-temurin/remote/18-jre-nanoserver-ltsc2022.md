## `eclipse-temurin:18-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:614b64ad7860c305abba03599838e3872d98a1cc3bd5943e20168c595ec0fed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.887; amd64

### `eclipse-temurin:18-jre-nanoserver-ltsc2022` - windows version 10.0.20348.887; amd64

```console
$ docker pull eclipse-temurin@sha256:e5e387d299266f2983421959771e3c47010e8666b1f92d9792d5cf10fce1765a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.4 MB (161388420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bba8d5d0e98ae3f294c8168e56504261d01fa002228a7c14d8a4485b1c4d7c4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Aug 2022 18:05:23 GMT
RUN Apply image 10.0.20348.887
# Wed, 10 Aug 2022 16:28:17 GMT
SHELL [cmd /s /c]
# Wed, 10 Aug 2022 16:33:50 GMT
ENV JAVA_VERSION=jdk-18.0.2+9
# Wed, 10 Aug 2022 16:33:51 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 10 Aug 2022 16:33:52 GMT
USER ContainerAdministrator
# Wed, 10 Aug 2022 16:34:03 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Aug 2022 16:34:04 GMT
USER ContainerUser
# Wed, 10 Aug 2022 16:34:49 GMT
COPY dir:cb1a0a94a679a671d2c9a1c60ff27dfac7a1768220183b4bef29235250155a74 in C:\openjdk-18 
# Wed, 10 Aug 2022 16:35:04 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:2ebf439f800cd4c1fccaf4a0545e6bff60caa5141295c8ab81f6c525073c423d`  
		Size: 118.1 MB (118088450 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5f1e06146ab0490d235fe89786637467a4b71853ee428e8740ea6efbc536c47c`  
		Last Modified: Wed, 10 Aug 2022 16:48:40 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f13999e9467c86cf2ef854733e78081046c1b26eaee3ab579f32308a22ad3f2`  
		Last Modified: Wed, 10 Aug 2022 16:50:57 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:984aadb5c294a031eb9bf139e089a14953bfd160b9e3fb63c5407283f238f4b0`  
		Last Modified: Wed, 10 Aug 2022 16:50:57 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b8e890683ee09a276afb5655197ed4536d7af93add242ec3ef49a79370b553`  
		Last Modified: Wed, 10 Aug 2022 16:50:57 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b0017fc6b7e0fc882e7f2169bdf28cd916bdd5becfc60b3660f256cd4bdeb7f`  
		Last Modified: Wed, 10 Aug 2022 16:50:55 GMT  
		Size: 84.8 KB (84820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5484fbab0fb42fe9cd48851c5207ac52537278b619798735df6ce414ff445b`  
		Last Modified: Wed, 10 Aug 2022 16:50:54 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0f0b9a62b6682a7362cf0eff3a58b5ef3604486f703f2ba6479604b3fc2e4a`  
		Last Modified: Wed, 10 Aug 2022 16:51:34 GMT  
		Size: 43.1 MB (43147480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f97cf57fefcfa8f573df62a2c9554d3f25131561b0f4be44d0bd3bcbaedaffa`  
		Last Modified: Wed, 10 Aug 2022 16:51:26 GMT  
		Size: 61.9 KB (61850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
