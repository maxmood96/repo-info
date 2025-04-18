## `eclipse-temurin:24_36-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:e56ee7e4ee550c3ad00d099d9ddd49e0411b4235f2733bfd7ab3e847ce8bba1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `eclipse-temurin:24_36-jre-nanoserver` - windows version 10.0.26100.3781; amd64

```console
$ docker pull eclipse-temurin@sha256:895c5b46fe6b6fabe814fb3752c7f0adbfbabe20ff5ed5c844177c9526ddc093
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.0 MB (248028806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af56c8e428a07361eca3e112733e87fef152d5ac37a804a3d450e9c903e79fb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Fri, 18 Apr 2025 04:14:31 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:14:33 GMT
ENV JAVA_VERSION=jdk-24+36
# Fri, 18 Apr 2025 04:14:35 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 18 Apr 2025 04:14:36 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:14:41 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:14:43 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:14:49 GMT
COPY dir:90c9828944ffcd2978afe702f80884cbf787022d7dcd7becc7c91cd2ab6f7dd5 in C:\openjdk-24 
# Fri, 18 Apr 2025 04:14:55 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 17 Apr 2025 02:52:17 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830db1f296ef76578cd03f67ea5ec749bd3034f6c1f38b0526181c9d816e2254`  
		Last Modified: Fri, 18 Apr 2025 04:15:01 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa0f7a3138c7ba1057e22a05faaf1a9c3fb6ad620918f1058cd53a0926a06af`  
		Last Modified: Fri, 18 Apr 2025 04:15:01 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd5d4252bc1cccbdb139376b965f49370d6ea4744631faee88c18a48d42b403`  
		Last Modified: Fri, 18 Apr 2025 04:15:01 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d2503b18180c028e4117124e2127e2de154358c9267961cdc3c437cbd37688`  
		Last Modified: Fri, 18 Apr 2025 04:14:59 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74fba3fb334c499a5a0d4c59c36a146d841532915aab902203af977a4ff7d36`  
		Last Modified: Fri, 18 Apr 2025 04:14:59 GMT  
		Size: 76.7 KB (76710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d27ec6faba382301c2ae6a6ae556b1f1d04f68a927271b7e65d6be7710b448e`  
		Last Modified: Fri, 18 Apr 2025 04:14:59 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba4365ad8e3222958a020f9ffdf5201c75816bc4ec0bf14d568069f56d7619f`  
		Last Modified: Fri, 18 Apr 2025 04:15:06 GMT  
		Size: 57.7 MB (57702446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea2a7897ec674360791db8509804f888d3a7d134b75adf3927255196b5704b9`  
		Last Modified: Fri, 18 Apr 2025 04:14:59 GMT  
		Size: 102.4 KB (102359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:24_36-jre-nanoserver` - windows version 10.0.20348.3566; amd64

```console
$ docker pull eclipse-temurin@sha256:b36595df4e61da3c715a3f902e6d0500b70a38b89b9bb3e6de9bb4b3500484f1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.4 MB (180428152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e57da52254538312d98d52f649507d3b5301b386eb118688bbc024ed92508ea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Fri, 18 Apr 2025 04:16:09 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:16:09 GMT
ENV JAVA_VERSION=jdk-24+36
# Fri, 18 Apr 2025 04:16:10 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 18 Apr 2025 04:16:11 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:16:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:16:14 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:16:19 GMT
COPY dir:90c9828944ffcd2978afe702f80884cbf787022d7dcd7becc7c91cd2ab6f7dd5 in C:\openjdk-24 
# Fri, 18 Apr 2025 04:16:24 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Wed, 16 Apr 2025 23:30:29 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c022bb6e1e619d8b2032cf6b93ab9a319c3cb44f21dd42561d29c0df725f73`  
		Last Modified: Fri, 18 Apr 2025 04:16:27 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d140dc61c35505c0f00b304c5a81676031bbdad8c8fd56d868eabda73c927b22`  
		Last Modified: Fri, 18 Apr 2025 04:16:27 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ede6cfd5a06bbf9bff3d1c3c6278559fcfd5ee19026d8d86a2d3bacc1b27c0`  
		Last Modified: Fri, 18 Apr 2025 04:16:27 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abcafd02fb4d5abd90dbdfc2060e0163b3961cb3ecf0557ab177a695da1166a8`  
		Last Modified: Fri, 18 Apr 2025 04:16:26 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9b6f598e53eb22aa4e29e607d678c401ff1c7dac256f4873ad492080c75de2`  
		Last Modified: Fri, 18 Apr 2025 04:16:26 GMT  
		Size: 76.8 KB (76787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3723571d74ae436416b8b1c676cff9148e5044f7460b7c2646356e1c9fc89dd`  
		Last Modified: Fri, 18 Apr 2025 04:16:26 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2774dfb378ef2f6a582e97114b3dc434a9bf35f205b59bb3f4b33e2a24454d87`  
		Last Modified: Fri, 18 Apr 2025 04:16:33 GMT  
		Size: 57.7 MB (57700665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75878bae5569e89ec743494bdf1b54cba4143fdc0109b0fec57b181b751b1b1b`  
		Last Modified: Fri, 18 Apr 2025 04:16:26 GMT  
		Size: 106.5 KB (106469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:24_36-jre-nanoserver` - windows version 10.0.17763.7249; amd64

```console
$ docker pull eclipse-temurin@sha256:d321487f705806591313728b448755c9683dc4c2e6ff738e96dc8de70290e271
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170424024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2325ded6a0aa9ba0e3899d3c5bb18408c07c8d35983e5f0ae46da0c82a14f929`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 04:17:21 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:17:23 GMT
ENV JAVA_VERSION=jdk-24+36
# Fri, 18 Apr 2025 04:17:25 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 18 Apr 2025 04:17:26 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:17:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:17:30 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:17:35 GMT
COPY dir:90c9828944ffcd2978afe702f80884cbf787022d7dcd7becc7c91cd2ab6f7dd5 in C:\openjdk-24 
# Fri, 18 Apr 2025 04:17:39 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0d1d2cde6a32525822fb3541394395d94c195b46050e9feaaea5e2403d77eb`  
		Last Modified: Fri, 18 Apr 2025 04:17:43 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e353f3c125cc943456c6cb8f515955a07f73d0fcddb5de5644b74925c229a756`  
		Last Modified: Fri, 18 Apr 2025 04:17:43 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d6d28f9c0b8ff013f68a60f87682646b76091afaf2d7c53e416b9fbd1e97b1e`  
		Last Modified: Fri, 18 Apr 2025 04:17:43 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a70146cfc0e9a2901839f1cc3f381ea3f1c86a943f937c3f0ffe47f550cade8`  
		Last Modified: Fri, 18 Apr 2025 04:17:42 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14096878a149676662dfd7623fcd08ab7fa224f8d90596278b1a3efccb28d5a6`  
		Last Modified: Fri, 18 Apr 2025 04:17:42 GMT  
		Size: 68.9 KB (68877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca03c4634929b2adf5d3cba824a7a692e07e2850e8a8db33dc0ab1a725ab014`  
		Last Modified: Fri, 18 Apr 2025 04:17:42 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b453066dd182cf08fff85f7a08195872cf116284768004f3276abb26b986a19`  
		Last Modified: Fri, 18 Apr 2025 04:17:49 GMT  
		Size: 57.7 MB (57700851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8e09ce66ed7c8f7231f66085f7a720ae4e964aee70d6d24e8c05db7961b060`  
		Last Modified: Fri, 18 Apr 2025 04:17:43 GMT  
		Size: 3.9 MB (3896808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
