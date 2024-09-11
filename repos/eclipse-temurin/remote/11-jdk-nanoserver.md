## `eclipse-temurin:11-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:0f801fcd7f40bc834bbe1fd95a2a15a1d03ae8e457aa827c94c60c1fb2a217ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.20348.2700; amd64

```console
$ docker pull eclipse-temurin@sha256:132285a2d732998557550926074f80927e2b6da724d9a5320fcc157a91bf931f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314312977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5207d8a7b7a14039bf30c588d2884427265962b4570cfd6ac74e4e14c4af013f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Sep 2024 23:48:03 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 01:05:47 GMT
SHELL [cmd /s /c]
# Wed, 11 Sep 2024 01:06:51 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 11 Sep 2024 01:06:52 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 11 Sep 2024 01:06:53 GMT
USER ContainerAdministrator
# Wed, 11 Sep 2024 01:07:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Sep 2024 01:07:01 GMT
USER ContainerUser
# Wed, 11 Sep 2024 01:07:12 GMT
COPY dir:b5e9d6d7234e205f01359f52140171f1743cc309a4dc5e4224755ced7d18fbfc in C:\openjdk-11 
# Wed, 11 Sep 2024 01:07:25 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 11 Sep 2024 01:07:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a447243899be39b01c34fc7e1bcecb47ce42b14668876fdd121f8b5e2d4d4a86`  
		Last Modified: Tue, 10 Sep 2024 22:28:02 GMT  
		Size: 120.5 MB (120509521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015f530aeae2fa9f5c34641a19099e9949880479ad7319678bd0506ba1927a95`  
		Last Modified: Wed, 11 Sep 2024 01:33:11 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb8fc165231f0ac01f3f49e3863537debb756f545e24faa797835d7a82c1104`  
		Last Modified: Wed, 11 Sep 2024 01:33:55 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226153802201755c536f792f8f86b0e0cf059c6b64f38dfd260dbc2ed394bc4e`  
		Last Modified: Wed, 11 Sep 2024 01:33:55 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea66e9d0f05f631f1b33df4a821d35938474f945ee3d182336e4de260af21e6`  
		Last Modified: Wed, 11 Sep 2024 01:33:55 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f03e4d90b49299418c82a3f1c052d100ba3199ec9d7ce399b989d5a1ddd8a0`  
		Last Modified: Wed, 11 Sep 2024 01:33:53 GMT  
		Size: 77.3 KB (77308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b0ed8186a4fc8838840ef3a2662b606b337a503db11f07a8e4cd97620cc9c0d`  
		Last Modified: Wed, 11 Sep 2024 01:33:53 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e37992b4245a13093ca83617e085f08411907bda1ae1766f250ca1d63db765`  
		Last Modified: Wed, 11 Sep 2024 01:34:09 GMT  
		Size: 193.7 MB (193658183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:642ed72f767beeec8ea862c536988199e6c62a84c9fb3fa842a5d8e7ed253aba`  
		Last Modified: Wed, 11 Sep 2024 01:33:53 GMT  
		Size: 61.2 KB (61168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1779d843aef6a8163c849b559922d222a75f682bf733ab9e3e5627b3e840b0dd`  
		Last Modified: Wed, 11 Sep 2024 01:33:53 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.17763.6293; amd64

```console
$ docker pull eclipse-temurin@sha256:6c0681fe6cbf5ddb0b5859abe78653efe8b4046938243a8b2ef54c83f80a00d5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.9 MB (348903230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92023fed24dafd4515e6f604447fa80343633eda17a307d9ff9c2ca0a887f330`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:38:01 GMT
SHELL [cmd /s /c]
# Wed, 11 Sep 2024 00:44:14 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 11 Sep 2024 00:44:15 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 11 Sep 2024 00:44:16 GMT
USER ContainerAdministrator
# Wed, 11 Sep 2024 00:44:23 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Sep 2024 00:44:23 GMT
USER ContainerUser
# Wed, 11 Sep 2024 00:44:35 GMT
COPY dir:b5e9d6d7234e205f01359f52140171f1743cc309a4dc5e4224755ced7d18fbfc in C:\openjdk-11 
# Wed, 11 Sep 2024 00:44:46 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 11 Sep 2024 00:44:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340318059288cbbdb326eea5b7079e789361251409038a37867d4e395c9404a5`  
		Last Modified: Wed, 11 Sep 2024 01:21:36 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53aeceeae01cd2700bfa285adb4e8aea90874ae765eb4010292810b4fc66f43`  
		Last Modified: Wed, 11 Sep 2024 01:24:08 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640dce13e93cb7fa86dee88df1ab878949bb33d05dc627cbafb56cb3d5bb1c4f`  
		Last Modified: Wed, 11 Sep 2024 01:24:08 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07e128bf684c16039994e9b0775db685540cf3f80d2551c91d773b6c2310282`  
		Last Modified: Wed, 11 Sep 2024 01:24:08 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7a9265b2317abc57266c983508810fdd20ea5991b90b5052b5049d2b68767a`  
		Last Modified: Wed, 11 Sep 2024 01:24:06 GMT  
		Size: 68.4 KB (68375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a505867a89571724a5bb7e0d3f76f5ba0e5a65e75970b028efd064065b82102`  
		Last Modified: Wed, 11 Sep 2024 01:24:06 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed645f1632fb08eea9317e04ee61110e60eb61a8bd212be54cc73fa9cf61eb48`  
		Last Modified: Wed, 11 Sep 2024 01:24:22 GMT  
		Size: 193.7 MB (193658298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d176d829920d07b9308f1abf5b52fb0f31950b40266a8e3de70011fea118a9fa`  
		Last Modified: Wed, 11 Sep 2024 01:24:06 GMT  
		Size: 88.9 KB (88865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac2834b08033380897977b6f29e3937ce1799e9ab02a4d1c4a651d6e2c32681`  
		Last Modified: Wed, 11 Sep 2024 01:24:06 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
