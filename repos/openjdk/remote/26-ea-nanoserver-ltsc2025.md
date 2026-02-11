## `openjdk:26-ea-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:d985966622507c812fe614464b539b03197ab680317f5cd2946a0b478ac08c94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `openjdk:26-ea-nanoserver-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull openjdk@sha256:893952e1de8e7b58cc3be13be91cfc9597961ccd2eab4899ed9527c54087ab46
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.3 MB (423321574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e65d22091116fa546109c6a0628228c87433ea7014d4a168f525c43d76219055`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 22:06:41 GMT
RUN Apply image 10.0.26100.32370
# Tue, 10 Feb 2026 23:36:23 GMT
SHELL [cmd /s /c]
# Tue, 10 Feb 2026 23:37:53 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 10 Feb 2026 23:37:54 GMT
USER ContainerAdministrator
# Tue, 10 Feb 2026 23:37:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 10 Feb 2026 23:37:55 GMT
USER ContainerUser
# Tue, 10 Feb 2026 23:37:56 GMT
ENV JAVA_VERSION=26-ea+33
# Tue, 10 Feb 2026 23:38:07 GMT
COPY dir:4b0b09721eb8a6a23e669a427b9022937722c5088501379523ae0d075ca2bcf0 in C:\openjdk-26 
# Tue, 10 Feb 2026 23:38:12 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 10 Feb 2026 23:38:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:77321bd03612cfa46920e790ae0c3b142758a5803ad759fdb406c98b6f2e4ed0`  
		Last Modified: Tue, 10 Feb 2026 22:50:26 GMT  
		Size: 199.3 MB (199251619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235d9628315965b68f4d378ddd929aeff0f5258c04acbaead21ad7d6b7979c7b`  
		Last Modified: Tue, 10 Feb 2026 23:36:46 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30088e4dc64cad6424a2d3964e65b0c1dcbfc8989b1ab592902c6d7353e2606`  
		Last Modified: Tue, 10 Feb 2026 23:38:17 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad54793ffc30ea8a8a18cc07150054266fcfd527b0f0820458d18a92fe71ee87`  
		Last Modified: Tue, 10 Feb 2026 23:38:18 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab864da79e74799579d898e21ebd6af3da3ae402d61930612a937f236647ba4a`  
		Last Modified: Tue, 10 Feb 2026 23:38:18 GMT  
		Size: 72.4 KB (72351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88942a6f91e306b35cd6218c2b49d3d8fa14d8a92ab43bd648305f9733d60bba`  
		Last Modified: Tue, 10 Feb 2026 23:38:16 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a351c9e37e69ff12cfffaff03223836b505a068cb60aa66507a4516f0d62b3`  
		Last Modified: Tue, 10 Feb 2026 23:38:16 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c17dd05302a6d98aecd4461bd14216ddbfb9963a7ceed034688a4a0402a261`  
		Last Modified: Tue, 10 Feb 2026 23:38:31 GMT  
		Size: 223.9 MB (223878753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ecdb9cea72a31149912dd0812d87da8ffdc458dcd93e5955a6c783f1d72777`  
		Last Modified: Tue, 10 Feb 2026 23:38:16 GMT  
		Size: 112.4 KB (112406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210fc6952d12ca4291517edf25ab7e5d17c91459fa4952782bc8eb74690fc5a4`  
		Last Modified: Tue, 10 Feb 2026 23:38:16 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
