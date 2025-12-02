## `openjdk:26-ea-26-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:78c712cebc3225e5a35355dcb5fac186e190f67a5d5a50ffd4f7d469aed40f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `openjdk:26-ea-26-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull openjdk@sha256:a88b4063b1f63daa8c5f84a4574a3f3e4bb8b29ba66de57538f9b8351d385314
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.6 MB (351578375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2d102cfd3a95087c13504a5e1790e3b0db2bb18ca063e10a06aaa4766f08af`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 02 Dec 2025 02:17:50 GMT
SHELL [cmd /s /c]
# Tue, 02 Dec 2025 02:17:51 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 02 Dec 2025 02:17:52 GMT
USER ContainerAdministrator
# Tue, 02 Dec 2025 02:18:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 02 Dec 2025 02:18:05 GMT
USER ContainerUser
# Tue, 02 Dec 2025 02:18:06 GMT
ENV JAVA_VERSION=26-ea+26
# Tue, 02 Dec 2025 02:19:06 GMT
COPY dir:af429b7e2d5dac7004e75510486adbb236437e3b8445f2d868ed1c16921e40c5 in C:\openjdk-26 
# Tue, 02 Dec 2025 02:19:14 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 02 Dec 2025 02:19:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caae71d6646d7df04678f56548bf76328718711f9964057f8e758f08d54fb7cf`  
		Last Modified: Tue, 02 Dec 2025 02:19:41 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ce64bfcb5d573929e71b8ded990f28d087845f83050e82bb67ace9ae03fb33`  
		Last Modified: Tue, 02 Dec 2025 02:19:41 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574174fb59fe79551ec62ddd22c5b5f8e7234e55a415b19a3c96e005e9d9a8f9`  
		Last Modified: Tue, 02 Dec 2025 02:19:41 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3843b65af1a047ed65c6192f9d2d7f3bb0aebf9379535a7443155a5329293cd`  
		Last Modified: Tue, 02 Dec 2025 02:19:41 GMT  
		Size: 82.8 KB (82773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:515c94ff26d6ab89259b54a1443711721bb15a0962465e4a263e8bef8698fbc9`  
		Last Modified: Tue, 02 Dec 2025 02:19:41 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0416203ed3d1dfbb960c2ed64d0ac3efe4515b48504eae9244d64fe868265c12`  
		Last Modified: Tue, 02 Dec 2025 02:19:41 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1bb0b187da7cf85e1b9f0385cb928b870c21338c46e58963acd21df6e43318`  
		Last Modified: Tue, 02 Dec 2025 04:24:17 GMT  
		Size: 225.0 MB (225028012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:667e70438e688c67a345ea53f21382509ab2260fe99830cf3b9fcc04da2269d5`  
		Last Modified: Tue, 02 Dec 2025 02:19:42 GMT  
		Size: 112.1 KB (112137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7474adc0d15e0800da486925c37889e5f50180d2f54bc45c2dce95e125e30e36`  
		Last Modified: Tue, 02 Dec 2025 02:19:41 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
