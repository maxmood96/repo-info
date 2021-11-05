## `eclipse-temurin:11-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:fcefbc338f249b08aa687df92ac03e5edabb3f6fda5450d73271e21c9ef67f14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.288; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2022` - windows version 10.0.20348.288; amd64

```console
$ docker pull eclipse-temurin@sha256:d9840dbcce5a19ed76d9b362b611104314b4bf7280aaa1a981e566970806c71f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159799697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa2c3ce3df75e2c7737912f5f3231a74ad6e36f74e7d3b2708e336f43e97f6ad`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 Oct 2021 11:15:04 GMT
RUN Apply image ltsc2022-amd64
# Wed, 13 Oct 2021 19:02:30 GMT
SHELL [cmd /s /c]
# Tue, 26 Oct 2021 22:27:04 GMT
ENV JAVA_VERSION=jdk-11.0.13+8
# Tue, 26 Oct 2021 22:27:05 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 26 Oct 2021 22:27:05 GMT
USER ContainerAdministrator
# Tue, 26 Oct 2021 22:27:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 26 Oct 2021 22:27:27 GMT
USER ContainerUser
# Fri, 05 Nov 2021 19:44:33 GMT
COPY dir:6031cfac1e4bd8de6c5533bea0aabc25715779d854db7f41b8aea3e1449ff0bf in C:\openjdk-11 
# Fri, 05 Nov 2021 19:44:46 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:91284e7e8fd4bd7ebcfa98544a3e4f59639f38281225c81c34b6fe22e0dba4e5`  
		Size: 116.9 MB (116939483 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ba797e8f93823c3d71c52fcae413f3a33ca28ff2711c09ba5141432948f8298`  
		Last Modified: Wed, 13 Oct 2021 19:43:54 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5496de008b770ec467d4156c4492e726ea95aacc468ead67297672335d946c3d`  
		Last Modified: Wed, 27 Oct 2021 00:33:04 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966e7576b2e9bf1bda4b03bc28938ca36d1725bc17494b2c11d6670d064a2551`  
		Last Modified: Wed, 27 Oct 2021 00:33:04 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb6df87291b64e881c924fa31b55558489e0aef315ac3bea896b2a6526894c8`  
		Last Modified: Wed, 27 Oct 2021 00:33:03 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ca23fc1aca87db648be45d76f6226d6a81ca9b6cfcbdc090eb82647b04b378`  
		Last Modified: Wed, 27 Oct 2021 00:33:01 GMT  
		Size: 79.8 KB (79756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71abbdb585b9b63c845550e8557957f5341227a10b425691575a040558888733`  
		Last Modified: Wed, 27 Oct 2021 00:33:01 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cafcc192548dc3eb24229726db7f251f518725dc5b19879f36e5ec43e23836b`  
		Last Modified: Fri, 05 Nov 2021 20:40:02 GMT  
		Size: 42.7 MB (42712861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40948583839a5c18f15e55ebe519cc7e1829daa61baac387497d54065adffc00`  
		Last Modified: Fri, 05 Nov 2021 20:39:54 GMT  
		Size: 61.8 KB (61805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
