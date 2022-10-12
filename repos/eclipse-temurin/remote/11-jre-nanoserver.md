## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:eb53a7d5ffa3fe11456b08fa5b756dea5658826fcb63b0c720d9e7a160f534aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1129; amd64
	-	windows version 10.0.17763.3532; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.20348.1129; amd64

```console
$ docker pull eclipse-temurin@sha256:73e978b82ad32ff11876da1b0d9063a8c98393cc7df8003cbd6a34607b8bd500
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161249852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087384442bad6d7f22cba0bda29d1c0ffc89a54e2de7f5a6e3eaa460f80d1ead`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Oct 2022 21:37:41 GMT
RUN Apply image 10.0.20348.1129
# Wed, 12 Oct 2022 15:54:21 GMT
SHELL [cmd /s /c]
# Wed, 12 Oct 2022 15:55:36 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Wed, 12 Oct 2022 15:55:37 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 12 Oct 2022 15:55:38 GMT
USER ContainerAdministrator
# Wed, 12 Oct 2022 15:55:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Oct 2022 15:55:47 GMT
USER ContainerUser
# Wed, 12 Oct 2022 15:56:36 GMT
COPY dir:b650de7fc0e3b0755f26a7348890f8f5a4e1b6ed07c2d2df82fc07e7eb59e165 in C:\openjdk-11 
# Wed, 12 Oct 2022 15:56:54 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:38fa349577729651ac1fc3ec785f908719a8100da5f5ba9bd3f549411061f583`  
		Size: 118.2 MB (118202895 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e0ed0041e3584df1952980c3f73fd2b6e154328c7a0165f37dbe92ef94ae8a95`  
		Last Modified: Wed, 12 Oct 2022 16:12:53 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ab62c13bec3daa2374e11924aff5844b58c17b97bf040906ea46e9d87126a5`  
		Last Modified: Wed, 12 Oct 2022 16:13:33 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37bbee8665c328438506c0329be6a2cc1854075fe5e2801d0b3c952b998a9107`  
		Last Modified: Wed, 12 Oct 2022 16:13:33 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e66cbf95270899e6f6482b57a9938446196777f75df9ac4cba512c6ea10d0d5`  
		Last Modified: Wed, 12 Oct 2022 16:13:33 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faaf96570d1a87f06ff0a504d54b541e39782a17fc7c2fcb2545ef8f313a85b1`  
		Last Modified: Wed, 12 Oct 2022 16:13:30 GMT  
		Size: 80.4 KB (80425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c27c4f4546488e95308e2f98edae9e1b084f46a560454acb4c4c5a273afc66`  
		Last Modified: Wed, 12 Oct 2022 16:13:30 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33933f26c44a57982543dd87663266a162be60be3691b33840899819c6c32c3e`  
		Last Modified: Wed, 12 Oct 2022 16:14:11 GMT  
		Size: 42.9 MB (42903436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ece20643098d82dcd4dbb2647ea9f17a9c4e9755a2ae00148eabe94b172c67`  
		Last Modified: Wed, 12 Oct 2022 16:14:04 GMT  
		Size: 57.3 KB (57347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.17763.3532; amd64

```console
$ docker pull eclipse-temurin@sha256:627d57cc0862547e67b1b4d09190a28a399c0cb98c304dadad4766d48ddc53f0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146458894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c0c5eda80c3d439019720835570f9c502908ff115e3ac8d5e1bf248938e8db`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Wed, 12 Oct 2022 15:20:49 GMT
SHELL [cmd /s /c]
# Wed, 12 Oct 2022 15:31:01 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Wed, 12 Oct 2022 15:31:01 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 12 Oct 2022 15:31:02 GMT
USER ContainerAdministrator
# Wed, 12 Oct 2022 15:31:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Oct 2022 15:31:15 GMT
USER ContainerUser
# Wed, 12 Oct 2022 15:35:40 GMT
COPY dir:b650de7fc0e3b0755f26a7348890f8f5a4e1b6ed07c2d2df82fc07e7eb59e165 in C:\openjdk-11 
# Wed, 12 Oct 2022 15:35:53 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:5ead999142ecce15e02523c49706a633fa708374d94bb65a254e3a3c117d609b`  
		Size: 103.4 MB (103377244 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4a6a667d76c19fca171390d60fb90c40e16c777050e943a7fe17ad7686841f0f`  
		Last Modified: Wed, 12 Oct 2022 16:02:59 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a5b3e1e569bda6c7c0f790d1a667813abefc5cae113d210ec6205941111d2e`  
		Last Modified: Wed, 12 Oct 2022 16:05:35 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde07e341e8acc4b8b07533e6d42bbc3dfa2a41511a76e65bdd2ff12faf517e0`  
		Last Modified: Wed, 12 Oct 2022 16:05:34 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d9d4e7a18b9439d8bcf71483c2450a4be68f4631870f38197439e1fcdd7785`  
		Last Modified: Wed, 12 Oct 2022 16:05:34 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1860ca093ea655e0f934c3258432233e68af7d44389b5f369fc75f37a134ed42`  
		Last Modified: Wed, 12 Oct 2022 16:05:32 GMT  
		Size: 78.8 KB (78849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa891f591bff349d725f02ea0e7f95c0694585653e8535664adc8e9654b7e61b`  
		Last Modified: Wed, 12 Oct 2022 16:05:32 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1f98982c09f6bc901c63cff9ba38135998a1af5324331d295b119f9616bbe7`  
		Last Modified: Wed, 12 Oct 2022 16:06:49 GMT  
		Size: 42.9 MB (42908469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c523e5bbc705552ed271376a47e5a9863eb774f6848ea2b55ab9feb3cbea6e`  
		Last Modified: Wed, 12 Oct 2022 16:06:41 GMT  
		Size: 88.9 KB (88930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
