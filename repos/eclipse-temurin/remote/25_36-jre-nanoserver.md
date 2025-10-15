## `eclipse-temurin:25_36-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:bd292084ed6ffc11a5e7ee6c81c68c97f78e1e19eaa8be1c763d5b59e5a7b495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6899; amd64
	-	windows version 10.0.20348.4294; amd64

### `eclipse-temurin:25_36-jre-nanoserver` - windows version 10.0.26100.6899; amd64

```console
$ docker pull eclipse-temurin@sha256:5e43d91f6eea4779d704bcf929e29dccfdf8ded6102db8faa8889fcee4e5758e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252738744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f49c0933ba58a2c8d7576df381b5151fc13033b84ceb65b19b4e2f06a7b2c8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 11 Oct 2025 15:58:41 GMT
RUN Apply image 10.0.26100.6899
# Tue, 14 Oct 2025 21:13:34 GMT
SHELL [cmd /s /c]
# Tue, 14 Oct 2025 21:13:35 GMT
ENV JAVA_VERSION=jdk-25+36
# Tue, 14 Oct 2025 21:13:36 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 14 Oct 2025 21:13:37 GMT
USER ContainerAdministrator
# Tue, 14 Oct 2025 21:13:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Oct 2025 21:13:45 GMT
USER ContainerUser
# Tue, 14 Oct 2025 21:13:59 GMT
COPY dir:8aa8ce0e84e7e6f80be28438d765894541d9d2eadfccff43ebe7257923223c3b in C:\openjdk-25 
# Tue, 14 Oct 2025 21:14:03 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:463edd10ad50b00cf92c69fc3eaa85e1fa40aad1b7938fa232899405bd80f001`  
		Last Modified: Tue, 14 Oct 2025 22:41:48 GMT  
		Size: 194.0 MB (194026741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94d8b2c15acef7845553a9d72f9a77f43d9d56b98080c9a986af1ca86b4be3e`  
		Last Modified: Tue, 14 Oct 2025 21:15:09 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4718e39d0c360551815001282221feabe332cbc007a5d7db62ae8308b08fdfa`  
		Last Modified: Tue, 14 Oct 2025 21:15:09 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90daced459138c792789055d99a9da17e9edd0074c128847f05bf626cf222fde`  
		Last Modified: Tue, 14 Oct 2025 21:15:09 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9798c8f5adf8cf4258c0da49f55ecb3d25b1c069aa3905c3c65cde3e38afdee`  
		Last Modified: Tue, 14 Oct 2025 21:15:09 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4d06154ccb5c19c8ad71359364d4459036d30d69749ab2d8d8da2fd483dd3d`  
		Last Modified: Tue, 14 Oct 2025 21:15:09 GMT  
		Size: 70.5 KB (70508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74ff31e421d004a149562080619ffd8ccc2f96c8821ef50a67fe5121fa29a5e`  
		Last Modified: Tue, 14 Oct 2025 21:15:09 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67dc37f8c8b87762645b5c871f98142a4535ed1be3fae6568d4059a9a208f61`  
		Last Modified: Tue, 14 Oct 2025 21:15:14 GMT  
		Size: 58.6 MB (58551326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3123ed6dadbec1d0f3745ab448b4a7ebcc53b623b8f3e0adf89120d610bd1441`  
		Last Modified: Tue, 14 Oct 2025 21:15:09 GMT  
		Size: 84.9 KB (84868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:25_36-jre-nanoserver` - windows version 10.0.20348.4294; amd64

```console
$ docker pull eclipse-temurin@sha256:ca76dfb3de5999fea4f48713fd6d3daeb19f9a0b873c884f0153d2be03d36b86
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181411895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56328491f7ad1f1cfb4c17bedf42537bb13cfc8f03a0879313e63a3a8a35217a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Oct 2025 07:34:08 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 21:12:07 GMT
SHELL [cmd /s /c]
# Tue, 14 Oct 2025 21:13:29 GMT
ENV JAVA_VERSION=jdk-25+36
# Tue, 14 Oct 2025 21:13:29 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 14 Oct 2025 21:13:29 GMT
USER ContainerAdministrator
# Tue, 14 Oct 2025 21:13:31 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Oct 2025 21:13:31 GMT
USER ContainerUser
# Tue, 14 Oct 2025 21:13:35 GMT
COPY dir:8aa8ce0e84e7e6f80be28438d765894541d9d2eadfccff43ebe7257923223c3b in C:\openjdk-25 
# Tue, 14 Oct 2025 21:13:38 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:f68a3bbf3ee20b515c5b8b801e5627a9dac3782ef264e37060c34ed80e5d8874`  
		Last Modified: Tue, 14 Oct 2025 20:41:53 GMT  
		Size: 122.7 MB (122688886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97004b1f45dbb42e74fcf45291378b73026f24a385f84780f274b7ff65e64f78`  
		Last Modified: Tue, 14 Oct 2025 21:13:14 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72254ac55b809ad01ad6da1d4e002cd519b30a12ea3f46649550173acbb89dce`  
		Last Modified: Tue, 14 Oct 2025 21:14:09 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed6dbdd8bb104fed1e39891f942cf37eb803d665d69151b315417444144d7558`  
		Last Modified: Tue, 14 Oct 2025 21:14:09 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f0222870d0a05487949e4ee81e611c9e4e4bdad70b8e6c8fc5d4eb70f065c1`  
		Last Modified: Tue, 14 Oct 2025 21:14:09 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be078139607dc728a5cd67277ee4ec2303a94bf32d64c3a70f0745341f1fbc3`  
		Last Modified: Tue, 14 Oct 2025 21:14:09 GMT  
		Size: 76.6 KB (76644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f149635137a9a3a66b68e1df257c066b7e6d922a9c235e47b555b871c42a0af`  
		Last Modified: Tue, 14 Oct 2025 21:14:09 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c72ef29a17eca7d8646c1e8b154f737f7852342db196d4206aa11388a60a7b`  
		Last Modified: Tue, 14 Oct 2025 21:14:26 GMT  
		Size: 58.6 MB (58550991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cb4db7a121728323e20e0169b7fe4f9fbd1e6dfb643399d5aa7ade6eec3443`  
		Last Modified: Tue, 14 Oct 2025 21:14:09 GMT  
		Size: 90.1 KB (90067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
