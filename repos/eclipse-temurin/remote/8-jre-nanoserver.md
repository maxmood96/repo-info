## `eclipse-temurin:8-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:d139aa4818982f519e4342af992ec6f57f55ea6bd7ab12ebb2f675d73ed532c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.20348.2582; amd64

```console
$ docker pull eclipse-temurin@sha256:50a5847cca6fa89f1e1594e6e231b320d1f8b79a8787e500b8a597733c856910
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160749343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d86e13c75382d11afddc323eebc8b7f749b91233430df900148ad3e1c39f9862`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 09:30:07 GMT
RUN Apply image 10.0.20348.2582
# Wed, 10 Jul 2024 17:17:20 GMT
SHELL [cmd /s /c]
# Wed, 10 Jul 2024 17:17:20 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Wed, 10 Jul 2024 17:17:21 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 10 Jul 2024 17:17:22 GMT
USER ContainerAdministrator
# Wed, 10 Jul 2024 17:17:33 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jul 2024 17:17:34 GMT
USER ContainerUser
# Wed, 10 Jul 2024 17:18:08 GMT
COPY dir:2b748c8b95a49802258ef446e3948354b660cf39e9ffa8b2cf36461ec042c5c0 in C:\openjdk-8 
# Wed, 10 Jul 2024 17:18:19 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:652774a5d82a114642848f8b0b8d486ec1b4995f9dda56e36fe4ac7563429990`  
		Last Modified: Tue, 09 Jul 2024 20:33:26 GMT  
		Size: 120.5 MB (120490378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1dbb650483c31087741ccfe7cfef17abfd7465711d0851e35d39eabc775bdae`  
		Last Modified: Wed, 10 Jul 2024 17:38:52 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b07b4ab2b5c1253e760d8d609ce086416c7f607dcd785ddc10ae04fc6dcf43`  
		Last Modified: Wed, 10 Jul 2024 17:38:52 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466a2a5b4537cebbb010784b348c6d9dcd47b4f8d69d7cf47584a4b2b06a7e1e`  
		Last Modified: Wed, 10 Jul 2024 17:38:52 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349dbf14a3f3dbc38bcf98fa084b4075217e8f81a60abc6a8419f18e28409955`  
		Last Modified: Wed, 10 Jul 2024 17:38:50 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44202090d90884ecdf62a2ed28b786bc9682ca7d588cdc44d14ebe2faee6ba39`  
		Last Modified: Wed, 10 Jul 2024 17:38:50 GMT  
		Size: 76.1 KB (76072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a2df7fd32b943df2a978a5227c92cbf590367f08819a2f021c1eb239e4ef10`  
		Last Modified: Wed, 10 Jul 2024 17:38:50 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c4ba3d4dc76b4e4253ccd9ce5c0ff10f257ccb0fe6c26961e70b40505e85a2`  
		Last Modified: Wed, 10 Jul 2024 17:39:25 GMT  
		Size: 40.1 MB (40115936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533c5495b40cc5dc6f7e2bb9e14512af5c3933fcc23a6a07c0e84b98a52f3ba8`  
		Last Modified: Wed, 10 Jul 2024 17:39:18 GMT  
		Size: 61.3 KB (61253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.17763.6054; amd64

```console
$ docker pull eclipse-temurin@sha256:e267a03d791ab1a04e0a5f15c56260fcc1890341e734bca948223ed4de2fadf3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.4 MB (195350838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ad5bd2572f0c10fcb7c6747cca64bc326b7cb9ae64378ce48b1c894ac315e3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 16:38:43 GMT
SHELL [cmd /s /c]
# Wed, 10 Jul 2024 16:38:43 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Wed, 10 Jul 2024 16:38:44 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 10 Jul 2024 16:38:44 GMT
USER ContainerAdministrator
# Wed, 10 Jul 2024 16:38:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jul 2024 16:38:53 GMT
USER ContainerUser
# Wed, 10 Jul 2024 16:42:28 GMT
COPY dir:2b748c8b95a49802258ef446e3948354b660cf39e9ffa8b2cf36461ec042c5c0 in C:\openjdk-8 
# Wed, 10 Jul 2024 16:42:37 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00a79547db1bc3ab4a5550f2ec9ba165e302f4a4984af3c1bfbbbe1726a3bf6`  
		Last Modified: Wed, 10 Jul 2024 17:28:00 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd3dd1b370e698d233bca9d38691b4d603232ec3e80613b652b90ae272c62aa`  
		Last Modified: Wed, 10 Jul 2024 17:28:00 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a2b5477760dae20db86c6d6529fa89fcfc8ceb4de0fe7ba849b19ba328c3bd`  
		Last Modified: Wed, 10 Jul 2024 17:28:00 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d51b65f5511b893cb79015a960daad47e830557616e8335cc43450ce7cadd1`  
		Last Modified: Wed, 10 Jul 2024 17:27:58 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672ff86607556cfacf2fca5f41b5573273f2e2331c55a9d4d898185cf00df449`  
		Last Modified: Wed, 10 Jul 2024 17:27:58 GMT  
		Size: 66.8 KB (66790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49814bb6e0056128b77482bd4ee3a7c198ff64b3e3380fac2f7699330bbf8093`  
		Last Modified: Wed, 10 Jul 2024 17:27:58 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7227d265f3edc1f60de433255cac2c1a8c81619f0b93696028fb5c240b5d1e3`  
		Last Modified: Wed, 10 Jul 2024 17:29:08 GMT  
		Size: 40.1 MB (40115876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d2335b803529e4dd0b4a7dee7c982b4d720d3cbe07f66f86a187d1df7eb936`  
		Last Modified: Wed, 10 Jul 2024 17:29:03 GMT  
		Size: 81.0 KB (81026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
