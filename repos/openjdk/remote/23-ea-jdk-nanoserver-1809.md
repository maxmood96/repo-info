## `openjdk:23-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:36ac5593d75bd8cb855314954d2b017ae27443b2f27ad0d36db760bf2870d37b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `openjdk:23-ea-jdk-nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull openjdk@sha256:5fe97ed7d93e196899868a3642a7a9e074b82ee07126956e1bc2abeda7c97030
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.0 MB (306027512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33ee1214672c60fcb6f78ac41845d93a49f9000f729d05260441d4f4da605f3c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Sat, 27 Jan 2024 00:53:19 GMT
SHELL [cmd /s /c]
# Sat, 27 Jan 2024 00:53:20 GMT
ENV JAVA_HOME=C:\openjdk-23
# Sat, 27 Jan 2024 00:53:20 GMT
USER ContainerAdministrator
# Sat, 27 Jan 2024 00:53:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 27 Jan 2024 00:53:30 GMT
USER ContainerUser
# Sat, 27 Jan 2024 00:53:30 GMT
ENV JAVA_VERSION=23-ea+7
# Sat, 27 Jan 2024 00:53:39 GMT
COPY dir:2c11acea4e299cf5d5c1f452d0e7bdb3c3c890ad6a0f55a6287bce434311dfd8 in C:\openjdk-23 
# Sat, 27 Jan 2024 00:53:47 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 27 Jan 2024 00:53:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497ead4634e0772137e0ed3db1304a5ab89ff695e9eb92fba040859a0c4ffeac`  
		Last Modified: Sat, 27 Jan 2024 00:53:56 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ffee95a3a7c180ae6b6af4bb51d677527a885dc6d9ff8d9b2c7fd669a0c3df2`  
		Last Modified: Sat, 27 Jan 2024 00:53:54 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290cc3c1148306ccf48c5bf43311455d3deb3ce8266133846f9fc3257fdf1e87`  
		Last Modified: Sat, 27 Jan 2024 00:53:54 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7d9f5b6753aa2b8fd5e3d51b1894618154774bc2fe808794d6e1a77f32a321`  
		Last Modified: Sat, 27 Jan 2024 00:53:54 GMT  
		Size: 68.0 KB (67962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41447096f6743dec8007893a8e43a34a7165aa0c5e9992059c34e0077a7284f`  
		Last Modified: Sat, 27 Jan 2024 00:53:52 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ee129849f0b71fde33951020a75651e561399b5fe04e07f229f7d5c6e098d2`  
		Last Modified: Sat, 27 Jan 2024 00:53:52 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb76f3b82ac266421d58d17e9bb6a1b8f3b2839e74c266d9f0894445903a6d7`  
		Last Modified: Sat, 27 Jan 2024 00:54:03 GMT  
		Size: 197.5 MB (197501504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c63e90f0d672ff2460711d70f00bc5b0a7ecb931291d1076cba6d35804722ba`  
		Last Modified: Sat, 27 Jan 2024 00:53:53 GMT  
		Size: 3.9 MB (3860597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd1bfa4d19e173375600fb59b10c16e8189c020b8b32882a08785c939e5a134`  
		Last Modified: Sat, 27 Jan 2024 00:53:52 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
