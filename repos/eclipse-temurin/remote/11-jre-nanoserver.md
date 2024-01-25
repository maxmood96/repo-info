## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:4c9d8b7b43b1e09ad6c8b3cff0348ad09c03ed83aab503035831f68f49d97f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.20348.2227; amd64

```console
$ docker pull eclipse-temurin@sha256:99f496259075b7d2dd196fac2d75142d031c41edcd4d3eb9d8392ab9dedef44f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164266909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ee65b8d954ad321e8b5a214dd1679ba6b7d970444d95ce63b1c85fcc0ad97e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 04 Jan 2024 03:13:36 GMT
RUN Apply image 10.0.20348.2227
# Wed, 10 Jan 2024 23:17:03 GMT
SHELL [cmd /s /c]
# Wed, 24 Jan 2024 21:54:51 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 21:54:52 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 24 Jan 2024 21:54:52 GMT
USER ContainerAdministrator
# Wed, 24 Jan 2024 21:55:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Jan 2024 21:55:03 GMT
USER ContainerUser
# Wed, 24 Jan 2024 21:55:52 GMT
COPY dir:dc1e2da1c34561e3d80ae1d96f99e65841adfcbd6fe35da2f57cba6532915179 in C:\openjdk-11 
# Wed, 24 Jan 2024 21:56:04 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:11d5cdc5eaac7bace3ae1ecd3c0df2a27ef5005ab296c56b7f83e24bf25c236c`  
		Last Modified: Tue, 09 Jan 2024 20:57:18 GMT  
		Size: 120.8 MB (120769267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a5f2601f3a3b05b34c1f8683e3c9ea81ea63dbe1b04c37b85d09170f020fc0`  
		Last Modified: Thu, 11 Jan 2024 04:18:57 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b94e45fae708b0f7158f355b5c7b1b612328d98382452767f92e76f1fad98a`  
		Last Modified: Wed, 24 Jan 2024 22:12:04 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6220560fcf99c5da84f2fb116b11dae64b5c37ee20c84b15ae5f68b809d23dfb`  
		Last Modified: Wed, 24 Jan 2024 22:12:03 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9331775eb15d41534d010478da59f4a5c5d63ab3e32f6e754cfd5661522195f`  
		Last Modified: Wed, 24 Jan 2024 22:12:03 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7775b294baabf771e1a966e97bd6f83782cabdc3f4f7a95c5e14fea5a1e52d73`  
		Last Modified: Wed, 24 Jan 2024 22:12:02 GMT  
		Size: 82.8 KB (82823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c270d1788f3d09c93f2fd4b98b47bd9f9f707b93d8ad12f90bbd9d4a19e622`  
		Last Modified: Wed, 24 Jan 2024 22:12:01 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499e57fbadc3dde8e634ba5a9a8692f9d186dc4309cd7eeaba38e0b4e135159d`  
		Last Modified: Wed, 24 Jan 2024 22:12:38 GMT  
		Size: 43.3 MB (43346950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0dfae3de989b336c08308586896c821f80ffc1588e5e71dad5f93507449193c`  
		Last Modified: Wed, 24 Jan 2024 22:12:31 GMT  
		Size: 62.1 KB (62063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull eclipse-temurin@sha256:eb5aa62547ebfff7f544f6303a8aea3ab9c279af626352c35cb808d7bacdefc4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148055319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89db54b0419026842c2c5f63de388ff381148e0054b57908cd5a23787d4187c6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Wed, 10 Jan 2024 22:41:06 GMT
SHELL [cmd /s /c]
# Wed, 24 Jan 2024 21:29:42 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 21:29:42 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 24 Jan 2024 21:29:43 GMT
USER ContainerAdministrator
# Wed, 24 Jan 2024 21:29:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Jan 2024 21:29:52 GMT
USER ContainerUser
# Wed, 24 Jan 2024 21:34:09 GMT
COPY dir:dc1e2da1c34561e3d80ae1d96f99e65841adfcbd6fe35da2f57cba6532915179 in C:\openjdk-11 
# Wed, 24 Jan 2024 21:34:18 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec88c6fd1d0cd14082069642ccb3b0dd5a7538a4b8b0c2d430549f345d8fd53`  
		Last Modified: Thu, 11 Jan 2024 04:09:21 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e033f014f5bfd19927c8437f77591cea9a7da834504ab83eee6fe1e69f9c17a`  
		Last Modified: Wed, 24 Jan 2024 22:04:34 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468440087d889f8eeb3a845fbffd4eb036178a323e07e1675241bcb48d9ba535`  
		Last Modified: Wed, 24 Jan 2024 22:04:34 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8e3acf960bcee55c49f64c053b4dc26794167193fc4ac14dda99c0dc2fbaf4`  
		Last Modified: Wed, 24 Jan 2024 22:04:34 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cadb0b7e805555804b0cb9b59ef11f4d2c902038e255e1baa8c1b919a75fbe`  
		Last Modified: Wed, 24 Jan 2024 22:04:32 GMT  
		Size: 72.5 KB (72478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648f7f679e5f81f847d0aa1b3cb711235ce7374d65c3320a07cdd47f9f5e0773`  
		Last Modified: Wed, 24 Jan 2024 22:04:32 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c3c14da39478ad894a57b88479e6cf7be5819ffb9c962826550d77e7b577f7`  
		Last Modified: Wed, 24 Jan 2024 22:05:50 GMT  
		Size: 43.3 MB (43336588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a40fff3cc5ac81d8f1917b53292aa383fb9374b203981a6419acc7686a67f7`  
		Last Modified: Wed, 24 Jan 2024 22:05:42 GMT  
		Size: 49.7 KB (49691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
