## `openjdk:24-ea-2-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:b7dc86cc3492ed26c7122c2e52d488f33d86d0289516bd75ba250231b42464c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `openjdk:24-ea-2-jdk-nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull openjdk@sha256:b9edb80307468b6e71a01be5f4f699df977bc55c7d3f26a9d64f10e8c99c10bd
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.4 MB (365408577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc694bba92fa506e9b140ead62ff3d82b99cbdec810e0debe846e72f380321a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Fri, 14 Jun 2024 02:09:16 GMT
SHELL [cmd /s /c]
# Fri, 14 Jun 2024 02:09:19 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 14 Jun 2024 02:09:20 GMT
USER ContainerAdministrator
# Fri, 14 Jun 2024 02:09:22 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 14 Jun 2024 02:09:23 GMT
USER ContainerUser
# Fri, 14 Jun 2024 02:09:24 GMT
ENV JAVA_VERSION=24-ea+2
# Fri, 14 Jun 2024 02:09:32 GMT
COPY dir:fe077db189be93524d6534b91377d96635001989a5ab7b04a3674170104c88ed in C:\openjdk-24 
# Fri, 14 Jun 2024 02:09:38 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 14 Jun 2024 02:09:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34efdb562c5b7529d8d4592d3c92118ee90ae9e199789ee73ee3ebe626f6dbcb`  
		Last Modified: Fri, 14 Jun 2024 02:09:46 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049b6396568b4d94101e8962396ab2a95d3fb63b54e64449c26546c2d803fb76`  
		Last Modified: Fri, 14 Jun 2024 02:09:45 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169a0793ade90f4f76f9d18952d01a6fe608291c32ccc8eee81661e102e00c45`  
		Last Modified: Fri, 14 Jun 2024 02:09:45 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c4bf1f851fb215b1cda2441f8da944b2041395827d20dfd24a9f92011140db`  
		Last Modified: Fri, 14 Jun 2024 02:09:45 GMT  
		Size: 73.9 KB (73853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e362ebd3c48369a2a1da5acf059986f98869be9cf8e9593eb61f0722b1686264`  
		Last Modified: Fri, 14 Jun 2024 02:09:43 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7685cb6cfa0667639363818a6f6d66a18b5ef9d01b7cd317da092ba7e03cf749`  
		Last Modified: Fri, 14 Jun 2024 02:09:43 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3274f9f3a490eaf3002e0786eff3de80756c6173e9fd6f0a7b727d643a1bafb`  
		Last Modified: Fri, 14 Jun 2024 02:09:55 GMT  
		Size: 206.2 MB (206159302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38fc5022a6723c53b69eb297b823ccd07912e02a23f21d8538c2092ec1dc933`  
		Last Modified: Fri, 14 Jun 2024 02:09:44 GMT  
		Size: 4.1 MB (4135988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc98637ddec09ffd049cf53280f1535237b9797bf8d805318693d8714a93116`  
		Last Modified: Fri, 14 Jun 2024 02:09:43 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
