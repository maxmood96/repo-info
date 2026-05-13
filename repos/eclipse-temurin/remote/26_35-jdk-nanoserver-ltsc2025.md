## `eclipse-temurin:26_35-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:a917dae73d2b2ff891660c0734581a5ee5d594ed3e8d5fc6c7da9a3789dadbb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `eclipse-temurin:26_35-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull eclipse-temurin@sha256:87f1ebd994fa89627fa27b42a621dde1a35b33cd8ee0c1eda1fbf1a24aa9c385
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.2 MB (341243876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3ce8b1afeeae28f778288a354b2f0a375334168d13626b8598f9cf8123f9c6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 May 2026 09:46:02 GMT
RUN Apply image 10.0.26100.32860
# Wed, 13 May 2026 00:29:43 GMT
SHELL [cmd /s /c]
# Wed, 13 May 2026 00:29:44 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 13 May 2026 00:29:44 GMT
ENV JAVA_HOME=C:\openjdk-26
# Wed, 13 May 2026 00:29:44 GMT
USER ContainerAdministrator
# Wed, 13 May 2026 00:29:46 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 May 2026 00:29:47 GMT
USER ContainerUser
# Wed, 13 May 2026 00:29:59 GMT
COPY dir:8f93d89558d485d03b81034182d43f2557754598b0731c760b32ca0af365b3c1 in C:\openjdk-26 
# Wed, 13 May 2026 00:30:04 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 May 2026 00:30:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:34ab6476d71f2d23d05a00ac439000ba4c19d17e5c66f15efbe329ed79bba2bf`  
		Last Modified: Tue, 12 May 2026 22:29:47 GMT  
		Size: 199.7 MB (199739001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed3151c47bcf72364a859dc86a2f8d056f4668b6c5f9fb296e9db2bbdf0e0343`  
		Last Modified: Wed, 13 May 2026 00:30:11 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e3cf506693a0290fa83e55c72f1ce3d3db23b9e774c9e06b0f1b2af846eab7`  
		Last Modified: Wed, 13 May 2026 00:30:11 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cfd7419c5cb7d481fc6d5bea583df415f515721fba23eb43f5b17217a3ef08a`  
		Last Modified: Wed, 13 May 2026 00:30:10 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755766846b7c2f71724da1521360d80505a420383cd77d8a0ae16a0927017435`  
		Last Modified: Wed, 13 May 2026 00:30:10 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6677883dd862922fe26514a7668ecfdb95be52f404ef9ade8e6d1a03e17475e8`  
		Last Modified: Wed, 13 May 2026 00:30:09 GMT  
		Size: 72.3 KB (72336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c2c319a8e85d97c678ac4401acbe06d034721df716a465b5f984db44f88ebf`  
		Last Modified: Wed, 13 May 2026 00:30:09 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d46aea7f25f201d8a56d479548c598e0cfc96845f79928a5d5bacefa4e948a47`  
		Last Modified: Wed, 13 May 2026 00:30:22 GMT  
		Size: 141.3 MB (141306917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bdd376a0aa948082ac5a858032f1d7dbacfb10b39f5e9759a0263700a5130e4`  
		Last Modified: Wed, 13 May 2026 00:30:09 GMT  
		Size: 119.3 KB (119269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20632ecd3efed12a62fc979a88d90c456b4ae5362837108c6cf1f844d46abb0`  
		Last Modified: Wed, 13 May 2026 00:30:09 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
