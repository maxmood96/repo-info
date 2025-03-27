## `openjdk:25-ea-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:0f63c5d03552fff8c6a07f231e42ce043b10caa0c0b508fc2a683e1cc789b328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `openjdk:25-ea-nanoserver-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull openjdk@sha256:7c55d3cbf90396a31c06af60def58fb09a540a2fd8fc38f5922a1606603b96a1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.8 MB (328783364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06e61dc1586815eabffc9111207ddbc01f9fc8374a432d48344d97ec3e5b9221`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Thu, 27 Mar 2025 21:00:10 GMT
SHELL [cmd /s /c]
# Thu, 27 Mar 2025 21:00:11 GMT
ENV JAVA_HOME=C:\openjdk-25
# Thu, 27 Mar 2025 21:00:12 GMT
USER ContainerAdministrator
# Thu, 27 Mar 2025 21:00:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 27 Mar 2025 21:00:15 GMT
USER ContainerUser
# Thu, 27 Mar 2025 21:00:15 GMT
ENV JAVA_VERSION=25-ea+16
# Thu, 27 Mar 2025 21:00:23 GMT
COPY dir:19cd448448f63399f0cc00bb4ac8df0759f681650f72cc2b82002a92d2bbe677 in C:\openjdk-25 
# Thu, 27 Mar 2025 21:00:28 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 27 Mar 2025 21:00:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:416c3c0ee530972ee66391f7d7c3ba14967d07dbbcad20f79c6117472c6b4f45`  
		Last Modified: Thu, 27 Mar 2025 21:00:33 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3fb424d3fcdc291cf3a81607d412fd00d3bc48a0e13377727fd1e566d1ed016`  
		Last Modified: Thu, 27 Mar 2025 21:00:33 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d03be61f99d8b8e8afce08290738b2ed785ccb79506ed79e4f3f37e693b5b48`  
		Last Modified: Thu, 27 Mar 2025 21:00:33 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d53526654b591009e11e7d32d5b20b38a33bbf39433ea2e1aced66c2e3f9b81`  
		Last Modified: Thu, 27 Mar 2025 21:00:33 GMT  
		Size: 76.0 KB (76001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54e86ea659cce85531d632375c0f6499a7f4fe613b569a0ed179e01c0817902`  
		Last Modified: Thu, 27 Mar 2025 21:00:32 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f45f637d5382a0b4ddc15efa749e12956f3c3f12a4c54d3f4c3eac412285ef3`  
		Last Modified: Thu, 27 Mar 2025 21:00:32 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41de6ce4c17845621943133737d1d466b7e62e36b560c69f038ac2fa758accab`  
		Last Modified: Thu, 27 Mar 2025 21:00:44 GMT  
		Size: 207.9 MB (207898397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319029c6dfe147da9599a47a6e8604dc4d8f420ac3f6926fc039c527d3e7b479`  
		Last Modified: Thu, 27 Mar 2025 21:00:32 GMT  
		Size: 107.2 KB (107243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90425a0cb46fbd79277a81d1d68014aa003b331fe5a99694a5e997226a08ff6`  
		Last Modified: Thu, 27 Mar 2025 21:00:32 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
