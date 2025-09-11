## `eclipse-temurin:8-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:ebb79245154d7773ab72c160e7317709ad0f5282d2fc7fb1fed6d679cf70046c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `eclipse-temurin:8-nanoserver-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull eclipse-temurin@sha256:12549455fe36951ae73f5e350f7128f1d3b26438a06d5fbc1fa825bb7481b0ca
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296146917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487db34fd12df6468696139efcbbbf83aba39b0c4123fe393848172776e78ceb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Sep 2025 02:12:39 GMT
RUN Apply image 10.0.26100.6584
# Wed, 10 Sep 2025 22:19:33 GMT
SHELL [cmd /s /c]
# Wed, 10 Sep 2025 22:19:34 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Wed, 10 Sep 2025 22:19:34 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 10 Sep 2025 22:19:35 GMT
USER ContainerAdministrator
# Wed, 10 Sep 2025 22:19:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Sep 2025 22:19:38 GMT
USER ContainerUser
# Wed, 10 Sep 2025 22:19:44 GMT
COPY dir:184da149c84a7d26eb59eea9818ea043a400cd17024f2fafd00950f1891aab87 in C:\openjdk-8 
# Wed, 10 Sep 2025 22:19:47 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:a75a4ab04983f989d9a1442633d6c3952b863719a00dd77cf160f7055beaded9`  
		Last Modified: Tue, 09 Sep 2025 22:28:08 GMT  
		Size: 193.6 MB (193550846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2cfd7aa063baad8e6a02d7e7afe1257fc6436c718887a62653060f5adf6ec4`  
		Last Modified: Wed, 10 Sep 2025 22:20:51 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1333b4ee387720d860291fb145f07ed98514e296cedfef036517dcddb9e7e5ca`  
		Last Modified: Wed, 10 Sep 2025 22:20:51 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0705bf9189de97690534c1dcadd3d79ff715b241c60a956bc3da4d02600a5fb6`  
		Last Modified: Wed, 10 Sep 2025 22:20:51 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a1691b585b7a95b6a83be017a2a0470d2fdfc2bbc27b021d0f764f5c42b35a`  
		Last Modified: Wed, 10 Sep 2025 22:20:51 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cf8d0a1cae8676b73082ed05045efad2b274a2b6603057e3f79fcb8b5779a7`  
		Last Modified: Wed, 10 Sep 2025 22:20:51 GMT  
		Size: 76.9 KB (76893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a733743a022feface09b4b9a193143292760fd8faf2269296f64dd4d45b433`  
		Last Modified: Wed, 10 Sep 2025 22:20:51 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a42a54d08784530d031576045753af6669422668c3181e79e1b14963e5f3e3`  
		Last Modified: Wed, 10 Sep 2025 22:21:06 GMT  
		Size: 102.4 MB (102434600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084858fb128a75b9a3ea3b520a375de0b83d1416ab2b1be51f77ea8e807ddd36`  
		Last Modified: Wed, 10 Sep 2025 22:20:51 GMT  
		Size: 79.2 KB (79212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
