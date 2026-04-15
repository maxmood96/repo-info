## `eclipse-temurin:26-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:f111875935effcd5418a9a1332779b31fd371dc0ca97145ddd7c31b718e6c7af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:26-jre-nanoserver` - windows version 10.0.26100.32690; amd64

```console
$ docker pull eclipse-temurin@sha256:c03c8ffb90c38a87f80f7bc76d6c85c7bfad898a21bb168dc0d2be38e4cc8b78
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.2 MB (260181186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26671da10f02b891b69305425b2017cea782902097b97e9f9fc098b793c7f205`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 06:39:57 GMT
RUN Apply image 10.0.26100.32690
# Tue, 14 Apr 2026 22:14:17 GMT
SHELL [cmd /s /c]
# Tue, 14 Apr 2026 22:14:17 GMT
ENV JAVA_VERSION=jdk-26+35
# Tue, 14 Apr 2026 22:14:17 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 14 Apr 2026 22:14:18 GMT
USER ContainerAdministrator
# Tue, 14 Apr 2026 22:14:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Apr 2026 22:14:20 GMT
USER ContainerUser
# Tue, 14 Apr 2026 22:14:38 GMT
COPY dir:45edd54e05e2fb7ffc611e6ef0c2df37aa13ac9c3c9a476003fc542e9ad17481 in C:\openjdk-26 
# Tue, 14 Apr 2026 22:14:42 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:8af320c3b6d19296bcc7947e3beb8bc0c69cb12143db52efe988dc998ac088dc`  
		Last Modified: Tue, 14 Apr 2026 21:00:37 GMT  
		Size: 199.7 MB (199717094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84021931477dfb29a332bf69444c211840756a55c1d55f1809f8ad7a1591778`  
		Last Modified: Tue, 14 Apr 2026 22:14:47 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d33c223c93c957f49300deee7db0ba7b7710e794405aff175a77479556d39fe`  
		Last Modified: Tue, 14 Apr 2026 22:14:47 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a1124d7a3400317727471500e409a23986e9c11717c46725d759cdbc7bf9f1`  
		Last Modified: Tue, 14 Apr 2026 22:14:47 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0393b6619508a52c853d491fa26c59e13e2b2a6e7a0f1700090dcbd12481bf`  
		Last Modified: Tue, 14 Apr 2026 22:14:46 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b95475246f912d5e73b52e1113972ffdf5add1cf9fa63962485aff0469d37f`  
		Last Modified: Tue, 14 Apr 2026 22:14:46 GMT  
		Size: 72.3 KB (72298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b332faecae5aa3bee35579017f0c06867e44de92ec500c29697a07fdc381fc`  
		Last Modified: Tue, 14 Apr 2026 22:14:46 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e7d87942a63ec79cdadad141ecfc559b84c2e9075eedc163878ea90ff5c5540`  
		Last Modified: Tue, 14 Apr 2026 22:14:54 GMT  
		Size: 60.3 MB (60266534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd880099ff90171b6c82c50f47f2e8c8ed1a2011464e70c6ced49fe1c42e2f9`  
		Last Modified: Tue, 14 Apr 2026 22:14:46 GMT  
		Size: 119.9 KB (119948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:26-jre-nanoserver` - windows version 10.0.20348.5020; amd64

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
