## `eclipse-temurin:24-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:821c5b942db47d83a9503b0afedfd796c9fd4a50f9aecbcd4bb988a4f7814ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `eclipse-temurin:24-jdk-nanoserver-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull eclipse-temurin@sha256:a0553dbe1c4406e7c4b677c1f915fddee600fbf45d9992129a0b4ccb73f62fda
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.7 MB (248740091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c2c8d17ce2a1307d0c67396ed39a2426b2290146e8afad638e402877e0b623`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Tue, 25 Mar 2025 23:14:57 GMT
SHELL [cmd /s /c]
# Tue, 25 Mar 2025 23:15:00 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 23:15:00 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 25 Mar 2025 23:15:01 GMT
USER ContainerAdministrator
# Tue, 25 Mar 2025 23:15:03 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 25 Mar 2025 23:15:04 GMT
USER ContainerUser
# Tue, 25 Mar 2025 23:15:11 GMT
COPY dir:82098476e422c0fd1b27846be91131b5a5073542830e51603132b80cd94d4318 in C:\openjdk-24 
# Tue, 25 Mar 2025 23:15:17 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 25 Mar 2025 23:15:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d870e42e7f6c7d99a4db68ec41feb180a4f0eb340ba043353d93752fc4aa5f3`  
		Last Modified: Tue, 25 Mar 2025 23:15:23 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1863918c094b9495e054f76ec871fb75161dedaae8fc03ffed0f6e414952833a`  
		Last Modified: Tue, 25 Mar 2025 23:15:22 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e89ee47c80546632a1b01a7ad5a332f48d1645836837b9200fea8e4e9fb944`  
		Last Modified: Tue, 25 Mar 2025 23:15:22 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc4a27e48af860be19436024decfab0152b011ef1ebc390e11d8d11ced061a3`  
		Last Modified: Tue, 25 Mar 2025 23:15:22 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb6875e454342557657bbb77921bb05e0af7d038946343eb435260340035648`  
		Last Modified: Tue, 25 Mar 2025 23:15:21 GMT  
		Size: 69.8 KB (69753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3a49255455a5ebeafcdf8db812a0e1e71f834773641c89c0f2c41ccd47c46f`  
		Last Modified: Tue, 25 Mar 2025 23:15:21 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb71b271686991f336591f6e191f7665b6ced81a998f829cce05005940af9ca`  
		Last Modified: Tue, 25 Mar 2025 23:15:32 GMT  
		Size: 137.4 MB (137354928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13a0676d6fdbef7bdedf6cd62b48d6b84a9bbc20d1caa2aa864740e5fcacebf`  
		Last Modified: Tue, 25 Mar 2025 23:15:21 GMT  
		Size: 4.4 MB (4401317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4865b5f4e44b21eaebd875f1faeeeb14ca7dfbee5d9687c5c86064e98844d597`  
		Last Modified: Tue, 25 Mar 2025 23:15:21 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
