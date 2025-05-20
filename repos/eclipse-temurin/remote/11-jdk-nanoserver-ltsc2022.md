## `eclipse-temurin:11-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:07b4be24b53937f79dbac022441125d385ae8e80e155ecda54cfc46e4b5378fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `eclipse-temurin:11-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull eclipse-temurin@sha256:917f56af584ab3b9a951240f7aa826cc9325fd89c5c33c0d9989472ad363fcd3
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.3 MB (317344996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77bb70463b18d567cf802da96326d935cd649bef9e8e9117157112e0dacb67e8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Wed, 14 May 2025 21:12:17 GMT
SHELL [cmd /s /c]
# Wed, 14 May 2025 21:12:18 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 14 May 2025 21:12:19 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 14 May 2025 21:12:20 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 21:12:23 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 May 2025 21:12:24 GMT
USER ContainerUser
# Wed, 14 May 2025 21:12:31 GMT
COPY dir:c61af6ceef573b3d63f31a61f55e07ef4d3bfab78d8c06e63a667655942ae5e8 in C:\openjdk-11 
# Wed, 14 May 2025 21:12:36 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 14 May 2025 21:12:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Tue, 13 May 2025 19:42:18 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e7aabc555018fc1414d1a7e5e274775e35c26d0658856ae8429d9c5e8c2acac`  
		Last Modified: Wed, 14 May 2025 21:12:44 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08db206934ff137d66a4531c3574ce4e337ed23fa645b4c26c46580c0d81c224`  
		Last Modified: Wed, 14 May 2025 21:12:43 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fada72004895314470ac66cd59b2028ba25172ea37dc94aa631127ab5dc318c`  
		Last Modified: Wed, 14 May 2025 21:12:43 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567bdbf7653f6df3a0ce36651f0bb8f402cc91077ee6ae77ddab5fd8615eef2e`  
		Last Modified: Wed, 14 May 2025 21:12:43 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22f4c40d70557451533e163bf5e095203feb393fb8faf1f95ddbebfcd5d5d57`  
		Last Modified: Wed, 14 May 2025 21:12:41 GMT  
		Size: 77.6 KB (77628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a6d0c092b16d9d12aadfcd20c4315bc2d8f632117233d3a233b23931f40e0a`  
		Last Modified: Wed, 14 May 2025 21:12:41 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f71050e04b68e30fc66ad86844ce94f77440679c4cc43a46d83a151ef6d2da7`  
		Last Modified: Wed, 14 May 2025 21:12:52 GMT  
		Size: 194.6 MB (194577180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891dc118ab9f7aae88eae1dfbada6b04f9d7b51ebf05fb624e9696cf9e3157f3`  
		Last Modified: Wed, 14 May 2025 21:12:41 GMT  
		Size: 107.4 KB (107386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf21a3595215fcbfd111b169603d14437fb7a5f2a7500ebb4301fafe9f275b55`  
		Last Modified: Wed, 14 May 2025 21:12:41 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
