## `openjdk:26-ea-24-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:c75cfb7fdf9205eddad64bd2c52e967472c253bf2493fb7aa08d44e91506aea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `openjdk:26-ea-24-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

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
