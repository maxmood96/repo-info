## `openjdk:27-ea-13-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:baa7037a70a119ee1bda55d40fcedbecfa0e53429f25d24d8d1559c3e1b37e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `openjdk:27-ea-13-jdk-nanoserver` - windows version 10.0.26100.32522; amd64

```console
$ docker pull openjdk@sha256:144504b4ca6b2ea7e30eb2693b9fe6484fa535d13e25881eb217bcc05f2acb2d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.0 MB (423951868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a89b4d4831e78dd76cfc7db1838e30b8c7a59cc35d658fba25ff956e0ef0366f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Mar 2026 01:45:55 GMT
RUN Apply image 10.0.26100.32522
# Mon, 16 Mar 2026 18:34:35 GMT
SHELL [cmd /s /c]
# Mon, 16 Mar 2026 18:34:36 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 16 Mar 2026 18:34:37 GMT
USER ContainerAdministrator
# Mon, 16 Mar 2026 18:34:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 16 Mar 2026 18:34:52 GMT
USER ContainerUser
# Mon, 16 Mar 2026 18:34:53 GMT
ENV JAVA_VERSION=27-ea+13
# Mon, 16 Mar 2026 18:35:28 GMT
COPY dir:ca78bd5d260af53bead7adb95949561813c6e4975e6f0b206283f4f7dd803a5b in C:\openjdk-27 
# Mon, 16 Mar 2026 18:35:37 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 16 Mar 2026 18:35:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:06fab7822816d5f43d6835d07ac8db280fdf81384187f36d8dc43bbb7064a76d`  
		Last Modified: Tue, 10 Mar 2026 20:41:46 GMT  
		Size: 199.4 MB (199409325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58c4522c1384943a9bb6d856983429f0d7fde7c2c8b2242da2967bbc022bc20`  
		Last Modified: Mon, 16 Mar 2026 18:35:44 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a051e579919ef386ff23c0cb2def6ec089c57522f4aac83f7789c1a1d6592a68`  
		Last Modified: Mon, 16 Mar 2026 18:35:43 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d85e59c01dbaf27ae5656705c2182ab1d3ba8f5987e64321c37bc3911822d0b9`  
		Last Modified: Mon, 16 Mar 2026 18:35:43 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b83574aefc181f1e149924ebad86bc68a7aacb78690ddd4e468ad7cb0195b1`  
		Last Modified: Mon, 16 Mar 2026 18:35:43 GMT  
		Size: 77.2 KB (77150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac6973f9a3897da65823f3b9f9177f287fab04fa1b4cbe24ad153a5b2f59f2a`  
		Last Modified: Mon, 16 Mar 2026 18:35:42 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d61c5e2ee07070009a89f698d0a6980c188ffe155872dc1515a6738fdbe4b39`  
		Last Modified: Mon, 16 Mar 2026 18:35:42 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb547adb826025dcb3685b448c545ace21e30ce988c58c3ebce25ae593adcad3`  
		Last Modified: Mon, 16 Mar 2026 18:35:58 GMT  
		Size: 224.4 MB (224361372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd6c95c8916e75b497f1d7d5f24d0e5997368fb10dcf38cfdbcd4f237ccc2998`  
		Last Modified: Mon, 16 Mar 2026 18:35:42 GMT  
		Size: 97.6 KB (97594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18be17daa076306738b9ddcc2b824e7607e5513e9157d544b8e67573764b404`  
		Last Modified: Mon, 16 Mar 2026 18:35:42 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-13-jdk-nanoserver` - windows version 10.0.20348.4893; amd64

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
