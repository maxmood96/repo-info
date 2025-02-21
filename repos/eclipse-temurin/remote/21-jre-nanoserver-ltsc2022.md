## `eclipse-temurin:21-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:9f0bf9f834eb5ebdbf767f5174bbcf1df7f1afb22d4bfcc51a442170aa4da4d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `eclipse-temurin:21-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull eclipse-temurin@sha256:caa905fd623ee5bc0a3903bacb15a7dddeaf82c774dde9f8b5c59d95778131e1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.8 MB (169787697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7ef2410e7a588f9cd3a93b919a1d45d8ffe84b47a65e2303d268b3a995d4e08`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 20:45:43 GMT
RUN Apply image 10.0.20348.3207
# Thu, 13 Feb 2025 01:12:27 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:12:28 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 13 Feb 2025 01:12:29 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 13 Feb 2025 01:12:29 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:12:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Feb 2025 01:12:32 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:12:35 GMT
COPY dir:c0b7c132c85049081486a93cd76fe016c559b0b921796f63592a768b082ae9e2 in C:\openjdk-21 
# Thu, 13 Feb 2025 01:12:40 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:938e4585b186fc3df3c1959d47ba7a634fea121cec7545db7923ceb191d99a33`  
		Last Modified: Tue, 11 Feb 2025 22:43:09 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468abfac4ce815f75110e371454a3472c6d3bba016bef7b40971137e8981ef46`  
		Last Modified: Thu, 13 Feb 2025 01:12:47 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f36f59ecae2e7086528dabbcf52a4815e9597e8d264116fa4e2026b7ad268b`  
		Last Modified: Thu, 13 Feb 2025 01:12:50 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8de2566e75d95038fdbad435bbf665ab097b9121f7ce6ba8f2f16c7a4f2bbc`  
		Last Modified: Thu, 13 Feb 2025 01:12:46 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63364163922f4c4b0ed9aeaaf98c813c8909e4b07eabb896e293d7ab95d59246`  
		Last Modified: Thu, 13 Feb 2025 01:12:44 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:361d9bea6ff0bae437b444be4f841ddeb90a9a896143312795dc99553062c315`  
		Last Modified: Thu, 13 Feb 2025 01:12:44 GMT  
		Size: 77.5 KB (77465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da93bf675da24a4646649c036a31e6bce0333782853f12de9e2b37a61967b45`  
		Last Modified: Thu, 13 Feb 2025 01:12:44 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc1800600f1054499a4fa8da7891928fbae955501346a310ac7e456c5fa60b7d`  
		Last Modified: Thu, 13 Feb 2025 01:12:50 GMT  
		Size: 48.9 MB (48940952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d17ee63b0ca6b31dbf440e80d6af13b5b9bf32d7b9c6ab03e67706eb950b1e2`  
		Last Modified: Thu, 13 Feb 2025 01:12:44 GMT  
		Size: 97.5 KB (97527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
