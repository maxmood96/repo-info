## `openjdk:27-ea-19-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:50f03b8c0927681eeff0499bfb1b9e5695246e883e14564d2f1b007757453138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `openjdk:27-ea-19-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.32690; amd64

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
