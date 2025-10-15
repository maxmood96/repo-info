## `eclipse-temurin:8-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:d056b663e127389bab3da2507168b2c1b7158a0c99197e57755e560c15166ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6899; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2025` - windows version 10.0.26100.6899; amd64

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
