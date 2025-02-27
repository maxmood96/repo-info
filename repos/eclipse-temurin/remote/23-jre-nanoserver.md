## `eclipse-temurin:23-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:903ab4eb0ddb18409e676cb18bc37130cf47fd7374bf52806bcb20543b68aea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3194; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `eclipse-temurin:23-jre-nanoserver` - windows version 10.0.26100.3194; amd64

```console
$ docker pull eclipse-temurin@sha256:062306f973bceb7ae688d5e82d3022b54e5ea01e26185967ccde2d77b05c1547
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (255044600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e07fe058c3d6af7c07db59e5bc24d13d3beef231fca563edabeb10daa203e9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 08 Feb 2025 22:31:47 GMT
RUN Apply image 10.0.26100.3194
# Thu, 27 Feb 2025 19:13:37 GMT
SHELL [cmd /s /c]
# Thu, 27 Feb 2025 19:13:38 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 27 Feb 2025 19:13:39 GMT
ENV JAVA_HOME=C:\openjdk-23
# Thu, 27 Feb 2025 19:13:39 GMT
USER ContainerAdministrator
# Thu, 27 Feb 2025 19:13:42 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 27 Feb 2025 19:13:42 GMT
USER ContainerUser
# Thu, 27 Feb 2025 19:13:47 GMT
COPY dir:f0b8f3d1970d52810d59047a7e1dfff98787b37140cc4aafc37fc86b09fa8be8 in C:\openjdk-23 
# Thu, 27 Feb 2025 19:13:51 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:e075dd07cbf907b7da8dbd8365b73a71ac92a834b78f520bd976cb97e0fcc0a1`  
		Last Modified: Wed, 12 Feb 2025 22:34:59 GMT  
		Size: 205.9 MB (205890263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1972b20bd706211d38ad6a7019c45938907494fab5759ae8f9a26d6ec1f4a68`  
		Last Modified: Thu, 27 Feb 2025 19:13:54 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb406cdea18c2ec88d14e20338053851b4e3457dc2c9f34c6704d5b153d6cf39`  
		Last Modified: Thu, 27 Feb 2025 19:13:54 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f79b7ddde2fc01a4ad1d4c8d23f18341aa270905f0c3913a7e5967521688776`  
		Last Modified: Thu, 27 Feb 2025 19:13:54 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeab4fdca0e3f87588f2a5e008a05aa7872567d2184e103d4be49e167d755028`  
		Last Modified: Thu, 27 Feb 2025 19:13:53 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d0d6d1238aab00e2c11dd10a6c66f23f9bf6bc5413417a8b658d324b4c085d`  
		Last Modified: Thu, 27 Feb 2025 19:13:53 GMT  
		Size: 76.0 KB (75993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04591fdd334575d9ba173028debb95997c59453bded7e0f100afc8807a652b4c`  
		Last Modified: Thu, 27 Feb 2025 19:13:53 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286b2c6089fe22ea9982c82ca6b4fe3750d40d3d2b2fefa037e6145a18131ee4`  
		Last Modified: Thu, 27 Feb 2025 19:13:58 GMT  
		Size: 49.0 MB (48979629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37f8c1194745d55fb0d8d6fe5a0aef5925976ecae322209a83b7ed70b1d3c65`  
		Last Modified: Thu, 27 Feb 2025 19:13:53 GMT  
		Size: 93.5 KB (93479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-jre-nanoserver` - windows version 10.0.20348.3207; amd64

```console
$ docker pull eclipse-temurin@sha256:12d414212274701e851ea72c569d79aea510f5024936b526c13a9b108a06fd3a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.8 MB (169828568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611234067a64f373940b630e3242f1f9742a8036ad5c5bdf7a93c3418f1ee515`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 20:45:43 GMT
RUN Apply image 10.0.20348.3207
# Thu, 13 Feb 2025 01:17:20 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:17:21 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 13 Feb 2025 01:17:21 GMT
ENV JAVA_HOME=C:\openjdk-23
# Thu, 13 Feb 2025 01:17:22 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:17:24 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Feb 2025 01:17:24 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:17:29 GMT
COPY dir:f0b8f3d1970d52810d59047a7e1dfff98787b37140cc4aafc37fc86b09fa8be8 in C:\openjdk-23 
# Thu, 13 Feb 2025 01:17:33 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:938e4585b186fc3df3c1959d47ba7a634fea121cec7545db7923ceb191d99a33`  
		Last Modified: Tue, 11 Feb 2025 22:43:09 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7661fcc7c8b1a22c8e195317cfba7af092eb5730d4bad6bc8c3fcd3c8e14db94`  
		Last Modified: Thu, 13 Feb 2025 01:17:37 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7177cd12a768e808d5c988ebf8ef05aef3247f9223c48834377dec30d4785723`  
		Last Modified: Thu, 13 Feb 2025 01:17:37 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c5aaf7e4ec21a97e3b6f49560be453218dd95e7bc407565c699c11908e881e`  
		Last Modified: Thu, 13 Feb 2025 01:17:37 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c9989c2f478e22e8f410b3be82227ea8d3381129146aa8605e3e86105eb50b`  
		Last Modified: Thu, 13 Feb 2025 01:17:36 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:763515b62c0f7371f01f95d6589fe46b94e163294af355611a8d0f823c844348`  
		Last Modified: Thu, 13 Feb 2025 01:17:35 GMT  
		Size: 75.9 KB (75922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f458f933cb2d48a064a6e47ce4b11ed49737f57b63c8695f7afe53aa017a1fa0`  
		Last Modified: Thu, 13 Feb 2025 01:17:35 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378f0df813d51c01a127ef5ea4042665fc0bf6219308205d362ae8424a840b3b`  
		Last Modified: Thu, 13 Feb 2025 01:17:41 GMT  
		Size: 49.0 MB (48980223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7481f750fbfa2b3297f3fe81859dd212f6dbd00b131ff61c1e2c80fa603ef0`  
		Last Modified: Thu, 13 Feb 2025 01:17:35 GMT  
		Size: 100.6 KB (100634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-jre-nanoserver` - windows version 10.0.17763.6893; amd64

```console
$ docker pull eclipse-temurin@sha256:124da68bb365b233f248ff5403cedec7a63e0f86343745b771fac6c4416b1483
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159589292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74fca2080e5362f6abf8ed0db7aabbc9da27275e0524b03d4de6bf6218f8d68b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:17:33 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:17:34 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 13 Feb 2025 01:17:35 GMT
ENV JAVA_HOME=C:\openjdk-23
# Thu, 13 Feb 2025 01:17:36 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:17:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Feb 2025 01:17:39 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:17:43 GMT
COPY dir:f0b8f3d1970d52810d59047a7e1dfff98787b37140cc4aafc37fc86b09fa8be8 in C:\openjdk-23 
# Thu, 13 Feb 2025 01:17:46 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9ae50f80add6e329a320188216ea095f83d125a3b6433ca4dd65d98af55251`  
		Last Modified: Thu, 13 Feb 2025 01:17:50 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0eadfeaa84a6f06352c7a13c6f24f96704a2c5a8d4b586c69524a340ef0bee2`  
		Last Modified: Thu, 13 Feb 2025 01:17:49 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718fdd28f0ffb30987b97d0eb3e073b21663791fb98c92ae6ae8ee8d25d5c11f`  
		Last Modified: Thu, 13 Feb 2025 01:17:49 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e32810f8b3f5d0fb96ec8915e6142e5e289c71fe1360a5b5ae978bf13509792`  
		Last Modified: Thu, 13 Feb 2025 01:17:48 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d625b2d9e0720c3f33161389c8715c4f4cdd9f2fb579292a70f49be5189eeeb`  
		Last Modified: Thu, 13 Feb 2025 01:17:48 GMT  
		Size: 71.5 KB (71505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ad516ee215ba25c94ac787527a8bca1052bc875a4586525766bf1a418ed0f8`  
		Last Modified: Thu, 13 Feb 2025 01:17:48 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1f3ad896ab8dd43b22465760df65e40d23c180ae9646892600f849345dfe17`  
		Last Modified: Thu, 13 Feb 2025 01:17:54 GMT  
		Size: 49.0 MB (48980135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09bd81810b4a794ec09957a07fd3bc48419899ae96bccf4718addb97fad695d2`  
		Last Modified: Thu, 13 Feb 2025 01:17:49 GMT  
		Size: 3.6 MB (3616991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
