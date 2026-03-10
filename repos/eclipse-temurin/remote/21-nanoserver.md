## `eclipse-temurin:21-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:c2abf8f1a253714c764be2d20d02bfab4e35754beb775537d416978507ae0fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `eclipse-temurin:21-nanoserver` - windows version 10.0.26100.32522; amd64

```console
$ docker pull eclipse-temurin@sha256:b92b6890938cddc2f0a5f36443bf9bb57d3e86a452db4ceb8d04fc070f5b1e76
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.4 MB (401366875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d53699d75c14e483691957331bf9048db7d93eaceb2934637ae762d735ac394d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Mar 2026 01:45:55 GMT
RUN Apply image 10.0.26100.32522
# Tue, 10 Mar 2026 22:43:50 GMT
SHELL [cmd /s /c]
# Tue, 10 Mar 2026 22:43:51 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 10 Mar 2026 22:43:51 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 10 Mar 2026 22:43:51 GMT
USER ContainerAdministrator
# Tue, 10 Mar 2026 22:43:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Mar 2026 22:43:56 GMT
USER ContainerUser
# Tue, 10 Mar 2026 22:44:09 GMT
COPY dir:a00a0ee8f4ae82aa8e2b5d2b9cb5c2941887de3e7b021ae64d7924c257e6915c in C:\openjdk-21 
# Tue, 10 Mar 2026 22:44:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 10 Mar 2026 22:44:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:06fab7822816d5f43d6835d07ac8db280fdf81384187f36d8dc43bbb7064a76d`  
		Last Modified: Tue, 10 Mar 2026 20:41:46 GMT  
		Size: 199.4 MB (199409325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6d87bab6e260069d1fe1c1d3cd5eb1720b5a34cc400a2ac750504952ec42e8`  
		Last Modified: Tue, 10 Mar 2026 22:44:22 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca4e57d22aec4bd811cd9a2e58f6640f645455eb14f8698cbaa1dcde131bce4`  
		Last Modified: Tue, 10 Mar 2026 22:44:21 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ffb831303b6d83fefe074fa01bac9446d48f2206a7b408a78f4457f29f4341c`  
		Last Modified: Tue, 10 Mar 2026 22:44:21 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a202954ddf388bb83f7f5fcfa6f096140f158d130a3e33367cb525329e412d3a`  
		Last Modified: Tue, 10 Mar 2026 22:44:21 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04791807b8830dc289d9ceae650cf6e37851ce07349ef05be590034bf6a4143b`  
		Last Modified: Tue, 10 Mar 2026 22:44:20 GMT  
		Size: 83.3 KB (83260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f790666f9f2592bdc22e1720e5f53d22235d768e0fae7c2c90f1d46f24b301d8`  
		Last Modified: Tue, 10 Mar 2026 22:44:20 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ab85e8249dfa4ffda6cfdaeb6172ebc814433511a98f84deead7ffa5d34911`  
		Last Modified: Tue, 10 Mar 2026 22:44:34 GMT  
		Size: 201.8 MB (201752827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2417fb582ee5f8482415d53514cff3a92f9fdf84579de68169c5b6c4fd3ca31`  
		Last Modified: Tue, 10 Mar 2026 22:44:20 GMT  
		Size: 115.1 KB (115062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c513a537b7ef5a76ce60e2e06c9acf99a8b66c3f1fac772185b2513841cdfa`  
		Last Modified: Tue, 10 Mar 2026 22:44:20 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-nanoserver` - windows version 10.0.20348.4893; amd64

```console
$ docker pull eclipse-temurin@sha256:45cdbd92754363964cd5a860216f66080157f306a320a4705cc65e9624e530e6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.6 MB (328599105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cae5dd321ed37c72a9cfd794ea74c5f5cf2c208e2ab495b33c62148ad87a2cd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 10 Mar 2026 22:36:11 GMT
SHELL [cmd /s /c]
# Tue, 10 Mar 2026 22:37:22 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 10 Mar 2026 22:37:23 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 10 Mar 2026 22:37:23 GMT
USER ContainerAdministrator
# Tue, 10 Mar 2026 22:37:25 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Mar 2026 22:37:25 GMT
USER ContainerUser
# Tue, 10 Mar 2026 22:37:33 GMT
COPY dir:a00a0ee8f4ae82aa8e2b5d2b9cb5c2941887de3e7b021ae64d7924c257e6915c in C:\openjdk-21 
# Tue, 10 Mar 2026 22:37:39 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 10 Mar 2026 22:37:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62fed3face2429e33d46c7bd16d631ccc57a3988e4f3168d9273ff5de0c9322`  
		Last Modified: Tue, 10 Mar 2026 22:36:27 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970c7d8fc49886fc839b9fe4265e939c37428596ff46abf22c571c910946d477`  
		Last Modified: Tue, 10 Mar 2026 22:37:45 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1d97dbe4f3f35c5536fd480f2a0c4431b120206ef514b9da0ca59cd80d6394`  
		Last Modified: Tue, 10 Mar 2026 22:37:45 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518251174411bcfa2d3c03225162cf4f3cf797ad38e6c40502ca6a6f53aa92c7`  
		Last Modified: Tue, 10 Mar 2026 22:37:45 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad46fc679fbe170b4124baed32b01caa04507dbea4268184e5611d1bb044f4f7`  
		Last Modified: Tue, 10 Mar 2026 22:37:43 GMT  
		Size: 77.4 KB (77379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac96d137bd728dc7fb900d9dc4caeedfdb2623c6dc32adf0a783e081107540c6`  
		Last Modified: Tue, 10 Mar 2026 22:37:43 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a4d1947a2792b04b729d5a7acaf0feae0f6949551bc5e5bbdf91bec5bd6f9d`  
		Last Modified: Tue, 10 Mar 2026 22:37:57 GMT  
		Size: 201.8 MB (201752423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7721d9ab96c131d1d4582745bf28be1f4973ddb48ade0fba7878e47da53f801e`  
		Last Modified: Tue, 10 Mar 2026 22:37:43 GMT  
		Size: 112.4 KB (112386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d73663b138cc3c631e5f65e6b3230715244bf0ba07ab94ec7b0e0813b7a1365`  
		Last Modified: Tue, 10 Mar 2026 22:37:43 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
