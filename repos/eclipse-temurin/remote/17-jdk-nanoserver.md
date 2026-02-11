## `eclipse-temurin:17-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:98a3d155c593152b1e7502dc7e3a6ba1b877da07eb8160d3c1b78752f3e12f2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32370; amd64
	-	windows version 10.0.20348.4773; amd64

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.26100.32370; amd64

```console
$ docker pull eclipse-temurin@sha256:fe0f2f5e657a96f81d94bae9798c01eb3d1f47193951713414bba05fc1ab0d2b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.9 MB (386920060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1348a9eca6c6ab2ce41c15c303cf5eac949d147d12987f3c216d90dcd3d6a24a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 22:06:41 GMT
RUN Apply image 10.0.26100.32370
# Tue, 10 Feb 2026 23:36:49 GMT
SHELL [cmd /s /c]
# Tue, 10 Feb 2026 23:36:50 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 10 Feb 2026 23:36:50 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 10 Feb 2026 23:36:51 GMT
USER ContainerAdministrator
# Tue, 10 Feb 2026 23:36:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Feb 2026 23:36:57 GMT
USER ContainerUser
# Tue, 10 Feb 2026 23:37:10 GMT
COPY dir:fb23a79434a3e7defa51a1bec1a7ef896ff849f7ba85f2629e1913957db57a2e in C:\openjdk-17 
# Tue, 10 Feb 2026 23:37:16 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 10 Feb 2026 23:37:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:77321bd03612cfa46920e790ae0c3b142758a5803ad759fdb406c98b6f2e4ed0`  
		Last Modified: Tue, 10 Feb 2026 22:50:26 GMT  
		Size: 199.3 MB (199251619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963da222bcfdb7ba90fdd4e0ef552017e7e7e8adf20cdb903e92e6d1d0aae61d`  
		Last Modified: Tue, 10 Feb 2026 23:37:22 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a80edc74780aa4ee9808047742ed62343967375ede7458c73a7584af39f6be`  
		Last Modified: Tue, 10 Feb 2026 23:37:22 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06e5c97b4cc9cb0e083ab30207fc8d8b2be9c68cfc7c289bc13c313e3314f09`  
		Last Modified: Tue, 10 Feb 2026 23:37:22 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fae35040674050cff4ee253854cc8a8f065f350482a0206eeb1c7c554ae5e6`  
		Last Modified: Tue, 10 Feb 2026 23:37:22 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0f5997bee577766ce82342e8dfb45a960c458a2cefe01537d15d0ec705ca71`  
		Last Modified: Tue, 10 Feb 2026 23:37:20 GMT  
		Size: 70.7 KB (70682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c43d89b52d42ad5f1ce86d121803f6cceff8038d1828e27443866644ea7f196`  
		Last Modified: Tue, 10 Feb 2026 23:37:20 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63924b24279c4fc550de91566dd8e1f26488d49a5657cfaf513ce594023a7713`  
		Last Modified: Tue, 10 Feb 2026 23:37:33 GMT  
		Size: 187.5 MB (187487450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4403cf9ec5f51e82ebfe058ef83135c012007eaa5741fae2a0e576d7d1639be`  
		Last Modified: Tue, 10 Feb 2026 23:37:20 GMT  
		Size: 103.8 KB (103849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d6c5b61f049f0d4da55ae8713ab4d3195a1ed6b9b2cc87af44b4932e4bca28`  
		Last Modified: Tue, 10 Feb 2026 23:37:20 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.20348.4773; amd64

```console
$ docker pull eclipse-temurin@sha256:f166a2a39d6db8d94c2d371991c1fde4a1f39ba561ff41af19ba6d8ee43626e2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314336650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a4bbb6403ba514bc302a17d451c117478a16a5f6d1cf75a697cea3fc3dbc5f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Tue, 10 Feb 2026 23:30:56 GMT
SHELL [cmd /s /c]
# Tue, 10 Feb 2026 23:30:57 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 10 Feb 2026 23:30:57 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 10 Feb 2026 23:30:58 GMT
USER ContainerAdministrator
# Tue, 10 Feb 2026 23:31:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Feb 2026 23:31:00 GMT
USER ContainerUser
# Tue, 10 Feb 2026 23:31:08 GMT
COPY dir:fb23a79434a3e7defa51a1bec1a7ef896ff849f7ba85f2629e1913957db57a2e in C:\openjdk-17 
# Tue, 10 Feb 2026 23:31:12 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 10 Feb 2026 23:31:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b005c26b3eb53f2a73969b3045aa2b8dfbd47327ae7840b25c73a4df0798a9`  
		Last Modified: Tue, 10 Feb 2026 23:31:19 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283fc896b5852fb4d57e90839e54314d16c9d1fd026fdea56d9f39269dec1b7e`  
		Last Modified: Tue, 10 Feb 2026 23:31:18 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d680ea3b9b2f8c77f3be52d6691805c5b13381df085565f0e75d4782f730657`  
		Last Modified: Tue, 10 Feb 2026 23:31:18 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d92bae2d731be2e34cda36ca42b0201e901172a5e661b5653e146a868970e1`  
		Last Modified: Tue, 10 Feb 2026 23:31:18 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efadadff715b53ed911df06d2017dc29e2474ae4b4b48e40dfd6e713deacbbcc`  
		Last Modified: Tue, 10 Feb 2026 23:31:17 GMT  
		Size: 77.4 KB (77381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfea66346a34e2b2231506c9aa24e7f0c0e46a857c8892c692a841d68cd2d10`  
		Last Modified: Tue, 10 Feb 2026 23:31:17 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009b2af3cd856165a295c3385dc422c95d89cdf0b442472cceaaab1eca0c6837`  
		Last Modified: Tue, 10 Feb 2026 23:31:29 GMT  
		Size: 187.5 MB (187486794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23809c1ed4f5806350689273478021e91c886dd004d7e46f40b28eb8f556d89`  
		Last Modified: Tue, 10 Feb 2026 23:31:17 GMT  
		Size: 120.2 KB (120210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5f3a36b99dd98364b6bbd4b15261c572f279acc73889fe7610aa3796263ea9`  
		Last Modified: Tue, 10 Feb 2026 23:31:17 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
