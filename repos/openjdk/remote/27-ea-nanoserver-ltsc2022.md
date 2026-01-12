## `openjdk:27-ea-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:7bbc6af597edd24a5c5e84c9ba57ea045fb9cb3026c57060a2f8f8b54b540e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `openjdk:27-ea-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

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
