## `eclipse-temurin:17-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:091555d9749f9d163f3ca4297c850f00760a48f310e086b10127aa92f1523e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3194; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.26100.3194; amd64

```console
$ docker pull eclipse-temurin@sha256:e74bece81c9b83e6c7befd3b63d101a64bc8c319ce208165dec9c93e62444542
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.3 MB (393301829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6925b5d50ffe8b9db335c6fafc08e337a71e66374a52a647aff67940b580df3f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 08 Feb 2025 22:31:47 GMT
RUN Apply image 10.0.26100.3194
# Thu, 27 Feb 2025 19:13:25 GMT
SHELL [cmd /s /c]
# Thu, 27 Feb 2025 19:13:26 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 27 Feb 2025 19:13:26 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 27 Feb 2025 19:13:27 GMT
USER ContainerAdministrator
# Thu, 27 Feb 2025 19:13:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 27 Feb 2025 19:13:30 GMT
USER ContainerUser
# Thu, 27 Feb 2025 19:13:36 GMT
COPY dir:5f87ec570fea10148b246e6a91d6cf8396b47b1e19a7e8d79bcea78e84a1d159 in C:\openjdk-17 
# Thu, 27 Feb 2025 19:13:43 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 27 Feb 2025 19:13:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e075dd07cbf907b7da8dbd8365b73a71ac92a834b78f520bd976cb97e0fcc0a1`  
		Last Modified: Wed, 12 Feb 2025 22:34:59 GMT  
		Size: 205.9 MB (205890263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b79ed0e3582afc14457b50f854db26ed7756424f145898eef1b1b8f0ad3eb88`  
		Last Modified: Thu, 27 Feb 2025 19:13:50 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a2017eef3ce0ce78e38fdc1bc97086abeb89080316df3a1194db7717b3ada4`  
		Last Modified: Thu, 27 Feb 2025 19:13:50 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deaae2e70ae4c0d6b25e943c7cda1871afec6e2db232b3e1168465c1b2290bc8`  
		Last Modified: Thu, 27 Feb 2025 19:13:50 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1579eeb73ecf7ef8043bb961cff408233ca2e20832d0bf7938e1d705abfc7e82`  
		Last Modified: Thu, 27 Feb 2025 19:13:50 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6924521e40be21be3e436e145d1cd6b50b7712f05f797944aa40943b07859f9b`  
		Last Modified: Thu, 27 Feb 2025 19:13:48 GMT  
		Size: 75.9 KB (75852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbe07143b0e5fc0dbf11be60a5ade673a0e8f4ac1c6abe295d49679d0f26bb9`  
		Last Modified: Thu, 27 Feb 2025 19:13:48 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3abe1901b34db8011c5790f95a1330a2162ddb4e07d5efebd78ba467c103b6`  
		Last Modified: Thu, 27 Feb 2025 19:13:58 GMT  
		Size: 187.2 MB (187235035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d50c828a6895ed5bd9a42339111cb6c2bbedfc52f9a0e945804091de5c7001`  
		Last Modified: Thu, 27 Feb 2025 19:13:48 GMT  
		Size: 94.3 KB (94341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f31e55e4ea92b9a52c2453ae3312db7d5a41c32ebff427c7c6315259d57e85d`  
		Last Modified: Thu, 27 Feb 2025 19:13:48 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.20348.3207; amd64

```console
$ docker pull eclipse-temurin@sha256:32bc5d3f786f1bfe3d061d66c76a7f0d3abee488d5c2f821351ba49b22e1aee9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.1 MB (308090334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36f62c6e3d00500d808506be3ffd9fe9d50486903c0932607e5f097b0f3b8cf`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 20:45:43 GMT
RUN Apply image 10.0.20348.3207
# Thu, 13 Feb 2025 01:17:24 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:17:25 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 13 Feb 2025 01:17:25 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 13 Feb 2025 01:17:26 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:17:28 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Feb 2025 01:17:29 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:17:36 GMT
COPY dir:5f87ec570fea10148b246e6a91d6cf8396b47b1e19a7e8d79bcea78e84a1d159 in C:\openjdk-17 
# Thu, 13 Feb 2025 01:17:40 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 13 Feb 2025 01:17:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:938e4585b186fc3df3c1959d47ba7a634fea121cec7545db7923ceb191d99a33`  
		Last Modified: Tue, 11 Feb 2025 22:43:09 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a85a1e7c321169232ce970d0099c3936d2e7acd4c38e9dec3239d5b2ed36e8`  
		Last Modified: Thu, 13 Feb 2025 01:17:46 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff847421f2f707e451b0771bdf7501b02ae34636af830973937afec23981c80`  
		Last Modified: Thu, 13 Feb 2025 01:17:45 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3edf2ad75e774a1fb50fc2f49b220f0f2e0d70ecaf71b9c5ba066b1fc8b9d2f2`  
		Last Modified: Thu, 13 Feb 2025 01:17:45 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e39c4b8cd83a263e68a80c9ca0e7ffa08a1c45b27e77768e1ec6c9d6f9d5f2`  
		Last Modified: Thu, 13 Feb 2025 01:17:45 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b648ef2af341ec2f76177ed0e419ff809215355474e9f2e5491dccd7aafcd0bd`  
		Last Modified: Thu, 13 Feb 2025 01:17:44 GMT  
		Size: 77.2 KB (77174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1fae38964c249babe34579ac72c9922bd146b2fd94375d3e56e6a1070573dd`  
		Last Modified: Thu, 13 Feb 2025 01:17:44 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed4241831ba6addc4478f38e4b7941e9948118a9e53877433c1f4fa1f302647`  
		Last Modified: Thu, 13 Feb 2025 01:17:54 GMT  
		Size: 187.2 MB (187233506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a669a941835e2fbf4b1a119a2a9e31ea09d0402fe5ef93937bc42d155914e56e`  
		Last Modified: Thu, 13 Feb 2025 01:17:44 GMT  
		Size: 106.9 KB (106861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987d3309e6799a87dfff87374968fa1ee5f7ec80151efca741f45c20dbded16c`  
		Last Modified: Thu, 13 Feb 2025 01:17:44 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.17763.6893; amd64

```console
$ docker pull eclipse-temurin@sha256:e9af9a45db445eeb644e95753d189e1dc8790aa19ad5a2ed5854ac6d0b9cfddc
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297845075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:827f068f3a713dd54bdb0622ec47fc917f1d08d70eaf299e48dd933039522c0a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:14:37 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:14:39 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 13 Feb 2025 01:14:39 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 13 Feb 2025 01:14:40 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:14:42 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Feb 2025 01:14:42 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:14:49 GMT
COPY dir:5f87ec570fea10148b246e6a91d6cf8396b47b1e19a7e8d79bcea78e84a1d159 in C:\openjdk-17 
# Thu, 13 Feb 2025 01:14:55 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 13 Feb 2025 01:14:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc76f37fdcdabe12fbf65a903e719a11bf3bfad416fe69f9106bce0cede1292`  
		Last Modified: Thu, 13 Feb 2025 01:15:02 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e63a5ee2bdaf50421e1a6248ba20e502d467fee610efa63c13053d5498d3cb`  
		Last Modified: Thu, 13 Feb 2025 01:15:02 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c65b7d7403119307f53f039c960b1b6ebf2b6700efd070060dd28d9580bb53`  
		Last Modified: Thu, 13 Feb 2025 01:15:02 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7c3bdd65f3a320edd317fbbdfa913bbb86917789c0084363b649b231b1947d`  
		Last Modified: Thu, 13 Feb 2025 01:15:01 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6ed4520ef3586fb49e8b522653e091fe98ed60816a4a6a3cf0ed6896dc5613`  
		Last Modified: Thu, 13 Feb 2025 01:15:00 GMT  
		Size: 73.4 KB (73385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8f274a1f56f860e797332863987d991ae4dfbb52d369446633a61da24efebe`  
		Last Modified: Thu, 13 Feb 2025 01:14:59 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6e8daebd93d7a57070b9b3c2605cb5636001e23771d99c6c9ba7b4116999a5`  
		Last Modified: Thu, 13 Feb 2025 01:15:10 GMT  
		Size: 187.2 MB (187233687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e09ad8dc0e0d1eefcdcc3f55a1239c2770530ffdfb9fc54a899dab1d578d90f`  
		Last Modified: Thu, 13 Feb 2025 01:15:00 GMT  
		Size: 3.6 MB (3616284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb6fcc7b544effb893be6493a48b538c1fb23d57074bb60466b3b2342f9e9f6`  
		Last Modified: Thu, 13 Feb 2025 01:14:59 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
