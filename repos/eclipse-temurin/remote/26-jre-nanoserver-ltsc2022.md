## `eclipse-temurin:26-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:8ebc5e61c33a3707a7b2ae55a978feb2e80dbe18c3d0b55bb94384ec7e316f60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:26-jre-nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull eclipse-temurin@sha256:dd7ec5c564f61427d89d4e8a29190f8badba2aa90c0fcbb00e9a9c9d4f1c6b7f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187422234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3317200917b9c42e35797d32e3398b8e0bf7278968ab8dea33b451df56ee2d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 22:11:10 GMT
SHELL [cmd /s /c]
# Tue, 14 Apr 2026 22:12:32 GMT
ENV JAVA_VERSION=jdk-26+35
# Tue, 14 Apr 2026 22:12:32 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 14 Apr 2026 22:12:33 GMT
USER ContainerAdministrator
# Tue, 14 Apr 2026 22:12:34 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Apr 2026 22:12:35 GMT
USER ContainerUser
# Tue, 14 Apr 2026 22:12:48 GMT
COPY dir:45edd54e05e2fb7ffc611e6ef0c2df37aa13ac9c3c9a476003fc542e9ad17481 in C:\openjdk-26 
# Tue, 14 Apr 2026 22:12:52 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8993acfdf4686dba6fe118f01f7811517ee4c5ef953a3f4ff4422198e46d0cd0`  
		Last Modified: Tue, 14 Apr 2026 22:11:39 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad6cfc1227181bb3cdd6ce728e3f5530ae830aea3ebd10d894433f8332838fe`  
		Last Modified: Tue, 14 Apr 2026 22:12:57 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44578d1e3d66adf801df28c8d2b0a8d6e79d02b1f37714f2651683b15690e680`  
		Last Modified: Tue, 14 Apr 2026 22:12:57 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9d1c35dc40b8751a941a62dd9a626c49c68c888b340f2bd1fdd0cd4b058508`  
		Last Modified: Tue, 14 Apr 2026 22:12:56 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da09a60cdff48859d32ef437d7e156408c781cf90bcd3b252802031604c29347`  
		Last Modified: Tue, 14 Apr 2026 22:12:56 GMT  
		Size: 85.1 KB (85094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e090d947b499cdd663219ae1eb9499cc5b79972231abef0e74b8a8b5004887`  
		Last Modified: Tue, 14 Apr 2026 22:12:56 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5450cd1259434c221ab986f25d17ca81b3def3c096ae26a3006fa9cb3a7973aa`  
		Last Modified: Tue, 14 Apr 2026 22:13:04 GMT  
		Size: 60.3 MB (60266405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d34a9e7d3bb85ae473b3f42803af6a1a3973b800dae0c431712bfdafb07493`  
		Last Modified: Tue, 14 Apr 2026 22:12:56 GMT  
		Size: 109.5 KB (109458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
