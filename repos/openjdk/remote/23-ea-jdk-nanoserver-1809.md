## `openjdk:23-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:caea42b9cc66044457e94e58801a2e7ee24b1b532cbac3c1063b95e44ef9c72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `openjdk:23-ea-jdk-nanoserver-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull openjdk@sha256:d3fa17e4a0cf58112ea22fcecd8a4c27dba36566e1a6f4a7eb1f46a618367555
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.8 MB (315752261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcf34a81cc5065ec2a0831313ee1a58ab29c7568172d15eaff7da64afdf97f03`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Wed, 10 Apr 2024 01:00:53 GMT
SHELL [cmd /s /c]
# Wed, 10 Apr 2024 01:00:55 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 10 Apr 2024 01:00:55 GMT
USER ContainerAdministrator
# Wed, 10 Apr 2024 01:00:58 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 Apr 2024 01:00:59 GMT
USER ContainerUser
# Wed, 10 Apr 2024 01:01:00 GMT
ENV JAVA_VERSION=23-ea+17
# Wed, 10 Apr 2024 01:01:09 GMT
COPY dir:5167fe4891c14c331f4ba4ef8d2f5decc066863be20ac52b35dd14a9c2c8a27a in C:\openjdk-23 
# Wed, 10 Apr 2024 01:01:18 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 10 Apr 2024 01:01:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18aac7d7b80cf9b09dfeb2b057be6e578634a5d6eaa476a1daf702737f7a7980`  
		Last Modified: Wed, 10 Apr 2024 01:01:27 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f264a92ee0375192246fce11aa44bc48086cca0ea11c8930ee591806814c0c4`  
		Last Modified: Wed, 10 Apr 2024 01:01:26 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282dd0a4fc25e9caad15b3209dc1d34efa8893207e90449c811790059a32f29d`  
		Last Modified: Wed, 10 Apr 2024 01:01:25 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc213de19222fd400cfd1047c4f837c38a3aedbf2444dc4ae6322ac0342c94a`  
		Last Modified: Wed, 10 Apr 2024 01:01:26 GMT  
		Size: 75.1 KB (75110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9511819c40468d08263d032d664e704f308dcbef394aff9d2971962b0920bf`  
		Last Modified: Wed, 10 Apr 2024 01:01:23 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68229bc55b1abbdf72c5f10321e2fb9900f75013a41022dd4fdba64a88933f89`  
		Last Modified: Wed, 10 Apr 2024 01:01:23 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d92225169a088e682cfc498c4470d63f079cedef0f3a32996e219205a35e843`  
		Last Modified: Wed, 10 Apr 2024 01:01:35 GMT  
		Size: 205.3 MB (205283603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cb55d19ba1ee14f4e6518ba1cdd783a96a17c2d71899dc4cb3cefa037b2b93`  
		Last Modified: Wed, 10 Apr 2024 01:01:25 GMT  
		Size: 5.5 MB (5498213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a7c03557ebd36d17df4083baa6b839e14b1b365c7076b8c50f96aa42773a7e`  
		Last Modified: Wed, 10 Apr 2024 01:01:23 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
