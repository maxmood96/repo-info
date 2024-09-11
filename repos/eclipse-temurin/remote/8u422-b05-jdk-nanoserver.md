## `eclipse-temurin:8u422-b05-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:74a77fd9bdf82e281f7f61c9fc38aae05a3c520e7e902c9fa56967ebca74489e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `eclipse-temurin:8u422-b05-jdk-nanoserver` - windows version 10.0.20348.2700; amd64

```console
$ docker pull eclipse-temurin@sha256:dd7a9ee0889ee9e5d59944f765c48889a194126d6c892d7265e9655de378ca9d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.2 MB (222202470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e10c92faf3d0c0ca0a26ef1325c9d73884089ce9f901a3970acf06870ab91ad`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Sep 2024 23:48:03 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 01:05:47 GMT
SHELL [cmd /s /c]
# Wed, 11 Sep 2024 01:05:48 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Wed, 11 Sep 2024 01:05:49 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 11 Sep 2024 01:05:49 GMT
USER ContainerAdministrator
# Wed, 11 Sep 2024 01:06:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Sep 2024 01:06:01 GMT
USER ContainerUser
# Wed, 11 Sep 2024 01:06:10 GMT
COPY dir:cf98fec7e439356342f3bf03fb67b0dac0e213296a20d5e427a9ebba9080193e in C:\openjdk-8 
# Wed, 11 Sep 2024 01:06:22 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:a447243899be39b01c34fc7e1bcecb47ce42b14668876fdd121f8b5e2d4d4a86`  
		Last Modified: Tue, 10 Sep 2024 22:28:02 GMT  
		Size: 120.5 MB (120509521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015f530aeae2fa9f5c34641a19099e9949880479ad7319678bd0506ba1927a95`  
		Last Modified: Wed, 11 Sep 2024 01:33:11 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef21dd038c1a6c24bf77ad129528c82f4db5372ddc60d7995e7e00d371596c7b`  
		Last Modified: Wed, 11 Sep 2024 01:33:11 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0e194644c9171125eb77ddd53d8e8ec733ef20766f72803cd7b1a0ed866b17`  
		Last Modified: Wed, 11 Sep 2024 01:33:11 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20417130e443b6ddae87f09a182af4de4d2fc54934e7f37c5ff7593c632f32ac`  
		Last Modified: Wed, 11 Sep 2024 01:33:09 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba644b18af11e2543cf583b6343beb7329f0d8c81d7bbb17d869e11bb7f364b`  
		Last Modified: Wed, 11 Sep 2024 01:33:09 GMT  
		Size: 79.5 KB (79477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4779375c8f2e097d1809a2d32a036d3e2c56431225c0eaa310afb7791eee429f`  
		Last Modified: Wed, 11 Sep 2024 01:33:09 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd59836a65fca6bddd5144eaa5c5bda2ec4e82e4c2492ecb5ef195308f683e09`  
		Last Modified: Wed, 11 Sep 2024 01:33:20 GMT  
		Size: 101.5 MB (101546512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b498248f0d47d65b188b532a3c635773ab80de8bea1561cdc596ddd2bc23826`  
		Last Modified: Wed, 11 Sep 2024 01:33:09 GMT  
		Size: 61.2 KB (61154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u422-b05-jdk-nanoserver` - windows version 10.0.17763.6293; amd64

```console
$ docker pull eclipse-temurin@sha256:cea71e3139d94ff8c0fa8333911d7a58835ca25be1c7893d419a42a25c0d00c9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 MB (256796318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d246709bf249ddfcc3ebcfcda9a97214b14b5e039d685a1911470ffcef2a1f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:38:01 GMT
SHELL [cmd /s /c]
# Wed, 11 Sep 2024 00:38:02 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Wed, 11 Sep 2024 00:38:03 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 11 Sep 2024 00:38:03 GMT
USER ContainerAdministrator
# Wed, 11 Sep 2024 00:38:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Sep 2024 00:38:14 GMT
USER ContainerUser
# Wed, 11 Sep 2024 00:38:22 GMT
COPY dir:cf98fec7e439356342f3bf03fb67b0dac0e213296a20d5e427a9ebba9080193e in C:\openjdk-8 
# Wed, 11 Sep 2024 00:38:36 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340318059288cbbdb326eea5b7079e789361251409038a37867d4e395c9404a5`  
		Last Modified: Wed, 11 Sep 2024 01:21:36 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02106b426902c7615863c4b56b01b06cc3d3b7fa8855c49224ee7699989fefba`  
		Last Modified: Wed, 11 Sep 2024 01:21:36 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c43928233a5d3038e98674df1be7f1f29e0801669f62acabaf0d113b33ee4e`  
		Last Modified: Wed, 11 Sep 2024 01:21:35 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b418b25d7d864e6ccdad65299b0972dcbd0dde17c1f20f6b0e3d2dd7829bca`  
		Last Modified: Wed, 11 Sep 2024 01:21:33 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a59736e850920a7737b3a01e95f615c9dd3ef10af0fa911b2ec0285135734c4`  
		Last Modified: Wed, 11 Sep 2024 01:21:34 GMT  
		Size: 69.5 KB (69510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d38143bdbd943337ada11ffd205aacee07168442061f9d5b5cbdd9bb6c7de211`  
		Last Modified: Wed, 11 Sep 2024 01:21:34 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03048e25deb4d7869eacfa3bc0b0431b816c21e13505e376f0ffd22503285f33`  
		Last Modified: Wed, 11 Sep 2024 01:21:45 GMT  
		Size: 101.5 MB (101549222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da10096a5ff9d6ab16275c9e4b75138780d8f8351132296effcede4c3271c3da`  
		Last Modified: Wed, 11 Sep 2024 01:21:34 GMT  
		Size: 91.0 KB (91003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
