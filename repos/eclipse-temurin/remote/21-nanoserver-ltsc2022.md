## `eclipse-temurin:21-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:cb59a28b32f775d3bc877332fe4f7e1e68faac60bef0159cd9f19d1cd5e9e982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `eclipse-temurin:21-nanoserver-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull eclipse-temurin@sha256:97fb53e30cd32fd4ddf7db5e03ac0c9ce2c52e18469534ace50765d4304e2081
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.4 MB (323370312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbfa5dd2f43610c65f0d23926c32b5dfdbabc9783099fe93205f64afd9007892`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 02 Nov 2024 23:34:35 GMT
RUN Apply image 10.0.20348.2849
# Thu, 14 Nov 2024 21:24:45 GMT
SHELL [cmd /s /c]
# Thu, 14 Nov 2024 21:24:46 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Thu, 14 Nov 2024 21:24:47 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 14 Nov 2024 21:24:47 GMT
USER ContainerAdministrator
# Thu, 14 Nov 2024 21:24:50 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 14 Nov 2024 21:24:50 GMT
USER ContainerUser
# Thu, 14 Nov 2024 21:24:58 GMT
COPY dir:cc909cc6d9328a16dd1468618a073abc368d41e200a32534756819e3433a0b04 in C:\openjdk-21 
# Thu, 14 Nov 2024 21:25:03 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 14 Nov 2024 21:25:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:815d6b7f925aef8327c34c34073ae54cc1c82120f1058682eac4c8c14ca21c70`  
		Last Modified: Tue, 12 Nov 2024 22:44:32 GMT  
		Size: 120.6 MB (120604951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afb90ba9407f8b87f2260dcb5650426525072f54bb05c67be3b1fd5b7eee4e4`  
		Last Modified: Thu, 14 Nov 2024 21:25:07 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb727bc1ec27372d7c01b0a49c571bf9b8a907e1f8e71f07a8d477a88f232ef`  
		Last Modified: Thu, 14 Nov 2024 21:25:07 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b178e1062cc579fff440caadf92699382be998ee76767d877d785f82f3277e1a`  
		Last Modified: Thu, 14 Nov 2024 21:25:07 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7025ba2a14978d7805267371d982e1d3f84fb7e1190c71ee8139a2c6bb38cb`  
		Last Modified: Thu, 14 Nov 2024 21:25:07 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe5606e7fcad8778d0111d52b5919442a3c9fe438fb9588b1d4218fc1886e0f5`  
		Last Modified: Thu, 14 Nov 2024 21:25:06 GMT  
		Size: 76.7 KB (76735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ba8be1fa44986acf1776acc19d425da64872989d10d5d8f0a53021597f30dd`  
		Last Modified: Thu, 14 Nov 2024 21:25:06 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157d799e41f4d433b5db0adde1d502b57e208e90711330fed8e9e2f8229393b2`  
		Last Modified: Thu, 14 Nov 2024 21:25:17 GMT  
		Size: 202.6 MB (202575495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64ff8957a125a3e1d02f4cd528ca43ae5472c5b10a8f0c53fc481b33a65e59d`  
		Last Modified: Thu, 14 Nov 2024 21:25:06 GMT  
		Size: 106.9 KB (106901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876b24f217b9925b7007977e8ff7e49a1b96711dfa167226e37bcd4959bfcd62`  
		Last Modified: Thu, 14 Nov 2024 21:25:06 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
