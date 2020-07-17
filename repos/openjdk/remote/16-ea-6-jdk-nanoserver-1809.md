## `openjdk:16-ea-6-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:4dca7efb1ed28766715259553bdef00d420ae16d22d2f06ff3096301fea42780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `openjdk:16-ea-6-jdk-nanoserver-1809` - windows version 10.0.17763.1339; amd64

```console
$ docker pull openjdk@sha256:80db17388b5613c49df95776bccad7a8edafbed99f387b30285db3d39c10737a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.5 MB (296483919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb03a7f0ddddcc286e256eea41f474ab63756db99755816d72875af5d801c7b1`
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
# Wed, 15 Jul 2020 01:55:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 15 Jul 2020 01:55:01 GMT
USER ContainerUser
# Thu, 16 Jul 2020 22:59:57 GMT
ENV JAVA_VERSION=16-ea+6
# Thu, 16 Jul 2020 23:00:50 GMT
COPY dir:1facadb59c44b1236d63ad87834bda7d2d2a5688be15d5ce365ca434f1a827ba in C:\openjdk-16 
# Thu, 16 Jul 2020 23:01:13 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Thu, 16 Jul 2020 23:01:14 GMT
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
	-	`sha256:a3532803eda54cf6b27e5f89a60ea866a566b1e68dc2a18b9e108adc19b202d0`  
		Last Modified: Wed, 15 Jul 2020 02:43:54 GMT  
		Size: 65.7 KB (65688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96519e5bd9ea0e996eef2754f2ea5fdffd216464dc67d36374e07735cd0134fc`  
		Last Modified: Wed, 15 Jul 2020 02:43:52 GMT  
		Size: 866.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08047eb7dae317ea31050ddbf6cca58c5a87d8eb08eb631c4a2ef2bd3e15400f`  
		Last Modified: Fri, 17 Jul 2020 00:20:04 GMT  
		Size: 831.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30ecfa015cd2801a37195a73527f96b792cca823dda85c81834cb090a34ea2e`  
		Last Modified: Fri, 17 Jul 2020 00:20:23 GMT  
		Size: 192.0 MB (191998188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7291e169f32817dd7505c69f353ba295b51b90df830fd3f070b9753c0756c978`  
		Last Modified: Fri, 17 Jul 2020 00:20:04 GMT  
		Size: 3.5 MB (3519272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af224b425a97e0b31e94adf9a73c443db3598011c3dad0f13d754430272c51f`  
		Last Modified: Fri, 17 Jul 2020 00:20:03 GMT  
		Size: 814.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
