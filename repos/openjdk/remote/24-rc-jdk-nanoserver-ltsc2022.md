## `openjdk:24-rc-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:e51c9bf9add97b8f6de3339f6f53112b74c4f37bba0b488f49c6f132b1761471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `openjdk:24-rc-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull openjdk@sha256:f4c93638f263137b23a65a478bd44619b0e00d7dee5267f8ee0f58204540f916
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.4 MB (329412851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04bb256eca5965ab27704bfe1a142cb75aa91944c140a48bae98fad33dfbb0d8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Wed, 12 Mar 2025 19:20:36 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:20:36 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 12 Mar 2025 19:20:37 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:20:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 12 Mar 2025 19:20:40 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:20:40 GMT
ENV JAVA_VERSION=24
# Wed, 12 Mar 2025 19:20:48 GMT
COPY dir:cf5ecdf170ed29d5224593d2b3a510464d2e7297517065c397a2229de8b2a139 in C:\openjdk-24 
# Wed, 12 Mar 2025 19:20:52 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 12 Mar 2025 19:20:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f50c106cbea715bd596ac3bd3d4d9d38b9966b18be67b816cf0a708d1ce7fe4`  
		Last Modified: Wed, 12 Mar 2025 19:20:56 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67bf0975e1011e1fa3c59572f5570d47501afc812266ff0132db3a8a07164c8`  
		Last Modified: Wed, 12 Mar 2025 19:20:56 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4908a201cd9667c15b0acb5a9d9c96079006f12cc6d32601cfd9b35235f40d`  
		Last Modified: Wed, 12 Mar 2025 19:20:56 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b2454158d0933710509175e5f75438c2df026004d9a5a808b4e582461d322b`  
		Last Modified: Wed, 12 Mar 2025 19:20:56 GMT  
		Size: 77.9 KB (77855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c96def51a2e52584a23c329bcc7228bf36d5bd1924f2da610c9d06f8733550e`  
		Last Modified: Wed, 12 Mar 2025 19:20:55 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ad963c115761292c5bc46519839dff88f092af97710d166c278fcdf15b9a54`  
		Last Modified: Wed, 12 Mar 2025 19:20:55 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb83d082dcf1cc7132c57a32ee69a8175e4c85bf0a42149da548768e36cdb85`  
		Last Modified: Wed, 12 Mar 2025 19:21:08 GMT  
		Size: 208.5 MB (208527151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352e9248248044ed1d678062f7d8834ae922359fb9e0dd044b7c4c365afe5606`  
		Last Modified: Wed, 12 Mar 2025 19:20:55 GMT  
		Size: 106.1 KB (106078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee0cb13e0f796f305a995a793edfb9f6b5a4a1823af092c23916ae25858d7ef`  
		Last Modified: Wed, 12 Mar 2025 19:20:55 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
