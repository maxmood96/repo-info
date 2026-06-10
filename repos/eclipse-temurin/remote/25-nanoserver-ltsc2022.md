## `eclipse-temurin:25-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:e1f39b0349388c37c47f9b1be9732202a4d2f6304e2dff04cfaed05921a8402e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `eclipse-temurin:25-nanoserver-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull eclipse-temurin@sha256:05875f4a7700e250e44f59b979a1340e01067e11bd3fd543095f9bc04b099531
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.2 MB (262242047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c6f0e5bd34f8437152474147fceff76001a4c1558629ea8eaf686738207146`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Tue, 09 Jun 2026 23:20:28 GMT
SHELL [cmd /s /c]
# Tue, 09 Jun 2026 23:22:18 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 09 Jun 2026 23:22:19 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 09 Jun 2026 23:22:20 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2026 23:22:22 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Jun 2026 23:22:22 GMT
USER ContainerUser
# Tue, 09 Jun 2026 23:22:52 GMT
COPY dir:93c9a33f6e3b7bf9a4cc6584352427179a8f4d1e9396155b43179dd1c4270396 in C:\openjdk-25 
# Tue, 09 Jun 2026 23:22:57 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 09 Jun 2026 23:22:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c10a1597ccfac50e0bee5f1f86b66638570a85b10d64ac0590eb5ce44dac1bf`  
		Last Modified: Tue, 09 Jun 2026 23:21:15 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7519050860fcc3c968f77908994d211c57ba04d9c6d5a68feb58575665c6d152`  
		Last Modified: Tue, 09 Jun 2026 23:23:03 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4bff087e91a0865ade8e84c296496469367f8bc0485328f128a2e0eb80353ba`  
		Last Modified: Tue, 09 Jun 2026 23:23:03 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7342d8b85e778e661de4ca621ba25c3a91e9b069f27421b22e580588ba946056`  
		Last Modified: Tue, 09 Jun 2026 23:23:03 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e85c07d3c0b5ebe2149305f4b4d83a9c57df31d208d4d13e653cf3bcc2b229`  
		Last Modified: Tue, 09 Jun 2026 23:23:01 GMT  
		Size: 87.5 KB (87520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2561170de0229b15f375dc1d32bdb3d16c5efa4e2205c8e2b4df6543668e8a6`  
		Last Modified: Tue, 09 Jun 2026 23:23:01 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c983da7856ee20b18a72f4c098d88a72feba621acbc3896593a4484816871d3d`  
		Last Modified: Tue, 09 Jun 2026 23:23:14 GMT  
		Size: 138.0 MB (138009959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd20f8ee14398820232dea122c4af62e7c11970da968ec7635a7871122e57ce`  
		Last Modified: Tue, 09 Jun 2026 23:23:01 GMT  
		Size: 140.7 KB (140689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df374250ac6b08c693374a9e7f420f53d2b0e38f5db1de306acddb02f069da90`  
		Last Modified: Tue, 09 Jun 2026 23:23:01 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
