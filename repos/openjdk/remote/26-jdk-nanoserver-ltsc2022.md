## `openjdk:26-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:7324ada16031b86f2df4d663a65d54f9fe7a831388246201cfdbf1ceacc474df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `openjdk:26-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull openjdk@sha256:69b33d3cef9d951d8a3e996fd46f2422ae15a2ca8115fd465f40ee13fd522c48
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.5 MB (341517971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28d630403a7772b9df16ad5a0622d739345de1d398c4115a224a6065f0b523f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Mon, 25 Aug 2025 21:08:08 GMT
SHELL [cmd /s /c]
# Mon, 25 Aug 2025 21:08:10 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 25 Aug 2025 21:08:11 GMT
USER ContainerAdministrator
# Mon, 25 Aug 2025 21:08:17 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 25 Aug 2025 21:08:18 GMT
USER ContainerUser
# Mon, 25 Aug 2025 21:08:19 GMT
ENV JAVA_VERSION=26-ea+12
# Mon, 25 Aug 2025 21:08:28 GMT
COPY dir:23627f427415b3b023db24eb5c90428360be7dfe45222aac34ba93035dd0822d in C:\openjdk-26 
# Mon, 25 Aug 2025 21:08:35 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 25 Aug 2025 21:08:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afffdf1d63be122cf2f3d6cb2347feb802fe8908e0a2de2ab3d1cb430342af5e`  
		Last Modified: Mon, 25 Aug 2025 21:09:11 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77219afaf85395f08795d374b77a15b325fca099d845e399cd27ea20e489b6c`  
		Last Modified: Mon, 25 Aug 2025 21:09:11 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4ea2a13207bcf764bb592069499e46eb0ea829a019df72c312349c7442c212`  
		Last Modified: Mon, 25 Aug 2025 21:09:11 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11180c2a36d1c2f985a2488774de129f1a1e2ff16d1d9bab96e8b554e1feab45`  
		Last Modified: Mon, 25 Aug 2025 21:09:11 GMT  
		Size: 76.3 KB (76334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8723e032193de2b8e6eef8b1e49868eb6c08efbde65c1f38eaf9491eaf5994d5`  
		Last Modified: Mon, 25 Aug 2025 21:09:12 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60958d1062feb1ead50513dfd33a7a5b3420b5052609664ed7c2ebe856de3b26`  
		Last Modified: Mon, 25 Aug 2025 21:09:12 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbcb7e2eabd9bad2fd134cb62c5c6e4624aea119b5f3cb8f2c172ff58082936`  
		Last Modified: Tue, 26 Aug 2025 00:24:39 GMT  
		Size: 218.7 MB (218668984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536467b9f622d3690b74b76535f70aaab293c3948ffe8b472e3e8d709b1ff71c`  
		Last Modified: Mon, 25 Aug 2025 21:09:12 GMT  
		Size: 106.2 KB (106161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c36301738c40b9c6016666ed4925b1fa97f8ead8b61c037d614214d2b9dc0ca`  
		Last Modified: Mon, 25 Aug 2025 21:09:11 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
