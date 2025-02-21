## `eclipse-temurin:17-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:c3db2c866d1529f15fff09f1e6f98518fd3a82617dae70637ab068eeb8e29ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `eclipse-temurin:17-nanoserver` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:0e6f0be52e255f47bff90cb12972ed463a7a6219c4a34f48591d831b3bd63f14
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.5 MB (386474128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d262e6594ace108e4c471ad8b12b0df7f668f313e23feac763c934e2002e0034`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Fri, 31 Jan 2025 03:16:22 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 03:16:23 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Fri, 31 Jan 2025 03:16:23 GMT
ENV JAVA_HOME=C:\openjdk-17
# Fri, 31 Jan 2025 03:16:24 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 03:16:27 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 03:16:28 GMT
USER ContainerUser
# Fri, 31 Jan 2025 03:16:35 GMT
COPY dir:5f87ec570fea10148b246e6a91d6cf8396b47b1e19a7e8d79bcea78e84a1d159 in C:\openjdk-17 
# Fri, 31 Jan 2025 03:16:44 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 31 Jan 2025 03:16:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5a8f86cf1082c6d8da048f47faaa777a0f0a07c86e89e655465d8f382ad475`  
		Last Modified: Fri, 31 Jan 2025 03:16:52 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858cae6910415b910de02793976b891a80902d8edd1baccce0163aedabca9075`  
		Last Modified: Fri, 31 Jan 2025 03:16:52 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc97b57717f5e1b9c2e2ef212e25e42e0a9ad6f3eb3233d8511454cdec8351c1`  
		Last Modified: Fri, 31 Jan 2025 03:16:52 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0289b9a02f58eebacc40384c3010281e725ad91acdc50c38d510aaa1c8d001e4`  
		Last Modified: Fri, 31 Jan 2025 03:16:52 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50aea942b0ee1e502bd271dfe3205ce946d2c6bc19185cc0d6a19869cd96f1dc`  
		Last Modified: Fri, 31 Jan 2025 03:16:51 GMT  
		Size: 76.0 KB (75974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb74267b8a3a0bbb33063118f9103fc1f9b446aa57c13748728e54f355ac940`  
		Last Modified: Fri, 31 Jan 2025 03:16:51 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70bc6c52c4990e353e4c53979882777e886b8552f5879594959e106276b8bd3`  
		Last Modified: Fri, 31 Jan 2025 03:17:03 GMT  
		Size: 187.2 MB (187235406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c59d63b13faf6848adef305cb15b7725d8953e414f5f910c966fbd76ed1453`  
		Last Modified: Fri, 31 Jan 2025 03:16:51 GMT  
		Size: 102.2 KB (102184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ea8d43c1a06238999dc5a31e4afc3eac20f6442ab8bf361fba1856084ccada`  
		Last Modified: Fri, 31 Jan 2025 03:16:51 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-nanoserver` - windows version 10.0.20348.3207; amd64

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

### `eclipse-temurin:17-nanoserver` - windows version 10.0.17763.6893; amd64

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
