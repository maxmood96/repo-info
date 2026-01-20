## `openjdk:26-ea-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:a6449f3121df7d84e98ea931b51d97d631b5a7834200d538883465e508890c55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `openjdk:26-ea-nanoserver-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull openjdk@sha256:1dd78a4e768f2e739d4e5a95996c71f99ad4f09da860a67953d6b95ad39ca29a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.1 MB (423112370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7deafeca8be97a36ede7e3552eadee58d86e82fd3206c3b86ab9eafd5a0febba`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 23:39:23 GMT
SHELL [cmd /s /c]
# Tue, 13 Jan 2026 23:41:07 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 13 Jan 2026 23:41:07 GMT
USER ContainerAdministrator
# Tue, 13 Jan 2026 23:41:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 13 Jan 2026 23:41:09 GMT
USER ContainerUser
# Tue, 13 Jan 2026 23:41:10 GMT
ENV JAVA_VERSION=26-ea+30
# Tue, 13 Jan 2026 23:41:22 GMT
COPY dir:e07e90760755fda5775e159516136ae7ac9e724b6c3d3e98906408d196af4b98 in C:\openjdk-26 
# Tue, 13 Jan 2026 23:41:27 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 13 Jan 2026 23:41:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:10 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449a8f38121ad9ab7bb32fd54119825e5f6c3a13152940fa400e7a44dd22a6bf`  
		Last Modified: Tue, 13 Jan 2026 23:40:44 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ced718e74d685b725f4052d135240c41b555fd8824695a48f9035a4858c1ed`  
		Last Modified: Tue, 13 Jan 2026 23:41:33 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff84be404aa57e42fe8a76f6706d4284542d81c9ed22b5b5dde873d94ccd6831`  
		Last Modified: Tue, 13 Jan 2026 23:41:55 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60edc2b0d87181243db16220d8d27184a5803d8b42b355e056e3e5eea50fad5`  
		Last Modified: Tue, 13 Jan 2026 23:41:55 GMT  
		Size: 72.0 KB (71951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413694019043a62fc6686df5b55296fe526d233c162e29f99f909beb4ff1f4d4`  
		Last Modified: Tue, 13 Jan 2026 23:41:56 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda0ec99d44ba1cdb0ccd89ac69e1e0e1a0875135b298c08256625493382f40e`  
		Last Modified: Tue, 13 Jan 2026 23:41:31 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d19551296afbace182d99da87c8a5bce8885636e533418f8716a5c2f06d33bf`  
		Last Modified: Tue, 13 Jan 2026 23:41:48 GMT  
		Size: 223.8 MB (223833233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d75a536adf46f39f39e08b47022e7b5c548dc4540ae37fc2e91d7827bdcea2`  
		Last Modified: Tue, 13 Jan 2026 23:41:55 GMT  
		Size: 124.2 KB (124197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9280b49445ed1411162e1e4385040239f63ec475ca48fa2b6f449c2e1ad461fb`  
		Last Modified: Tue, 13 Jan 2026 23:41:55 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
