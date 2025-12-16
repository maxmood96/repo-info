## `openjdk:26-ea-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:64aa27003de247785f8b828f1accd7e1360c673f4d1eb1667a5018efd3ecb2d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `openjdk:26-ea-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull openjdk@sha256:1a1664c45ce829b48bfbb09a9b3027cefc44ca0ca183596d59887b5a0d0f96cf
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.4 MB (350354213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f39722aab2d7608ce99bd7c8a9fa0c412fcabfcac43b458bba329c5f58b5764`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 16 Dec 2025 01:09:34 GMT
SHELL [cmd /s /c]
# Tue, 16 Dec 2025 01:09:35 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 16 Dec 2025 01:09:36 GMT
USER ContainerAdministrator
# Tue, 16 Dec 2025 01:09:43 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 16 Dec 2025 01:09:44 GMT
USER ContainerUser
# Tue, 16 Dec 2025 01:09:44 GMT
ENV JAVA_VERSION=26-ea+28
# Tue, 16 Dec 2025 01:11:14 GMT
COPY dir:eacc860438b809f9859b19e16ae39a947eb51a2178590a6f10254cdc1bcc414c in C:\openjdk-26 
# Tue, 16 Dec 2025 01:11:18 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 16 Dec 2025 01:11:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1534c7635137aae9170bdf1c71b679926ddb9fe813e926158a336cb217fd1d85`  
		Last Modified: Tue, 16 Dec 2025 01:12:24 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d428a5c454ac7ae01c53db0626e9d8230d3f0f04eeca27bf7b3881ee58f10d68`  
		Last Modified: Tue, 16 Dec 2025 01:12:24 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581bf41afe080927253db1cab89ebc70efef2c14a42ca627f9efd694b8574273`  
		Last Modified: Tue, 16 Dec 2025 01:12:24 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400db2004eaff1ed159a420b62722411b74e70308f10fae27e392e647361f799`  
		Last Modified: Tue, 16 Dec 2025 01:12:24 GMT  
		Size: 65.5 KB (65455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4746aa5035b6788ada4f7632079cd07b269c77aca6fb07ef6f7cc2fd9add921`  
		Last Modified: Tue, 16 Dec 2025 01:12:24 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3071320c70dd29652f1f3632016ece1572d218c8b0a7de739f0c8b1ce8661170`  
		Last Modified: Tue, 16 Dec 2025 01:12:24 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25c0bc1b5f938f5bf48bce75866ad380d9f2b79275b198664e15fb8985d6391`  
		Last Modified: Tue, 16 Dec 2025 01:12:43 GMT  
		Size: 223.8 MB (223831325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b908b3a7d6c39d215914ce8c33c302ad63353e80c2e31879230bf24097ea4fc`  
		Last Modified: Tue, 16 Dec 2025 01:12:24 GMT  
		Size: 92.7 KB (92670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:433b72fc9a86cea0757772f2d9f51b45c5e058a59ed62620c0f860be876f3a12`  
		Last Modified: Tue, 16 Dec 2025 01:12:24 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
