## `openjdk:18-nanoserver-1809`

```console
$ docker pull openjdk@sha256:86383b8dde6256c8aafc7ee019e3dba1c39aa5274be5e2472f99f81bdf7993f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `openjdk:18-nanoserver-1809` - windows version 10.0.17763.2237; amd64

```console
$ docker pull openjdk@sha256:d0d134b5ed905df7796069d6caa685dd51c478b554d2a7fc390981457f7fdf33
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289539233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1c95a994c9b0bea4f9d2ba5b2977e7cdcdcaaa36003b405c23a58dfb1a52ce`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 Oct 2021 08:01:14 GMT
RUN Apply image 1809-amd64
# Wed, 13 Oct 2021 18:17:55 GMT
SHELL [cmd /s /c]
# Thu, 14 Oct 2021 00:38:45 GMT
ENV JAVA_HOME=C:\openjdk-18
# Thu, 14 Oct 2021 00:38:45 GMT
USER ContainerAdministrator
# Thu, 14 Oct 2021 00:38:59 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 14 Oct 2021 00:38:59 GMT
USER ContainerUser
# Mon, 01 Nov 2021 18:19:39 GMT
ENV JAVA_VERSION=18-ea+21
# Mon, 01 Nov 2021 18:19:54 GMT
COPY dir:2484c24fc278a2a4f9b1faf3e56bed024398b36a40c94d33298963a00cd29cac in C:\openjdk-18 
# Mon, 01 Nov 2021 18:20:15 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 01 Nov 2021 18:20:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:934e212983f208dc2bebc5de38259a6a62f1761868aacfee2cb3585a13b1e24b`  
		Size: 102.7 MB (102661372 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ceff24c3c0c2c360cd3788fcde5c41e1d6601339f4944623c732558a6030e631`  
		Last Modified: Wed, 13 Oct 2021 19:12:58 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11210a1a14144795863cc9df7368535adbfcea9f756732c5757ce09ae1126ff9`  
		Last Modified: Sat, 16 Oct 2021 00:39:37 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef4f8f1bc44cf5deaf0e09239eb5f99652025d58114cc36025894b724e1e593`  
		Last Modified: Sat, 16 Oct 2021 00:39:37 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528cd68420af607e2ba2867ba7f9e41b2412cc5fcd6ad946de4355966a18b56b`  
		Last Modified: Sat, 16 Oct 2021 00:39:37 GMT  
		Size: 71.6 KB (71641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee7149c120a9a849ece2e9be315293f5b77a4443d8f1cc13b6d4745290851a9`  
		Last Modified: Sat, 16 Oct 2021 00:39:34 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f6ab0e8125909b4839fa3630f814e15752ae94184aeb644c131c36e86f7ed7`  
		Last Modified: Mon, 01 Nov 2021 18:29:54 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0194863ebb0b4ca3e95ef49b881b951b764c564ca69beb7893fcca10c7a14d5`  
		Last Modified: Mon, 01 Nov 2021 18:33:15 GMT  
		Size: 183.3 MB (183276570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b594411f0677c7d4da62c798a8c77e14e730fa26a00d9c2baae81457f6620f`  
		Last Modified: Mon, 01 Nov 2021 18:29:55 GMT  
		Size: 3.5 MB (3522798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8a1012c6318fbad5cad38c5704026c28f875b258b677e93ddc1a8d81afb1b9`  
		Last Modified: Mon, 01 Nov 2021 18:29:54 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
