## `openjdk:25-rc-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:f70d87eb08e599917e02a08ae0217ce7c21d36c7aae05f9cdc288ce899828383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `openjdk:25-rc-nanoserver-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull openjdk@sha256:67a901f754a1a3397ad3305c16f7107ede855afdabbc8602f316db114aa4ed81
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.3 MB (412300581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9235ae94769b0682211626d873a14b85b652689be859dadc6963b9347387e0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Sep 2025 02:12:39 GMT
RUN Apply image 10.0.26100.6584
# Wed, 10 Sep 2025 22:19:29 GMT
SHELL [cmd /s /c]
# Wed, 10 Sep 2025 22:21:27 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 10 Sep 2025 22:21:27 GMT
USER ContainerAdministrator
# Wed, 10 Sep 2025 22:21:28 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 Sep 2025 22:21:29 GMT
USER ContainerUser
# Wed, 10 Sep 2025 22:21:29 GMT
ENV JAVA_VERSION=25
# Wed, 10 Sep 2025 22:21:38 GMT
COPY dir:af1d593aa380a5189ac7ad7e58ca0fcfe62de322216fccee65cb868225e0c49a in C:\openjdk-25 
# Wed, 10 Sep 2025 22:21:43 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 10 Sep 2025 22:21:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a75a4ab04983f989d9a1442633d6c3952b863719a00dd77cf160f7055beaded9`  
		Last Modified: Tue, 09 Sep 2025 22:28:08 GMT  
		Size: 193.6 MB (193550846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:405e4f0a195de15bbe1dd36da41bdd9fe1bbc1c1080c2dcabfc4f6e553e3ba2c`  
		Last Modified: Wed, 10 Sep 2025 23:08:32 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59ea069936131ad5e3db6a28faa9e426fde98a5eba67aced92dd6562be9a8f1`  
		Last Modified: Wed, 10 Sep 2025 22:22:31 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34db6cf081084173fd5e7ad1465eab86f9cb69982a2f0d02cca7f19ba16ea169`  
		Last Modified: Wed, 10 Sep 2025 22:22:32 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0738d7c897b85b736a05985c54fec0bba7f469b8b56319c8dee37241b8d762`  
		Last Modified: Wed, 10 Sep 2025 22:22:32 GMT  
		Size: 71.9 KB (71910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2f1926591a3473ea5260d165d75b8d9b33535b6b5118e2c5da5361a168d61e`  
		Last Modified: Wed, 10 Sep 2025 22:22:31 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e468210207b39218ca8ab64837b3a42813651917c7f026a74446cbbb51b3058`  
		Last Modified: Wed, 10 Sep 2025 22:22:32 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c87daf802996240bcafaabdfa6acd19d02cc7a070c74bfc2d46f55465fc834e`  
		Last Modified: Thu, 11 Sep 2025 00:24:07 GMT  
		Size: 218.6 MB (218553106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b0e8e0bd46be7050678dd7e1c1d6c6c6f7f96536bc872e5ae501e4c437817ff`  
		Last Modified: Wed, 10 Sep 2025 22:22:32 GMT  
		Size: 118.3 KB (118269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:725dea058d00fa9941b38d39fa2d356ffb4dc75dc4756dcb6f91cb6a9373ad69`  
		Last Modified: Wed, 10 Sep 2025 22:22:31 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
