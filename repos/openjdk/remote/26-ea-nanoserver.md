## `openjdk:26-ea-nanoserver`

```console
$ docker pull openjdk@sha256:752da98ee6ebdaaba838f2c2d94f3d69c4b77a33f57cb3a3b54150c075d082cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64

### `openjdk:26-ea-nanoserver` - windows version 10.0.26100.4061; amd64

```console
$ docker pull openjdk@sha256:fc411099f4d5872e09e62f456bc1e9262dddd60d258381f432c26c8c4c69aa77
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.1 MB (410139869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c2de2b9286967ae609d740995dd9357e204cbdf5fbf671ba410e560ff5d50f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 10 May 2025 00:58:48 GMT
RUN Apply image 10.0.26100.4061
# Mon, 09 Jun 2025 23:12:24 GMT
SHELL [cmd /s /c]
# Mon, 09 Jun 2025 23:12:25 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 09 Jun 2025 23:12:26 GMT
USER ContainerAdministrator
# Mon, 09 Jun 2025 23:12:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 09 Jun 2025 23:12:30 GMT
USER ContainerUser
# Mon, 09 Jun 2025 23:12:31 GMT
ENV JAVA_VERSION=26-ea+1
# Mon, 09 Jun 2025 23:12:39 GMT
COPY dir:457747d16cd2fadf291c9e74f2db19f460bea57b69501abf66c1c6daf147dfd2 in C:\openjdk-26 
# Mon, 09 Jun 2025 23:12:47 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 09 Jun 2025 23:12:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9824510349be04d2eb26f9aaba1d016eddcbed10bdcd6681f4636c948766f3d1`  
		Last Modified: Thu, 15 May 2025 20:15:30 GMT  
		Size: 191.4 MB (191412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bebc050849d2b6aea24f180172b64b8047f7cd1ab43105aad9fd1883699401b`  
		Last Modified: Mon, 09 Jun 2025 23:13:36 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feefadce58e972b4944e795d9c36295ba9840be4f08fc75b2442e380b6d343e0`  
		Last Modified: Mon, 09 Jun 2025 23:13:36 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f719f61be2afee3ed457203f2e0130a6715a186b2c9ab807ddf9237c490c6566`  
		Last Modified: Mon, 09 Jun 2025 23:13:36 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaec0693d062e0a72738e74b6c95ca05f78380493e5aade94c4fc5be9b14b3dc`  
		Last Modified: Mon, 09 Jun 2025 23:13:36 GMT  
		Size: 76.1 KB (76070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e08ef0c68b9f6718a3c806b47d902ac945fcd009d4f2b1536679b88665560dd`  
		Last Modified: Mon, 09 Jun 2025 23:13:36 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b883646337141eda167b46ae24e45b3d9f76a3f769a9ef5f4a32e6cc511c0d6`  
		Last Modified: Mon, 09 Jun 2025 23:13:36 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f1363c6d58a3c69de6c37735f2766a594b7e7fe6d702abac5d7337ef721595`  
		Last Modified: Tue, 10 Jun 2025 00:26:06 GMT  
		Size: 218.5 MB (218529233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e6fccd1d614790b0ad93ba2a75e8fcf209c338e8635a699bd3ecd1b8869747`  
		Last Modified: Mon, 09 Jun 2025 23:13:37 GMT  
		Size: 116.3 KB (116258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d514d351ad2c5e76b15a7a6bf7957a03dc37ca17b39bac5f822a04031001b598`  
		Last Modified: Mon, 09 Jun 2025 23:13:37 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-ea-nanoserver` - windows version 10.0.20348.3692; amd64

```console
$ docker pull openjdk@sha256:260ba2d16f532483cccab08463331c7f022920c7234782e42a1a75a26cc482e1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.3 MB (341274004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d29c5dc7125ba3aacb3cf58556534be76beceba6cbdbba60e1f2926335a31a3f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Mon, 09 Jun 2025 22:10:54 GMT
SHELL [cmd /s /c]
# Mon, 09 Jun 2025 22:10:55 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 09 Jun 2025 22:10:55 GMT
USER ContainerAdministrator
# Mon, 09 Jun 2025 22:11:11 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 09 Jun 2025 22:11:12 GMT
USER ContainerUser
# Mon, 09 Jun 2025 22:11:12 GMT
ENV JAVA_VERSION=26-ea+1
# Mon, 09 Jun 2025 22:11:23 GMT
COPY dir:457747d16cd2fadf291c9e74f2db19f460bea57b69501abf66c1c6daf147dfd2 in C:\openjdk-26 
# Mon, 09 Jun 2025 22:11:28 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 09 Jun 2025 22:11:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad89a70052f467803812b73a950344133683c6e20a126defb778d2b7efedbdb`  
		Last Modified: Mon, 09 Jun 2025 22:12:53 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c7bbb8f526fff84916c571e1d503eb6b8bb9924a0686e7ebf7fe42b697643d`  
		Last Modified: Mon, 09 Jun 2025 22:12:53 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7029588985ff59ebd9059a384e8599373f9904fdaafddd3758c807692874d400`  
		Last Modified: Mon, 09 Jun 2025 22:12:54 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d676deffc613be72225c21093dd09121bdf9358d1f0c31a6f2d7b567da10501`  
		Last Modified: Mon, 09 Jun 2025 22:12:54 GMT  
		Size: 79.5 KB (79497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00c41f628b91effc35b2f3cd72dbc28af7ba6b7c84e6d24f19e458960f911ab7`  
		Last Modified: Mon, 09 Jun 2025 22:12:54 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0138dfe93d20b5ebaabf6fe95157717f87c424cb56f85e35a0a1a2723a7e64bc`  
		Last Modified: Mon, 09 Jun 2025 22:12:54 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f459b02065e0b370fd26606ab4fc1351a90dd1c45562df4c0a75170e93e1f464`  
		Last Modified: Tue, 10 Jun 2025 00:26:05 GMT  
		Size: 218.5 MB (218527850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c67ae5c65671fa0bdd468853709302c0a1a1e333cdc1be08dd5fe039196ea42`  
		Last Modified: Mon, 09 Jun 2025 22:12:54 GMT  
		Size: 83.8 KB (83840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11befbcd4183b183d03faf1aa70c728f3fe288af593a6f12963d8547c87d6a2c`  
		Last Modified: Mon, 09 Jun 2025 22:12:54 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
