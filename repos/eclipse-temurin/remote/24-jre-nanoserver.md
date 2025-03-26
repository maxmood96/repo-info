## `eclipse-temurin:24-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:672417aeb8c689c8399eb21cddb99f384bf93c3798968fc698504f962a075b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `eclipse-temurin:24-jre-nanoserver` - windows version 10.0.26100.3476; amd64

```console
$ docker pull eclipse-temurin@sha256:e8cb80cff1cf0f787c8e4e046fe1407eb6d6083d38670ddd43a12f7a823cd6e3
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.2 MB (264178185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b8f0b9f48ead99709caf89f3be43cf39ca3bdc85b57f17e3ebd0152044ea51`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Tue, 25 Mar 2025 22:12:51 GMT
SHELL [cmd /s /c]
# Tue, 25 Mar 2025 22:12:52 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 22:12:53 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 25 Mar 2025 22:12:53 GMT
USER ContainerAdministrator
# Tue, 25 Mar 2025 22:12:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 25 Mar 2025 22:12:58 GMT
USER ContainerUser
# Tue, 25 Mar 2025 22:13:02 GMT
COPY dir:90c9828944ffcd2978afe702f80884cbf787022d7dcd7becc7c91cd2ab6f7dd5 in C:\openjdk-24 
# Tue, 25 Mar 2025 22:13:07 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb647fa7ed2635f43b536686a3e62e23c2090b29ce299c11f569bf6962cb8708`  
		Last Modified: Tue, 25 Mar 2025 22:13:13 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b09f0e264b81c0bafabbeb8e28067bf297d70dd69746bf0cede6003ba7849d`  
		Last Modified: Tue, 25 Mar 2025 22:13:13 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b479da94240c95456a32c253fe0676639a0a567b63f9e7a3a9c0fd16a080f7`  
		Last Modified: Tue, 25 Mar 2025 22:13:12 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012e843b677f712576f9a0c643ef15ed60e4b60658e535763aaf42322db00283`  
		Last Modified: Tue, 25 Mar 2025 22:13:11 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2232ab6250a0f6d93e0beadcb80e37e325c53cd1636ffb7462f769c4be77de78`  
		Last Modified: Tue, 25 Mar 2025 22:13:11 GMT  
		Size: 76.0 KB (75987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1519959fc5570a9ba256420794eecd8311a22dec5d3e6472e4187404bf7ff887`  
		Last Modified: Tue, 25 Mar 2025 22:13:11 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ed35eddd4406e44359c490bd809ab860fb848a0bfddaf665406c2c5771f0c7`  
		Last Modified: Tue, 25 Mar 2025 22:13:18 GMT  
		Size: 57.7 MB (57701308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cd84de29d2b62c6a59b3bdccf7742bf657a1b03918bb60740423f8ecf96cd2`  
		Last Modified: Tue, 25 Mar 2025 22:13:11 GMT  
		Size: 93.4 KB (93399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:24-jre-nanoserver` - windows version 10.0.20348.3328; amd64

```console
$ docker pull eclipse-temurin@sha256:57131b7ece1057a579bcf4b713fcda3b8ffa3571ded0e9939109cd35c39d8e77
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.6 MB (178575993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7cc540105e151acfa7e2bf11f45e502168d52a9884a470eb6d440edd79c5cd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Tue, 25 Mar 2025 23:23:25 GMT
SHELL [cmd /s /c]
# Tue, 25 Mar 2025 23:23:26 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 23:23:27 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 25 Mar 2025 23:23:27 GMT
USER ContainerAdministrator
# Tue, 25 Mar 2025 23:23:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 25 Mar 2025 23:23:31 GMT
USER ContainerUser
# Tue, 25 Mar 2025 23:23:35 GMT
COPY dir:90c9828944ffcd2978afe702f80884cbf787022d7dcd7becc7c91cd2ab6f7dd5 in C:\openjdk-24 
# Tue, 25 Mar 2025 23:23:40 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf9dddd7da9a70eac8a7048d104817e052046ff648b5e3a869add8fcee45e6b6`  
		Last Modified: Tue, 25 Mar 2025 23:23:45 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abb9d74c9b1b7713d1309ee4cb0bfc9641ccb2d22e71fc571dd8e97facd13c2`  
		Last Modified: Tue, 25 Mar 2025 23:23:45 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87e2b1edd7419dc29ba3c9b13ee367f8d42244eda0057c2e3617b2b486a9a91`  
		Last Modified: Tue, 25 Mar 2025 23:23:45 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e776c47f588273589d3e4b7aab1fdda4e514e9806635c3adbcff4b1fcc5148`  
		Last Modified: Tue, 25 Mar 2025 23:23:44 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b1902f7ffea612782f86025c222acb396a6bb5ea83f8c14b94a643588d870b`  
		Last Modified: Tue, 25 Mar 2025 23:23:44 GMT  
		Size: 77.0 KB (77005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b097a2b47469115f0533545676071f28c690c9e0893bc4402b7607259e89b721`  
		Last Modified: Tue, 25 Mar 2025 23:23:44 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8b28d2bcb4f16fc130f07bea062baac775e931268a5ca3e3fb2d71e68a2e35`  
		Last Modified: Tue, 25 Mar 2025 23:23:51 GMT  
		Size: 57.7 MB (57700729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b869ba14727d4d26920b073f39df29f41a9131d6e95a3e45bea0d2c63bb4fac`  
		Last Modified: Tue, 25 Mar 2025 23:23:44 GMT  
		Size: 97.5 KB (97470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:24-jre-nanoserver` - windows version 10.0.17763.7009; amd64

```console
$ docker pull eclipse-temurin@sha256:18287b19009c453389840241bbe676a5c0a074c9a9933e37208f04b31a14d809
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168584110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e61d42e037db37dac87b24caf2d5dd5300d226841c9e3e74eb5bacfbab08b35`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Tue, 25 Mar 2025 23:18:27 GMT
SHELL [cmd /s /c]
# Tue, 25 Mar 2025 23:18:29 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 23:18:30 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 25 Mar 2025 23:18:30 GMT
USER ContainerAdministrator
# Tue, 25 Mar 2025 23:18:33 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 25 Mar 2025 23:18:34 GMT
USER ContainerUser
# Tue, 25 Mar 2025 23:18:39 GMT
COPY dir:90c9828944ffcd2978afe702f80884cbf787022d7dcd7becc7c91cd2ab6f7dd5 in C:\openjdk-24 
# Tue, 25 Mar 2025 23:18:42 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d42a0811c09bb7f0cc287a9b055a55a251e1639a924bcd1217ff35bcb1fa77a3`  
		Last Modified: Tue, 25 Mar 2025 23:18:46 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162977662480aec0e59d689b90cd91db862f5459e0e2fedab921c8e143c07040`  
		Last Modified: Tue, 25 Mar 2025 23:18:46 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30aefc727fb4e9f6733e0b4ed73dbbcef05d3edbcddd469f8dde64450c1f2c5c`  
		Last Modified: Tue, 25 Mar 2025 23:18:46 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dc45bc7581625cb5c1227ed95e921ec5f8181e3ac6dc0eedff82aa06068014`  
		Last Modified: Tue, 25 Mar 2025 23:18:45 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf563a55f51833614596eb35bfa0b6f0f6a8947d72ccc1fecd5c1cb11af1841`  
		Last Modified: Tue, 25 Mar 2025 23:18:45 GMT  
		Size: 70.3 KB (70285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc65f99a24cf7764374e24ec5911536994f58f83c9f3922b741522a7d94b4a85`  
		Last Modified: Tue, 25 Mar 2025 23:18:45 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b359a30bd1d01353d142067fb8e72dce94ac44cb58eb2e800d47417b117bf1`  
		Last Modified: Tue, 25 Mar 2025 23:18:52 GMT  
		Size: 57.7 MB (57700848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60ea89829296b5810e00af267a460d679d88530377780e1542a455eab8f9aaa`  
		Last Modified: Tue, 25 Mar 2025 23:18:45 GMT  
		Size: 3.9 MB (3899992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
