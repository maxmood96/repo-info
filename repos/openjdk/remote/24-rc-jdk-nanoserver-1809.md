## `openjdk:24-rc-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:48a3813d3cacd77bf22ffe9277675baa6d31372e2179267967b17f4c92b4e5a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `openjdk:24-rc-jdk-nanoserver-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull openjdk@sha256:296396df4bb3a27df6f57305a46c036bc95239f9b067da25109484c9e141b9e1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.9 MB (319947495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe27c8d69bd53797c7cba7c49cee2885338a2b2f99ddfc43ef7123ce20e75d6b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:15:32 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:15:33 GMT
ENV JAVA_HOME=C:\openjdk-24
# Thu, 13 Feb 2025 01:15:34 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:15:36 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 13 Feb 2025 01:15:36 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:15:37 GMT
ENV JAVA_VERSION=24
# Thu, 13 Feb 2025 01:15:44 GMT
COPY dir:cf5ecdf170ed29d5224593d2b3a510464d2e7297517065c397a2229de8b2a139 in C:\openjdk-24 
# Thu, 13 Feb 2025 01:15:49 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 13 Feb 2025 01:15:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d693e20229b4584d695af0ea22ff9983a8de5c2580d824746662df0d098f502`  
		Last Modified: Thu, 13 Feb 2025 01:15:57 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048de90e4af2eabd8e88300d174a6eaf8d1affb9595bcb44a910aa550b022535`  
		Last Modified: Thu, 13 Feb 2025 01:15:56 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19bb4302440864df2605567730ccb6b95ebc4b08573d103a940c53acf995219`  
		Last Modified: Thu, 13 Feb 2025 01:15:56 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d6b5ce27eeb5fe93f3581fa080e78a5b7323e2324ad9d7d06be329180949cb`  
		Last Modified: Thu, 13 Feb 2025 01:15:56 GMT  
		Size: 71.8 KB (71844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f236e3498e94674c64603c786bf6df9aaf5094fb7432f19754a7f1bc615b010`  
		Last Modified: Thu, 13 Feb 2025 01:15:54 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555c2989c1b53c407da6d9802d5c6defa5d3e1792cafc3729a6ff5708bca5633`  
		Last Modified: Thu, 13 Feb 2025 01:15:54 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f41e9c89e8697db60ccd4b7fc32bf2e9f9dd03475e4dd99beddffd626920a5d`  
		Last Modified: Thu, 13 Feb 2025 01:16:05 GMT  
		Size: 208.5 MB (208527262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42030d586c0ee7286f1ab46a1f0682b98fb2b2935a3e2769b0c20ba5b22d66b`  
		Last Modified: Thu, 13 Feb 2025 01:15:55 GMT  
		Size: 4.4 MB (4426662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf7b48f254b4096babf9224902bad9fc075703ed90c1c0e1864722b25ee4867`  
		Last Modified: Thu, 13 Feb 2025 01:15:54 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
