## `openjdk:15-ea-23-nanoserver`

```console
$ docker pull openjdk@sha256:927864c7cf50bf244b08c2a447c07e7797d7f3d0cc470e45e2913cc8fbdbb1f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `openjdk:15-ea-23-nanoserver` - windows version 10.0.17763.1217; amd64

```console
$ docker pull openjdk@sha256:44f31dbdf036328d22a778ea32309825cbc40a5e55be3ab944a04ac2946e571c
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.2 MB (292206178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef14bc02db2dc9eb158eb14a38da4aa4edbea7ba28cf6cf056f731bbd32f552d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 06 May 2020 12:39:06 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 15:30:41 GMT
SHELL [cmd /s /c]
# Wed, 13 May 2020 15:30:42 GMT
ENV JAVA_HOME=C:\openjdk-15
# Wed, 13 May 2020 15:30:43 GMT
USER ContainerAdministrator
# Wed, 13 May 2020 15:31:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 13 May 2020 15:31:01 GMT
USER ContainerUser
# Fri, 15 May 2020 21:48:48 GMT
ENV JAVA_VERSION=15-ea+23
# Fri, 15 May 2020 21:49:26 GMT
COPY dir:e5dfd63365e91cf07e43b094db214e5cdc8114adc1980d2758829e99c3b0b79d in C:\openjdk-15 
# Fri, 15 May 2020 21:49:53 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Fri, 15 May 2020 21:49:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b9e6fec25718aef5ed18d499b27e43adb524f9ee4f2eb3f0fffaea018e7e86b0`  
		Size: 101.0 MB (101019852 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3c597e8fceaeb76628095f6dcfa538d497e85739068a817b45d73be2b96a3b37`  
		Last Modified: Wed, 13 May 2020 16:09:16 GMT  
		Size: 891.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe4a1ac076e1dee08c07748ed0bf748357ec3c058f29131ddb0c6903b01c5b3`  
		Last Modified: Wed, 13 May 2020 16:09:16 GMT  
		Size: 837.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00cb774af18b914ba24ccfaba030aaee1af53cc965b45edd9166b2cbdc59558`  
		Last Modified: Wed, 13 May 2020 16:09:15 GMT  
		Size: 930.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0bbbe06e51300ecf6f12747f98fa77f8b3370196f85b87015dca501577f4aa`  
		Last Modified: Wed, 13 May 2020 16:09:14 GMT  
		Size: 64.1 KB (64131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0840576e1fb16bf2edf823eb58f597b05345e558ebba64301d718163d95b93d`  
		Last Modified: Wed, 13 May 2020 16:09:12 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b27fb9c7172c0031a9549a3fe97c8541faf0d9a10608ebf0b55ac565374eebc`  
		Last Modified: Fri, 15 May 2020 22:01:39 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c28a8b16d695ea30453d5f35fb0f63bd25ff46b6d2add3ae0f8288e1fc610b`  
		Last Modified: Fri, 15 May 2020 22:04:50 GMT  
		Size: 187.6 MB (187598546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00927bda319ba2506ba32616f77a5a947b87b8890bf59f75cdb6be7f65d653a5`  
		Last Modified: Fri, 15 May 2020 22:01:40 GMT  
		Size: 3.5 MB (3518352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57fc2b8e1a0a31f1037519a4e40a47733fb8a8d4d4c5ecdf8504857f9d6495ae`  
		Last Modified: Fri, 15 May 2020 22:01:39 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
