## `eclipse-temurin:8u472-b08-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:802ce6b27d38c24b704d88915348f4bf8002ead19af6b2924adb11eff221c0da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `eclipse-temurin:8u472-b08-jre-nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull eclipse-temurin@sha256:59589248fecd252ecab12b4c3228d9bc7f96f16522741dfc06595331b642fc6f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163431416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e3d08677b8c8112736b79dc50d209b764a567ae37c0d3dbb3c8db0561fca9a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Sat, 08 Nov 2025 18:23:50 GMT
SHELL [cmd /s /c]
# Sat, 08 Nov 2025 18:23:51 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 18:23:52 GMT
ENV JAVA_HOME=C:\openjdk-8
# Sat, 08 Nov 2025 18:23:53 GMT
USER ContainerAdministrator
# Sat, 08 Nov 2025 18:24:03 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 08 Nov 2025 18:24:04 GMT
USER ContainerUser
# Sat, 08 Nov 2025 18:24:21 GMT
COPY dir:d46ae848a780de83988aca6679aeefb6cb592f306ae2eca344ddb66bc6559a89 in C:\openjdk-8 
# Sat, 08 Nov 2025 18:24:25 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f3d1b99aefd432856f0f4f98d27b5fc5c2951dd239b9d32746c7be474a64ff`  
		Last Modified: Sat, 08 Nov 2025 18:24:42 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a57bd6e68039542479b85990ec2d046fa3f5af7a9c508a3ae77a90be64b6b9`  
		Last Modified: Sat, 08 Nov 2025 18:24:42 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a78af6eddc59f287a7ecb9f93c47b7059fe67067aed8f656d29604ee8dfa209`  
		Last Modified: Sat, 08 Nov 2025 18:24:44 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0daa312075efaef75a9be3281324de5f81a0ce53d6e54f28fda2f92616f79eaa`  
		Last Modified: Sat, 08 Nov 2025 18:24:44 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8363dbe7195d3c9dca6936ca3938fc8994b81146c8b8d3ff00ea774af7feee`  
		Last Modified: Sat, 08 Nov 2025 18:24:44 GMT  
		Size: 81.2 KB (81223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02544e3c0cd892fadc13ac4e1ff560e2d5cc02099ed4f1490d4b338a36de9b61`  
		Last Modified: Sat, 08 Nov 2025 18:24:45 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63fb7bbde907e99c2946732038ad0a0de0406d0ed15971d753f7969d6e9fe972`  
		Last Modified: Sat, 08 Nov 2025 18:24:54 GMT  
		Size: 40.6 MB (40554912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff9d1baaf7151f2ea06920a0c6487b53ab0f7e9b86b40f3fb01fc498cfb6044`  
		Last Modified: Sat, 08 Nov 2025 18:24:45 GMT  
		Size: 105.9 KB (105918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
