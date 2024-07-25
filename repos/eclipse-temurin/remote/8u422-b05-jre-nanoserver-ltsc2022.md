## `eclipse-temurin:8u422-b05-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:f4cda96c1b3ec98d5d66214d3983706444b80dd1188961327e234cadeae9663d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `eclipse-temurin:8u422-b05-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull eclipse-temurin@sha256:5e11b1f72cca5866df5f34348dcd9b7f8afab120c2a2505b06dcf827bf765cbe
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160655969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebbd0613928c686ff42e0bf847f58fd283eb9941eb8a278ed2edf08f512d9db`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 09:30:07 GMT
RUN Apply image 10.0.20348.2582
# Wed, 10 Jul 2024 17:17:20 GMT
SHELL [cmd /s /c]
# Thu, 25 Jul 2024 17:25:11 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 25 Jul 2024 17:25:12 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 25 Jul 2024 17:25:13 GMT
USER ContainerAdministrator
# Thu, 25 Jul 2024 17:25:22 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 25 Jul 2024 17:25:22 GMT
USER ContainerUser
# Thu, 25 Jul 2024 17:26:08 GMT
COPY dir:9cd76711a1e21cd053ac2280c0520b18fc7c9ba73d3efc8192b2b62cbbddbbff in C:\openjdk-8 
# Thu, 25 Jul 2024 17:26:19 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:652774a5d82a114642848f8b0b8d486ec1b4995f9dda56e36fe4ac7563429990`  
		Last Modified: Tue, 09 Jul 2024 20:33:26 GMT  
		Size: 120.5 MB (120490378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1dbb650483c31087741ccfe7cfef17abfd7465711d0851e35d39eabc775bdae`  
		Last Modified: Wed, 10 Jul 2024 17:38:52 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd0adf4702d813bb7fa724c9bf2343c201391c6d70a7a35135b18cc53499721`  
		Last Modified: Thu, 25 Jul 2024 17:31:42 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94884a864d317b3caa2f721285e95de08018c4d1388ebfcc7b74d0b3371564c`  
		Last Modified: Thu, 25 Jul 2024 17:31:41 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4085421efae24344eed5fb063a3fed76207a5fa6434c58e5060c180b76b7821`  
		Last Modified: Thu, 25 Jul 2024 17:31:40 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82df57eb258bb9e82243a6cda569545565c89aa9f4d19b7a9d443746926e680`  
		Last Modified: Thu, 25 Jul 2024 17:31:40 GMT  
		Size: 80.4 KB (80387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183f1e530fbf61205e4a140565535007984ca4ba7ad524ccc77eca5b3a7d54d9`  
		Last Modified: Thu, 25 Jul 2024 17:31:40 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aeca43d3843d868cb322fbfe0a707c3dea0e24a6450c9017cf02367bd7ec672`  
		Last Modified: Thu, 25 Jul 2024 17:32:06 GMT  
		Size: 40.0 MB (40018511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f70d05893177c60583e6002fad80a813fc3bdb1cad17eacb716312fb8236c9`  
		Last Modified: Thu, 25 Jul 2024 17:32:01 GMT  
		Size: 60.9 KB (60914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
