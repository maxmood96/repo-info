## `eclipse-temurin:8u412-b08-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:b39331b6ac124344d407895a9d06771f610d3eb5ae32becca936c22ac26dcd9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:8u412-b08-jre-nanoserver-1809` - windows version 10.0.17763.6054; amd64

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
