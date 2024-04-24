## `eclipse-temurin:21-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:dbf6970b97ad6c5a21ab966974fe4899485f28ec8dc0370d2af0febd1c0075ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `eclipse-temurin:21-jdk-nanoserver` - windows version 10.0.20348.2402; amd64

```console
$ docker pull eclipse-temurin@sha256:94f765bf240883bf206fab4c00ab8302b1da6406d66bfe001fc542fc9c9bcece
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322289416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:557cba953091cc6417aca13c0e3e77e193d075f45e76cda018beaa0aa772fb9c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Apr 2024 08:53:11 GMT
RUN Apply image 10.0.20348.2402
# Wed, 10 Apr 2024 00:34:53 GMT
SHELL [cmd /s /c]
# Wed, 24 Apr 2024 19:26:52 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Wed, 24 Apr 2024 19:26:53 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 24 Apr 2024 19:26:54 GMT
USER ContainerAdministrator
# Wed, 24 Apr 2024 19:27:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Apr 2024 19:27:05 GMT
USER ContainerUser
# Wed, 24 Apr 2024 19:27:19 GMT
COPY dir:23b4ead9c2036754f644b00182bded9da6af0a8e5b9adaf18f46a103fb435a07 in C:\openjdk-21 
# Wed, 24 Apr 2024 19:27:36 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 24 Apr 2024 19:27:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:755fc767289b8847bd0d0d8d75efc308c040140acf2a3426973ba9fbf022c4c0`  
		Last Modified: Tue, 09 Apr 2024 23:50:18 GMT  
		Size: 121.0 MB (120993754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70887eeae6a5d6d5fd81661024afc84fee637f674dee5e7127112cbfce90750`  
		Last Modified: Wed, 10 Apr 2024 01:00:01 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5073ce61d37d8fd4d08613c9f3a71ce2bd93082380f6a522a9936ae916ae4f25`  
		Last Modified: Wed, 24 Apr 2024 19:48:21 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e178760818d5722db2d5c0e64effa0e2e08f9d665d1f1f1a0f3383cdd421c1`  
		Last Modified: Wed, 24 Apr 2024 19:48:21 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ab01696df06cd68ecd1bc661d18803e5be87ffc4238a771382fab6f59489dc`  
		Last Modified: Wed, 24 Apr 2024 19:48:21 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b530d78830b88a301d87ef726d16e1f6ec9b24d2292e624242c3f93065973909`  
		Last Modified: Wed, 24 Apr 2024 19:48:19 GMT  
		Size: 79.4 KB (79404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159ad8d313c0012825ca2290c5dd48de29c486e0f6cb6af0afee5034f39f7688`  
		Last Modified: Wed, 24 Apr 2024 19:48:19 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f6bd33ea133d841f6f3c870073d625eb46648980429ccccffccb12433236fe`  
		Last Modified: Wed, 24 Apr 2024 19:48:39 GMT  
		Size: 201.1 MB (201148304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca1ef0164cd034fe066227ccd2ca8ded48988f78d9095d12794473dc3e92ffb`  
		Last Modified: Wed, 24 Apr 2024 19:48:19 GMT  
		Size: 61.2 KB (61164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78528d8dfa1691ddd22bf154518df7043ce27e1de89756b26e904fdc15166a34`  
		Last Modified: Wed, 24 Apr 2024 19:48:19 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jdk-nanoserver` - windows version 10.0.17763.5696; amd64

```console
$ docker pull eclipse-temurin@sha256:6b0a6917aeb3f2efc03d8d787448119e0c9536ec8ccf2ef6061377cbadf71a73
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.9 MB (309924070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afff5824fc116328a2d5e04745bad049a5ad4e617ad0c0b4858808a6e8c1b718`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Tue, 09 Apr 2024 23:42:55 GMT
SHELL [cmd /s /c]
# Wed, 24 Apr 2024 19:05:16 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Wed, 24 Apr 2024 19:05:16 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 24 Apr 2024 19:05:17 GMT
USER ContainerAdministrator
# Wed, 24 Apr 2024 19:05:27 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Apr 2024 19:05:28 GMT
USER ContainerUser
# Wed, 24 Apr 2024 19:05:42 GMT
COPY dir:23b4ead9c2036754f644b00182bded9da6af0a8e5b9adaf18f46a103fb435a07 in C:\openjdk-21 
# Wed, 24 Apr 2024 19:05:56 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 24 Apr 2024 19:05:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b591b5f81c02344da39dc8a9084b5791cbf552c1eb85e79db1f38dfc715a681`  
		Last Modified: Wed, 10 Apr 2024 00:47:46 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dcf091fcbebbebeea32531bf662cf81e86b1fcb615435e409da811c0f478220`  
		Last Modified: Wed, 24 Apr 2024 19:41:36 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a6fcfb47ceb8b4eb2308c3ec1e799ad906c69b94f3d90599861bf994fb6ed2`  
		Last Modified: Wed, 24 Apr 2024 19:41:36 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48af84976cbb1708013331be6262b5a5b8d6aca50c6e24793cf4ec1910152194`  
		Last Modified: Wed, 24 Apr 2024 19:41:36 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5c1823c2ef5030c4e9fc741157cd268455663bdfbc1c10381b61d3c6e4d819`  
		Last Modified: Wed, 24 Apr 2024 19:41:34 GMT  
		Size: 66.6 KB (66564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8ac211f89ba3fc2f98c74bf5ca9f06f2b84fd4526df1b6e01e18394a353264`  
		Last Modified: Wed, 24 Apr 2024 19:41:33 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0479e7eafab8eaaebe4926c0dcd053e9497477bff49ac19e5b46a6f3e045c4bb`  
		Last Modified: Wed, 24 Apr 2024 19:41:54 GMT  
		Size: 201.1 MB (201147784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d22bf8763a458a52d06e86bdaa2170e7313fc665275f37888e62179f1c1e013`  
		Last Modified: Wed, 24 Apr 2024 19:41:35 GMT  
		Size: 3.8 MB (3814158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ea3847671abc6f9250d07df20c6b2f93c7a518850b80a7988412c3de7aa4cf`  
		Last Modified: Wed, 24 Apr 2024 19:41:33 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
