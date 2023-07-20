## `openjdk:22-ea-nanoserver-1809`

```console
$ docker pull openjdk@sha256:f4ad84b8ca7ea58bf936db3e767ae68295b1c3849098f531df435655a448d6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `openjdk:22-ea-nanoserver-1809` - windows version 10.0.17763.4645; amd64

```console
$ docker pull openjdk@sha256:15d30154a738f37c745ed37b14992bff82b45d776dcc16f3649c84f32c6fabe0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.2 MB (307184036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f46d37fdfb2246b9add1c80ec95a8915ac2e8a1fe1425670c2292c55be827c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jul 2023 07:42:59 GMT
RUN Apply image 10.0.17763.4645
# Thu, 13 Jul 2023 21:36:32 GMT
SHELL [cmd /s /c]
# Fri, 14 Jul 2023 00:14:58 GMT
ENV JAVA_HOME=C:\openjdk-22
# Fri, 14 Jul 2023 00:14:58 GMT
USER ContainerAdministrator
# Fri, 14 Jul 2023 00:15:08 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 14 Jul 2023 00:15:09 GMT
USER ContainerUser
# Thu, 20 Jul 2023 20:37:29 GMT
ENV JAVA_VERSION=22-ea+7
# Thu, 20 Jul 2023 20:37:45 GMT
COPY dir:f3a6e96b36bdfe48c5e8d2b12327ae159e9278b9afd64510da644d4da0694146 in C:\openjdk-22 
# Thu, 20 Jul 2023 20:37:57 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 20 Jul 2023 20:37:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5c5b06ba65934bcf850a1a54ecf4b3da34d3e6d6c8e90dbc897719c3ea377c8a`  
		Last Modified: Tue, 11 Jul 2023 17:31:37 GMT  
		Size: 104.4 MB (104408241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13c473988daf5951866dd9b290bd6417227c1d7df6e811cfe11438d033a1eba`  
		Last Modified: Thu, 13 Jul 2023 22:19:06 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544d6fd540738704e91e0cdf5ce429fe06193ca6f57b912ecd37720a5398c73e`  
		Last Modified: Fri, 14 Jul 2023 00:23:01 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184aebbaa7a5b561357f50ab1e278ddea12853b5513f6ccee076e8977ee17cb5`  
		Last Modified: Fri, 14 Jul 2023 00:23:00 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f517a720df0787d39ebc3c54f30149bad465e8af46947e6dd7c609c5c63d3ef3`  
		Last Modified: Fri, 14 Jul 2023 00:23:00 GMT  
		Size: 71.4 KB (71362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ee6f2b90fa1d7c818530d35c4808f44d5fa2414919c02d26f5b7db881751ed`  
		Last Modified: Fri, 14 Jul 2023 00:22:58 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df1d4ad2dab71f67d888f89686c1ed41eb7998791633f14c9f4bb244f3cc97c`  
		Last Modified: Thu, 20 Jul 2023 20:43:52 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158be6f841a412d3384788e9115c6c9f5ce87f825bffecfdef79e07bb55723a5`  
		Last Modified: Thu, 20 Jul 2023 20:44:12 GMT  
		Size: 198.9 MB (198881436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b438d423571dc5d3f12ffcf76cd93b74c4fa9a484544ec6b30de9e8f38286c38`  
		Last Modified: Thu, 20 Jul 2023 20:43:53 GMT  
		Size: 3.8 MB (3816243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51877a5206e98054ece43721ff32dafc136c8eae4414221e2676527969a0f425`  
		Last Modified: Thu, 20 Jul 2023 20:43:52 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
