## `openjdk:25-ea-12-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:4e9753f751e6af73c1f0c4f1cf70f43623ef380149d86b2db0b6f1d8e4920b14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `openjdk:25-ea-12-nanoserver-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull openjdk@sha256:ee3dd26e990906bf8953fe1fff7f1e6ee3e96134be30a9a4850daf120c4b3260
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.6 MB (413618536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80deb00cfee2da575662aede9bb7104a4f61a85f0b44845a421750053ebff5e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 08 Feb 2025 22:31:47 GMT
RUN Apply image 10.0.26100.3194
# Tue, 04 Mar 2025 23:16:24 GMT
SHELL [cmd /s /c]
# Tue, 04 Mar 2025 23:16:25 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 04 Mar 2025 23:16:25 GMT
USER ContainerAdministrator
# Tue, 04 Mar 2025 23:16:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 04 Mar 2025 23:16:30 GMT
USER ContainerUser
# Tue, 04 Mar 2025 23:16:31 GMT
ENV JAVA_VERSION=25-ea+12
# Tue, 04 Mar 2025 23:16:37 GMT
COPY dir:e3a80d16f60f733e38f65676798afaa74a4cc6b6b9e0edd1774eacf12556d4ac in C:\openjdk-25 
# Tue, 04 Mar 2025 23:16:45 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 04 Mar 2025 23:16:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e075dd07cbf907b7da8dbd8365b73a71ac92a834b78f520bd976cb97e0fcc0a1`  
		Last Modified: Wed, 12 Feb 2025 22:34:59 GMT  
		Size: 205.9 MB (205890263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76761fd2e245b1e403d649a70752cdf0616d6994d479b43cc56a67786201e04d`  
		Last Modified: Tue, 04 Mar 2025 23:16:49 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9991ce78411fa1ec567ea38fd441c3754e39f4444cfb2d4ecef50b6fbf57e576`  
		Last Modified: Tue, 04 Mar 2025 23:16:49 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c6188898568e1a61f8e563cdc3efe7bb56622fa8f3feefa86fc254a41bb753`  
		Last Modified: Tue, 04 Mar 2025 23:16:49 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987bb5021dce531b24c9c3c119c2f93067cf27eb460a4b44bb97bb366987e6cd`  
		Last Modified: Tue, 04 Mar 2025 23:16:49 GMT  
		Size: 77.1 KB (77076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1980b4694b50d71ccc57e6f470e79cb09d08e7556de210632a17679d88acdb`  
		Last Modified: Tue, 04 Mar 2025 23:16:48 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739d672e2a8690261e96ac0091a9606132ae2193545d0209ff13f60f445d127a`  
		Last Modified: Tue, 04 Mar 2025 23:16:48 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152155a8db3edd812443377d8f3472161628687b1e68c864ba185b817d431793`  
		Last Modified: Tue, 04 Mar 2025 23:17:00 GMT  
		Size: 207.5 MB (207540093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9580863c552293d72409cc4e077eccb6e6b0267e49fcc42e90429e6e87c697a5`  
		Last Modified: Tue, 04 Mar 2025 23:16:49 GMT  
		Size: 104.8 KB (104765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cdceda218bce764a3cce306bb3ce9bf322e1187f594314c1e1820bff8c54f6d`  
		Last Modified: Tue, 04 Mar 2025 23:16:48 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
