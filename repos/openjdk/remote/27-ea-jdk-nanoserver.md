## `openjdk:27-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:5ed53fa60c978f80fe7290a05147683f44314243d77d6ca9445e91aa5913e2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `openjdk:27-ea-jdk-nanoserver` - windows version 10.0.26100.32690; amd64

```console
$ docker pull openjdk@sha256:3d116ce5728d5d8b9581103bf04647acffb2f8c03e5053b60c8fb0e021cfa003
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.7 MB (424720019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff80676c14ab275b09961ddd9af5e66f36a838a2e9fe81db3ac6970dde722b5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 06:39:57 GMT
RUN Apply image 10.0.26100.32690
# Tue, 14 Apr 2026 22:10:47 GMT
SHELL [cmd /s /c]
# Tue, 14 Apr 2026 22:15:01 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 14 Apr 2026 22:15:01 GMT
USER ContainerAdministrator
# Tue, 14 Apr 2026 22:15:03 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 14 Apr 2026 22:15:03 GMT
USER ContainerUser
# Tue, 14 Apr 2026 22:15:04 GMT
ENV JAVA_VERSION=27-ea+17
# Tue, 14 Apr 2026 22:15:15 GMT
COPY dir:0691f65abcad9aa5e8b70bfb251a5fc900e0d4cf82de17dca757301a739d34d1 in C:\openjdk-27 
# Tue, 14 Apr 2026 22:15:20 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 14 Apr 2026 22:15:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8af320c3b6d19296bcc7947e3beb8bc0c69cb12143db52efe988dc998ac088dc`  
		Last Modified: Tue, 14 Apr 2026 21:00:37 GMT  
		Size: 199.7 MB (199717094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9283504e7a4dc0b9369ebeee673efd11bfea17126a3b7e1ef073687a6f63449`  
		Last Modified: Tue, 14 Apr 2026 22:11:40 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311e5e730d319f5bb5f985558b9be47a1b4ea7f553deedb53bd26db44038cd69`  
		Last Modified: Tue, 14 Apr 2026 22:15:26 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab1fefce2b2d76b01dbae60914a5ef5b08bf86fa78c7174cfbad8790018637a`  
		Last Modified: Tue, 14 Apr 2026 22:15:26 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05e8212d5157fcec0f9b41b501582e3cd4dc492f99eeeca8385a47a95bcbb57`  
		Last Modified: Tue, 14 Apr 2026 22:15:26 GMT  
		Size: 73.1 KB (73072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1197a7175afb7b4c4abe99915efba1d82e192b7016592a6dee7a4460cd17f2`  
		Last Modified: Tue, 14 Apr 2026 22:15:24 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634a1c98bc1df0e4e971029588cb2b31f206597cb57f046dc5efc086b97a2c13`  
		Last Modified: Tue, 14 Apr 2026 22:15:24 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02dfce1b326d8ca65abe78449c28a88119e52bc014e134cad1d493df0abb767`  
		Last Modified: Tue, 14 Apr 2026 22:15:40 GMT  
		Size: 224.8 MB (224811468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bdc1d5374cfca19d14679d2e7b11720efb0ce452a0562de8cab8153d8d36b65`  
		Last Modified: Tue, 14 Apr 2026 22:15:24 GMT  
		Size: 112.0 KB (111980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d1a9c671bfcae6aacf4ecaff93537a826dbb6eb863588f9dc5bec1b39f5a4e`  
		Last Modified: Tue, 14 Apr 2026 22:15:24 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-jdk-nanoserver` - windows version 10.0.20348.5020; amd64

```console
$ docker pull openjdk@sha256:2ce06361119fa8a5ab2f2fe945d605d33b91a0dc74c342ce4c24dbbacd2cfd53
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.0 MB (352002872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bdc345ae9d9cce5ab5d4cbb4f61daa3ed79b7444eb5f75b351f7b29ed331d4b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 22:11:19 GMT
SHELL [cmd /s /c]
# Tue, 14 Apr 2026 22:15:21 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 14 Apr 2026 22:15:22 GMT
USER ContainerAdministrator
# Tue, 14 Apr 2026 22:15:24 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 14 Apr 2026 22:15:25 GMT
USER ContainerUser
# Tue, 14 Apr 2026 22:15:27 GMT
ENV JAVA_VERSION=27-ea+17
# Tue, 14 Apr 2026 22:15:57 GMT
COPY dir:0691f65abcad9aa5e8b70bfb251a5fc900e0d4cf82de17dca757301a739d34d1 in C:\openjdk-27 
# Tue, 14 Apr 2026 22:16:04 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 14 Apr 2026 22:16:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a92e0e44c72d10bf75d0edaa06ddcc97f14d6c2afb302cffe065c90d3dee37`  
		Last Modified: Tue, 14 Apr 2026 22:11:56 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3766390d50944426798a56c14603210869c055d2a1d5a05eedfd6f066fc3b609`  
		Last Modified: Tue, 14 Apr 2026 22:16:10 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76091565f49863a6bccb0e404eba432f03fcd8a77cc27b96d7c1ec8a0bab9c4e`  
		Last Modified: Tue, 14 Apr 2026 22:16:10 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee7044106cf59d26f234a2c7c6708d2e270fe82d09df2480f307888facbbe20`  
		Last Modified: Tue, 14 Apr 2026 22:16:10 GMT  
		Size: 76.4 KB (76449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24944b8b2118691d166efcd8a784c9145239cb3e31b4c36522cdfec18101a1ee`  
		Last Modified: Tue, 14 Apr 2026 22:16:09 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176211b85a36785dc9a7f9a93a802c836934b908c797bdd618ce1846c597961f`  
		Last Modified: Tue, 14 Apr 2026 22:16:09 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e540bb065c65b9a958891ae9aadcf63cf280c78a471cc8ad269ac2630ccd7ae3`  
		Last Modified: Tue, 14 Apr 2026 22:16:24 GMT  
		Size: 224.8 MB (224811347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fce8067ec9a787d2149e28365a5d4bf101f701dcd4cca198f97c177f2d2bf1c`  
		Last Modified: Tue, 14 Apr 2026 22:16:09 GMT  
		Size: 152.7 KB (152664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303e6651e5cdf4aaefabda17debfc4a04d0ebd392ed5851484ba035af4084e91`  
		Last Modified: Tue, 14 Apr 2026 22:16:09 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
