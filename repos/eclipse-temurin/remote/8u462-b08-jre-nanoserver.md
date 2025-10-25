## `eclipse-temurin:8u462-b08-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:836df9c3601cd7615c8d589b8a9d8e815fa8559b800d53fbdd2a771e3a41fba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `eclipse-temurin:8u462-b08-jre-nanoserver` - windows version 10.0.26100.6905; amd64

```console
$ docker pull eclipse-temurin@sha256:2fd79343ca4d17763f8f8356f8624fe52bb10c44ff8648f9f207fdd8b2579f33
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234767082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c37d75ef5e91dedcfd606f2910f985bbb2183e919bd9f23dac24a7fa19c7a9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 07:22:01 GMT
RUN Apply image 10.0.26100.6905
# Fri, 24 Oct 2025 19:20:51 GMT
SHELL [cmd /s /c]
# Fri, 24 Oct 2025 19:20:52 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 24 Oct 2025 19:20:53 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 24 Oct 2025 19:20:53 GMT
USER ContainerAdministrator
# Fri, 24 Oct 2025 19:20:58 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 24 Oct 2025 19:20:58 GMT
USER ContainerUser
# Fri, 24 Oct 2025 19:21:03 GMT
COPY dir:dae5853f4b111011cf1e21d00736b413be35f27636dbbe76d1c13e33a12f455a in C:\openjdk-8 
# Fri, 24 Oct 2025 19:21:07 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:9188956580c47f583c927f17e42f8825823890544237141f21ca4ef10ea55e60`  
		Last Modified: Fri, 24 Oct 2025 11:13:56 GMT  
		Size: 194.0 MB (194029378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8407703267a708f1e861d96ba7297b491ec4181f89a12fcf487a7b283523fd8a`  
		Last Modified: Fri, 24 Oct 2025 19:21:56 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54292356ef002a246ae14ad8d9bacc4ae5219c9db3f5bf270d39276a10979e5c`  
		Last Modified: Fri, 24 Oct 2025 19:21:56 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67509d601dcc388f095a258a6c0a25058beba808819da3e8e5ff663049fe51c9`  
		Last Modified: Fri, 24 Oct 2025 19:21:56 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823f68e46c596940b7564b86fb15f86994fb43136d277f1f7fc043fdf3abf0e9`  
		Last Modified: Fri, 24 Oct 2025 19:21:56 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d79d4086ef409528d92a6868c108c26288c0d3d022f74e175072df0360f51a8`  
		Last Modified: Fri, 24 Oct 2025 19:21:56 GMT  
		Size: 72.0 KB (71960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5284c3bd386bc6b4a13d0b74d3368f052e0f0538fd72fa314b4237640ce0da`  
		Last Modified: Fri, 24 Oct 2025 19:21:56 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81812a76a42ea5d9f73af608faa8d06e539fd5e76677efa46e06a4a5234a5f63`  
		Last Modified: Fri, 24 Oct 2025 19:22:00 GMT  
		Size: 40.5 MB (40548135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd1c13c223db4bb6cd997e28d88b7ce0a5103e0aa12130c851911c037f309dff`  
		Last Modified: Fri, 24 Oct 2025 19:21:56 GMT  
		Size: 112.3 KB (112336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u462-b08-jre-nanoserver` - windows version 10.0.20348.4297; amd64

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
