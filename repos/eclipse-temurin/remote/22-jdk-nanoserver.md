## `eclipse-temurin:22-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:c2dbbd26ac6729d348f341a07998a3167dc990417d3789b58944e4b37589aa5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `eclipse-temurin:22-jdk-nanoserver` - windows version 10.0.20348.2461; amd64

```console
$ docker pull eclipse-temurin@sha256:b0bcc2520abc09cad4d742610302b3eef330bcf493cbb11565720ea18b450b8b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.6 MB (320615056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a18a88594325a0f6ea597c15e586016e4e756fc55976db5551d8dfe4a929c7d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 10 May 2024 20:16:48 GMT
RUN Apply image 10.0.20348.2461
# Wed, 15 May 2024 20:32:41 GMT
SHELL [cmd /s /c]
# Wed, 15 May 2024 20:38:17 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Wed, 15 May 2024 20:38:18 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 15 May 2024 20:38:18 GMT
USER ContainerAdministrator
# Wed, 15 May 2024 20:38:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 May 2024 20:38:30 GMT
USER ContainerUser
# Wed, 15 May 2024 20:38:44 GMT
COPY dir:b848142647370c7b57f8798114952350d05bf467cc96eb22cf5219409c8a4580 in C:\openjdk-22 
# Wed, 15 May 2024 20:39:00 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 15 May 2024 20:39:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:90b3a5622f8d62905d0a3029df4f91b934558ad375bef25c596214df31acac88`  
		Last Modified: Tue, 14 May 2024 17:22:15 GMT  
		Size: 120.4 MB (120425316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5560c76ac3d9aa2d8a6dbf79d443a7e1d170aae31c940cf791c9b532d5756a1`  
		Last Modified: Wed, 15 May 2024 20:58:04 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901805c453a3db5b81fbc5d7d76e019125a99325c46faa1f0b249503920c008b`  
		Last Modified: Wed, 15 May 2024 21:01:17 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f149c4c0118609d2025fd94d42ca722b9067880f610f3fdad29b66ef847ca824`  
		Last Modified: Wed, 15 May 2024 21:01:17 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc98af44c3d06c23e98453c26b8e25353d2f83fd7b96c7ae493040b1ec15b02a`  
		Last Modified: Wed, 15 May 2024 21:01:17 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced33bf6b165e04ab1f9b71b5848ed0c96e644eb880d246c00a7153fffb77d8c`  
		Last Modified: Wed, 15 May 2024 21:01:15 GMT  
		Size: 81.0 KB (80953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9e59eaac6374219cc1d44150b7730ae29db255a59201697a09fcfc13f25285`  
		Last Modified: Wed, 15 May 2024 21:01:15 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55195a33cf6f53826b68a83e734a7e093954e9ad7c18d6e746d912c2be50bd55`  
		Last Modified: Wed, 15 May 2024 21:01:34 GMT  
		Size: 200.0 MB (200044291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff3f1196f64894d74f8bf5c39c36a5fa47c01906cff476af43ce9aae2714a2e`  
		Last Modified: Wed, 15 May 2024 21:01:15 GMT  
		Size: 57.6 KB (57579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c244cfb9457c535a8555ef2a14422da881247e9183ea06faeac94f98c3127c`  
		Last Modified: Wed, 15 May 2024 21:01:15 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22-jdk-nanoserver` - windows version 10.0.17763.5820; amd64

```console
$ docker pull eclipse-temurin@sha256:9dd84c6efe9dc21c864e3eb3fa99c6228798da3951b27103cff80d9b2fba374b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.9 MB (358906992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc19198709ad5fd1e0744d037e2367248f4cd38ef336a20cc4e45491023ea7d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 19:42:01 GMT
SHELL [cmd /s /c]
# Wed, 15 May 2024 20:26:54 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Wed, 15 May 2024 20:26:54 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 15 May 2024 20:26:55 GMT
USER ContainerAdministrator
# Wed, 15 May 2024 20:27:03 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 May 2024 20:27:04 GMT
USER ContainerUser
# Wed, 15 May 2024 20:27:19 GMT
COPY dir:b848142647370c7b57f8798114952350d05bf467cc96eb22cf5219409c8a4580 in C:\openjdk-22 
# Wed, 15 May 2024 20:27:34 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 15 May 2024 20:27:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6a511fea8e874efc08e5058ac5b12b6433c36ba6570862a619dd80cfb0e190`  
		Last Modified: Wed, 15 May 2024 20:45:52 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669d46c5473324cf40984d096642388c0ff968a8d940fc95ba8e6b5b4baabe10`  
		Last Modified: Wed, 15 May 2024 20:56:36 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b2723b86f179c5ffe5e67735fdf7a007445eabb272f0e31ce2ec9af946d129`  
		Last Modified: Wed, 15 May 2024 20:56:36 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e755da26d8fee192ec9c229a40dab140f4b3f46e1a3a39cc05e5d79050118e`  
		Last Modified: Wed, 15 May 2024 20:56:36 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5375ef98ec8afff2597120d8b251c18263cb4910493f33e9016d112625c6d32`  
		Last Modified: Wed, 15 May 2024 20:56:34 GMT  
		Size: 68.1 KB (68063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6296c8ff1dec0ed54bb1085b1b67566eedee8ab41b9ad0233e993d3331e30ce0`  
		Last Modified: Wed, 15 May 2024 20:56:34 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6022716739c008823d65016d00662e68043d741123ea0610ffb2ffc8caa7ed6b`  
		Last Modified: Wed, 15 May 2024 20:56:54 GMT  
		Size: 200.1 MB (200055804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:985011d04fc8bf59b0aa216f97da1990c62681168114169ab855c3e75185bbe8`  
		Last Modified: Wed, 15 May 2024 20:56:35 GMT  
		Size: 3.8 MB (3834749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfb437e2f185efcf4f2bba15a77965d867f2ec70e0fca25451820e7e7802b01`  
		Last Modified: Wed, 15 May 2024 20:56:34 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
