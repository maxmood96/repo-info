## `openjdk:24-nanoserver`

```console
$ docker pull openjdk@sha256:349f68f5dfd2883d4233370aa60ed5336ae915c5a18690dc1878d5270cf95688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `openjdk:24-nanoserver` - windows version 10.0.17763.5820; amd64

```console
$ docker pull openjdk@sha256:41f7bf6decb9884f4a60fc813ea724241f853fdd99291ef467520d5d43106d8e
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.3 MB (366305164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bdb221a0c9f832b8ec5b190104ec658061a78bd3f12f60d158cbd5713814c2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 12 Jun 2024 01:51:15 GMT
SHELL [cmd /s /c]
# Wed, 12 Jun 2024 01:51:16 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 12 Jun 2024 01:51:17 GMT
USER ContainerAdministrator
# Wed, 12 Jun 2024 01:51:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 12 Jun 2024 01:51:27 GMT
USER ContainerUser
# Wed, 12 Jun 2024 01:51:27 GMT
ENV JAVA_VERSION=24-ea+1
# Wed, 12 Jun 2024 01:51:35 GMT
COPY dir:65f162ff11cc2a31de446754da8c804d9d59bb6267610365535eba662147bf29 in C:\openjdk-24 
# Wed, 12 Jun 2024 01:51:45 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 12 Jun 2024 01:51:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0778987f8503dc699b22d5d82344cf8f75188b6200ed8918f23a02f3cb08e2b7`  
		Last Modified: Wed, 12 Jun 2024 01:51:50 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec908ed238b31da1568e4fdcf32e9c65f2369b0e5998bda1afd1f2567743782`  
		Last Modified: Wed, 12 Jun 2024 01:51:49 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95a0bcce933c865b8ae6e898de6a7e46a4b32656f195de4aef635822537afe2`  
		Last Modified: Wed, 12 Jun 2024 01:51:49 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4f9881c5ba3e71cf91e9529b97860037dac0bad54bc54b81c0728602bccc59`  
		Last Modified: Wed, 12 Jun 2024 01:51:49 GMT  
		Size: 67.6 KB (67585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b7607ef4ffd64c68f078c7fa81aed242af84f2616041e23b4a324264104a2f`  
		Last Modified: Wed, 12 Jun 2024 01:51:48 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aef60f7c6b48fe029c9f4309b8d7ee1a09e92e80fd03b12737ec6fd96e04b2b`  
		Last Modified: Wed, 12 Jun 2024 01:51:48 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b031a491a865b4b4845ce9e8cbd761dea58d0ced1cfdcb26e739e024838acea`  
		Last Modified: Wed, 12 Jun 2024 01:52:02 GMT  
		Size: 206.1 MB (206107306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593232a011d9d39368349b98eca75329b90ee50b19ed7aec856217a3a9e9608b`  
		Last Modified: Wed, 12 Jun 2024 01:51:49 GMT  
		Size: 5.2 MB (5182651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076720e7702df919022288efb20f79cd5d652827df4710995bebca118b247ef4`  
		Last Modified: Wed, 12 Jun 2024 01:51:48 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
