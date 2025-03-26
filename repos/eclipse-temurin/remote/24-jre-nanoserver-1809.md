## `eclipse-temurin:24-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:4ec76f772f0eef2856da7c3a96da4669b62baebef6e3914a2ef6e5013ad56059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `eclipse-temurin:24-jre-nanoserver-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull eclipse-temurin@sha256:18287b19009c453389840241bbe676a5c0a074c9a9933e37208f04b31a14d809
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168584110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e61d42e037db37dac87b24caf2d5dd5300d226841c9e3e74eb5bacfbab08b35`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Tue, 25 Mar 2025 23:18:27 GMT
SHELL [cmd /s /c]
# Tue, 25 Mar 2025 23:18:29 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 23:18:30 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 25 Mar 2025 23:18:30 GMT
USER ContainerAdministrator
# Tue, 25 Mar 2025 23:18:33 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 25 Mar 2025 23:18:34 GMT
USER ContainerUser
# Tue, 25 Mar 2025 23:18:39 GMT
COPY dir:90c9828944ffcd2978afe702f80884cbf787022d7dcd7becc7c91cd2ab6f7dd5 in C:\openjdk-24 
# Tue, 25 Mar 2025 23:18:42 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d42a0811c09bb7f0cc287a9b055a55a251e1639a924bcd1217ff35bcb1fa77a3`  
		Last Modified: Tue, 25 Mar 2025 23:18:46 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162977662480aec0e59d689b90cd91db862f5459e0e2fedab921c8e143c07040`  
		Last Modified: Tue, 25 Mar 2025 23:18:46 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30aefc727fb4e9f6733e0b4ed73dbbcef05d3edbcddd469f8dde64450c1f2c5c`  
		Last Modified: Tue, 25 Mar 2025 23:18:46 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dc45bc7581625cb5c1227ed95e921ec5f8181e3ac6dc0eedff82aa06068014`  
		Last Modified: Tue, 25 Mar 2025 23:18:45 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf563a55f51833614596eb35bfa0b6f0f6a8947d72ccc1fecd5c1cb11af1841`  
		Last Modified: Tue, 25 Mar 2025 23:18:45 GMT  
		Size: 70.3 KB (70285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc65f99a24cf7764374e24ec5911536994f58f83c9f3922b741522a7d94b4a85`  
		Last Modified: Tue, 25 Mar 2025 23:18:45 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b359a30bd1d01353d142067fb8e72dce94ac44cb58eb2e800d47417b117bf1`  
		Last Modified: Tue, 25 Mar 2025 23:18:52 GMT  
		Size: 57.7 MB (57700848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60ea89829296b5810e00af267a460d679d88530377780e1542a455eab8f9aaa`  
		Last Modified: Tue, 25 Mar 2025 23:18:45 GMT  
		Size: 3.9 MB (3899992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
