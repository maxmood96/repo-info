## `openjdk:16-nanoserver-1809`

```console
$ docker pull openjdk@sha256:bd5c0591528e1fe048d9810b2c9ef11cf043b6496d0a484d8d38c53d24f590c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `openjdk:16-nanoserver-1809` - windows version 10.0.17763.1339; amd64

```console
$ docker pull openjdk@sha256:b634f577fbf636afd84e9b140e05cdc6ca27db5ee06e4ea078ef3a30b653615e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.7 MB (296669170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c3271375afcf9762787bc3a45ec9cc0f09f7eb748be460b870e43ba56691649`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 07 Jul 2020 13:50:07 GMT
RUN Apply image 1809-amd64
# Wed, 15 Jul 2020 01:54:43 GMT
SHELL [cmd /s /c]
# Wed, 15 Jul 2020 01:54:44 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 15 Jul 2020 01:54:45 GMT
USER ContainerAdministrator
# Fri, 24 Jul 2020 18:21:01 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Fri, 24 Jul 2020 18:21:02 GMT
USER ContainerUser
# Fri, 07 Aug 2020 23:35:29 GMT
ENV JAVA_VERSION=16-ea+9
# Fri, 07 Aug 2020 23:36:03 GMT
COPY dir:e2d94f447255630b2f23327408c6183bf8ac1833da5fb2b9945a4c90e6940da7 in C:\openjdk-16 
# Fri, 07 Aug 2020 23:36:28 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Fri, 07 Aug 2020 23:36:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dc95608099543221ef539391bfece5c1ce37b97af9da457f5990349cab028a12`  
		Size: 100.9 MB (100895619 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9f6486e4debac36806ed3527d9b1baea75c1a807e26baccdd0a2f521c814273f`  
		Last Modified: Wed, 15 Jul 2020 02:43:55 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952f154db0b1aa57586a649f933acc22620a18dc11bfe0f2369af17af77fd616`  
		Last Modified: Wed, 15 Jul 2020 02:43:54 GMT  
		Size: 860.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d574471402fee7c0d2fb574eb4bbfd848f720c971dc4d9318a7437da54d1ee`  
		Last Modified: Wed, 15 Jul 2020 02:43:54 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa94d52ff38f89a9e35647ee58e1b9d5c1ee9f238d17d1d94d294263683a8fc7`  
		Last Modified: Fri, 24 Jul 2020 18:34:41 GMT  
		Size: 65.3 KB (65316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70146e6967d5a15f9a4884bb2688dbc7af97e64172e951cc00ccbe779da256fe`  
		Last Modified: Fri, 24 Jul 2020 18:34:38 GMT  
		Size: 822.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba753461b8a86ade1552f3cff5990b6cb47b5357ed9e6d69bf14a449c357d7a2`  
		Last Modified: Fri, 07 Aug 2020 23:48:26 GMT  
		Size: 864.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88cef93dc0c74790959e48b2119940b01e9aef0437d65acff4a50c4daf68bf08`  
		Last Modified: Fri, 07 Aug 2020 23:52:00 GMT  
		Size: 192.2 MB (192171158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a7a898a8ff0061c4d0fb71d5a26bb54a6bb34d5ab01ca23ba2a03681cfbb0c`  
		Last Modified: Fri, 07 Aug 2020 23:48:30 GMT  
		Size: 3.5 MB (3531796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8def48b24fdcbf2805ed57f6b620a3001992965ab3a45fd94f028cf0195999d`  
		Last Modified: Fri, 07 Aug 2020 23:48:26 GMT  
		Size: 954.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
