## `openjdk:23-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:e8d22c85b01018943b502b6fe91ca08d1f903f78aecd9aa773f33e9c209521d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `openjdk:23-ea-jdk-nanoserver-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull openjdk@sha256:635642d39f045437a36e8f095e28613479792a39110d572350ad6fde3c08a811
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.4 MB (366362850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81bcdabe6ac0f49ab10f057040c5d2485c64ebd16b65feacc287216edea6ef65`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Mon, 08 Jul 2024 21:50:07 GMT
SHELL [cmd /s /c]
# Mon, 08 Jul 2024 21:50:09 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 08 Jul 2024 21:50:10 GMT
USER ContainerAdministrator
# Mon, 08 Jul 2024 21:50:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 08 Jul 2024 21:50:22 GMT
USER ContainerUser
# Mon, 08 Jul 2024 21:50:22 GMT
ENV JAVA_VERSION=23-ea+30
# Mon, 08 Jul 2024 21:50:30 GMT
COPY dir:e9035bffe394ece7120e7b4862d3651b9290e44805dce1863f06816afaf00705 in C:\openjdk-23 
# Mon, 08 Jul 2024 21:50:41 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 08 Jul 2024 21:50:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1123264c84b281221377b02a364683d746451f1b05d061aa2fd9bc1f80c9b6a`  
		Last Modified: Mon, 08 Jul 2024 21:50:46 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31274a9bd600e4a0b73bdb565444a1389d3aabcdb2afba74b2ba2f65cbbc1c98`  
		Last Modified: Mon, 08 Jul 2024 21:50:46 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a14fe8916cc14f93076b087b3c978c66d3946805df0bc9b7b171a8f01d7b22c`  
		Last Modified: Mon, 08 Jul 2024 21:50:45 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d8c5efd9409c87ddb585ea7aced6759e3010886ffb1bc1b63c970215ca0b8e`  
		Last Modified: Mon, 08 Jul 2024 21:50:45 GMT  
		Size: 67.4 KB (67396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427168c929fe60b7a92938a8709e6bee887cfcef039fc8a9972b70d4bdb91a8e`  
		Last Modified: Mon, 08 Jul 2024 21:50:44 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f3bd1c57f0b2c9a30c3bf13460e644f236927a7b8701b10ec6b4a50ff69504`  
		Last Modified: Mon, 08 Jul 2024 21:50:45 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6111f9e4bc35645de59394886327397ec1b2f3f9e5b554b52955ce078dc6ad5f`  
		Last Modified: Mon, 08 Jul 2024 21:50:55 GMT  
		Size: 206.1 MB (206059102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:105d3b0af2c1baad7ebf1c631bfffa1c7c2afa56410fbae4094b5b76133c2ef3`  
		Last Modified: Mon, 08 Jul 2024 21:50:45 GMT  
		Size: 5.2 MB (5196915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf78f368438871d5cc719a1664e21c96300287e45fa287172444a211fd0a4888`  
		Last Modified: Mon, 08 Jul 2024 21:50:44 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
