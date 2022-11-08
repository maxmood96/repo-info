## `eclipse-temurin:19-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:fd4ee72c3348d3c800e7e5d39483bfa71b727f7d9157e9a63c5a052dd76082ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1249; amd64

### `eclipse-temurin:19-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.1249; amd64

```console
$ docker pull eclipse-temurin@sha256:52d5d19d2a43c7b1b5d2b882e264f39038f50930eebe73d28a5b5bdbca3ab252
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.7 MB (315711886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0859b068695eadde37236a9e157a406e9e76ddac4171f9e113028ac8ac1b6ebe`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Nov 2022 07:21:30 GMT
RUN Apply image 10.0.20348.1249
# Tue, 08 Nov 2022 19:27:23 GMT
SHELL [cmd /s /c]
# Tue, 08 Nov 2022 19:34:05 GMT
ENV JAVA_VERSION=jdk-19.0.1+10
# Tue, 08 Nov 2022 19:34:06 GMT
ENV JAVA_HOME=C:\openjdk-19
# Tue, 08 Nov 2022 19:34:07 GMT
USER ContainerAdministrator
# Tue, 08 Nov 2022 19:34:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 08 Nov 2022 19:34:21 GMT
USER ContainerUser
# Tue, 08 Nov 2022 19:34:39 GMT
COPY dir:2282de048661e89f3c315adc23c8954e0ca245f9a969462117712d8342758a69 in C:\openjdk-19 
# Tue, 08 Nov 2022 19:35:10 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 08 Nov 2022 19:35:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:72e5d750fe8c1a32d4a26ef3b4a4e1f6124ac079b142f12724af2abfcba1c8b3`  
		Last Modified: Tue, 08 Nov 2022 19:57:58 GMT  
		Size: 122.1 MB (122092167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd83067a7e6c6d9dab3ac0265a21919de95a0bf4e737e647fbf3e43c9874b0`  
		Last Modified: Tue, 08 Nov 2022 19:57:27 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc58ee776ee996bbdb4b7704f470c9d773da6812227c768764de2ae387772b4e`  
		Last Modified: Tue, 08 Nov 2022 20:00:21 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fcaa2ceb7ce7d67710f68c8fe3b5c1ad6b524bf25773e6e07f3b98770005ab`  
		Last Modified: Tue, 08 Nov 2022 20:00:21 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:125e8573df5b799214f6e9f9ebd6861e86b7f7fbe7080034f95d58b0fa1cda57`  
		Last Modified: Tue, 08 Nov 2022 20:00:21 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefe11d7fe70a6ec9787dcd7928a0a3ac1f15aebc23fd271489479520c900938`  
		Last Modified: Tue, 08 Nov 2022 20:00:23 GMT  
		Size: 81.1 KB (81081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095f561971d7be3547ea865cc72e4f4decb14abf6bc0af5e6ecaaac0b9f10566`  
		Last Modified: Tue, 08 Nov 2022 20:00:19 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e695854cbdf9b093d908bb2bc7e2d827b948deb7d941623ab2eab5935cf19a4`  
		Last Modified: Tue, 08 Nov 2022 20:00:41 GMT  
		Size: 193.4 MB (193445628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532a208a30b7f7cd8dd206171f4b387fbb9c284b0caca687c302d9c8786e8970`  
		Last Modified: Tue, 08 Nov 2022 20:00:19 GMT  
		Size: 86.1 KB (86068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0736f7aa57dff9910017c9daadbc1cd9e29e3b50f053bf32c76ee83c73e67d40`  
		Last Modified: Tue, 08 Nov 2022 20:00:19 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
