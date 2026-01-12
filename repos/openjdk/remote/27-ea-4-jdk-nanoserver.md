## `openjdk:27-ea-4-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:091a539136b23f4e43104c0d4c0398f162e524f996b9035cc568e530f8f7a23b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `openjdk:27-ea-4-jdk-nanoserver` - windows version 10.0.26100.7462; amd64

```console
$ docker pull openjdk@sha256:2b1b4c6daba50c15302b1af13beb054e13362b8900ad3115e8e3058f50b00151
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.0 MB (422972738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5afeb670786fb681dc2fd4ae0ccc10ed9fb4cfb420b2fa8fcffbbfe91dff3a6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Dec 2025 21:31:34 GMT
RUN Apply image 10.0.26100.7462
# Mon, 12 Jan 2026 21:12:46 GMT
SHELL [cmd /s /c]
# Mon, 12 Jan 2026 21:14:30 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 12 Jan 2026 21:14:30 GMT
USER ContainerAdministrator
# Mon, 12 Jan 2026 21:14:31 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 12 Jan 2026 21:14:32 GMT
USER ContainerUser
# Mon, 12 Jan 2026 21:14:32 GMT
ENV JAVA_VERSION=27-ea+4
# Mon, 12 Jan 2026 21:15:03 GMT
COPY dir:55417311536b64386669c9f543375752cfd39486cb0c7d8403a74e4cd382a3c4 in C:\openjdk-27 
# Mon, 12 Jan 2026 21:15:07 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 12 Jan 2026 21:15:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a092205b76ca656d8483e99445def9f0619cb3acb2688bf9a33244c43ad44ce`  
		Last Modified: Tue, 09 Dec 2025 22:15:12 GMT  
		Size: 198.9 MB (198873947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae0c30a24f290070e5783e9d1fe48a8f8ae05edd00cbb7a4d624c8138a5784a`  
		Last Modified: Mon, 12 Jan 2026 21:14:09 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03221970c68403632bc3305de7fe2d92a62c35434b9372502ba421c4b2dfd11`  
		Last Modified: Mon, 12 Jan 2026 21:15:39 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168d1e7546f481e895be322821f3ffd454b563c56e55543208673618c4257a0f`  
		Last Modified: Mon, 12 Jan 2026 21:15:39 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e04504c56acf24766d8b59efff587a4890d8b5c910eaf018a1d5e8f953004da`  
		Last Modified: Mon, 12 Jan 2026 21:15:45 GMT  
		Size: 71.9 KB (71931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5e31c5d07aa3b8a441b10202f73f4968de47ecfeb24e9298b0cc7054c1c437`  
		Last Modified: Mon, 12 Jan 2026 21:15:39 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f1ff4dd4b5626aa082dde6bd836e68fabba394ad4aa2b89fa365ee8226f719`  
		Last Modified: Mon, 12 Jan 2026 21:15:39 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126c9fea63238a74d462d7409afe34d15e6a221673e2394c3f9158ca3847b4f1`  
		Last Modified: Mon, 12 Jan 2026 21:16:10 GMT  
		Size: 223.9 MB (223909756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afce9d894d3b36ce8d363cfb3f8597456c79ed402a4940cd3ebc864314385a4d`  
		Last Modified: Mon, 12 Jan 2026 21:15:40 GMT  
		Size: 110.7 KB (110680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed2c4e07e86e56a31977a63c7c6f75b1c2a15049ae2ed4b3dac54b50443ce11`  
		Last Modified: Mon, 12 Jan 2026 21:15:40 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-4-jdk-nanoserver` - windows version 10.0.20348.4529; amd64

```console
$ docker pull openjdk@sha256:4612ad1a102bf42fa00d998746d3a7192a6e0baa84c8cf84cdc03da0952ce030
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.5 MB (350493676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538918143a5ab909fb4e162b3e7a7e21ce0e5bb8700925925ca52de43fd0753a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Mon, 12 Jan 2026 21:36:06 GMT
SHELL [cmd /s /c]
# Mon, 12 Jan 2026 21:38:29 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 12 Jan 2026 21:38:30 GMT
USER ContainerAdministrator
# Mon, 12 Jan 2026 21:38:33 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 12 Jan 2026 21:38:34 GMT
USER ContainerUser
# Mon, 12 Jan 2026 21:38:35 GMT
ENV JAVA_VERSION=27-ea+4
# Mon, 12 Jan 2026 21:39:26 GMT
COPY dir:55417311536b64386669c9f543375752cfd39486cb0c7d8403a74e4cd382a3c4 in C:\openjdk-27 
# Mon, 12 Jan 2026 21:39:36 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 12 Jan 2026 21:39:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b3f59c2a2a510228fd4f8632a9f997a8da7163939246e89711c940e6054c8b`  
		Last Modified: Mon, 12 Jan 2026 21:38:08 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ffda8995aa429d321a263bd3c035fb16d05b5c8c3ea584d89510ccfbf90a5c4`  
		Last Modified: Mon, 12 Jan 2026 21:40:04 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e844ff478fadaac95ea6adbdc2a624009e0a6fb7eea2988d4850a03d56d4541`  
		Last Modified: Mon, 12 Jan 2026 21:40:04 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95579545527b2862ad8fb3811bee59043e19f79717e89aff2070f50f8ce4cd7`  
		Last Modified: Mon, 12 Jan 2026 21:40:04 GMT  
		Size: 88.7 KB (88696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78e83618bd51d4ce4e57ab464492d4f408d3a9709ce6cb27296e763e77d7950`  
		Last Modified: Mon, 12 Jan 2026 21:40:04 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1faed139d33a9720478a21c6dd5ef5ad8706473a7bcd9ad534f57ac6c985684`  
		Last Modified: Mon, 12 Jan 2026 21:40:04 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13961ab582189dc184cc2074db1cfa4694aee213a508caadeaf530c7e89642b6`  
		Last Modified: Mon, 12 Jan 2026 21:40:55 GMT  
		Size: 223.9 MB (223909653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8426a7854026e61ce6694353ec820191410eab5cf73a8b5869d65eb27e8b5cca`  
		Last Modified: Mon, 12 Jan 2026 21:40:04 GMT  
		Size: 130.6 KB (130567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bef1ec907b2bee2013937e8e7e655dea0310c75b462d1b42cf640a792ffb0e2`  
		Last Modified: Mon, 12 Jan 2026 21:40:04 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
