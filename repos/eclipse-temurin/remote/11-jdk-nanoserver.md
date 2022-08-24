## `eclipse-temurin:11-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:eda67d67dcbd45d9313cec8bb23c82df34067297c2ed8378056c6dc84df0e095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.887; amd64
	-	windows version 10.0.17763.3287; amd64

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.20348.887; amd64

```console
$ docker pull eclipse-temurin@sha256:f62140294f532014b035964278811687e8544f3f940526a75eaf26aecc77b1dd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310627166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492fc7d14d11d2bbcc2aeeea4a4d1a4c37e2c8679d3f1231656e567dc9e08210`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Aug 2022 18:05:23 GMT
RUN Apply image 10.0.20348.887
# Wed, 10 Aug 2022 16:28:17 GMT
SHELL [cmd /s /c]
# Wed, 24 Aug 2022 19:38:52 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Wed, 24 Aug 2022 19:38:54 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 24 Aug 2022 19:38:55 GMT
USER ContainerAdministrator
# Wed, 24 Aug 2022 19:39:10 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Aug 2022 19:39:12 GMT
USER ContainerUser
# Wed, 24 Aug 2022 19:39:28 GMT
COPY dir:b7b3112beefc8be2dd5c6a3897a52ba756c9a344294f20db387fa022b341211c in C:\openjdk-11 
# Wed, 24 Aug 2022 19:39:49 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 24 Aug 2022 19:39:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ebf439f800cd4c1fccaf4a0545e6bff60caa5141295c8ab81f6c525073c423d`  
		Size: 118.1 MB (118088450 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5f1e06146ab0490d235fe89786637467a4b71853ee428e8740ea6efbc536c47c`  
		Last Modified: Wed, 10 Aug 2022 16:48:40 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552df7312ccb2e6d922d6f01e4724f3b3d6476ea66250954b2fca74f99cbef64`  
		Last Modified: Wed, 24 Aug 2022 19:51:49 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736c1676086df0f6671638cbaffea34375022178641fa815899599219e34505d`  
		Last Modified: Wed, 24 Aug 2022 19:51:49 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4bf431c912d3f6a0ac493da931e2511889e92c89cca4fb739323c81e786c4a`  
		Last Modified: Wed, 24 Aug 2022 19:51:49 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050e66f4a83838f72987c29f696c98c331ffbc0eba773d77b29d81b6c63c2024`  
		Last Modified: Wed, 24 Aug 2022 19:51:47 GMT  
		Size: 84.6 KB (84612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b38c9bea5c240256e7483d2c0b07d7404ec0d1681ff4707c11583372a76524`  
		Last Modified: Wed, 24 Aug 2022 19:51:47 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8172543552474ca4dda8935d13c0f0b01e5299581a4f13ab26192f0760485bb7`  
		Last Modified: Wed, 24 Aug 2022 19:52:10 GMT  
		Size: 192.4 MB (192371224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b69400d0d37e581a7007cd39970ca0414f27460e8501d72e09fbb5b7b85c8e`  
		Last Modified: Wed, 24 Aug 2022 19:51:47 GMT  
		Size: 75.9 KB (75902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84661da252ae3c82036acbf2f07fe606fdf1fa7effe62d56bd8399007f46cdbf`  
		Last Modified: Wed, 24 Aug 2022 19:51:47 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.17763.3287; amd64

```console
$ docker pull eclipse-temurin@sha256:20bbc71468db3d7c824729c734b31858881be948ef2be1068e0b5773a590796d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295728967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4bd3a0094a350d13edb2e3f9f9ef3bf0c7083740fcf28f5841993c7abf1be55`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Aug 2022 18:08:38 GMT
RUN Apply image 10.0.17763.3287
# Wed, 10 Aug 2022 15:57:07 GMT
SHELL [cmd /s /c]
# Wed, 24 Aug 2022 19:21:39 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Wed, 24 Aug 2022 19:21:41 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 24 Aug 2022 19:21:43 GMT
USER ContainerAdministrator
# Wed, 24 Aug 2022 19:21:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Aug 2022 19:21:59 GMT
USER ContainerUser
# Wed, 24 Aug 2022 19:22:15 GMT
COPY dir:b7b3112beefc8be2dd5c6a3897a52ba756c9a344294f20db387fa022b341211c in C:\openjdk-11 
# Wed, 24 Aug 2022 19:22:36 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 24 Aug 2022 19:22:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5c9d6483dab113d2d9b50fdf3156622aa2ec3d6faaed5664d15a5568032d1714`  
		Size: 103.2 MB (103204200 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0f4438539876006761cb687527bd8cb94cc7a273cf8bb47563981044f2e1771e`  
		Last Modified: Wed, 10 Aug 2022 16:38:40 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f2f6c8eb61ace777481cf2506fbc21fd41bdf97aac59169f8ba88ebcb59b43`  
		Last Modified: Wed, 24 Aug 2022 19:46:42 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab83a38af2808ef87862a89fad80ded3cad4214a649e01f9c495f60cc6ffd5db`  
		Last Modified: Wed, 24 Aug 2022 19:46:42 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8830235d8ecb76d37af874b4cf3c79d939255218c70b3afad253d8e81b665c72`  
		Last Modified: Wed, 24 Aug 2022 19:46:41 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41583d9d5e18a6064d0fdc0c7814e90f601656705b9b3f153d638ecf7e6a0145`  
		Last Modified: Wed, 24 Aug 2022 19:46:39 GMT  
		Size: 69.0 KB (69042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3503782ceaee2cddd02d6ab1562f5bc4e5ddc13cb756a7bb2fa77781ba8643`  
		Last Modified: Wed, 24 Aug 2022 19:46:39 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f419adfd130ed6f2dd47d0e939ef88c9f26f66b54dd05c828d7344b169e1c245`  
		Last Modified: Wed, 24 Aug 2022 19:46:59 GMT  
		Size: 192.4 MB (192366818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a5433cf98c7bb2cc9265244593170d4cf79124efb00c3d17c738e793be490d`  
		Last Modified: Wed, 24 Aug 2022 19:46:39 GMT  
		Size: 81.9 KB (81939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de88067079c4110a269a7015e1fe01d02c67e02a0f5fcdc724e988e7b24fa05`  
		Last Modified: Wed, 24 Aug 2022 19:46:39 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
