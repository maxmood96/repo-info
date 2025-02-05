## `openjdk:24-nanoserver-1809`

```console
$ docker pull openjdk@sha256:1eb8fdf73c72837cb82232de62207f79b542c0bd5dd18f94cc339d722d232654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `openjdk:24-nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:8c07eac8b9eb2c5aa3d0240ed444cc4c70e535af1206c7e7a70d3bacd162ea5b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368247835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da552079ccf825c65911dfdce47f94ccee825cba25cd9d612faab375c0c16962`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 05 Feb 2025 00:10:17 GMT
SHELL [cmd /s /c]
# Wed, 05 Feb 2025 00:10:19 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 05 Feb 2025 00:10:19 GMT
USER ContainerAdministrator
# Wed, 05 Feb 2025 00:10:36 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 05 Feb 2025 00:10:36 GMT
USER ContainerUser
# Wed, 05 Feb 2025 00:10:37 GMT
ENV JAVA_VERSION=24-ea+35
# Wed, 05 Feb 2025 00:10:48 GMT
COPY dir:8f8aac6961c71e892e6587cdd6058441c6f263293987c0242380c839d9a86912 in C:\openjdk-24 
# Wed, 05 Feb 2025 00:10:54 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 05 Feb 2025 00:10:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd324af9df9425355d38657a79d8a27b8468eb22cda48aae4ebc495779ae7830`  
		Last Modified: Wed, 05 Feb 2025 00:11:00 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4f1afe5ac3c309a81dcede2f8e8471b4689dc96c87ea62e5f13a33d36402b9`  
		Last Modified: Wed, 05 Feb 2025 00:10:59 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65517efc507012e38195a1be6059593595219f4b02861bd07e0f6cf2039f59cb`  
		Last Modified: Wed, 05 Feb 2025 00:10:59 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a2479a8adb0d60a44993664e1b44c0e10684727704cdac822562ad5dd73eee`  
		Last Modified: Wed, 05 Feb 2025 00:10:59 GMT  
		Size: 66.9 KB (66864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14fbfe3ff2e5fecd95e7584bf21520ae46b5afbadc2434675b6020f07185b7cd`  
		Last Modified: Wed, 05 Feb 2025 00:10:58 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925a7bcb06109036b1baf30c0b9160a22ecc5f2a00f8f9dd0204528024f03c45`  
		Last Modified: Wed, 05 Feb 2025 00:10:58 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b69323be0afe81a742763675be9e74daffefb137c8524fa261159e7b86d167`  
		Last Modified: Wed, 05 Feb 2025 00:11:09 GMT  
		Size: 208.5 MB (208532517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5524c4941984fc8d93892fec42c5902a6354d96a1e3c06826a79f1516468aac2`  
		Last Modified: Wed, 05 Feb 2025 00:10:59 GMT  
		Size: 4.4 MB (4374492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c9b0f4d1eb787181a2aad3866e422347f5a01b35c43cc0187fe7f208bdee6d`  
		Last Modified: Wed, 05 Feb 2025 00:10:58 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
