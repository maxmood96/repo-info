## `openjdk:27-ea-26-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:f8f47c9297d7911230821ddcf551ecb5885654b9a5d62e427920c0d73241c9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `openjdk:27-ea-26-jdk-nanoserver` - windows version 10.0.26100.32995; amd64

```console
$ docker pull openjdk@sha256:c512ce42982c1e5a02e3e930cf4a950299fbcba1f411f2439fb5c7ce1b144dd3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.9 MB (419931535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2e839999880fa14a6338db44e8e914b9db04953c7ec59d5e3f68bd362b919d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 07:06:15 GMT
RUN Apply image 10.0.26100.32995
# Wed, 17 Jun 2026 00:09:06 GMT
SHELL [cmd /s /c]
# Wed, 17 Jun 2026 00:09:07 GMT
ENV JAVA_HOME=C:\openjdk-27
# Wed, 17 Jun 2026 00:09:09 GMT
USER ContainerAdministrator
# Wed, 17 Jun 2026 00:09:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 17 Jun 2026 00:09:27 GMT
USER ContainerUser
# Wed, 17 Jun 2026 00:09:27 GMT
ENV JAVA_VERSION=27-ea+26
# Wed, 17 Jun 2026 00:10:37 GMT
COPY dir:a7799beb07c872d6daa4270ad4935855c84179de6db285791c6085d98f3d469c in C:\openjdk-27 
# Wed, 17 Jun 2026 00:10:46 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 17 Jun 2026 00:10:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:64f5cd94d3bcd0fae94830b1fad0f8b3dc33677f8d7dc15c5219b56fe2a6584e`  
		Last Modified: Tue, 09 Jun 2026 22:11:30 GMT  
		Size: 196.7 MB (196668131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ddb5c8c82f727fecf805506ce2355d621cb0758cb4e92e693988a0ea827f69e`  
		Last Modified: Wed, 17 Jun 2026 00:10:54 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cad79c8fae8a71e162f120cf94f5461843793c7a98642d76cddf4c1c62db15e`  
		Last Modified: Wed, 17 Jun 2026 00:10:54 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403360c54f1f19d88365bdf6c72e15ff64f06949a0d0350e1f6fd0486343225e`  
		Last Modified: Wed, 17 Jun 2026 00:10:54 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafbc175012c4255f0fb204fe6db33d5d6826fbdd70b5184ef0092c0449a3a5d`  
		Last Modified: Wed, 17 Jun 2026 00:10:54 GMT  
		Size: 70.2 KB (70192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603cb7f9799a427232a141b1a3e80cbcb48d532a6b562b7fc1c92933b8ac4739`  
		Last Modified: Wed, 17 Jun 2026 00:10:53 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979617f4abfe75141a4c752aa410aff519399b8ab140e9e84df933c1b73786cd`  
		Last Modified: Wed, 17 Jun 2026 00:10:52 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1a457918a0911cbe6fd7ffd213014561c3dbe7606d8442f9348f350ce4bb3f`  
		Last Modified: Wed, 17 Jun 2026 00:11:07 GMT  
		Size: 223.1 MB (223094704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da730052ba076bd141af406405f2c9fcf89e3bf2430645cfc1a1822c4ca8e533`  
		Last Modified: Wed, 17 Jun 2026 00:10:52 GMT  
		Size: 92.3 KB (92267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81eda12997a5b7a4d6ad14ab77c101ed6e6151b93fa8dfdba173bfbeedc460d`  
		Last Modified: Wed, 17 Jun 2026 00:10:52 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-26-jdk-nanoserver` - windows version 10.0.20348.5256; amd64

```console
$ docker pull openjdk@sha256:4d05d78af85e775fe5b69435cace2607b4e73cdb216910aa31432b7c49ca04e4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.3 MB (347257367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df5c97c4f3671884b7c7a9ca461865208e3de1231546b08eb35d550e6b3fa9a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Wed, 17 Jun 2026 00:08:52 GMT
SHELL [cmd /s /c]
# Wed, 17 Jun 2026 00:08:52 GMT
ENV JAVA_HOME=C:\openjdk-27
# Wed, 17 Jun 2026 00:08:53 GMT
USER ContainerAdministrator
# Wed, 17 Jun 2026 00:09:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 17 Jun 2026 00:09:05 GMT
USER ContainerUser
# Wed, 17 Jun 2026 00:09:05 GMT
ENV JAVA_VERSION=27-ea+26
# Wed, 17 Jun 2026 00:10:16 GMT
COPY dir:a7799beb07c872d6daa4270ad4935855c84179de6db285791c6085d98f3d469c in C:\openjdk-27 
# Wed, 17 Jun 2026 00:10:22 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 17 Jun 2026 00:10:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c1b513973465eaa8cb21b11b07b2022075ebb7a15da5e998419b107acb8b2a`  
		Last Modified: Wed, 17 Jun 2026 00:10:33 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e94fc5759895210a07ea2181800f9b7de66d7600a0359e07041554414dfbf1`  
		Last Modified: Wed, 17 Jun 2026 00:10:33 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7496e0d22e8efbbbc593c06cfaaf9c1b3e12d6c61bd0c5b0dbfda3ee155445c`  
		Last Modified: Wed, 17 Jun 2026 00:10:32 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987fee44a2a96f23a314259f07520b41ccf70fecf607cb01a4f16044c2053caa`  
		Last Modified: Wed, 17 Jun 2026 00:10:32 GMT  
		Size: 65.6 KB (65553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b94eee0df2e7e1688399f8d7ee3a0a4862f3abb89bd636c3d335248568298c`  
		Last Modified: Wed, 17 Jun 2026 00:10:31 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6b9d765c18e972b7bb8b7c5c890ce0d9a47df6f25f3359ee77e59f0ec35201`  
		Last Modified: Wed, 17 Jun 2026 00:10:31 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebed2163b25ece5a336668caa7d0849d70dce7a73ccecc96721a6ad50b46838c`  
		Last Modified: Wed, 17 Jun 2026 00:10:46 GMT  
		Size: 223.1 MB (223094680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3d1f3d9e2fc0ba377846a283268967cecab0622509a29434ad55bd42dd6f240`  
		Last Modified: Wed, 17 Jun 2026 00:10:31 GMT  
		Size: 93.2 KB (93214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1373035a509f256cb599d695b8b5210f5b08ab423c5c4273d8a7cc2edb4a5298`  
		Last Modified: Wed, 17 Jun 2026 00:10:31 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
