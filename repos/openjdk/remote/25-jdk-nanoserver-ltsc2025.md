## `openjdk:25-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:9b47e5d4d7acd30b4752a3e2f459feaf21ebf22c40e470c9ac126032d8081fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `openjdk:25-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull openjdk@sha256:dae59f0a703012a0e9708cf0a7848ab52405a12aa7c75731cda0f55279a6adff
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.5 MB (413469265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5604521b977f302b234174163f78b4da2ed11accaed450775e59adc4e030968`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 08 Feb 2025 22:31:47 GMT
RUN Apply image 10.0.26100.3194
# Mon, 10 Mar 2025 22:15:46 GMT
SHELL [cmd /s /c]
# Mon, 10 Mar 2025 22:15:47 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 10 Mar 2025 22:15:48 GMT
USER ContainerAdministrator
# Mon, 10 Mar 2025 22:15:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 10 Mar 2025 22:15:52 GMT
USER ContainerUser
# Mon, 10 Mar 2025 22:15:53 GMT
ENV JAVA_VERSION=25-ea+13
# Mon, 10 Mar 2025 22:16:01 GMT
COPY dir:41adcea28f6e8239eac0b74c19049c5daef67ad138ba9db7bdf8df0acc8b0b9b in C:\openjdk-25 
# Mon, 10 Mar 2025 22:16:08 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 10 Mar 2025 22:16:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e075dd07cbf907b7da8dbd8365b73a71ac92a834b78f520bd976cb97e0fcc0a1`  
		Last Modified: Wed, 12 Feb 2025 22:34:59 GMT  
		Size: 205.9 MB (205890263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6384975e3c826b0d7168f7d1234bbc540f11efb184206b1fdfa88ea5bb28bd1`  
		Last Modified: Mon, 10 Mar 2025 22:16:12 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a7473dbe7a78cc9a4b05ae5664fc9a1231ebcde4c043f75836a92883616ac10`  
		Last Modified: Mon, 10 Mar 2025 22:16:12 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f841f40725853d2cf06f48c366d2b2024f67b9fc8affe7bc22f7c767170161`  
		Last Modified: Mon, 10 Mar 2025 22:16:12 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be311aa95923e557c660c3e2cfe6d1e2af3d88dafe93898a60d808db3724130`  
		Last Modified: Mon, 10 Mar 2025 22:16:12 GMT  
		Size: 77.3 KB (77343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9269698873f93d2d6c2fcf918b22f538dfc35cdc8c4796ad92553e4e4ba72f`  
		Last Modified: Mon, 10 Mar 2025 22:16:11 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c89b5dd7fa7375fcf704b123db9784dd316b8d30c0dd45667df5144a6d41202`  
		Last Modified: Mon, 10 Mar 2025 22:16:11 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d82ce82484bff28427e47fd8cab82daa1e4370b9517d6c914ced983fcee084`  
		Last Modified: Mon, 10 Mar 2025 22:16:22 GMT  
		Size: 207.4 MB (207398896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dea4510e6131cc06aa41dfa6ed56c3d6a8ae8cf2d56716f32062ef062834722`  
		Last Modified: Mon, 10 Mar 2025 22:16:11 GMT  
		Size: 96.4 KB (96413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13617a1a7848553e867202207ab2caf5ebe95f729cd927378fd86d83d58db0af`  
		Last Modified: Mon, 10 Mar 2025 22:16:11 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
