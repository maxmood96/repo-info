## `openjdk:27-ea-13-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:2f91395f8bff9f2557ccab85963b179c028bc8e72516b0ecd0f291c6781429c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `openjdk:27-ea-13-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull openjdk@sha256:b07d755c0b491c317eccebdc24c2ddf21faf6180a44a25f5b74cac2c002c685f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.2 MB (351207046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8464c6e083c0eaee33eb5ccc86aeef7de5ad066d6e56394ec8935cefb1847b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Mon, 16 Mar 2026 19:04:00 GMT
SHELL [cmd /s /c]
# Mon, 16 Mar 2026 19:04:03 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 16 Mar 2026 19:04:04 GMT
USER ContainerAdministrator
# Mon, 16 Mar 2026 19:04:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 16 Mar 2026 19:04:23 GMT
USER ContainerUser
# Mon, 16 Mar 2026 19:04:23 GMT
ENV JAVA_VERSION=27-ea+13
# Mon, 16 Mar 2026 19:05:56 GMT
COPY dir:ca78bd5d260af53bead7adb95949561813c6e4975e6f0b206283f4f7dd803a5b in C:\openjdk-27 
# Mon, 16 Mar 2026 19:06:03 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 16 Mar 2026 19:06:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22bb38c64ef466ed840d69a3d51544eb6bd25efc87e9351de0f9a73152b8797f`  
		Last Modified: Mon, 16 Mar 2026 19:06:10 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9741edf5ca125cbc53c44f2f0c2d5e647813ced9407bbd8f95c8c545a3215fc1`  
		Last Modified: Mon, 16 Mar 2026 19:06:09 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1ec2f638bcaa18d29a6d710f3bd75f70b742012839d1c79e6aeb90003e159e`  
		Last Modified: Mon, 16 Mar 2026 19:06:09 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34181c1b3e1220f502652ac47bf1e7ada3d37ece4604d6698b906a54032e9ea8`  
		Last Modified: Mon, 16 Mar 2026 19:06:09 GMT  
		Size: 71.5 KB (71459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e1636a00a0ccb7734b4dc75a512c21aab67b14d0c9e3b8b0b693e8af0dc81b`  
		Last Modified: Mon, 16 Mar 2026 19:06:08 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc4b614074d824c05b28dc30548b8335b4b1639c5d7b82542c1e1b3661e5003`  
		Last Modified: Mon, 16 Mar 2026 19:06:08 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4302d3184cfbc77c7f507ef20cba519933dbf34a9f7359d9ff3a9f910753cf25`  
		Last Modified: Mon, 16 Mar 2026 19:06:23 GMT  
		Size: 224.4 MB (224360570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459c3e89eb0476df2e07aa03df6c7efc86ec6c54c26c56ab7b14716a4def60f5`  
		Last Modified: Mon, 16 Mar 2026 19:06:08 GMT  
		Size: 118.2 KB (118156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09697ba352e80e08c4cd9efd571dfde929739747232268d950cd976d0bd9a4bb`  
		Last Modified: Mon, 16 Mar 2026 19:06:08 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
