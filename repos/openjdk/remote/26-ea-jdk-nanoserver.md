## `openjdk:26-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:47f0f170c74d2621a0f537db9e279921e56cf2abbc28651e3e347e4455f07300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `openjdk:26-ea-jdk-nanoserver` - windows version 10.0.26100.7171; amd64

```console
$ docker pull openjdk@sha256:a929f4f8a23182e2081394a925c774d62a11515c96fbe11fb72157aed81223b1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.1 MB (423144467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fadfa39fe8b013cee9d5a1b7c21e6dd4ff630f91637e5c121cda9a1e1a434cf2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 09 Nov 2025 10:04:50 GMT
RUN Apply image 10.0.26100.7171
# Tue, 02 Dec 2025 02:17:11 GMT
SHELL [cmd /s /c]
# Tue, 02 Dec 2025 02:17:12 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 02 Dec 2025 02:17:13 GMT
USER ContainerAdministrator
# Tue, 02 Dec 2025 02:17:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 02 Dec 2025 02:17:26 GMT
USER ContainerUser
# Tue, 02 Dec 2025 02:17:26 GMT
ENV JAVA_VERSION=26-ea+26
# Tue, 02 Dec 2025 02:18:22 GMT
COPY dir:af429b7e2d5dac7004e75510486adbb236437e3b8445f2d868ed1c16921e40c5 in C:\openjdk-26 
# Tue, 02 Dec 2025 02:18:31 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 02 Dec 2025 02:18:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:87c91227213eb6e7c8cfe33b6bd0429350e524756878f37f3860b013f804bf59`  
		Last Modified: Tue, 11 Nov 2025 20:41:49 GMT  
		Size: 197.9 MB (197936447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9c42dc6bd6cf6d0b1831d7e233e0904ce0b44c83daf5c0473d1984555ff6dd`  
		Last Modified: Tue, 02 Dec 2025 02:19:02 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50b931a9027207ef8b6801f89ce5ad118219f392a3172509e1df6acfa99bc9c`  
		Last Modified: Tue, 02 Dec 2025 02:19:06 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e35998e1fb76d1b7dd15f7ecfe3ef0f9f73b666cc1a71e3a505193398ab4cc`  
		Last Modified: Tue, 02 Dec 2025 02:19:02 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09e8c584df6d13ca99c351d02f49a54f30920528d33ba4ce77b22a8a0f4f78a`  
		Last Modified: Tue, 02 Dec 2025 02:19:02 GMT  
		Size: 71.0 KB (70994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b21ac62e07012a0de91208a7c49a97acb6e4fd8f47a9addb4f2c5d04c202a56`  
		Last Modified: Tue, 02 Dec 2025 02:19:02 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7089158482ad16419fff0bd48fc094ac16acaca438540eb66a70e9a180b51f`  
		Last Modified: Tue, 02 Dec 2025 02:19:02 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f9925afa1bdb4d51a23ce463066c191a7be56fb945e96e979c0b48ea759288`  
		Last Modified: Tue, 02 Dec 2025 04:24:23 GMT  
		Size: 225.0 MB (225028174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e39f841cab6613c4811924ea703e101e857e7583bdb38805ce22eaba5b98ee6`  
		Last Modified: Tue, 02 Dec 2025 02:19:02 GMT  
		Size: 102.5 KB (102451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3917e41fdd7b0473075bf7f4575dbef2d0c46ec754dd1c90f3f16aadf0d4e5b4`  
		Last Modified: Tue, 02 Dec 2025 02:19:02 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-ea-jdk-nanoserver` - windows version 10.0.20348.4405; amd64

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
