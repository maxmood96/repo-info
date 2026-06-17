## `openjdk:27-ea-26-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:e1914fa1326e878b519473d4d9d1d016bcbd8548d2e07912bed80a1528695751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `openjdk:27-ea-26-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.32995; amd64

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
