## `eclipse-temurin:21-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:fd9a6df6618618aa041ec1febaeba6668422325298f9e44eb67039d3f68961c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.20348.2582; amd64

```console
$ docker pull eclipse-temurin@sha256:f6bd0566463531eb4c194f345b3f0bdae963d2860213cfd638f6c3bbe939f461
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.3 MB (169300125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7dd6f8efcdb75459abcb3bb4b15a7711dee8d3a512ac06caf57b55de3fcafa`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 09:30:07 GMT
RUN Apply image 10.0.20348.2582
# Wed, 10 Jul 2024 17:17:20 GMT
SHELL [cmd /s /c]
# Tue, 23 Jul 2024 00:33:42 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Tue, 23 Jul 2024 00:33:42 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 23 Jul 2024 00:33:43 GMT
USER ContainerAdministrator
# Tue, 23 Jul 2024 00:33:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 23 Jul 2024 00:33:51 GMT
USER ContainerUser
# Tue, 23 Jul 2024 00:34:25 GMT
COPY dir:6441dab14d212c21b2c8fcb6fc00e95950b0c66ee3c049dbfd71b18f09e541f6 in C:\openjdk-21 
# Tue, 23 Jul 2024 00:34:34 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:e8c638ac9eb4f9a87146aa1d1a84626862874c0223efea130b7bab729061daca`  
		Last Modified: Tue, 23 Jul 2024 00:42:28 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde235753362014f52c1bbd326ed0fceb9db0500b5273687e7a8bf3c7f78ead7`  
		Last Modified: Tue, 23 Jul 2024 00:42:28 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fc1888ccfc63ec92b1ec9aa565746092f3283a204089a20b3aff3221045ef4`  
		Last Modified: Tue, 23 Jul 2024 00:42:28 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d81c8968674b5ff745790bcd5009e118749e45f20f8423fcd89bba0a38120c`  
		Last Modified: Tue, 23 Jul 2024 00:42:26 GMT  
		Size: 78.2 KB (78155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3aab0f4a46f0b159522fcd7a18111ec9c28e05d1882350b24f93187813c144b`  
		Last Modified: Tue, 23 Jul 2024 00:42:26 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71057cdd996255485986858a656c901894be7e400f34b4fda1b7c82bd57b6dc3`  
		Last Modified: Tue, 23 Jul 2024 00:43:00 GMT  
		Size: 48.7 MB (48664493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f14f43e29ad4f04cff6d1e224e570fe29ed5b3a3493f30a3da7a0f13016c82`  
		Last Modified: Tue, 23 Jul 2024 00:42:53 GMT  
		Size: 61.3 KB (61302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.17763.6054; amd64

```console
$ docker pull eclipse-temurin@sha256:c5b3bd441de306c8f59cfeacf4a078c02f695b6ad54ea31546f00dc4cad3d099
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207194585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35158701992620b44fa7c00c2b8ac0269af471a64e5f96313f053a43964a14ac`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 16:38:43 GMT
SHELL [cmd /s /c]
# Tue, 23 Jul 2024 00:27:42 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Tue, 23 Jul 2024 00:27:42 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 23 Jul 2024 00:27:43 GMT
USER ContainerAdministrator
# Tue, 23 Jul 2024 00:27:50 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 23 Jul 2024 00:27:50 GMT
USER ContainerUser
# Tue, 23 Jul 2024 00:31:29 GMT
COPY dir:6441dab14d212c21b2c8fcb6fc00e95950b0c66ee3c049dbfd71b18f09e541f6 in C:\openjdk-21 
# Tue, 23 Jul 2024 00:31:38 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:edbf574c8643be142a434d3320463979f63505cb12ea751eaf2afb4f62ddb2af`  
		Last Modified: Tue, 23 Jul 2024 00:40:27 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f330806fe0fd7929a9920c95862329e67f77d28ac66efc279e05c844a680b876`  
		Last Modified: Tue, 23 Jul 2024 00:40:27 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efffd37584636aa53a833b5c5846dd62625e18d372075bb4ce58b572783acbd1`  
		Last Modified: Tue, 23 Jul 2024 00:40:27 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597250a8581cffa6ddffb62b6517fa77145cb20926a760daca98a333b83f8385`  
		Last Modified: Tue, 23 Jul 2024 00:40:25 GMT  
		Size: 69.1 KB (69142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0beaac908c6bf94597150808a1bc0e0f9c0503d799d08cd4b747e88e4f297b6b`  
		Last Modified: Tue, 23 Jul 2024 00:40:25 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415493aac386ee17df647e38fcb8e5e5a9083c17b491fe0c043018320419fdad`  
		Last Modified: Tue, 23 Jul 2024 00:41:33 GMT  
		Size: 48.7 MB (48665186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4ab0ceb3a509057ce7b0920e2347dd441a6c03f943a95fb8a52c694dd243c9`  
		Last Modified: Tue, 23 Jul 2024 00:41:26 GMT  
		Size: 3.4 MB (3373234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
