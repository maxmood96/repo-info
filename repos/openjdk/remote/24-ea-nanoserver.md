## `openjdk:24-ea-nanoserver`

```console
$ docker pull openjdk@sha256:c68c2c0031dc9690559d0fc2ac69af659d462447e5269d0c41a2b1798aefd881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `openjdk:24-ea-nanoserver` - windows version 10.0.17763.6189; amd64

```console
$ docker pull openjdk@sha256:880f2f71b4efe500507856f699734dd1e1e00976d81c7af420b60021e86ccba4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367270968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ea621677928a2a348ce019053ae7e040bc2fe444e1cfa6436669be0763c208`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Fri, 16 Aug 2024 23:00:24 GMT
SHELL [cmd /s /c]
# Fri, 16 Aug 2024 23:00:27 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 16 Aug 2024 23:00:27 GMT
USER ContainerAdministrator
# Fri, 16 Aug 2024 23:00:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 16 Aug 2024 23:00:30 GMT
USER ContainerUser
# Fri, 16 Aug 2024 23:00:30 GMT
ENV JAVA_VERSION=24-ea+11
# Fri, 16 Aug 2024 23:00:37 GMT
COPY dir:fa9c1b64880615ad4e9fb29d206a8848a2cae5c906dabcd0c7376dfa01c3eafc in C:\openjdk-24 
# Fri, 16 Aug 2024 23:00:43 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 16 Aug 2024 23:00:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c4e5a6832ff8986e5f371e5f5a2454121f006cc4c98cbfefb8bb0445da2a9431`  
		Last Modified: Tue, 13 Aug 2024 18:40:28 GMT  
		Size: 155.1 MB (155083093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af597510eb1b6bd0c6ea3c20fcb965e67e06e16d04dba1bcf45a2b6fc288a51c`  
		Last Modified: Fri, 16 Aug 2024 23:00:50 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca60165c38ffc9f74bb12123e9cccda4b226d99d0e1e99d9f4f888376427ab97`  
		Last Modified: Fri, 16 Aug 2024 23:00:49 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c36e128a2fde45a4c1bb73cd1bfc0c95c7b274c2dce4d9a7002da538f77200`  
		Last Modified: Fri, 16 Aug 2024 23:00:49 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474e564f1c751c9247ab0af26f5aed9baef8937f4c8cbfb3cc6c194ebfb1261a`  
		Last Modified: Fri, 16 Aug 2024 23:00:49 GMT  
		Size: 75.3 KB (75288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8d92c57d1f3ddc7a0891578268ae7787023b92ef210b98b726935498d27dc6`  
		Last Modified: Fri, 16 Aug 2024 23:00:47 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9ff0d4e79c6083967c731ba5c55280bd229c0cc40aa46a7dc0871d94d34b77`  
		Last Modified: Fri, 16 Aug 2024 23:00:47 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b0ff1cf27cd982aa6b2a393c362a19c331c3e20fe103ec1dc2b5bc5b8e319e0`  
		Last Modified: Fri, 16 Aug 2024 23:00:59 GMT  
		Size: 207.6 MB (207551201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20368fc2ef4fab061dd9d5e30ddbb1dbdb6be4a638a765fd4c2b3b99962b8e25`  
		Last Modified: Fri, 16 Aug 2024 23:00:48 GMT  
		Size: 4.6 MB (4554852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e8e6738c89edb3e4ba8625ccc819552253d6766c27f0c5f1c33a21c354dc04`  
		Last Modified: Fri, 16 Aug 2024 23:00:47 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
