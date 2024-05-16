## `eclipse-temurin:22-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:8d30bfaf2f736456bf1dba576d4a171685a918aebe93bfd57e7744826eab18f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `eclipse-temurin:22-jdk-nanoserver-1809` - windows version 10.0.17763.5820; amd64

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
