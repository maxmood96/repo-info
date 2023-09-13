## `eclipse-temurin:11-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:75df048ba45036195df189479db44c3bb83e9ec282488fd5ea19c054580d798d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1970; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2022` - windows version 10.0.20348.1970; amd64

```console
$ docker pull eclipse-temurin@sha256:68385127137832679b1b61c301eda8a451199a7bcc63db554fe6aab702f937de
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.9 MB (163939158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5cd60f66bcf25f9279535cbc9f2c8da7d7a33f1d196b647749f9a65e4653a59`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 01 Sep 2023 00:20:14 GMT
RUN Apply image 10.0.20348.1970
# Wed, 13 Sep 2023 03:28:54 GMT
SHELL [cmd /s /c]
# Wed, 13 Sep 2023 03:30:07 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Wed, 13 Sep 2023 03:30:08 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 13 Sep 2023 03:30:08 GMT
USER ContainerAdministrator
# Wed, 13 Sep 2023 03:30:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Sep 2023 03:30:16 GMT
USER ContainerUser
# Wed, 13 Sep 2023 03:30:59 GMT
COPY dir:8fefe94e6208edfa85d9fa21e3e899009fbc5498c10b88818044df54f9a7b652 in C:\openjdk-11 
# Wed, 13 Sep 2023 03:31:07 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:8f8cef0759210af9d01a2fb45d79956a2db738bbd3734b7244b17e14ad945cab`  
		Last Modified: Tue, 12 Sep 2023 18:47:39 GMT  
		Size: 120.6 MB (120567584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d67aef4c483590cefd40495efc212f13e4c62993e8036c20bb4e19bc8620508`  
		Last Modified: Wed, 13 Sep 2023 03:47:03 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a0b30f2089f682233e849be924051a10d628f414320caac8a5a6f50b98d15e`  
		Last Modified: Wed, 13 Sep 2023 03:47:43 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b7cce41e641a325af63bf023a73c01e332b7e83e98b12728c75261f7c241c8`  
		Last Modified: Wed, 13 Sep 2023 03:47:43 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd204e8f2437159f557f90ecd6b3c0f3c7aaafdb4cc8be3ba9b4960934edd74e`  
		Last Modified: Wed, 13 Sep 2023 03:47:43 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31acb22a6c8082f300c7132162fb8038358488a6f8bbdfd550c5cc1113a417eb`  
		Last Modified: Wed, 13 Sep 2023 03:47:41 GMT  
		Size: 86.8 KB (86798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe12df0fdfaaab58abba8ee6bf0b57eb81b8b88f8332eab856004b6045687499`  
		Last Modified: Wed, 13 Sep 2023 03:47:41 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87c966a81f2e1a21c5cf02dec49f8e1e391920590845fbbdfde2f8de8e23fcb`  
		Last Modified: Wed, 13 Sep 2023 03:48:22 GMT  
		Size: 43.2 MB (43218578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311cebd0471f91d9bf9ce577f636037e23f5880ae600a64947029328750f8067`  
		Last Modified: Wed, 13 Sep 2023 03:48:14 GMT  
		Size: 60.9 KB (60859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
