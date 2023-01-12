## `eclipse-temurin:19-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:eb54fce8052f499203d38e1af7ffa3c2b96f7debafb39d287b1bbc60bc1c74ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `eclipse-temurin:19-jdk-nanoserver-1809` - windows version 10.0.17763.3887; amd64

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
