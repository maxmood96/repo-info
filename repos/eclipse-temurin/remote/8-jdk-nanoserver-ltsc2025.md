## `eclipse-temurin:8-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:0abfe3240d13331ed9baa431b7735949abc5f693cb918d62686c0e12423071a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `eclipse-temurin:8-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull eclipse-temurin@sha256:6fd41e90990bfd2427b9526642d153310f82c9de2234ffd3e4326a034b3ff575
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.5 MB (308499143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa01fcaf8fd497bb7a121fb14e7a724b2824a90f86e376f179522437edcc128`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 08 Feb 2025 22:31:47 GMT
RUN Apply image 10.0.26100.3194
# Thu, 27 Feb 2025 19:13:27 GMT
SHELL [cmd /s /c]
# Thu, 27 Feb 2025 19:13:28 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 27 Feb 2025 19:13:29 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 27 Feb 2025 19:13:29 GMT
USER ContainerAdministrator
# Thu, 27 Feb 2025 19:13:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 27 Feb 2025 19:13:32 GMT
USER ContainerUser
# Thu, 27 Feb 2025 19:13:38 GMT
COPY dir:bdaea23e3e57be9dfb95abf135786259c631aa0db2125cb7a86f299ac37b3921 in C:\openjdk-8 
# Thu, 27 Feb 2025 19:13:42 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:e075dd07cbf907b7da8dbd8365b73a71ac92a834b78f520bd976cb97e0fcc0a1`  
		Last Modified: Wed, 12 Feb 2025 22:34:59 GMT  
		Size: 205.9 MB (205890263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bcb5f70b5dce8ba36af9b3be16d4bac537bc13dffa6cbe5bdf299aa41464ba6`  
		Last Modified: Thu, 27 Feb 2025 19:13:48 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423db6130f96c5fb8f661bb890164acc7650183441d070c3e84daaa06a96503d`  
		Last Modified: Thu, 27 Feb 2025 19:13:48 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fac19c45f2b383478e941dfeeea0893af93ec96194989227e55bebda13d27c`  
		Last Modified: Thu, 27 Feb 2025 19:13:48 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c0e77b78e26496d60333488d63b6b68e33bf81348aeadf88636f45d273078d`  
		Last Modified: Thu, 27 Feb 2025 19:13:46 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c485311ca770b885722acf7e6b164f44f0e63caac9430f0909a60fca04208f`  
		Last Modified: Thu, 27 Feb 2025 19:13:47 GMT  
		Size: 76.5 KB (76499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3108b9770969682026af6dded166f6adc618c0c09f9d338b4f3b65507249ecb1`  
		Last Modified: Thu, 27 Feb 2025 19:13:47 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb7bc0e1204ca2b551f18ad9c060c9ddf903f902ef1fd401b6bd79668cea9f9`  
		Last Modified: Thu, 27 Feb 2025 19:13:53 GMT  
		Size: 102.4 MB (102433882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d0176eb36bd56a1e62f3b3be04be0e436871afc18037cb94ef0677377ea2be`  
		Last Modified: Thu, 27 Feb 2025 19:13:47 GMT  
		Size: 93.2 KB (93238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
