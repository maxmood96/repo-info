## `openjdk:24-nanoserver`

```console
$ docker pull openjdk@sha256:fde0f22c0b01b1328ec1be5361a7b3f5586e907349b872d5601b14e35cb3da27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `openjdk:24-nanoserver` - windows version 10.0.17763.6414; amd64

```console
$ docker pull openjdk@sha256:4aa7580d6f0c6add3054e0de717de16e66768144ffabff13ae198772457530e7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.7 MB (367740532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2449871bf36eb5ee850b9109f899f6fa9effad8e7ef52161a9cc4313d1686dc`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Mon, 04 Nov 2024 23:52:01 GMT
SHELL [cmd /s /c]
# Mon, 04 Nov 2024 23:52:02 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 04 Nov 2024 23:52:02 GMT
USER ContainerAdministrator
# Mon, 04 Nov 2024 23:52:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 04 Nov 2024 23:52:14 GMT
USER ContainerUser
# Mon, 04 Nov 2024 23:52:14 GMT
ENV JAVA_VERSION=24-ea+22
# Mon, 04 Nov 2024 23:52:24 GMT
COPY dir:5e50887c940da79d56a5169252f15d264bd5cf89ab6beeed3fbfea87d60dd508 in C:\openjdk-24 
# Mon, 04 Nov 2024 23:52:30 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 04 Nov 2024 23:52:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d645f09ff47157f9a90f1af7d2962ed77bd6a64229c210bebcaa0abac02dff4`  
		Last Modified: Mon, 04 Nov 2024 23:52:37 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab87ce6d265b211f1f8a2068308873f0ee2b4a06069e728102b4bd039b972f53`  
		Last Modified: Mon, 04 Nov 2024 23:52:36 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df4cec5af392c1a705377630953d480cdb2bf63001076d6b34f1b312767b54a`  
		Last Modified: Mon, 04 Nov 2024 23:52:36 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88cb1f30700f8b9b040670afe5a2077cd7971748f23943500b63e584119439f`  
		Last Modified: Mon, 04 Nov 2024 23:52:36 GMT  
		Size: 67.2 KB (67165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3084375adac5a3ccd1140d3a6ae69b536d61ea0204b74d10729a2869bb301070`  
		Last Modified: Mon, 04 Nov 2024 23:52:34 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e855d2e558cfb8394b277a35eff7d1ad3c824e7d4093090acbda2a984d47913`  
		Last Modified: Mon, 04 Nov 2024 23:52:34 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9774e9f722314bc02cfd1e0d68279522b1a98e6cfd2bee56843aa9b414cf890`  
		Last Modified: Mon, 04 Nov 2024 23:52:45 GMT  
		Size: 208.0 MB (207967183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0b8caa1a498ec3c71721b99662917d56a5e5e64a9c7e46232835146f78cccf`  
		Last Modified: Mon, 04 Nov 2024 23:52:35 GMT  
		Size: 4.6 MB (4606169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ae0661c25c42d951c6f4e0d2c7b6284883629f3b06f73a44799db18851f930`  
		Last Modified: Mon, 04 Nov 2024 23:52:34 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
