## `eclipse-temurin:17-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:568aafb40bb6f5b74c0ae7aa2f4dcd8aef01f2be80aa09734044f18895013d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.26100.3476; amd64

```console
$ docker pull eclipse-temurin@sha256:e5ad72aeae2ccb894c8bebec832a1ea8b47b03f4d21527011c907534e9b65110
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250214574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa821429a908e1302c4e768128b9d56d47b06d2aa604c3064a492663def6185`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Wed, 12 Mar 2025 19:17:25 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:17:27 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Wed, 12 Mar 2025 19:17:29 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 12 Mar 2025 19:17:31 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:17:35 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:17:36 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:17:42 GMT
COPY dir:e48212bf4bd9a001a558a3ce6925b9b3b6903c8af46347cbb9e06ca86192ff86 in C:\openjdk-17 
# Wed, 12 Mar 2025 19:17:48 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c093e2e312f62246bc05476903eaf67a078df6766f941bcdc4b393118159cd`  
		Last Modified: Wed, 12 Mar 2025 19:17:52 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4053f2b50a24a1b2086ee88a7678be65adc24b25b2d4de83a19a596fd1006249`  
		Last Modified: Wed, 12 Mar 2025 19:17:52 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34924676270f6fac3c21f8827abff03ff39f4d0a204f01645d788d85a44d30db`  
		Last Modified: Wed, 12 Mar 2025 19:17:52 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728eccc8a5bfd433aa974f91967c48bf381aefdbb75c099326d2a6b9b3bdc0cd`  
		Last Modified: Wed, 12 Mar 2025 19:17:51 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aaa51a6d06fc23c39df562b22d5fc2f376673ed3f491432e59abd6bae863bd8`  
		Last Modified: Wed, 12 Mar 2025 19:17:51 GMT  
		Size: 76.1 KB (76063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c6f7a7256273cf78cd7f6207aa2c4fef5ada7fbc59a2fd87af99827f0bc699`  
		Last Modified: Wed, 12 Mar 2025 19:17:51 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab70bb7907e13388019210b1a33e14339d7f28328989079ec7853e71bacad6e`  
		Last Modified: Wed, 12 Mar 2025 19:17:57 GMT  
		Size: 43.7 MB (43729189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f9e696aca12263eff0b4c05ff60451e947d5a7be2e56d4c005ca12bc90686a`  
		Last Modified: Wed, 12 Mar 2025 19:17:51 GMT  
		Size: 101.8 KB (101767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.20348.3328; amd64

```console
$ docker pull eclipse-temurin@sha256:389faf696098bc411c2124ccb71d3c11b0f76b6eaa74dbdc1ce94d9368cb9f78
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164602105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2139b5f81aa0689f564193e77446a1875a1cbedae457214f080efd7465039c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Wed, 12 Mar 2025 19:20:09 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:20:10 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Wed, 12 Mar 2025 19:20:11 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 12 Mar 2025 19:20:12 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:20:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:20:15 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:20:19 GMT
COPY dir:e48212bf4bd9a001a558a3ce6925b9b3b6903c8af46347cbb9e06ca86192ff86 in C:\openjdk-17 
# Wed, 12 Mar 2025 19:20:22 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fb765e128f52f9e45e75e1ab7d267aae32907e48745c6e18e4cce7033dc8cd`  
		Last Modified: Wed, 12 Mar 2025 19:20:26 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61685d0e4c8b460f2944103c97ca0d5d3abfc6a8864e2cbb1a3889703e0da96f`  
		Last Modified: Wed, 12 Mar 2025 19:20:26 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c15e60d44756b76643aa406e99a453e9d3a23be34cca1f7785e3fdee977b9a7`  
		Last Modified: Wed, 12 Mar 2025 19:20:26 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc48506b30c50c4dfe9a1ff72f86a3a3d4a3d262c7a31975ca4caf0b0d1a4060`  
		Last Modified: Wed, 12 Mar 2025 19:20:25 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73354be15c05d474b674d3c99d9ed2909a3413c655880c26082317b07f72528`  
		Last Modified: Wed, 12 Mar 2025 19:20:25 GMT  
		Size: 77.3 KB (77290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7970a4ce3f8b4304088627c29968ac69b91bf5157060df46c9d2099bc9a317d0`  
		Last Modified: Wed, 12 Mar 2025 19:20:25 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef4bfe0c803ec6f929b41c2297fc0b45e61130f1727d2fd6cb31340c9c93e64`  
		Last Modified: Wed, 12 Mar 2025 19:20:29 GMT  
		Size: 43.7 MB (43726673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513e7f0b726aed00cd426db0fd567d5730bf7fd1ffd54ab2bd2636410bbf3949`  
		Last Modified: Wed, 12 Mar 2025 19:20:25 GMT  
		Size: 97.4 KB (97449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.17763.7009; amd64

```console
$ docker pull eclipse-temurin@sha256:066d150620296d22268d58337502b9bce72126669accb7ba8f0e7486aee812d3
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.7 MB (153702357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8f30bd7f21d529c4b30f9b81b6f659370327be7747ea8eca4168e4e46c7c2c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Wed, 12 Mar 2025 19:21:51 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:21:52 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Wed, 12 Mar 2025 19:21:53 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 12 Mar 2025 19:21:53 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:21:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:21:56 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:22:01 GMT
COPY dir:e48212bf4bd9a001a558a3ce6925b9b3b6903c8af46347cbb9e06ca86192ff86 in C:\openjdk-17 
# Wed, 12 Mar 2025 19:22:05 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbcdb05d17a35d4540cbff011027f76dd304c4a4f7ae4cf919ce03d2dbab5e4`  
		Last Modified: Wed, 12 Mar 2025 19:22:12 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6491a02174ed611b5c08cd5a6ca10faa8b95227abd0a08473bfffb6d9625a0d`  
		Last Modified: Wed, 12 Mar 2025 19:22:12 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec08622e8b2702c55ce643f805c84177d5601662f920f7f0aefa480f76530e0c`  
		Last Modified: Wed, 12 Mar 2025 19:22:12 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64645226d162a4c87d2c83a020973b457806b181bf6c7a127a6ff1bd51316943`  
		Last Modified: Wed, 12 Mar 2025 19:22:10 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55b95865f475adf72dad2d6be1118c2a95efcca04c380c00d7ab6b6eaf8a584`  
		Last Modified: Wed, 12 Mar 2025 19:22:10 GMT  
		Size: 69.1 KB (69057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c2c687d6057e406e00ce86aa72858009eea06ee10871616156f8f0d3aa29a7`  
		Last Modified: Wed, 12 Mar 2025 19:22:10 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d563e27763c6606c000230a4040628104ca097daed128c354be956924b51cbc`  
		Last Modified: Wed, 12 Mar 2025 19:22:15 GMT  
		Size: 43.7 MB (43727211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88592db5e555a15d8d87f3982b54c4ee07afa3ca7ae106900ba914368e2cfb44`  
		Last Modified: Wed, 12 Mar 2025 19:22:11 GMT  
		Size: 3.0 MB (2993204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
