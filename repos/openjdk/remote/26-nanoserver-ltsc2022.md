## `openjdk:26-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:40b3b5305da51815a0e21d153645d46d91a8ad3cdd6b43532df8121a12443548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `openjdk:26-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull openjdk@sha256:a9a8eb9e0250cd2025a4fd6644173892f96c66a0cce207d16aa39699c91544c0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.7 MB (341736751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4bc7b405a2211f6c443a3944815a03354a6a3e4a57b1c3b3c1b92cbfcf8b22d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:19:27 GMT
SHELL [cmd /s /c]
# Wed, 10 Sep 2025 22:21:06 GMT
ENV JAVA_HOME=C:\openjdk-26
# Wed, 10 Sep 2025 22:21:07 GMT
USER ContainerAdministrator
# Wed, 10 Sep 2025 22:21:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 Sep 2025 22:21:09 GMT
USER ContainerUser
# Wed, 10 Sep 2025 22:21:10 GMT
ENV JAVA_VERSION=26-ea+14
# Wed, 10 Sep 2025 22:21:40 GMT
COPY dir:d50107523f417125c2242d5366bf04295424e0a959b88dfcf6f8074b4fb0cc43 in C:\openjdk-26 
# Wed, 10 Sep 2025 22:21:44 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 10 Sep 2025 22:21:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9a238b296b863260af62360805baa85f9d2fb272823e764b654e58032e367a`  
		Last Modified: Wed, 10 Sep 2025 23:08:42 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f090545af493136aaff79babf145490f923a2bdd50029ac5ee0a7186dd447b36`  
		Last Modified: Wed, 10 Sep 2025 22:22:31 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11693c159ac41721b77f00a946a65f19157d846f76af5234ecbea8df8b02a516`  
		Last Modified: Wed, 10 Sep 2025 22:22:31 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73854d2d6cebe20bdcf587664bb7516ccac951124877d5aaf3387ec1ba54dc3`  
		Last Modified: Wed, 10 Sep 2025 22:22:31 GMT  
		Size: 76.5 KB (76471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9c12ab36c3ddafd637da6ed02710756965f8db8ad5118cea76d6e55f27ecff`  
		Last Modified: Wed, 10 Sep 2025 22:22:32 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2761bf0c315d7fd00f15796a9d448c1c34a910ea27710c06caad51446ad3563`  
		Last Modified: Wed, 10 Sep 2025 22:22:32 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9299124a176285a747c423f15972955efea691186e1d1f39b4032b20b4009011`  
		Last Modified: Thu, 11 Sep 2025 00:26:21 GMT  
		Size: 218.8 MB (218786193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7011946b3e8e62e4d47a154b977a395ddf06a64433cb6c781a66d5b931e670`  
		Last Modified: Wed, 10 Sep 2025 22:22:32 GMT  
		Size: 147.8 KB (147789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfb4a8469ea5759484916af1ee1c916f42ebf7f58807dd49189fb4954a19693`  
		Last Modified: Wed, 10 Sep 2025 22:22:32 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
