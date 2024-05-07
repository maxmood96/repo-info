## `openjdk:23-nanoserver`

```console
$ docker pull openjdk@sha256:6026b4111ede3b58c6226385e3558dcd0f36a5707b2d3e414f4523ff4858d57e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `openjdk:23-nanoserver` - windows version 10.0.17763.5696; amd64

```console
$ docker pull openjdk@sha256:cc9888caffd70147b31e7ddf3d00a101d6dbaa0c6e301ec6dc2ac3dd414559bb
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.1 MB (313129018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0017f1bd19a9e1e94863c3e8a91d72800323a14ed43e34f13b3efeb1ad330e2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Tue, 07 May 2024 00:53:15 GMT
SHELL [cmd /s /c]
# Tue, 07 May 2024 00:53:17 GMT
ENV JAVA_HOME=C:\openjdk-23
# Tue, 07 May 2024 00:53:18 GMT
USER ContainerAdministrator
# Tue, 07 May 2024 00:53:37 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 07 May 2024 00:53:38 GMT
USER ContainerUser
# Tue, 07 May 2024 00:53:38 GMT
ENV JAVA_VERSION=23-ea+21
# Tue, 07 May 2024 00:53:47 GMT
COPY dir:46ff76b54504bbd09b6d1807df39eacdbd5afd7a9adfdfb43e3c3dedbf203f3d in C:\openjdk-23 
# Tue, 07 May 2024 00:53:54 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 07 May 2024 00:53:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c6e73bb0f65dfe5bf9201026a53246df060392b8fca8900e31c35fc06b503d`  
		Last Modified: Tue, 07 May 2024 00:53:58 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f1a5d1fa8cdd11d205864b98ae6c50d1d829427ea3846570027edeec7f833c`  
		Last Modified: Tue, 07 May 2024 00:53:58 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9117931a06c55b69fd24dca1cf57035a344113a29ec49b27fb668d88cf405160`  
		Last Modified: Tue, 07 May 2024 00:53:57 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5e7724834203e2f2e6e44a837f5d568d0fee4b7e39f071d95bd57463b75354`  
		Last Modified: Tue, 07 May 2024 00:53:58 GMT  
		Size: 66.6 KB (66643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80259ca737dd3f52db859a2b20824cb889fb2e49f83925d36f4e9922ae51857e`  
		Last Modified: Tue, 07 May 2024 00:53:57 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2d0290f22f6ac3cb7c5006f56a7c0df24e4f628e276047267122cd95373cb1`  
		Last Modified: Tue, 07 May 2024 00:53:57 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1da6daed732092bd0afcb2ff36b440372382ea70ad6305582da1f4bb66bb512`  
		Last Modified: Tue, 07 May 2024 00:54:08 GMT  
		Size: 204.4 MB (204360472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f4ded9c0a44d59823060dc52078f903c300132f358b1a537a40a8184c99088`  
		Last Modified: Tue, 07 May 2024 00:53:57 GMT  
		Size: 3.8 MB (3806559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6409aa714e9b359ec9b6e314c25f9c668d58e581bbd5c505aa033d16f6914f8`  
		Last Modified: Tue, 07 May 2024 00:53:57 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
