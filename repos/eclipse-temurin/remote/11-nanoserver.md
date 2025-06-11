## `eclipse-temurin:11-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:aa291727dcc0fc4ec2b92bdccb37570aafedc549f6a81ea7fba6ae57844f0b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `eclipse-temurin:11-nanoserver` - windows version 10.0.26100.4349; amd64

```console
$ docker pull eclipse-temurin@sha256:0107bfc553a3d7ae49ea605d42683482c93a08c93acfc76dbed07493b8b94154
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.9 MB (386856066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7601b22710fe2fb6f54ef9f2bf2fe4914a47675250f9ac6ed5afc998574fd6a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 07 Jun 2025 15:19:59 GMT
RUN Apply image 10.0.26100.4349
# Tue, 10 Jun 2025 22:14:33 GMT
SHELL [cmd /s /c]
# Tue, 10 Jun 2025 22:14:33 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Tue, 10 Jun 2025 22:14:34 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 10 Jun 2025 22:14:35 GMT
USER ContainerAdministrator
# Tue, 10 Jun 2025 22:14:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Jun 2025 22:14:38 GMT
USER ContainerUser
# Tue, 10 Jun 2025 22:14:45 GMT
COPY dir:c61af6ceef573b3d63f31a61f55e07ef4d3bfab78d8c06e63a667655942ae5e8 in C:\openjdk-11 
# Tue, 10 Jun 2025 22:14:52 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 10 Jun 2025 22:14:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:709fa8bff22087ae5c45c65a3b0777eb6ee12afd1b773aece2a322e84b66b1d1`  
		Last Modified: Tue, 10 Jun 2025 22:41:49 GMT  
		Size: 192.1 MB (192082516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213df7c36ce49724ba0780616db23dd587a4e2c61b647a3dfe1b6cec80ae661b`  
		Last Modified: Tue, 10 Jun 2025 22:15:35 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd9ac08a52689edf5f158f446d3e7b9dc9c26d7a9a765a5054fad4856d02e3e`  
		Last Modified: Tue, 10 Jun 2025 22:15:36 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da0e5d44a4f69ec51265ef946f9ad137e22fac4ab7e7e9101a19453d0ed6df60`  
		Last Modified: Tue, 10 Jun 2025 22:15:36 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71484381ae4d7d8a6935684902ce09ec7fddc8acaffd9c70e2cc5406e286aaf9`  
		Last Modified: Tue, 10 Jun 2025 22:15:36 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9437cec4c7dbb409db895e3ee5708da83cd7caafda95f7df0b0d5b074e686cc`  
		Last Modified: Tue, 10 Jun 2025 22:15:36 GMT  
		Size: 75.8 KB (75757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3ce2398c7e4c84b8356b068f61f8ee09e12f619c9dd5eea8330c758c2b4b48`  
		Last Modified: Tue, 10 Jun 2025 22:15:36 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5267e2ac960e49bd47993a10d4a3a7c2c77239e867c1b869117480d8797420`  
		Last Modified: Wed, 11 Jun 2025 00:13:05 GMT  
		Size: 194.6 MB (194577632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd5d3bfebaa28f37f8df6aa8c76d5106eb0ff2c6c8d8b360e070f7716631254`  
		Last Modified: Tue, 10 Jun 2025 22:15:37 GMT  
		Size: 113.9 KB (113908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01193902ebcbf564b0204ad6623926bb53a9d2b34c73e0cff671dab665d0491d`  
		Last Modified: Tue, 10 Jun 2025 22:15:37 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-nanoserver` - windows version 10.0.20348.3807; amd64

```console
$ docker pull eclipse-temurin@sha256:76cc32373fb0ebc0a3d4260386a286a73162a35a7c2bee4bd55f512aee55b585
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.3 MB (317310372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e1934b259c93599e3f33a791e74c66a6123b33f3e914083d88c0f1e1a98a87b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Tue, 10 Jun 2025 22:13:24 GMT
SHELL [cmd /s /c]
# Tue, 10 Jun 2025 22:13:24 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Tue, 10 Jun 2025 22:13:25 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 10 Jun 2025 22:13:26 GMT
USER ContainerAdministrator
# Tue, 10 Jun 2025 22:13:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Jun 2025 22:13:30 GMT
USER ContainerUser
# Tue, 10 Jun 2025 22:13:37 GMT
COPY dir:c61af6ceef573b3d63f31a61f55e07ef4d3bfab78d8c06e63a667655942ae5e8 in C:\openjdk-11 
# Tue, 10 Jun 2025 22:13:43 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 10 Jun 2025 22:13:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6e2da87273a18701b50679d0f33ab483e146c12d7b8b602deb54b9faec9205`  
		Last Modified: Tue, 10 Jun 2025 22:14:24 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9232c1390efc28b22b599aab39834419bd69d6448c4133e633692b92479f25f1`  
		Last Modified: Tue, 10 Jun 2025 22:14:24 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f757ffcb82a3e1886ca32a7db7fa5179a067d90a4cf291848d3cdd600f391a3`  
		Last Modified: Tue, 10 Jun 2025 22:14:24 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b2c0d6685be3ac5acab8d3be827a08d4cf6dfba2a591cab3dd7cd09b5f47dd`  
		Last Modified: Tue, 10 Jun 2025 22:14:24 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8407366a950d9ccd0074db3db0e9a9fbbe82ac5f056a8025cf034711fdb3e5bc`  
		Last Modified: Tue, 10 Jun 2025 22:14:24 GMT  
		Size: 78.3 KB (78297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ecfa4a3fe271e36115a1a56f3d94f910054e1281e5232e552cc300a6b31284`  
		Last Modified: Tue, 10 Jun 2025 22:14:25 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9487236b04ce9653240b580d03c89e61899ad3e3ad11cbbf32e032b7325e63`  
		Last Modified: Wed, 11 Jun 2025 00:12:59 GMT  
		Size: 194.6 MB (194577527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ab9ff3108cdc10737bc3b3ed255985d29420f4101cd9123cc9f20fbef4e7be`  
		Last Modified: Tue, 10 Jun 2025 22:14:25 GMT  
		Size: 107.8 KB (107813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b538d90469ac9ff0e282bee3ba35d2317d15ee00706dd727cb7b69296a1e8118`  
		Last Modified: Tue, 10 Jun 2025 22:14:25 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
