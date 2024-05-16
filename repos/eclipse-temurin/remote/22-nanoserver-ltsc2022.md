## `eclipse-temurin:22-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:408fb9ca5d7a1cc4c5b48bbf91c39a57f0c5953784fe98297ab332715fa8d03d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `eclipse-temurin:22-nanoserver-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull eclipse-temurin@sha256:b0bcc2520abc09cad4d742610302b3eef330bcf493cbb11565720ea18b450b8b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.6 MB (320615056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a18a88594325a0f6ea597c15e586016e4e756fc55976db5551d8dfe4a929c7d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 10 May 2024 20:16:48 GMT
RUN Apply image 10.0.20348.2461
# Wed, 15 May 2024 20:32:41 GMT
SHELL [cmd /s /c]
# Wed, 15 May 2024 20:38:17 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Wed, 15 May 2024 20:38:18 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 15 May 2024 20:38:18 GMT
USER ContainerAdministrator
# Wed, 15 May 2024 20:38:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 May 2024 20:38:30 GMT
USER ContainerUser
# Wed, 15 May 2024 20:38:44 GMT
COPY dir:b848142647370c7b57f8798114952350d05bf467cc96eb22cf5219409c8a4580 in C:\openjdk-22 
# Wed, 15 May 2024 20:39:00 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 15 May 2024 20:39:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:90b3a5622f8d62905d0a3029df4f91b934558ad375bef25c596214df31acac88`  
		Last Modified: Tue, 14 May 2024 17:22:15 GMT  
		Size: 120.4 MB (120425316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5560c76ac3d9aa2d8a6dbf79d443a7e1d170aae31c940cf791c9b532d5756a1`  
		Last Modified: Wed, 15 May 2024 20:58:04 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901805c453a3db5b81fbc5d7d76e019125a99325c46faa1f0b249503920c008b`  
		Last Modified: Wed, 15 May 2024 21:01:17 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f149c4c0118609d2025fd94d42ca722b9067880f610f3fdad29b66ef847ca824`  
		Last Modified: Wed, 15 May 2024 21:01:17 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc98af44c3d06c23e98453c26b8e25353d2f83fd7b96c7ae493040b1ec15b02a`  
		Last Modified: Wed, 15 May 2024 21:01:17 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced33bf6b165e04ab1f9b71b5848ed0c96e644eb880d246c00a7153fffb77d8c`  
		Last Modified: Wed, 15 May 2024 21:01:15 GMT  
		Size: 81.0 KB (80953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9e59eaac6374219cc1d44150b7730ae29db255a59201697a09fcfc13f25285`  
		Last Modified: Wed, 15 May 2024 21:01:15 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55195a33cf6f53826b68a83e734a7e093954e9ad7c18d6e746d912c2be50bd55`  
		Last Modified: Wed, 15 May 2024 21:01:34 GMT  
		Size: 200.0 MB (200044291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff3f1196f64894d74f8bf5c39c36a5fa47c01906cff476af43ce9aae2714a2e`  
		Last Modified: Wed, 15 May 2024 21:01:15 GMT  
		Size: 57.6 KB (57579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c244cfb9457c535a8555ef2a14422da881247e9183ea06faeac94f98c3127c`  
		Last Modified: Wed, 15 May 2024 21:01:15 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
