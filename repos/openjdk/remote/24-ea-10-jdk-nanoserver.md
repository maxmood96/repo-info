## `openjdk:24-ea-10-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:274ccd6154c5cb23796949da4607a7a7f82af5f5e80ab6af11f08f01fa60ea28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `openjdk:24-ea-10-jdk-nanoserver` - windows version 10.0.17763.6054; amd64

```console
$ docker pull openjdk@sha256:439af465ee53f461663fbdb5b7dd7eb8880707dc32cbd44c25a001274986cd96
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.7 MB (365747281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e26cb22b8db948a3008e911a7fb19e955185e03c578b8e17b49bbd9f609fe5a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Mon, 12 Aug 2024 18:54:26 GMT
SHELL [cmd /s /c]
# Mon, 12 Aug 2024 18:54:28 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 12 Aug 2024 18:54:28 GMT
USER ContainerAdministrator
# Mon, 12 Aug 2024 18:54:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 12 Aug 2024 18:54:46 GMT
USER ContainerUser
# Mon, 12 Aug 2024 18:54:46 GMT
ENV JAVA_VERSION=24-ea+10
# Mon, 12 Aug 2024 18:54:54 GMT
COPY dir:a0005413b1ff002c67299af627065453fb2f1c08570e500b2c608b78686ad9ab in C:\openjdk-24 
# Mon, 12 Aug 2024 18:54:59 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 12 Aug 2024 18:55:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd61529bca6bd24118d837b77608e684ee34c8ecf02dd588bfbdca40d131c9ee`  
		Last Modified: Mon, 12 Aug 2024 18:55:04 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661377d7a4cffd4a317856ea4831d016a26976d441952ff5fdbf6a92eeeef684`  
		Last Modified: Mon, 12 Aug 2024 18:55:04 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5063ce6c63a0e4a0ead4c1b940381021c0d099c8eaa8b884053df1e38cf4c5`  
		Last Modified: Mon, 12 Aug 2024 18:55:03 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4c006456db7dee8276dd9ce52ce7b08f5552022292a04e5c752dc817a8033c`  
		Last Modified: Mon, 12 Aug 2024 18:55:03 GMT  
		Size: 68.0 KB (68013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a1e1d621777aac380de0b7fd2505890eae7c120e40ee3887af7f985ad27b7d`  
		Last Modified: Mon, 12 Aug 2024 18:55:02 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1aabfd5feae92a1bb642040c85a847af4422f8f960eec3f001602c2b4cfbd75`  
		Last Modified: Mon, 12 Aug 2024 18:55:02 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecd153157d70dc5d23dce34475e1f4147070b853c396e2e75e37faa263bc8f1e`  
		Last Modified: Mon, 12 Aug 2024 18:55:14 GMT  
		Size: 206.5 MB (206549118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b73a81d79d350564c5408061f79ad42a29d8a74fa266076c5c06d3844eaa8a`  
		Last Modified: Mon, 12 Aug 2024 18:55:03 GMT  
		Size: 4.0 MB (4042550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdc2cf69406253923b89d9eaf2aa1329f8a498d3ced382a5695699dca8b874e`  
		Last Modified: Mon, 12 Aug 2024 18:55:03 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
