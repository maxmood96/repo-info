## `openjdk:25-ea-13-nanoserver`

```console
$ docker pull openjdk@sha256:7cd74e20ea813a8b4a1e0efef8e28ac84efb3d8c374889dcef2b6cd11bba3812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `openjdk:25-ea-13-nanoserver` - windows version 10.0.26100.3476; amd64

```console
$ docker pull openjdk@sha256:15dd6d18cca310e976f1194de7d28e0efbde24ff944fc24390eb40a0b590a18c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.9 MB (413898526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4ea0193c5aa52e5694fbf04ff9b7dd0685c82c40cc53738f7fb3f7031ba447`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Wed, 12 Mar 2025 19:17:32 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:17:33 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 12 Mar 2025 19:17:34 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:17:36 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 12 Mar 2025 19:17:37 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:17:37 GMT
ENV JAVA_VERSION=25-ea+13
# Wed, 12 Mar 2025 19:17:45 GMT
COPY dir:41adcea28f6e8239eac0b74c19049c5daef67ad138ba9db7bdf8df0acc8b0b9b in C:\openjdk-25 
# Wed, 12 Mar 2025 19:17:52 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 12 Mar 2025 19:17:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e613ab96b2ca62c89b368c48e5bbe28db973bd4201adca9d267cc2876ed9fd2d`  
		Last Modified: Wed, 12 Mar 2025 19:17:56 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edcef208ed4c4473ae0d055992d18ccde447bee0d0fa8b0c8efdd17e798647b1`  
		Last Modified: Wed, 12 Mar 2025 19:17:56 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e3a3b1ff09815997575fdf009d7ec4b044e03d4a91a7384bdd62a8f4d83cce`  
		Last Modified: Wed, 12 Mar 2025 19:17:56 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3f8326eaca13881197bdc2307a37a60b8f30b5fcc5e6cb0eae5139be2d11f4`  
		Last Modified: Wed, 12 Mar 2025 19:17:56 GMT  
		Size: 76.2 KB (76186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863590b5ca2eec1f0d3fa2f63963f064796eb0509eda9993c77b13580217e7eb`  
		Last Modified: Wed, 12 Mar 2025 19:17:55 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f4d8f45c2fe0ec276ce226ba6ce8be6edee8e88ed99821eba73f63be0f1ee6`  
		Last Modified: Wed, 12 Mar 2025 19:17:55 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ba0f62807efbee03152b49a1dcbbf9caab397334a8bae7fbe6aa894b38763a`  
		Last Modified: Wed, 12 Mar 2025 19:18:07 GMT  
		Size: 207.4 MB (207398796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1ff3bce5a2499fc81d755c17a820a93a199f3db7d676dfc9ac306d05c91c91`  
		Last Modified: Wed, 12 Mar 2025 19:17:55 GMT  
		Size: 114.9 KB (114901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed24ba2c25c4b63036c7f375ebdcd56143b211f40cd5bce1ce113ae3a2eaf2c`  
		Last Modified: Wed, 12 Mar 2025 19:17:55 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-13-nanoserver` - windows version 10.0.20348.3328; amd64

```console
$ docker pull openjdk@sha256:332117e23363b6d7be48e35f79848aedaf23d8e8658efade088f80bbd074571a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.3 MB (328271277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8aefde0ab5d11ad4ebb2d276e94d2186b87452361be593c1b3c5a97fcff0076`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Wed, 12 Mar 2025 19:22:18 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:22:19 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 12 Mar 2025 19:22:20 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:22:24 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 12 Mar 2025 19:22:25 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:22:26 GMT
ENV JAVA_VERSION=25-ea+13
# Wed, 12 Mar 2025 19:22:34 GMT
COPY dir:41adcea28f6e8239eac0b74c19049c5daef67ad138ba9db7bdf8df0acc8b0b9b in C:\openjdk-25 
# Wed, 12 Mar 2025 19:22:39 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 12 Mar 2025 19:22:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c2f17cecf881f104c1c9863a9939b7951a727238e9cef089c188c26320657e`  
		Last Modified: Wed, 12 Mar 2025 19:22:45 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b8fb0c1c384a3635a96c4b7a79c57756b8aae9b195babdd37119f42546be93`  
		Last Modified: Wed, 12 Mar 2025 19:22:46 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a61f49c35186bcd6dff87df3755ae19e196edab80d5bca0bcaa480bcf89d37`  
		Last Modified: Wed, 12 Mar 2025 19:22:45 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a318be4c4c064770438b69f3fa62d2976e9310545b4d7d25fecbc2f4732efbe2`  
		Last Modified: Wed, 12 Mar 2025 19:22:45 GMT  
		Size: 73.1 KB (73086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ac77ec3f311bdb46c1a4311ff49f2565283440164928d92446078689dd2eb3`  
		Last Modified: Wed, 12 Mar 2025 19:22:43 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab50dc0c2d10d2bc209422267bd346fc140120ed38ca35f29337b5807bc816c`  
		Last Modified: Wed, 12 Mar 2025 19:22:43 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80281f30648e178a66ef27279490823213c3551a501e687fe01774c862359569`  
		Last Modified: Wed, 12 Mar 2025 19:22:55 GMT  
		Size: 207.4 MB (207398992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87243abdb80a42b54ea68cf29209463726ceac287ca9af6be95abb3afe7f6c3`  
		Last Modified: Wed, 12 Mar 2025 19:22:43 GMT  
		Size: 97.3 KB (97341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2109cac3a05aeec383a0b1af8dbb1611a97772a09c0540651876a346deb010e`  
		Last Modified: Wed, 12 Mar 2025 19:22:43 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-13-nanoserver` - windows version 10.0.17763.7009; amd64

```console
$ docker pull openjdk@sha256:b595e03b9e781eae4ab348da92d2827b4e7bbda1587e6897e96e1c01e1d11a20
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.8 MB (318812528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732d2791758dc65843c233a16db14df992fcaf696a037382e623664af3c4269d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Wed, 12 Mar 2025 19:18:03 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:18:05 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 12 Mar 2025 19:18:06 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:18:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 12 Mar 2025 19:18:10 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:18:10 GMT
ENV JAVA_VERSION=25-ea+13
# Wed, 12 Mar 2025 19:18:17 GMT
COPY dir:41adcea28f6e8239eac0b74c19049c5daef67ad138ba9db7bdf8df0acc8b0b9b in C:\openjdk-25 
# Wed, 12 Mar 2025 19:18:24 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 12 Mar 2025 19:18:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a3a60d876a6532ca19dde160af76ce891f2b9481df62c486a62a9f9ed03650`  
		Last Modified: Wed, 12 Mar 2025 19:18:32 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645f14e8f64c5cf823605e69d297a392bdf3c84450a326f5d7bd9b9123899ae7`  
		Last Modified: Wed, 12 Mar 2025 19:18:31 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f32d04711ac06a732e03419a288c5e265849261f0e97bc8d6f2822c9e1decf2`  
		Last Modified: Wed, 12 Mar 2025 19:18:31 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2e3e4032d2f2c615bf835ca2fbb224e63146299ab65fe1c507189cefcb9b72`  
		Last Modified: Wed, 12 Mar 2025 19:18:31 GMT  
		Size: 69.0 KB (68971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78a6d1516da2a30023bf06767f26de0ed886bb47b78ce83541b8ce177934d70`  
		Last Modified: Wed, 12 Mar 2025 19:18:29 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9dbd1b50e4a192f59304e3a7773b2d03cd6aaafa2a9c07203299faa43293113`  
		Last Modified: Wed, 12 Mar 2025 19:18:29 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a30e8f11fc3997c1c55599ebc652d663f64a867bd26b94352cc768284b5c1a`  
		Last Modified: Wed, 12 Mar 2025 19:18:40 GMT  
		Size: 207.4 MB (207399325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3c140474df4351300bf44644e8edb1bb16be1912f5e52c9a6666fba9cb1135`  
		Last Modified: Wed, 12 Mar 2025 19:18:30 GMT  
		Size: 4.4 MB (4430325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c5581ba06d056095beeaf4635a96c0068fa4c5f715d0c091ad8e0ad5bb2b48`  
		Last Modified: Wed, 12 Mar 2025 19:18:29 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
