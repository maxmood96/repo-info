## `openjdk:27-ea-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:8d5bbd343a18a3baf08db7319e7434085d1a5a616135c45e755fe77fd21cac32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `openjdk:27-ea-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull openjdk@sha256:3a8c20669293ba54363658536067a6d386e524817d459dd7c06213b8ecbc4f46
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.7 MB (351680256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2a1fa066fc80699df61d926792f45fddf66b3b62ed0961c5001a8fa84ea7a5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Wed, 29 Apr 2026 00:08:58 GMT
SHELL [cmd /s /c]
# Wed, 29 Apr 2026 00:08:58 GMT
ENV JAVA_HOME=C:\openjdk-27
# Wed, 29 Apr 2026 00:09:00 GMT
USER ContainerAdministrator
# Wed, 29 Apr 2026 00:09:11 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 29 Apr 2026 00:09:12 GMT
USER ContainerUser
# Wed, 29 Apr 2026 00:09:12 GMT
ENV JAVA_VERSION=27-ea+19
# Wed, 29 Apr 2026 00:10:00 GMT
COPY dir:378159f457185cd7a701708bc44b3323875aa0cdc2561534dae1874c52fc8b46 in C:\openjdk-27 
# Wed, 29 Apr 2026 00:10:06 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 29 Apr 2026 00:10:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfd150c8ce2e100aa6449a618e2c48f5a4223da8f76c6d3ad38d6aa153c6826`  
		Last Modified: Wed, 29 Apr 2026 00:10:15 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492db6ce264a7692e3345f92cbca8b8e7d4d2a7504b04c040fd72b505831c803`  
		Last Modified: Wed, 29 Apr 2026 00:10:14 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cabba79b4c997c85ed2687235439e51c09c16c922131ca22eed744940c689745`  
		Last Modified: Wed, 29 Apr 2026 00:10:14 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ae9ade6388a8d6c40617a3cfeabe52aad325a2408af60ac85de04f37a91c95`  
		Last Modified: Wed, 29 Apr 2026 00:10:14 GMT  
		Size: 70.8 KB (70758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfbbd3a24780c459bce41e952025bc88ccc9f526c7c12da45db5ec202a78b95`  
		Last Modified: Wed, 29 Apr 2026 00:10:12 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d64b40ed2ab04ec84f0a608e19f54f209a25801114792b81d8846a3ad267fe`  
		Last Modified: Wed, 29 Apr 2026 00:10:12 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151110e57a6759b2b4e8339317597800b5ff1f1059d9d095fe589d2cb04aae45`  
		Last Modified: Wed, 29 Apr 2026 00:10:28 GMT  
		Size: 224.5 MB (224538811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74de6c7ae20adb5b8388976143cdd1260dfb1b8ce5c0c813730c09f3ef959cf5`  
		Last Modified: Wed, 29 Apr 2026 00:10:13 GMT  
		Size: 108.3 KB (108346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0023e6dcd613fdf38347c42e2d76fa8bdf1b5b7355630e75cf498eecc579ae28`  
		Last Modified: Wed, 29 Apr 2026 00:10:12 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
