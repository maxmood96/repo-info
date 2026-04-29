## `openjdk:27-ea-19-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:338657dab998a36b62ee62cb1d9382d5ee986ba1175d5ed5e8ae822465ac8895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `openjdk:27-ea-19-jdk-nanoserver` - windows version 10.0.26100.32690; amd64

```console
$ docker pull openjdk@sha256:4cb87273ee8c13366a912a69c0befe6b54c3a96334caa6c586a65c927d26120e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.4 MB (424436439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ef994d47473e60c3d5a35e304391e428a890274f5395e6be8dc700a2724c46`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 06:39:57 GMT
RUN Apply image 10.0.26100.32690
# Wed, 29 Apr 2026 00:08:53 GMT
SHELL [cmd /s /c]
# Wed, 29 Apr 2026 00:08:54 GMT
ENV JAVA_HOME=C:\openjdk-27
# Wed, 29 Apr 2026 00:08:54 GMT
USER ContainerAdministrator
# Wed, 29 Apr 2026 00:09:10 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 29 Apr 2026 00:09:11 GMT
USER ContainerUser
# Wed, 29 Apr 2026 00:09:11 GMT
ENV JAVA_VERSION=27-ea+19
# Wed, 29 Apr 2026 00:09:43 GMT
COPY dir:378159f457185cd7a701708bc44b3323875aa0cdc2561534dae1874c52fc8b46 in C:\openjdk-27 
# Wed, 29 Apr 2026 00:09:53 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 29 Apr 2026 00:09:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8af320c3b6d19296bcc7947e3beb8bc0c69cb12143db52efe988dc998ac088dc`  
		Last Modified: Tue, 14 Apr 2026 21:00:37 GMT  
		Size: 199.7 MB (199717094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3325a888b834585e732271dee62bac66a784afd2d0528e73af597ca5c47426b0`  
		Last Modified: Wed, 29 Apr 2026 00:09:59 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba3f58f09c6109fab4c412806669545ccf8a434c7b9ff9c626bf8ddba757340`  
		Last Modified: Wed, 29 Apr 2026 00:09:59 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ac52dbf74b05e9caa17a5f18f6d4e37292ebdb7db2b9c65ee87e6860288be8`  
		Last Modified: Wed, 29 Apr 2026 00:09:59 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1035c4fe9e7483f0fc0f59276e928b56b8372ec05b185a02266d6eed17698d46`  
		Last Modified: Wed, 29 Apr 2026 00:09:59 GMT  
		Size: 71.4 KB (71364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7717a699786acbe4b05adff9fa5907f43373993b6aa7eca08c8c9c096d48e14e`  
		Last Modified: Wed, 29 Apr 2026 00:09:58 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0fe053ad48f63ae7889cf9de905546daae5cf6c857a27ffe544ec135a7569e`  
		Last Modified: Wed, 29 Apr 2026 00:09:58 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1625bcf4aa62bdc073f5b71368f280b4a4396977d24eabf497a6cd2776752bc4`  
		Last Modified: Wed, 29 Apr 2026 00:10:14 GMT  
		Size: 224.5 MB (224538685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086bf9b5efe45f33f68d7a3f460955549da42467c16201f4916e73ec45df4800`  
		Last Modified: Wed, 29 Apr 2026 00:09:58 GMT  
		Size: 102.8 KB (102830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a9d37af3c06a8cd4826935f7beb529f0bfd12560611c225c19e48ae8764e5d`  
		Last Modified: Wed, 29 Apr 2026 00:09:58 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-19-jdk-nanoserver` - windows version 10.0.20348.5020; amd64

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
