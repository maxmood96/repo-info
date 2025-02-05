## `openjdk:24-ea-35-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:77c1402b8e2df7419167b933950a08dd4a68d0395e9a1f12fdbe293037f20c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `openjdk:24-ea-35-jdk-nanoserver` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:5c744e67951631ffc63b264579947e23513e6b8d5fcafd03a98f36f6c728aa68
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.8 MB (407774989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f081db26796f39b8b6d16c7a7ba9baaaea7395bf2d94473788bbbb8996535f1d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Wed, 05 Feb 2025 00:14:16 GMT
SHELL [cmd /s /c]
# Wed, 05 Feb 2025 00:14:17 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 05 Feb 2025 00:14:18 GMT
USER ContainerAdministrator
# Wed, 05 Feb 2025 00:14:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 05 Feb 2025 00:14:22 GMT
USER ContainerUser
# Wed, 05 Feb 2025 00:14:23 GMT
ENV JAVA_VERSION=24-ea+35
# Wed, 05 Feb 2025 00:14:31 GMT
COPY dir:8f8aac6961c71e892e6587cdd6058441c6f263293987c0242380c839d9a86912 in C:\openjdk-24 
# Wed, 05 Feb 2025 00:14:39 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 05 Feb 2025 00:14:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3785065b8aefe375f35a653421ce594381c387f22decbefb76bc070f9d5651ca`  
		Last Modified: Wed, 05 Feb 2025 00:14:48 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65f9a8f92a2b846e6566cc48ff72a0874c5abf3a9a5e8f9e630c15eac6edd2a`  
		Last Modified: Wed, 05 Feb 2025 00:14:48 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab57c1382df5388a6759ef6f51be49eaf016f80572daffed37c3d0d929b93e8`  
		Last Modified: Wed, 05 Feb 2025 00:14:48 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5ee7f6e299d1039fa0c5296c2ae317b0325d6e4918102631da3f1b50b4123a`  
		Last Modified: Wed, 05 Feb 2025 00:14:48 GMT  
		Size: 76.4 KB (76393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39040b7cb015ac6868d25900120d01b31f82ff8b2076d4a56c637ba9271d1da`  
		Last Modified: Wed, 05 Feb 2025 00:14:46 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a2fd83e1d741103614546cf6e1a5367c0eca07b4861b80ad9f29b59d613114`  
		Last Modified: Wed, 05 Feb 2025 00:14:46 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df307f49b6529e01caff3f062db9dc9dff7a0028d42f3a8f77bc231b33b30a6e`  
		Last Modified: Wed, 05 Feb 2025 00:14:57 GMT  
		Size: 208.5 MB (208533782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c71558448a4307e5df5c4906e88a77756a580b9be24e7156ae231a8ac99871a`  
		Last Modified: Wed, 05 Feb 2025 00:14:46 GMT  
		Size: 104.3 KB (104306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d01de5a4c01828b161d0943b856dc3d3545258b041e3ad1cde7fa1725febe7`  
		Last Modified: Wed, 05 Feb 2025 00:14:46 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-ea-35-jdk-nanoserver` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:22dbcd150da908fa2046bf69b4c1c9b874cbb30b37ab552b2e194a556dd5b89f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.4 MB (329382456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:790120bd65638fca7cb59a633f96b37d8c9bae6e321eeebf7529ee75707bd36a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Wed, 05 Feb 2025 00:10:19 GMT
SHELL [cmd /s /c]
# Wed, 05 Feb 2025 00:10:19 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 05 Feb 2025 00:10:20 GMT
USER ContainerAdministrator
# Wed, 05 Feb 2025 00:10:43 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 05 Feb 2025 00:10:43 GMT
USER ContainerUser
# Wed, 05 Feb 2025 00:10:44 GMT
ENV JAVA_VERSION=24-ea+35
# Wed, 05 Feb 2025 00:10:52 GMT
COPY dir:8f8aac6961c71e892e6587cdd6058441c6f263293987c0242380c839d9a86912 in C:\openjdk-24 
# Wed, 05 Feb 2025 00:10:59 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 05 Feb 2025 00:10:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0ddb5ee07b0f40d5a387b47ac5c7d1f5cee3ab894851431cb8300f7b767e13`  
		Last Modified: Wed, 05 Feb 2025 00:11:03 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff33d38bd3905004e335b47e5a8d1d9f8f7aee84cd402bf91d9007cab491e94`  
		Last Modified: Wed, 05 Feb 2025 00:11:03 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2094754633c776c3f8ec6ba01b957858b81e0bdfc4633abd6db125341982e86e`  
		Last Modified: Wed, 05 Feb 2025 00:11:03 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0670eedf40c7fda8e15f9a6079ae34d71db4f5960db0bb6442746668b304be`  
		Last Modified: Wed, 05 Feb 2025 00:11:03 GMT  
		Size: 85.2 KB (85250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101056cceb797f5da16b0adac709a2063a2f88fcdb3a0fdec4a7b25209ef41e1`  
		Last Modified: Wed, 05 Feb 2025 00:11:02 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e7928282fce0d74428716e46516676b4ff19c5ad60061c3169a9a906cdb20f2`  
		Last Modified: Wed, 05 Feb 2025 00:11:02 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:629ca0f598a0cc0162cef8957cc8b3ab236d5d98e8b321e32f9f5fd4d727f4a7`  
		Last Modified: Wed, 05 Feb 2025 00:11:14 GMT  
		Size: 208.5 MB (208531980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0496a77d0be821da49b160621120f788a233b733a0c237e6045a3f7b50828ab`  
		Last Modified: Wed, 05 Feb 2025 00:11:02 GMT  
		Size: 97.5 KB (97458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1376eec32258737d0e53a225f0f2255abeaa1082e4d305f576e5479375ad09ce`  
		Last Modified: Wed, 05 Feb 2025 00:11:02 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-ea-35-jdk-nanoserver` - windows version 10.0.17763.6775; amd64

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
