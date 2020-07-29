## `openjdk:14-nanoserver-1809`

```console
$ docker pull openjdk@sha256:8cd886a6551f0c3cd2b6c5646b53efb56d87693c5c371cc8b02583085ebb951c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `openjdk:14-nanoserver-1809` - windows version 10.0.17763.1339; amd64

```console
$ docker pull openjdk@sha256:42a183914eef02021a6fc23e557cbbe11c044de3de53902f225f4d10dea63b07
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298415589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d89f8f0d5a231723e72bce1f1795e0db0b00365b7851b008885c3c6c8ec520ec`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 07 Jul 2020 13:50:07 GMT
RUN Apply image 1809-amd64
# Wed, 15 Jul 2020 01:54:43 GMT
SHELL [cmd /s /c]
# Wed, 15 Jul 2020 02:12:39 GMT
ENV JAVA_HOME=C:\openjdk-14
# Wed, 15 Jul 2020 02:12:39 GMT
USER ContainerAdministrator
# Wed, 29 Jul 2020 01:22:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 29 Jul 2020 01:22:05 GMT
USER ContainerUser
# Wed, 29 Jul 2020 01:22:06 GMT
ENV JAVA_VERSION=14.0.2
# Wed, 29 Jul 2020 01:22:54 GMT
COPY dir:3af480213c50f048b93f5646f49ddcfa051042f65b9b399de73d2b228bd2576f in C:\openjdk-14 
# Wed, 29 Jul 2020 01:23:13 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Wed, 29 Jul 2020 01:23:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dc95608099543221ef539391bfece5c1ce37b97af9da457f5990349cab028a12`  
		Size: 100.9 MB (100895619 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9f6486e4debac36806ed3527d9b1baea75c1a807e26baccdd0a2f521c814273f`  
		Last Modified: Wed, 15 Jul 2020 02:43:55 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d3e6cef870db96286acadd1f120ec81c36417ee6a78d10f6fc2f8c22a2cc75`  
		Last Modified: Wed, 15 Jul 2020 02:48:53 GMT  
		Size: 863.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9395c647ca5e721143135d323ee31b938bb8873a7a95682f423118071b7262a3`  
		Last Modified: Wed, 15 Jul 2020 02:48:52 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79edb773b7bb32c8cafef89d504f2ddd0ef8ef30fda5d5dffbfb366dc9b306a`  
		Last Modified: Wed, 29 Jul 2020 01:47:53 GMT  
		Size: 67.1 KB (67116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1871daf0485aa60bc35f5ae0e61bf77bd5e64f18e9f22a72b921e3b046727d90`  
		Last Modified: Wed, 29 Jul 2020 01:47:50 GMT  
		Size: 905.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1807df8c45b7b92957dabf5097df23ad7a76baaef363a9727cde6b9703edb05a`  
		Last Modified: Wed, 29 Jul 2020 01:47:50 GMT  
		Size: 909.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235036880c320022df266c39b423b9419e6d627a082e0677547fbbcd264e7326`  
		Last Modified: Wed, 29 Jul 2020 01:51:18 GMT  
		Size: 194.0 MB (193968703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c94020bf95dea824dff2f1c26ad6ee4214bdb7d3207b03067e7e4e50069e6b5`  
		Last Modified: Wed, 29 Jul 2020 01:47:54 GMT  
		Size: 3.5 MB (3478774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab0d87a91dbbb55fc522b6dde2f2719d356ab019f2be5532bfec8f69059cc8b`  
		Last Modified: Wed, 29 Jul 2020 01:47:50 GMT  
		Size: 919.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
