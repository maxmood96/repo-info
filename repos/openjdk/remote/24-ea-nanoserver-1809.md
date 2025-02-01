## `openjdk:24-ea-nanoserver-1809`

```console
$ docker pull openjdk@sha256:3af5fbd65dfd483a6eceeff39acc1cc802ee652ae3b2915397cf7be6c73f2566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `openjdk:24-ea-nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:6becba0ec6c2e3bec4143b45db006214baaea98466a967279bb02c1c5cb03581
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.3 MB (368290739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68335dabcbaea2173fbe949372931498e76233969e5f32cd6b43206621235b6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Fri, 31 Jan 2025 23:28:15 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 23:28:18 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 31 Jan 2025 23:28:18 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 23:28:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 31 Jan 2025 23:28:40 GMT
USER ContainerUser
# Fri, 31 Jan 2025 23:28:41 GMT
ENV JAVA_VERSION=24-ea+34
# Fri, 31 Jan 2025 23:28:54 GMT
COPY dir:0417d4640b3e9898160c754927e6892a89119d4a6294484281d02c0d6a35e95f in C:\openjdk-24 
# Fri, 31 Jan 2025 23:29:01 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 31 Jan 2025 23:29:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a99c5ebd4604be337c7fb6e6cb45247b83cba51bbdc92c8bc6e9b6f9b24810`  
		Last Modified: Fri, 31 Jan 2025 23:29:06 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c4d8208345e4826977d57e36bd7985f0fd36b36a45a45cfdc2ca9d56f85b39`  
		Last Modified: Fri, 31 Jan 2025 23:29:05 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617939baf63e87a8bf207f917e213b24794a798fbc744c50240844c3db578356`  
		Last Modified: Fri, 31 Jan 2025 23:29:05 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def3112b3583e5a4bbf414f9947f51eb136e573de78e0a736289b3d8aaac9070`  
		Last Modified: Fri, 31 Jan 2025 23:29:05 GMT  
		Size: 81.7 KB (81734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa0e96e02182b98cab8c9e2d390f0b013d48b675db9fa45a84a3e3b0227f261`  
		Last Modified: Fri, 31 Jan 2025 23:29:04 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8553526d363f93c9a2acfa09e58bd9e87ce94ea7698283a46835f6a7c864433f`  
		Last Modified: Fri, 31 Jan 2025 23:29:04 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963fa4fe915f76e0f99cb0eaeb5451b858d9d028fbe98441a2a3dd9e4ef137be`  
		Last Modified: Fri, 31 Jan 2025 23:29:15 GMT  
		Size: 208.5 MB (208532469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cb451df3f3c45f09858c5f9ec62f469c3feec176df32ccc63de2b93743b4b0`  
		Last Modified: Fri, 31 Jan 2025 23:29:05 GMT  
		Size: 4.4 MB (4402621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cdc86c81aa56273b46de2d3d6ec74adcee38bee7bfe165b5efcdeb5975861c`  
		Last Modified: Fri, 31 Jan 2025 23:29:04 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
