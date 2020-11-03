## `openjdk:16-ea-22-nanoserver-1809`

```console
$ docker pull openjdk@sha256:f101e509f7bd9235b31175ec3542d432b4480667f7764f57ee72883078109564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `openjdk:16-ea-22-nanoserver-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull openjdk@sha256:7d248b7cd7751506e8e8bbc29d719438457771f8f4b8e6ba08ad4280f74d0ca8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.5 MB (299500471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9569c5d8d46434725758ef21d2a8b51cb9a6c6e5b2f8dc56152ef677cd30b52b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 30 Sep 2020 11:25:56 GMT
RUN Apply image 1809-amd64
# Wed, 14 Oct 2020 17:46:04 GMT
SHELL [cmd /s /c]
# Wed, 14 Oct 2020 17:46:05 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 14 Oct 2020 17:46:06 GMT
USER ContainerAdministrator
# Wed, 14 Oct 2020 17:46:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 14 Oct 2020 17:46:22 GMT
USER ContainerUser
# Mon, 02 Nov 2020 23:19:10 GMT
ENV JAVA_VERSION=16-ea+22
# Mon, 02 Nov 2020 23:19:47 GMT
COPY dir:20a85106f1ecd9fb7affbb1654229a7f6d0e60c4d52ce2224f17833f0f1891c2 in C:\openjdk-16 
# Mon, 02 Nov 2020 23:20:16 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Mon, 02 Nov 2020 23:20:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:aab6118ce69c93410df7fa15842a6e3b3c7ff20b639c779b5d5f78e7653eaa07`  
		Size: 101.2 MB (101205155 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:40f59dc77cd194db29e444ce30cc9a91a3d555f7d4d7329fb6f46c13e559dc2f`  
		Last Modified: Wed, 14 Oct 2020 18:31:55 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2c5c7ff5b97e2384ad57c7cd4094b1a40907ea3634e923a539236764052c20`  
		Last Modified: Wed, 14 Oct 2020 18:31:53 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e535cf22ef1ca77aebd1948de6ab3937b1f63d64895ea717d71cff42d95815`  
		Last Modified: Wed, 14 Oct 2020 18:31:54 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a209bbfc514f45496baa96d8592838b00434aae4cd11fb8ffbcf643dfe386c`  
		Last Modified: Wed, 14 Oct 2020 18:31:52 GMT  
		Size: 72.2 KB (72249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc31a2a793752d0400745705f15ea0e51a67ed288dc5bc3c6eda4520ca139549`  
		Last Modified: Wed, 14 Oct 2020 18:31:50 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84bee22dfbf7e8a20b6194035060e1d02c63ca0555d9a8b0ba0fd90fb539b86`  
		Last Modified: Mon, 02 Nov 2020 23:33:15 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8becc1d59d5b65ec16f69e88a6b819e1f979648bff12c08a3b96bb689164b9`  
		Last Modified: Mon, 02 Nov 2020 23:34:32 GMT  
		Size: 194.6 MB (194550995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9373832506254f5850a95c031bebc30dc5d5f5f0625d5ec78d28aa22c271d4ee`  
		Last Modified: Mon, 02 Nov 2020 23:33:18 GMT  
		Size: 3.7 MB (3666747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eea98e44517975387ea47f9909c87f37a7879d7bf94f18d3e4ae991eba129a7`  
		Last Modified: Mon, 02 Nov 2020 23:33:15 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
