## `eclipse-temurin:17-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:4fb87d1af8d7f1df6219eb62b5161f7f09e8aefb776d6a617b4226ca92561476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `eclipse-temurin:17-jdk-nanoserver-1809` - windows version 10.0.17763.6893; amd64

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
		Last Modified: Wed, 12 Feb 2025 21:38:54 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc76f37fdcdabe12fbf65a903e719a11bf3bfad416fe69f9106bce0cede1292`  
		Last Modified: Thu, 13 Feb 2025 04:13:52 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e63a5ee2bdaf50421e1a6248ba20e502d467fee610efa63c13053d5498d3cb`  
		Last Modified: Thu, 13 Feb 2025 04:13:53 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c65b7d7403119307f53f039c960b1b6ebf2b6700efd070060dd28d9580bb53`  
		Last Modified: Thu, 13 Feb 2025 04:13:52 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7c3bdd65f3a320edd317fbbdfa913bbb86917789c0084363b649b231b1947d`  
		Last Modified: Thu, 13 Feb 2025 04:13:52 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6ed4520ef3586fb49e8b522653e091fe98ed60816a4a6a3cf0ed6896dc5613`  
		Last Modified: Thu, 13 Feb 2025 04:13:53 GMT  
		Size: 73.4 KB (73385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8f274a1f56f860e797332863987d991ae4dfbb52d369446633a61da24efebe`  
		Last Modified: Thu, 13 Feb 2025 04:13:53 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6e8daebd93d7a57070b9b3c2605cb5636001e23771d99c6c9ba7b4116999a5`  
		Last Modified: Thu, 13 Feb 2025 04:14:05 GMT  
		Size: 187.2 MB (187233687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e09ad8dc0e0d1eefcdcc3f55a1239c2770530ffdfb9fc54a899dab1d578d90f`  
		Last Modified: Thu, 13 Feb 2025 04:13:53 GMT  
		Size: 3.6 MB (3616284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb6fcc7b544effb893be6493a48b538c1fb23d57074bb60466b3b2342f9e9f6`  
		Last Modified: Thu, 13 Feb 2025 04:13:53 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
