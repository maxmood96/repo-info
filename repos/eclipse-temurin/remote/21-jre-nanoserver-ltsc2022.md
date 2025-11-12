## `eclipse-temurin:21-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:c7b7116c5dde8674becd8e3f8eb76548b242b19fababe47ba86ab4f2b2e99620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `eclipse-temurin:21-jre-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull eclipse-temurin@sha256:cf5281eecf5d677fd248efb3f61ec9d1d6e5aabe48dd754a3b3e5506d0075e02
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175556570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aacbddb20552c6071e3fbfe2cec9db45f89ef99d58bba55e6b21eeef409f3f58`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 11 Nov 2025 20:10:44 GMT
SHELL [cmd /s /c]
# Tue, 11 Nov 2025 20:11:33 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Tue, 11 Nov 2025 20:11:34 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 11 Nov 2025 20:11:34 GMT
USER ContainerAdministrator
# Tue, 11 Nov 2025 20:11:36 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 11 Nov 2025 20:11:37 GMT
USER ContainerUser
# Tue, 11 Nov 2025 20:11:51 GMT
COPY dir:1612d20d6d454244847586ca6f13699611833617704a1c55730e9c479e5d220d in C:\openjdk-21 
# Tue, 11 Nov 2025 20:11:53 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98d596b44731ccc546a8f48a8a6e760b6816cd774426ad0bf327076f1a5d218`  
		Last Modified: Tue, 11 Nov 2025 20:11:33 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d6a8f06efd44c9f4692927c54456710391e872040f509c647cf2afd4b6cf90`  
		Last Modified: Tue, 11 Nov 2025 20:12:09 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada32de99168373337ebd8266caa3c2d26d257fb7a37b3f4492c97beed61a1ad`  
		Last Modified: Tue, 11 Nov 2025 20:12:09 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc1359956c784731d2bd7bdd48776a403171514b989c9db8525a360b6ebb908`  
		Last Modified: Tue, 11 Nov 2025 20:12:09 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db75cfe124aeaf7b2a29396642a0a070cb12c459e179035dc83cc2b84d7a4aea`  
		Last Modified: Tue, 11 Nov 2025 20:12:09 GMT  
		Size: 77.1 KB (77084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c15e3ef04f8d7714487db3e2521cc396801b6a3bc2eb36ff2b2415b727de491`  
		Last Modified: Tue, 11 Nov 2025 20:12:09 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df25fe312f2c65fe3af9adc9147d9ec3ca59358941a283814439615f6de8f2b`  
		Last Modified: Tue, 11 Nov 2025 20:12:15 GMT  
		Size: 49.0 MB (49035037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb307576428c6d1533cfbaf0093d14a0dc0562a6d9a8a03673dd70f20a5dd57`  
		Last Modified: Tue, 11 Nov 2025 20:12:09 GMT  
		Size: 90.1 KB (90107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
