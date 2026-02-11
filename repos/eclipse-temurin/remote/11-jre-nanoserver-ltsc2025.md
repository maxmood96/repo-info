## `eclipse-temurin:11-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:039b9209f1a8e10d497e8f37fd3391273261a21af75892ac487d58548b2bbb4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull eclipse-temurin@sha256:18037257a958b7b8dd59b6252ff492c6391d3bd5816084dada4f9e5a034ff556
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243128822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd99c771f7824029b845dd1515f2003fdd5fbd31d728017c319d3f70f4f69ec1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 22:06:41 GMT
RUN Apply image 10.0.26100.32370
# Tue, 10 Feb 2026 23:36:23 GMT
SHELL [cmd /s /c]
# Tue, 10 Feb 2026 23:36:24 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 10 Feb 2026 23:36:24 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 10 Feb 2026 23:36:25 GMT
USER ContainerAdministrator
# Tue, 10 Feb 2026 23:36:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Feb 2026 23:36:30 GMT
USER ContainerUser
# Tue, 10 Feb 2026 23:36:37 GMT
COPY dir:9d7273a61bdbfae69a7bd32ee7f3a7621be43375d7aad513ad72640646f9a6e0 in C:\openjdk-11 
# Tue, 10 Feb 2026 23:36:40 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:77321bd03612cfa46920e790ae0c3b142758a5803ad759fdb406c98b6f2e4ed0`  
		Last Modified: Tue, 10 Feb 2026 22:50:26 GMT  
		Size: 199.3 MB (199251619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235d9628315965b68f4d378ddd929aeff0f5258c04acbaead21ad7d6b7979c7b`  
		Last Modified: Tue, 10 Feb 2026 23:36:46 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b929920623541cda31b00a74188f2bc02e0e7b0833b5e81b2d8cee0e635c873`  
		Last Modified: Tue, 10 Feb 2026 23:36:46 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b097153a4365c1e7ebab60d2057d386ff0cd6928db83ec35ece740106a4677`  
		Last Modified: Tue, 10 Feb 2026 23:36:46 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f599e7cbb8277bd500a40e6e5f307bcd13dcc46863f62255665375caa9d153`  
		Last Modified: Tue, 10 Feb 2026 23:36:44 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321f9023a0f535107da315c37bc2efa55fdebf7f210231b2150d636de29efc82`  
		Last Modified: Tue, 10 Feb 2026 23:36:44 GMT  
		Size: 69.0 KB (68975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e036f009642a4d7928d79a72eb1d84c4bbac1a7760d3023d90b07f1b4fb0244`  
		Last Modified: Tue, 10 Feb 2026 23:36:44 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6aa5480eda6201b789d813f86bbb648d3723570f4521513acd8bb8566860e3e`  
		Last Modified: Tue, 10 Feb 2026 23:36:49 GMT  
		Size: 43.7 MB (43718802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff7c5bef0dab8d700ea8ddce334f462ef10c2063c17418d462bea5530591a5b`  
		Last Modified: Tue, 10 Feb 2026 23:36:44 GMT  
		Size: 84.1 KB (84062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
