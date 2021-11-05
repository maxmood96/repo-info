## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:ea7af88bd0b6ff45d36fc4906f8fb37d2cdda287a090f9c0c10a40623a9b4953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.288; amd64
	-	windows version 10.0.17763.2237; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.20348.288; amd64

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

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.17763.2237; amd64

```console
$ docker pull eclipse-temurin@sha256:f449b75b5fde0075b88c847dd2e042283736ce7b4a681d990c6f554292e5662d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145533834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080372085ef6d370cd802b13fd52721e1b021c95daba003080ceea7e09cb428c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 Oct 2021 08:01:14 GMT
RUN Apply image 1809-amd64
# Wed, 13 Oct 2021 18:17:55 GMT
SHELL [cmd /s /c]
# Tue, 26 Oct 2021 22:20:29 GMT
ENV JAVA_VERSION=jdk-11.0.13+8
# Tue, 26 Oct 2021 22:20:29 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 26 Oct 2021 22:20:30 GMT
USER ContainerAdministrator
# Tue, 26 Oct 2021 22:20:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 26 Oct 2021 22:20:49 GMT
USER ContainerUser
# Fri, 05 Nov 2021 19:31:35 GMT
COPY dir:6031cfac1e4bd8de6c5533bea0aabc25715779d854db7f41b8aea3e1449ff0bf in C:\openjdk-11 
# Fri, 05 Nov 2021 19:31:46 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:934e212983f208dc2bebc5de38259a6a62f1761868aacfee2cb3585a13b1e24b`  
		Size: 102.7 MB (102661372 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ceff24c3c0c2c360cd3788fcde5c41e1d6601339f4944623c732558a6030e631`  
		Last Modified: Wed, 13 Oct 2021 19:12:58 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72bf1d9a4ed65dc7c2d297d6accf2237e8d3c392264abe115ab738f7512fb675`  
		Last Modified: Wed, 27 Oct 2021 00:28:30 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d9ef8bb608957f2fa7a69ec5d555c99c76274b51e4a845469299710efbdf220`  
		Last Modified: Wed, 27 Oct 2021 00:28:30 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3260f5c3d01a05e2e0dbeb33f59ce0545312759c50bdd0cf6976915ce9e3262`  
		Last Modified: Wed, 27 Oct 2021 00:28:30 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b17e2ad1c0a4e9019931b781569d9c7ed7587c0235de93c303788d0c9f51537a`  
		Last Modified: Wed, 27 Oct 2021 00:28:28 GMT  
		Size: 70.0 KB (70026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20fde5701368c93a648331a822d4f92e37b8a08a1c4f1d4eabc9a1dfca7593da`  
		Last Modified: Wed, 27 Oct 2021 00:28:28 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ebe6622a755ff8111216701787b0156988af0aeac056241ca1c5dfa9675646`  
		Last Modified: Fri, 05 Nov 2021 20:29:03 GMT  
		Size: 42.7 MB (42715372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5071099d98c1e5dec823789c240fdc5e13bc021f8d85658f99ad33888fefa574`  
		Last Modified: Fri, 05 Nov 2021 20:28:55 GMT  
		Size: 81.4 KB (81403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
