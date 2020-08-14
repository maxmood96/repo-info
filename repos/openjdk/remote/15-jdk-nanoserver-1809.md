## `openjdk:15-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:dab3750182cd637d8c419f279f2c728e44ce1562e86519eb4d837c5a7ab28220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `openjdk:15-jdk-nanoserver-1809` - windows version 10.0.17763.1397; amd64

```console
$ docker pull openjdk@sha256:142ed616171f71e354ebfc7ed58ac0bfa621aac1f8fb2a383967b0bfc36afb82
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295933622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7a62002ab943abd71ad0d196115370dcfdf50f1a3d53eeecf4664452c88c2c3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Aug 2020 01:28:42 GMT
RUN Apply image 1809-amd64
# Wed, 12 Aug 2020 15:28:05 GMT
SHELL [cmd /s /c]
# Wed, 12 Aug 2020 15:35:41 GMT
ENV JAVA_HOME=C:\openjdk-15
# Wed, 12 Aug 2020 15:35:42 GMT
USER ContainerAdministrator
# Wed, 12 Aug 2020 15:35:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 12 Aug 2020 15:35:53 GMT
USER ContainerUser
# Wed, 12 Aug 2020 15:35:53 GMT
ENV JAVA_VERSION=15
# Fri, 14 Aug 2020 21:25:38 GMT
COPY dir:c7e08674451932ee3e39dd647bf57a58f604f71d6631e01f3c30405731e02d63 in C:\openjdk-15 
# Fri, 14 Aug 2020 21:25:58 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Fri, 14 Aug 2020 21:25:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ce1c649a3e5b5b5449776d4afce631c673cade12336ccb5a38a0aac7c9d8b2bc`  
		Size: 101.0 MB (100984944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1c7c341c7a3d0c7b6e849b6faec560815682d07ce87df2e4d1e83f928aab306b`  
		Last Modified: Wed, 12 Aug 2020 16:10:21 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908c3f69eea8e2eeda13b3a2bc36cb5bddc8f02e4add43f8074ea08d0254ab6b`  
		Last Modified: Wed, 12 Aug 2020 16:12:20 GMT  
		Size: 831.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfa99a5cb7aa58c10707652cd6441f23958888cdb3de7292e9f805230737eb0`  
		Last Modified: Wed, 12 Aug 2020 16:12:20 GMT  
		Size: 827.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21f16c0f1eef9755ced9deac574ce43f9d82e3b5d8f235ff69a39d2d3ada378`  
		Last Modified: Wed, 12 Aug 2020 16:12:20 GMT  
		Size: 67.3 KB (67309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4d1d1646f8cee0a046ee309f0100de2962628c9942413c59f33e2eff3374ab`  
		Last Modified: Wed, 12 Aug 2020 16:12:17 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcb5d3af38d42a971343edc08139ef1411452f01359595908be6153bfb1b1b9`  
		Last Modified: Wed, 12 Aug 2020 16:12:17 GMT  
		Size: 837.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1fae88a7885018a6a55cdc731a34492de066be6e7ea4a374ff4d1e031a39b1`  
		Last Modified: Fri, 14 Aug 2020 21:34:23 GMT  
		Size: 191.4 MB (191359166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994e139dbbd1ef0ab5f5695946a477033940aabed07f283d0f0bd61c723892fe`  
		Last Modified: Fri, 14 Aug 2020 21:34:05 GMT  
		Size: 3.5 MB (3517169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8671245f8869d811dcdf523046d03ec5e992f1ae7f122b45fba6528135ac5a32`  
		Last Modified: Fri, 14 Aug 2020 21:34:04 GMT  
		Size: 827.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
