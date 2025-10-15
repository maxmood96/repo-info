## `eclipse-temurin:8-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:af5a1be72f13039146682dd6f47d39b5801d63180248609d2cefc2626971d609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6899; amd64
	-	windows version 10.0.20348.4294; amd64

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.26100.6899; amd64

```console
$ docker pull eclipse-temurin@sha256:95372bb8be17076cba897759cd278881ffc2e5da086b54455b928cbf055e1af0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.7 MB (234733709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:133614349150da5bf997c0495d93780b15172b5b1871221a468886c95f53d81d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 11 Oct 2025 15:58:41 GMT
RUN Apply image 10.0.26100.6899
# Tue, 14 Oct 2025 21:13:10 GMT
SHELL [cmd /s /c]
# Tue, 14 Oct 2025 21:13:10 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Tue, 14 Oct 2025 21:13:11 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 14 Oct 2025 21:13:11 GMT
USER ContainerAdministrator
# Tue, 14 Oct 2025 21:13:16 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Oct 2025 21:13:16 GMT
USER ContainerUser
# Tue, 14 Oct 2025 21:13:20 GMT
COPY dir:dae5853f4b111011cf1e21d00736b413be35f27636dbbe76d1c13e33a12f455a in C:\openjdk-8 
# Tue, 14 Oct 2025 21:13:23 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:463edd10ad50b00cf92c69fc3eaa85e1fa40aad1b7938fa232899405bd80f001`  
		Last Modified: Tue, 14 Oct 2025 22:41:48 GMT  
		Size: 194.0 MB (194026741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd64bb809ff21416f04109f1cf7efdec601e1aeb0d4aa580654b82ead42caa4`  
		Last Modified: Tue, 14 Oct 2025 21:14:10 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbd35a8cfbf8c5d58b86880e516d9009eec3a004db3b4ce4c272c8a9b808c4e`  
		Last Modified: Tue, 14 Oct 2025 21:14:10 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0178faae325a270e4e1df8817264c5e665e9b14c646506654bdc40b97f3a40c0`  
		Last Modified: Tue, 14 Oct 2025 21:14:10 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e1f8536eeddc383f5a980725daf0ce4e4ca80a4e8be582f5e6d5a68ab2e6b4`  
		Last Modified: Tue, 14 Oct 2025 21:14:10 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1008530aaa73eacc3f4e9b68827c75f20060edb447d87f0199df52635423fc23`  
		Last Modified: Tue, 14 Oct 2025 21:14:10 GMT  
		Size: 69.9 KB (69875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effb9c57e65be9d516ecdd800ee5a1faaa8eb15bd8a5660d86d0da7db252f0f7`  
		Last Modified: Tue, 14 Oct 2025 21:14:10 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea35a1b209f44c79879e1fc40e46955077bc718bdac9446cb4a263cb8e5af335`  
		Last Modified: Tue, 14 Oct 2025 21:14:14 GMT  
		Size: 40.5 MB (40547980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b1c66ce4a867d551475b2abcb6235723e1e0718f026af159ddba3d3fe643d5`  
		Last Modified: Tue, 14 Oct 2025 21:14:10 GMT  
		Size: 83.8 KB (83777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.20348.4294; amd64

```console
$ docker pull eclipse-temurin@sha256:65b406b7c14e78c5659d7de210f3ae10e49a0aecc441ce25ef5a8a11eab98401
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163421527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c92203c74eec048d23712029304f3aefcc333617b720dc00b4cb2c601d47960`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Oct 2025 07:34:08 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 21:12:23 GMT
SHELL [cmd /s /c]
# Tue, 14 Oct 2025 21:12:23 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Tue, 14 Oct 2025 21:12:23 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 14 Oct 2025 21:12:24 GMT
USER ContainerAdministrator
# Tue, 14 Oct 2025 21:12:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Oct 2025 21:12:26 GMT
USER ContainerUser
# Tue, 14 Oct 2025 21:12:30 GMT
COPY dir:dae5853f4b111011cf1e21d00736b413be35f27636dbbe76d1c13e33a12f455a in C:\openjdk-8 
# Tue, 14 Oct 2025 21:12:33 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:f68a3bbf3ee20b515c5b8b801e5627a9dac3782ef264e37060c34ed80e5d8874`  
		Last Modified: Tue, 14 Oct 2025 20:41:53 GMT  
		Size: 122.7 MB (122688886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c23b710b333987aafcdf1771380232af85431ac0f5fff7fe41a912c36003916`  
		Last Modified: Tue, 14 Oct 2025 21:13:11 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e56e640aac29b8b6dbe1688b9aa15d245666f9c8f597771bdd6ddad3877656a`  
		Last Modified: Tue, 14 Oct 2025 21:13:11 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6afa03639d49e5833427766f783e77113974fd68c657fb19b893f216000cc8`  
		Last Modified: Tue, 14 Oct 2025 21:13:11 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343521c5e978febc419ef3e221d1502daf17b924c9a8bea9dd47755ec2e9bd21`  
		Last Modified: Tue, 14 Oct 2025 21:13:11 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed8995588531b693c2e1700be6d68944b833ddb4df5a4fc2d2dcda6e1b28f43`  
		Last Modified: Tue, 14 Oct 2025 21:13:11 GMT  
		Size: 83.9 KB (83915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1e2bd354b422c0510eecd36c8f8a57a50b338ef6f0bc072ccb22cfbfd71991`  
		Last Modified: Tue, 14 Oct 2025 21:13:11 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74068a5efc6a087573800aa26668e2ff18127d75fb010944059c81fb25871860`  
		Last Modified: Tue, 14 Oct 2025 21:13:15 GMT  
		Size: 40.5 MB (40548195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7aa13790f1b8e62885a5da4cf29339273c09e30315fa778fe14fbf43b3c79a`  
		Last Modified: Tue, 14 Oct 2025 21:13:11 GMT  
		Size: 95.2 KB (95235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
