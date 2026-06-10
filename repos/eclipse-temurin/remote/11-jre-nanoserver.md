## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:c1a476813a90610e01146eba4e27835b162b9ac565f152221408c4c0efa5237a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.26100.32995; amd64

```console
$ docker pull eclipse-temurin@sha256:40387efe30155ec9528962a74866ec58160d0e787f76fafceb7665813705d5f4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240588715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b01e703411e3f7224ebcb2fa917bd49507fa9fd62cf6e8cfe4f8b4ad18002c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 07:06:15 GMT
RUN Apply image 10.0.26100.32995
# Tue, 09 Jun 2026 23:20:24 GMT
SHELL [cmd /s /c]
# Tue, 09 Jun 2026 23:20:25 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 09 Jun 2026 23:20:26 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 09 Jun 2026 23:20:26 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2026 23:20:34 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Jun 2026 23:20:34 GMT
USER ContainerUser
# Tue, 09 Jun 2026 23:20:47 GMT
COPY dir:b48d35a79d584b4e6e30bd64a65514a5a8dd37c415c758cd9c300ebbad014bb0 in C:\openjdk-11 
# Tue, 09 Jun 2026 23:20:52 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:64f5cd94d3bcd0fae94830b1fad0f8b3dc33677f8d7dc15c5219b56fe2a6584e`  
		Last Modified: Tue, 09 Jun 2026 22:11:30 GMT  
		Size: 196.7 MB (196668131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab1bce81b4ccafb935ec08f868e26772e38ddc1cfc703fb6aee03b707852a19`  
		Last Modified: Tue, 09 Jun 2026 23:20:58 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f94fc94a8a04cdbfe63ad9ba2940acb0f1a178fcf4f4585839ad8a1ee2a5586`  
		Last Modified: Tue, 09 Jun 2026 23:20:58 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ccb41287ccd64ad187f43067468e079c42c466923b4c526be3ce2fa2aacc8f`  
		Last Modified: Tue, 09 Jun 2026 23:20:58 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367fffe2b4c46737f4c5cd7755acbd0c276b7bbb75c83e6976deb36710c9a860`  
		Last Modified: Tue, 09 Jun 2026 23:20:56 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83d22f6688ee90568b974ab469c397735fd0dda73ef3e864a3244b5e19d356b`  
		Last Modified: Tue, 09 Jun 2026 23:20:56 GMT  
		Size: 69.8 KB (69817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4291424b0487885b94842e0b7350939e47f345b668a4da6686a2f7a6fbcf5d63`  
		Last Modified: Tue, 09 Jun 2026 23:20:56 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1c9ecb9fd07c57479d2df78114758f2a2499650f59e2d017ec42ff03e955da`  
		Last Modified: Tue, 09 Jun 2026 23:21:02 GMT  
		Size: 43.7 MB (43738693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402caeda524e3ad436ea2ba3a6dacd0be9179348973660d5c387d5383fbd51d0`  
		Last Modified: Tue, 09 Jun 2026 23:20:56 GMT  
		Size: 106.9 KB (106921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.20348.5256; amd64

```console
$ docker pull eclipse-temurin@sha256:cbd614e7ce89cf0637fc971d6d117ba46e2c4999f19893dfed5a0df4c142a320
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.9 MB (167919875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a2aa237096e8a340c377fb62d383b3a081554869e45d2df9699b5a2802eaba`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Tue, 09 Jun 2026 23:21:49 GMT
SHELL [cmd /s /c]
# Tue, 09 Jun 2026 23:21:50 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 09 Jun 2026 23:21:50 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 09 Jun 2026 23:21:50 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2026 23:21:53 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Jun 2026 23:21:54 GMT
USER ContainerUser
# Tue, 09 Jun 2026 23:22:00 GMT
COPY dir:b48d35a79d584b4e6e30bd64a65514a5a8dd37c415c758cd9c300ebbad014bb0 in C:\openjdk-11 
# Tue, 09 Jun 2026 23:22:03 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e97e8b9098cc4d050c642b320fe6d5a7ddda866e0c41c7a307e5ca8734409b`  
		Last Modified: Tue, 09 Jun 2026 23:22:09 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0746f2a64935596b7ba1c3a304b27ede4814885676103452f03df6faa53b858`  
		Last Modified: Tue, 09 Jun 2026 23:22:09 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfed6a13a0183dde0b6709423b79e48fc014271c8c0dfba3a3df3065728faabc`  
		Last Modified: Tue, 09 Jun 2026 23:22:09 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9770dad4c1dc01c99707ee1beaa3677f4f3c1d9c6489f316514313a02355c5`  
		Last Modified: Tue, 09 Jun 2026 23:22:07 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0dc744c2218706ae353de6cbd83bf3684c337f9f40958a22a56ae664af28c1`  
		Last Modified: Tue, 09 Jun 2026 23:22:08 GMT  
		Size: 86.9 KB (86881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6362b77963ae89774db3c95e9548dc4e1a455257696ec2a0692ef8a70cdb8848`  
		Last Modified: Tue, 09 Jun 2026 23:22:07 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3997506b4ef746cf8161abddfe88587652515d7ccf571afa405a0dec29e009af`  
		Last Modified: Tue, 09 Jun 2026 23:22:13 GMT  
		Size: 43.7 MB (43738888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5f5ecf23f1ceccc6c838e51859cedb622f6a7c7ef9f6a79d543f9ddc12c83e`  
		Last Modified: Tue, 09 Jun 2026 23:22:07 GMT  
		Size: 91.3 KB (91318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
