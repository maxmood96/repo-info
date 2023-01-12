## `eclipse-temurin:19-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:f3bab1c487a437ee6969dfa101c68f7a34f4e25d5cc38963541d21c4611cd817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1487; amd64
	-	windows version 10.0.17763.3887; amd64

### `eclipse-temurin:19-nanoserver` - windows version 10.0.20348.1487; amd64

```console
$ docker pull eclipse-temurin@sha256:d44d7a28c0a61e9c76dfb8919f3a4c1d951e46d51a4d39634ba26e5e3587fc09
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.7 MB (315726583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee3537acbc75c72949bda49bae68c64dcbaa6230c331d40ea6f39477e2c8c93d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Jan 2023 23:36:49 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 02:19:48 GMT
SHELL [cmd /s /c]
# Thu, 12 Jan 2023 02:25:35 GMT
ENV JAVA_VERSION=jdk-19.0.1+10
# Thu, 12 Jan 2023 02:25:36 GMT
ENV JAVA_HOME=C:\openjdk-19
# Thu, 12 Jan 2023 02:25:37 GMT
USER ContainerAdministrator
# Thu, 12 Jan 2023 02:25:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 12 Jan 2023 02:25:51 GMT
USER ContainerUser
# Thu, 12 Jan 2023 02:26:10 GMT
COPY dir:2282de048661e89f3c315adc23c8954e0ca245f9a969462117712d8342758a69 in C:\openjdk-19 
# Thu, 12 Jan 2023 02:26:37 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 12 Jan 2023 02:26:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:83e9437e818022c1c28f0e07002dd46995c8614e62b9366138fa23b94f43d9ad`  
		Last Modified: Thu, 12 Jan 2023 02:51:06 GMT  
		Size: 122.1 MB (122099566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbebbf572ebe7984b715b8dfe99bc1273403a831c0079b95afa12162b7266f16`  
		Last Modified: Thu, 12 Jan 2023 02:50:38 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbac7f900a9c01a3fb16d84eedf744987c8045fef7fb7d056174f5136108e77`  
		Last Modified: Thu, 12 Jan 2023 02:53:07 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c16d2606ed201b9849f39a4da4ce8e764ab707f7d6dca05e374564f41672d87`  
		Last Modified: Thu, 12 Jan 2023 02:53:06 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6052e97af270f61fa97aa379410fd26e01069b19613d8fb30e6c13065d61c92e`  
		Last Modified: Thu, 12 Jan 2023 02:53:06 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45075737173e212d3905c32f22add977b909cf031d39042fe28f2b8b8b928181`  
		Last Modified: Thu, 12 Jan 2023 02:53:05 GMT  
		Size: 81.1 KB (81078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e385c57e79b6097f2e28b91a12cdc521c9cb974833d8e9c098e5b03431cd3a38`  
		Last Modified: Thu, 12 Jan 2023 02:53:04 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac52af7c232ce615d5585f2356875899b5d424bdc5367c33bd170ca7dbe3edd5`  
		Last Modified: Thu, 12 Jan 2023 02:53:26 GMT  
		Size: 193.4 MB (193444536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:851979b9278e59f0ded3e2a6c8c7fc79c54999a52a4a44c5d7d28b4a49979e3f`  
		Last Modified: Thu, 12 Jan 2023 02:53:05 GMT  
		Size: 95.0 KB (95040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cb50aec0f1883050bddfd6e39e1c317f7cab9a75d34b09b4aabdf5b6e808e6`  
		Last Modified: Thu, 12 Jan 2023 02:53:04 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:19-nanoserver` - windows version 10.0.17763.3887; amd64

```console
$ docker pull eclipse-temurin@sha256:c09e00d42c1e4bbe428b95a7a5fe44c8b2c04f99767010625652d99f4defa530
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303878857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9a7b4fadefc506f6cbe0af1a1faaf260e74671704605082698d9d53595d197`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 07 Jan 2023 05:17:01 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:45:31 GMT
SHELL [cmd /s /c]
# Thu, 12 Jan 2023 02:14:19 GMT
ENV JAVA_VERSION=jdk-19.0.1+10
# Thu, 12 Jan 2023 02:14:20 GMT
ENV JAVA_HOME=C:\openjdk-19
# Thu, 12 Jan 2023 02:14:20 GMT
USER ContainerAdministrator
# Thu, 12 Jan 2023 02:14:33 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 12 Jan 2023 02:14:34 GMT
USER ContainerUser
# Thu, 12 Jan 2023 02:14:49 GMT
COPY dir:2282de048661e89f3c315adc23c8954e0ca245f9a969462117712d8342758a69 in C:\openjdk-19 
# Thu, 12 Jan 2023 02:15:31 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 12 Jan 2023 02:15:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e58f9ad3b15a2a4882ab0a845e8e619cc8c3c411ddbe8b50046c1618a95c1397`  
		Last Modified: Thu, 12 Jan 2023 02:40:44 GMT  
		Size: 106.7 MB (106666138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea67a6bd980bdee35399883e5abcc31c738b338ad384b2f92d91a15cf09d9df`  
		Last Modified: Thu, 12 Jan 2023 02:40:16 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a097ddafe1db6b90c63bc2e1ee113e718163fe4ec2cce9aa8d647f1ec0207a46`  
		Last Modified: Thu, 12 Jan 2023 02:49:09 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c585af211d5a537202e96a308362cf3960f1d5d4dc47d8319fb1a04909e09327`  
		Last Modified: Thu, 12 Jan 2023 02:49:08 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d417dfce819a16bf9fbd631fa670e73620a8674a79873ee91ce990582762f8e`  
		Last Modified: Thu, 12 Jan 2023 02:49:08 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd67542e6c548da3584bc37880aef7acf2ac586ecd62689631f34c9fde76e813`  
		Last Modified: Thu, 12 Jan 2023 02:49:07 GMT  
		Size: 71.9 KB (71891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b7ac5bb71e91bff2e01f749c68e4ecd58ccedf4487a63bbd715a76f62bb84a`  
		Last Modified: Thu, 12 Jan 2023 02:49:06 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5691058be01ae708f9885f5bf83300e430524c445f45beb754eb522c027e41`  
		Last Modified: Thu, 12 Jan 2023 02:49:27 GMT  
		Size: 193.4 MB (193446513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71376f55fb2a57ce099a2c9c03c6c6f27e0fbbc465fc0966f843f795e61e5454`  
		Last Modified: Thu, 12 Jan 2023 02:49:07 GMT  
		Size: 3.7 MB (3687408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976cd4dadd5f6d8dfc51ff4d749ebf7621ee0186be31fd0ae38b0cd436bd647e`  
		Last Modified: Thu, 12 Jan 2023 02:49:06 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
