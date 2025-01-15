## `openjdk:25-ea-5-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:17366bd2a6c59deaeed27723175c1b6b5c5356e01571ce31e720c907dd3d0ca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `openjdk:25-ea-5-jdk-nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:0bf4b6656a136ce082a9257c7ec6d9b14b5096a415c8d1141de62c953c215c7e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.4 MB (368386708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d08153647c0aeccec0df962729ac3a4519bfa4ddf775a79a7fe45302a532e46`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 15 Jan 2025 18:09:07 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2025 18:09:10 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 15 Jan 2025 18:09:10 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 18:09:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 15 Jan 2025 18:09:13 GMT
USER ContainerUser
# Wed, 15 Jan 2025 18:09:14 GMT
ENV JAVA_VERSION=25-ea+5
# Wed, 15 Jan 2025 18:09:21 GMT
COPY dir:63c8c2c9000bce70ab79161ee8d862be4b6eb9e24d02b8adc700a46d4799aaa8 in C:\openjdk-25 
# Wed, 15 Jan 2025 18:09:26 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 15 Jan 2025 18:09:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4681b2451d6a664a9a00ae9b95a136e502cc69093b6fde7af097cddf881cc4de`  
		Last Modified: Wed, 15 Jan 2025 18:09:34 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3f33743ca09f8cb72f63e7dbd89bc58c9ba3332234afb7cf5a1324502f7206`  
		Last Modified: Wed, 15 Jan 2025 18:09:33 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e94fc2e60b1599e861083ac4a74c8127ec9f149db0d0f3bc5602bed244bf573`  
		Last Modified: Wed, 15 Jan 2025 18:09:33 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b945d80dce7f9f8e5557d4614b2ee8b96f0c8b9795a631fb457bee1eca3b7f`  
		Last Modified: Wed, 15 Jan 2025 18:09:33 GMT  
		Size: 88.0 KB (87951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87221052ba2e06b9413adae232d8824ea02f6714fcb464a979d155c2fdec5b21`  
		Last Modified: Wed, 15 Jan 2025 18:09:31 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e9b3df29c96a0e57f17b9d70f966ffade0ff5c7455cdbdf9bd5404166b82f8`  
		Last Modified: Wed, 15 Jan 2025 18:09:31 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4e5d8c6ce5704348e5dc0db1737c9ef6d8ac116816154b97bed32b4f6ea36e`  
		Last Modified: Wed, 15 Jan 2025 18:09:43 GMT  
		Size: 208.6 MB (208624192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea140511be13b145cb4ce2997d73a6bb241b8ac83fcdf0895c8799e590ab0223`  
		Last Modified: Wed, 15 Jan 2025 18:09:32 GMT  
		Size: 4.4 MB (4400750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e07bb95550e070cf78ff6d8fc329443b646c4348ccccfb092073a4173f2e46b`  
		Last Modified: Wed, 15 Jan 2025 18:09:31 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
