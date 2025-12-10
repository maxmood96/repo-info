## `eclipse-temurin:21-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:2312f44c0d80324481b8b9b3c1a17edde5789fd8709087e261e7a6071b721cc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `eclipse-temurin:21-jdk-nanoserver` - windows version 10.0.26100.7462; amd64

```console
$ docker pull eclipse-temurin@sha256:bd217a98f3892e70c5974f9891a72bf7eeb4d0ab16916fd94f4c42ebba069efb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.9 MB (400855116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed0b19ff2af80dd317518ecd1618e6782c27da99dbd48eb25f3ad5173d622cf`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Dec 2025 21:31:34 GMT
RUN Apply image 10.0.26100.7462
# Tue, 09 Dec 2025 21:13:13 GMT
SHELL [cmd /s /c]
# Tue, 09 Dec 2025 21:14:49 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Tue, 09 Dec 2025 21:14:49 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 09 Dec 2025 21:14:50 GMT
USER ContainerAdministrator
# Tue, 09 Dec 2025 21:14:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Dec 2025 21:14:52 GMT
USER ContainerUser
# Tue, 09 Dec 2025 21:15:00 GMT
COPY dir:ca3f22bac3b96b31650dd9d8b46eabc8cfc824f09a5d61f04cd758713bcc4892 in C:\openjdk-21 
# Tue, 09 Dec 2025 21:15:04 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 09 Dec 2025 21:15:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a092205b76ca656d8483e99445def9f0619cb3acb2688bf9a33244c43ad44ce`  
		Last Modified: Tue, 09 Dec 2025 22:15:12 GMT  
		Size: 198.9 MB (198873947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c3e9ac772555dbb907a48e4dcac3181c5961b789f6ef74dc9cf30cd0cc60ba`  
		Last Modified: Tue, 09 Dec 2025 21:14:21 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870b9b6bd74ee638fa61ee8d0fd1a32023c54a682589232d93d656d8838eab16`  
		Last Modified: Tue, 09 Dec 2025 21:15:30 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0eb29b90adeae3d9616e6eec9db4d32987261a9e516d2a6752adcc7a00c8ea`  
		Last Modified: Tue, 09 Dec 2025 21:15:30 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1f7f2d1d77cbd0c08233a30b1feaf66aaaa4168d30905364e8aba28467748a`  
		Last Modified: Tue, 09 Dec 2025 21:15:31 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8b78eb05c749433260b47e477291dcda6a5802988852201630de0890d4ec04`  
		Last Modified: Tue, 09 Dec 2025 21:15:30 GMT  
		Size: 73.5 KB (73453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31160b86f959c821aeeb1d7160ad7eacdb61e9f76d7a3ba5009290780430450`  
		Last Modified: Tue, 09 Dec 2025 21:15:30 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5504ffb0e98dbdb2bf5f6de3269e9284afed082413505c7c5d75eb80dfe5045f`  
		Last Modified: Tue, 09 Dec 2025 21:15:23 GMT  
		Size: 201.8 MB (201782599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1008cf0ed26e7ab76ab5d21ecee825f12121bfd8a10597f538032037397a1cd`  
		Last Modified: Tue, 09 Dec 2025 21:15:30 GMT  
		Size: 118.6 KB (118649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7054842c9da3298a653e8973ce2c4384edb703daa0a3be2ec449a7f022119113`  
		Last Modified: Tue, 09 Dec 2025 21:15:30 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jdk-nanoserver` - windows version 10.0.20348.4529; amd64

```console
$ docker pull eclipse-temurin@sha256:098172f556d4b36f18c0ca260ff0a948bf28fe81db19b8968a98106031c50e0a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.3 MB (328339647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00441a429125faae610ace052488a87cb6d48881064f6559f1f35698b1a23c55`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 09 Dec 2025 21:12:08 GMT
SHELL [cmd /s /c]
# Tue, 09 Dec 2025 21:13:03 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Tue, 09 Dec 2025 21:13:04 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 09 Dec 2025 21:13:05 GMT
USER ContainerAdministrator
# Tue, 09 Dec 2025 21:13:08 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Dec 2025 21:13:08 GMT
USER ContainerUser
# Tue, 09 Dec 2025 21:13:45 GMT
COPY dir:ca3f22bac3b96b31650dd9d8b46eabc8cfc824f09a5d61f04cd758713bcc4892 in C:\openjdk-21 
# Tue, 09 Dec 2025 21:13:49 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 09 Dec 2025 21:13:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e4bbd94f6866974611ee8943ff09ce009d2d821f9047398dbedef687b98c2d`  
		Last Modified: Tue, 09 Dec 2025 21:12:35 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d986ddf334e195fc05ece92b133c8f96b156c554af43d607292ca237e8633940`  
		Last Modified: Tue, 09 Dec 2025 21:14:21 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d9fec8feb22dfadb14236b29e435132daaa367daa4139f98ddcaa1a0e5be53`  
		Last Modified: Tue, 09 Dec 2025 21:14:21 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e917682a2997cad31861acad7f238d218b3f363234ea40da46edd87821d8e5`  
		Last Modified: Tue, 09 Dec 2025 21:14:21 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c159b5bb6747ba123a82dcec3f22ddac41fa92673fa9ff6f9c09968779445b`  
		Last Modified: Tue, 09 Dec 2025 21:14:21 GMT  
		Size: 88.6 KB (88583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d2359ba29c8f1fc8f17f27c29ae237d84d62d305f6168b4f7821af51aa93b1`  
		Last Modified: Tue, 09 Dec 2025 21:14:21 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1da70834feec40e864a55a6d3b74921cd22d772be614abf76698a3943754bd`  
		Last Modified: Tue, 09 Dec 2025 22:15:41 GMT  
		Size: 201.8 MB (201782562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbaf81a15c09477cc66db144f49e9f9b4539980b8ede9152f0fc4115c0cedb9`  
		Last Modified: Tue, 09 Dec 2025 21:14:21 GMT  
		Size: 103.9 KB (103869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd817f6f7682656274041f697ec70659d7fcfc9f4e703ef715e2b53554e880b`  
		Last Modified: Tue, 09 Dec 2025 21:14:21 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
