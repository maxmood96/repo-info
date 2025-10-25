## `eclipse-temurin:8u462-b08-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:9f73a00d5eda6292acec81fd2e87d5d1276c49683fa9d8daa34e3f91c7200925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `eclipse-temurin:8u462-b08-jre-nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull eclipse-temurin@sha256:2c1152784f26f6ad6d75854ef4f69416053535dc0ae99504bcd8d595e380a6db
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163400171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2e2a52c723fb3ac6702e6a8e99ff07240d961337f8f50046868ba5fa0869c5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Fri, 24 Oct 2025 19:21:10 GMT
SHELL [cmd /s /c]
# Fri, 24 Oct 2025 19:21:10 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 24 Oct 2025 19:21:11 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 24 Oct 2025 19:21:11 GMT
USER ContainerAdministrator
# Fri, 24 Oct 2025 19:21:16 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 24 Oct 2025 19:21:17 GMT
USER ContainerUser
# Fri, 24 Oct 2025 19:21:22 GMT
COPY dir:dae5853f4b111011cf1e21d00736b413be35f27636dbbe76d1c13e33a12f455a in C:\openjdk-8 
# Fri, 24 Oct 2025 19:21:25 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82b48116bbc9a2e910b540133b83e660486e482b11dfc8c0a08bbedb3698ce1`  
		Last Modified: Fri, 24 Oct 2025 19:22:16 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5cd692cb244b593f8fdaf524a7ef647f2f9a01fd6eaa0e5d172b5a034b59c16`  
		Last Modified: Fri, 24 Oct 2025 19:22:16 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18a0e32ecaab0b1ee4d06106e1bde38639379adbc2b4fb43c1d96c35c1c8924b`  
		Last Modified: Fri, 24 Oct 2025 19:22:16 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8fa38e1cd869fe17d312e938667cc2f9a62b6ee02f77507793256c696a6c63`  
		Last Modified: Fri, 24 Oct 2025 19:22:18 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30207f7511d099f8f3037280b661d5d5dbd8e2435e03daa46f94b282ea754e6`  
		Last Modified: Fri, 24 Oct 2025 19:22:16 GMT  
		Size: 73.1 KB (73102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4746acd1bf5bd4999cff94f27e1cb683f2f417ae761bf80ece2df501eb9a8ab`  
		Last Modified: Fri, 24 Oct 2025 19:22:16 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45781a9b733b0ab25b8c73c9a7f7654950dfbfc2b677d2da45d8d446d23ddae2`  
		Last Modified: Fri, 24 Oct 2025 19:22:20 GMT  
		Size: 40.5 MB (40548097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5d02e47ab88e081ca8c952824ebc1879b446c7b37ca1fc5d72153188bf26b9`  
		Last Modified: Fri, 24 Oct 2025 19:22:16 GMT  
		Size: 89.5 KB (89505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
