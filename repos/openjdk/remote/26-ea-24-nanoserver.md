## `openjdk:26-ea-24-nanoserver`

```console
$ docker pull openjdk@sha256:cce510f746688717d4c924b91a0e4171f7d7929ced7fe04788e011dfba164c5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `openjdk:26-ea-24-nanoserver` - windows version 10.0.26100.7171; amd64

```console
$ docker pull openjdk@sha256:7b7884243ed023d085dec398ff39a730aee244346286846e36b2ac19fee8e2cd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.3 MB (421250970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3fd17ccaf7cebf8c2264edd01c4f810b4b2c81cbff5a85c1399e1bf74a39bf3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 09 Nov 2025 10:04:50 GMT
RUN Apply image 10.0.26100.7171
# Tue, 18 Nov 2025 00:45:33 GMT
SHELL [cmd /s /c]
# Tue, 18 Nov 2025 00:45:34 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 18 Nov 2025 00:45:35 GMT
USER ContainerAdministrator
# Tue, 18 Nov 2025 00:45:43 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 18 Nov 2025 00:45:43 GMT
USER ContainerUser
# Tue, 18 Nov 2025 00:45:44 GMT
ENV JAVA_VERSION=26-ea+24
# Tue, 18 Nov 2025 00:46:27 GMT
COPY dir:580fa45a384b12cb70c75bbdb47b5399a06812987f2bb40365d6f1c31468fec4 in C:\openjdk-26 
# Tue, 18 Nov 2025 00:46:33 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 18 Nov 2025 00:46:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:87c91227213eb6e7c8cfe33b6bd0429350e524756878f37f3860b013f804bf59`  
		Last Modified: Tue, 11 Nov 2025 20:41:49 GMT  
		Size: 197.9 MB (197936447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdc9adaebb0e2db8d513eb5331987e9eab8584be574b803f294162fb9a706ea`  
		Last Modified: Tue, 18 Nov 2025 00:47:52 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6462b50fe72ed7962477a69d48cb04a029e244cd6cb5852acd5072b03ed85b5`  
		Last Modified: Tue, 18 Nov 2025 00:47:52 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020a7d27b5fedf5ae34e14337f8cc220e51f8acfc0eb50f5dcfe0bdf04daf099`  
		Last Modified: Tue, 18 Nov 2025 00:47:52 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b67d8e48a00015c8297185a4d0a75eb5509a9c758ee6c87c23addab45aec27`  
		Last Modified: Tue, 18 Nov 2025 00:47:52 GMT  
		Size: 70.4 KB (70404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1de02e08bd00e70d065e2e39a3867b1954fa45d0b6061438e82e9b18bfd72c`  
		Last Modified: Tue, 18 Nov 2025 00:47:52 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c9d2463df6058b30ece2d49d4e9817ec4dda47d1c649fa6c1a0f37940083e2`  
		Last Modified: Tue, 18 Nov 2025 00:47:52 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0732d14b69a38e3b2ca234b9a3df5c4d3d405ea770b2d2a06027d58660c8c8c7`  
		Last Modified: Tue, 18 Nov 2025 01:23:58 GMT  
		Size: 223.2 MB (223154105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6aaab9f372542f76a5d86bc391ceb39e562f7db9fdd76beda360eb37a1ab5dc`  
		Last Modified: Tue, 18 Nov 2025 00:47:52 GMT  
		Size: 83.5 KB (83549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88c6e598900e3770b59fd7e2c055ac7a548e531c7fc36b4cead9c43add8177f`  
		Last Modified: Tue, 18 Nov 2025 00:47:52 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-ea-24-nanoserver` - windows version 10.0.20348.4405; amd64

```console
$ docker pull openjdk@sha256:04c25823130808c463f78b7151372617c5d38e768d72332eef205d3ff9afd602
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.7 MB (349723782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a8ece85ebc221a66ab32cb4819ac9c0f630a47d35cee981cc604f5a4608f65`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 18 Nov 2025 01:13:45 GMT
SHELL [cmd /s /c]
# Tue, 18 Nov 2025 01:13:47 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 18 Nov 2025 01:13:49 GMT
USER ContainerAdministrator
# Tue, 18 Nov 2025 01:14:08 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 18 Nov 2025 01:14:09 GMT
USER ContainerUser
# Tue, 18 Nov 2025 01:14:11 GMT
ENV JAVA_VERSION=26-ea+24
# Tue, 18 Nov 2025 01:16:02 GMT
COPY dir:580fa45a384b12cb70c75bbdb47b5399a06812987f2bb40365d6f1c31468fec4 in C:\openjdk-26 
# Tue, 18 Nov 2025 01:16:13 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 18 Nov 2025 01:16:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f1188afec01bab00d767f2483c03cd52633916ffaaf9cdf422c0cf05035077`  
		Last Modified: Tue, 18 Nov 2025 01:16:45 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa5caf9202b235a8d0c9119de9fd15606df382b4349310e30bf5cfbcef150a9`  
		Last Modified: Tue, 18 Nov 2025 01:16:45 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f49f62be225ad92065dd4e9f437021ab11ec9589f233aa4fed620dfcad192d`  
		Last Modified: Tue, 18 Nov 2025 01:16:45 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a655ce9f07a57318401fe96ec167581180d1f58ff5a4dd73c018d5f62872a5bc`  
		Last Modified: Tue, 18 Nov 2025 01:16:45 GMT  
		Size: 83.1 KB (83101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bbca86edaf07fd3f16b5acaff0bf102e809f80f5fe7be31c587faaa0a53398e`  
		Last Modified: Tue, 18 Nov 2025 01:16:45 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad57ad133b40a22bb9551f7cb7766ca5c1cbc7f530178128b55ae3451607d71`  
		Last Modified: Tue, 18 Nov 2025 01:16:45 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc699769d58041f684a056a44611d664e986d5c34a9a4f63f65f6295f5a05fe`  
		Last Modified: Tue, 18 Nov 2025 04:25:54 GMT  
		Size: 223.2 MB (223154173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95bf0b53ae9362bad69b9b3dd9fa6d022a1b9f5b188a0597e7c36138528a3da`  
		Last Modified: Tue, 18 Nov 2025 01:16:45 GMT  
		Size: 131.1 KB (131076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d026d4a8cb69f6e67fa1e1230b5d125ccd02e6ad3e4884fadbb4ed3b308b61`  
		Last Modified: Tue, 18 Nov 2025 01:16:45 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
