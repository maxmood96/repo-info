## `openjdk:15-ea-24-nanoserver-1809`

```console
$ docker pull openjdk@sha256:244b284142fa52532886131df2f68b621e1b98800d88ef146d8389ac9090a5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `openjdk:15-ea-24-nanoserver-1809` - windows version 10.0.17763.1217; amd64

```console
$ docker pull openjdk@sha256:ab0f5aaaf71c890de32334a24ccea06d5a156b06452c9addb6af7853c040f316
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295862264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92952f5c4b30c63fd51c71141cd511d70888a597658851935180afc91ff007cf`
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
# Sat, 23 May 2020 01:20:18 GMT
ENV JAVA_VERSION=15-ea+24
# Sat, 23 May 2020 01:21:08 GMT
COPY dir:dcd0dbe86082ea125cfecab278526d3395ea20e7fd5941c8ddc4770bf97bec10 in C:\openjdk-15 
# Sat, 23 May 2020 01:21:30 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Sat, 23 May 2020 01:21:31 GMT
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
	-	`sha256:dd2ea09b9e7dc25d69b5941e951dbd385a90c2a8e584363be12da9068e5d95e7`  
		Last Modified: Sat, 23 May 2020 01:27:04 GMT  
		Size: 867.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a3437282f188df19f0905b85b5815807e685a192beb30fff4500f8ca208e71`  
		Last Modified: Sat, 23 May 2020 01:30:09 GMT  
		Size: 191.3 MB (191270073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:287f3253258fb61ce31e1cbe8bb45ec4e021dca420d72f7a5c8b1cd92d873d2b`  
		Last Modified: Sat, 23 May 2020 01:27:06 GMT  
		Size: 3.5 MB (3502920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed950c5f57b5f0743f872ca865c452f215f514d55c3a21ff85c8aa6131b25c68`  
		Last Modified: Sat, 23 May 2020 01:27:05 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
