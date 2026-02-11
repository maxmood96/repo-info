## `openjdk:26-ea-33-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:e6317265ab957bdd63b0343b11090d462c20e8808b39522e932693d090d66cb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `openjdk:26-ea-33-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull openjdk@sha256:5709e20a98fe2398560d73bac3d7842833aff443f551eb85f3d68ef218c3230d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.7 MB (350730746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f85c443b393c5ae51a95e30f4c031002ed3afdc5843d10cfd2306c595ac4189`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Wed, 11 Feb 2026 00:15:11 GMT
SHELL [cmd /s /c]
# Wed, 11 Feb 2026 00:15:12 GMT
ENV JAVA_HOME=C:\openjdk-26
# Wed, 11 Feb 2026 00:15:13 GMT
USER ContainerAdministrator
# Wed, 11 Feb 2026 00:15:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 11 Feb 2026 00:15:20 GMT
USER ContainerUser
# Wed, 11 Feb 2026 00:15:20 GMT
ENV JAVA_VERSION=26-ea+33
# Wed, 11 Feb 2026 00:15:43 GMT
COPY dir:4b0b09721eb8a6a23e669a427b9022937722c5088501379523ae0d075ca2bcf0 in C:\openjdk-26 
# Wed, 11 Feb 2026 00:15:48 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 11 Feb 2026 00:15:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830454e5f5006baaed992eaa3a90117cf766e34bdc26cf719312b2f9d4b1ab22`  
		Last Modified: Wed, 11 Feb 2026 00:15:55 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049b6e110ae2c7a6612f0d6e61a8316ab30ad9fbd1bbc39704305938a75323ac`  
		Last Modified: Wed, 11 Feb 2026 00:15:55 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c4fd96085bc762d349f301615ac9ebdff208ae73c933f53943d2da38fa4920`  
		Last Modified: Wed, 11 Feb 2026 00:15:54 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:467e22a56011bcb5d4f62950eec2c6e47cf98560c122cc0c08cccadbc31518f6`  
		Last Modified: Wed, 11 Feb 2026 00:15:55 GMT  
		Size: 72.9 KB (72947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bfec93a1fdc5c395856f64a565766d7fd452ed0494f4a7b74f12acfd855b76`  
		Last Modified: Wed, 11 Feb 2026 00:15:53 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5bf1cd3c67ebce263c765ef47f8cf52e45e11b29de8ac02a32fc705dc4813b`  
		Last Modified: Wed, 11 Feb 2026 00:15:53 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b8515d47f6a15fa81242254d99a39cb13352c80819f81af23268b2ba754736`  
		Last Modified: Wed, 11 Feb 2026 00:16:09 GMT  
		Size: 223.9 MB (223878869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c40a6e99a28e0e0ba34881ba57c10a38a28cc1dc716d21700e3443345ac5a04`  
		Last Modified: Wed, 11 Feb 2026 00:15:53 GMT  
		Size: 126.7 KB (126684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9365d3693703484a703c9d7512cfc4204af1cbb34d4bbcc38eb5375b45864819`  
		Last Modified: Wed, 11 Feb 2026 00:15:53 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
