## `eclipse-temurin:21-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:41f75526c8e5e01c38c28b15aca163950d3f8cf3dd490e699eab48cf91b094c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.20348.2402; amd64

```console
$ docker pull eclipse-temurin@sha256:17bce438bcbf6ac016e1e2ca608eb81a97dbcd4cbb1fe7f5cc3fcd7f3febda77
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.9 MB (169901054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8387061a85c600f8f8089fbda3d86011ad26754fb83a08be0da86c4eebbda071`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Wed, 24 Apr 2024 19:27:59 GMT
COPY dir:30866ffc44919960ba2d43fceab02c0cbcad12e73e3b28316799617dca9a13d0 in C:\openjdk-21 
# Wed, 24 Apr 2024 19:28:12 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:d88bca1aef1135522eb9e6046666b34d31f7e8f824a5015fab88ef325b0f9e3e`  
		Last Modified: Wed, 24 Apr 2024 19:48:59 GMT  
		Size: 48.8 MB (48757469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fde9699b744fcd7fe84be0c9b4f6daa5c7faa8e149f0d8af735e1fc1bf0a6a`  
		Last Modified: Wed, 24 Apr 2024 19:48:50 GMT  
		Size: 64.8 KB (64814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.17763.5696; amd64

```console
$ docker pull eclipse-temurin@sha256:bbafba9eae6b3b698bee10bec184122c37bd3e5b68e3b0f8066a73c0c54cfc30
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157079184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65c84a914a08012075abdc6bc0b5d21980dcac985fced7380a0beeed99ba234`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Wed, 24 Apr 2024 19:10:47 GMT
COPY dir:30866ffc44919960ba2d43fceab02c0cbcad12e73e3b28316799617dca9a13d0 in C:\openjdk-21 
# Wed, 24 Apr 2024 19:10:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:4665deef0832d476d0f11d63fa78ed0128f34b1f7c502ccec9d6c24624b91cdc`  
		Last Modified: Wed, 24 Apr 2024 19:43:00 GMT  
		Size: 48.8 MB (48757297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0495d030ef4498951eb142c844e5af716c65ab9cfc53a83a64fff1016187b6e1`  
		Last Modified: Wed, 24 Apr 2024 19:42:51 GMT  
		Size: 3.4 MB (3360792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
