## `eclipse-temurin:11-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:921a727e15e24df37b68132c669416f71c474d721b4d3427a96cb8672565074a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3932; amd64

### `eclipse-temurin:11-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3932; amd64

```console
$ docker pull eclipse-temurin@sha256:80af0084feab8230a666cd8e6a4a5e452ec62bc56f79ada130edddfc01e8a155
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.4 MB (317399434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce4150f6c7b7858b49157dd6a68e6559d5b0f88f77f42ec2a77c306cbf4cb5e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Jul 2025 05:15:23 GMT
RUN Apply image 10.0.20348.3932
# Wed, 09 Jul 2025 19:13:40 GMT
SHELL [cmd /s /c]
# Wed, 09 Jul 2025 19:13:41 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 09 Jul 2025 19:13:43 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 09 Jul 2025 19:13:44 GMT
USER ContainerAdministrator
# Wed, 09 Jul 2025 19:13:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Jul 2025 19:13:50 GMT
USER ContainerUser
# Wed, 09 Jul 2025 19:13:59 GMT
COPY dir:c61af6ceef573b3d63f31a61f55e07ef4d3bfab78d8c06e63a667655942ae5e8 in C:\openjdk-11 
# Wed, 09 Jul 2025 19:14:07 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 09 Jul 2025 19:14:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b1cf2c299ff70c52cb8ecf52e66d64d5068519867510919d8807ed2c58a54ba2`  
		Last Modified: Tue, 08 Jul 2025 21:55:51 GMT  
		Size: 122.6 MB (122630906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80d12bd1a5a9eb431c54d755bb716afe475ced344874a03b85737c01723e1d1`  
		Last Modified: Wed, 09 Jul 2025 19:14:32 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85700f43e2b0853fe94bc00c6569f9320e16f92a0373f4d33a308d857ddf066c`  
		Last Modified: Wed, 09 Jul 2025 19:14:32 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47af69df6327d6045f1a5ef07ed414c59e76b89983b4933434bc44832ef3f9db`  
		Last Modified: Wed, 09 Jul 2025 19:14:32 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0735e849c76526a7b0f4548a2d0a1ef12e6fa0b97fb56e3a4af39871c0efbf2`  
		Last Modified: Wed, 09 Jul 2025 19:14:32 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea680c7c2991eaba83d49f7352f0a3645244fd70a979a97e43a0f5790d73adf`  
		Last Modified: Wed, 09 Jul 2025 19:14:32 GMT  
		Size: 78.6 KB (78617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d6d7d8413fbc7768c4cc4b43fb888bea34cdeecaec741cbc016ee5fec181968`  
		Last Modified: Wed, 09 Jul 2025 19:14:32 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9f1efa05368e395e75c2871b83d20ad5a5461c3e73412b19b2600638654373`  
		Last Modified: Wed, 09 Jul 2025 21:13:23 GMT  
		Size: 194.6 MB (194576725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228b0c4af011180356af299139329af2bb950317d3bc758c993b71afedb0147f`  
		Last Modified: Wed, 09 Jul 2025 19:14:32 GMT  
		Size: 107.0 KB (107004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017febacbb74585a5c7883079ec8713c5ded4ad918b8306b6d1eb5122bd1d58e`  
		Last Modified: Wed, 09 Jul 2025 19:14:32 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
