## `openjdk:24-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:b835eff3c9d0bb47b80ff77ee3c7fde14368087f1cb6bfeb497163bf8a020834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `openjdk:24-jdk-nanoserver-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull openjdk@sha256:119d2e9a50534ab87da7b1b9401dbccd74aa189c7f85ea900571103604c6b033
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.5 MB (365507525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bea9811049390f3e4dcbca0739c52e33fad030d96466ac09d1e30d3f9ce6f3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Mon, 22 Jul 2024 22:10:11 GMT
SHELL [cmd /s /c]
# Mon, 22 Jul 2024 22:10:13 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 22 Jul 2024 22:10:14 GMT
USER ContainerAdministrator
# Mon, 22 Jul 2024 22:10:37 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 22 Jul 2024 22:10:37 GMT
USER ContainerUser
# Mon, 22 Jul 2024 22:10:38 GMT
ENV JAVA_VERSION=24-ea+7
# Mon, 22 Jul 2024 22:10:45 GMT
COPY dir:490a2affd56e284696be409c9aed261b68c52507efe6462d52ee09f6a158ca40 in C:\openjdk-24 
# Mon, 22 Jul 2024 22:10:53 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 22 Jul 2024 22:10:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc8c06dd0c8ca023c0383709605e814e00d17340a634e68a6f01d4220d3b28b`  
		Last Modified: Mon, 22 Jul 2024 22:10:58 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe8971995cb8a125263fb29a7051d4ec4e25f6bdb799528646650c376aeba47`  
		Last Modified: Mon, 22 Jul 2024 22:10:58 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7df209e47cb90530bc021d24fd4d14aa00d53a799ce6ddad3011dea2d42243`  
		Last Modified: Mon, 22 Jul 2024 22:10:57 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6965324a4f13bc6d2de6932688d6ac6d3c4a098d57c3e9a0474eb76c766b8f51`  
		Last Modified: Mon, 22 Jul 2024 22:10:58 GMT  
		Size: 66.6 KB (66562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bcd43f83a6862e3ce6ae469498c3d1d95096de72481d8d17f26ecd05ec7f7e9`  
		Last Modified: Mon, 22 Jul 2024 22:10:57 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d95dfb3dc179c97a70be8cff1a6ffe8663d1bb6d444200a6818586df24d04e9`  
		Last Modified: Mon, 22 Jul 2024 22:10:57 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7231137db2fbcace769829899122a5a314aad4cf89dd98a09eb8f9d2bcbb054e`  
		Last Modified: Mon, 22 Jul 2024 22:11:07 GMT  
		Size: 206.3 MB (206324809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688bd65cbd900056c5caf949fe2d416dcaf718cdbdfbd8855cfcfeaf7217dfdb`  
		Last Modified: Mon, 22 Jul 2024 22:10:57 GMT  
		Size: 4.0 MB (4028550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5a8b4e40bc3233f767261af1d0c54ebd5e3eede54b9839903adaa477cf6e6b`  
		Last Modified: Mon, 22 Jul 2024 22:10:57 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
