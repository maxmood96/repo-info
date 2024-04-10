## `eclipse-temurin:8-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:10cce44ebe5b5cf60a19907d14b8554e47a8225d11f20cf6d1eda98193984267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `eclipse-temurin:8-nanoserver-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull eclipse-temurin@sha256:4a3859eed9e24bd8c8f8b087502d0ee45cb59287f04f719acd9d3ef9571f8e27
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.8 MB (222834738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3a2f7310893035a2866adc771146992dd9694b54929d3cf8ec6b84cda0171ab`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Apr 2024 08:53:11 GMT
RUN Apply image 10.0.20348.2402
# Wed, 10 Apr 2024 00:34:53 GMT
SHELL [cmd /s /c]
# Wed, 10 Apr 2024 00:34:54 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 10 Apr 2024 00:34:54 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 10 Apr 2024 00:34:55 GMT
USER ContainerAdministrator
# Wed, 10 Apr 2024 00:35:10 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Apr 2024 00:35:11 GMT
USER ContainerUser
# Wed, 10 Apr 2024 00:35:22 GMT
COPY dir:9ab35a15e19e8247451d444f7de2a75fe407ec1749c1b49082dcaaef6c80dafd in C:\openjdk-8 
# Wed, 10 Apr 2024 00:35:36 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:755fc767289b8847bd0d0d8d75efc308c040140acf2a3426973ba9fbf022c4c0`  
		Last Modified: Tue, 09 Apr 2024 23:50:18 GMT  
		Size: 121.0 MB (120993754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70887eeae6a5d6d5fd81661024afc84fee637f674dee5e7127112cbfce90750`  
		Last Modified: Wed, 10 Apr 2024 01:00:01 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd369f71bfeb425febd0cb510cb4c9904a6bec60ab46b466e761190e244d9ee1`  
		Last Modified: Wed, 10 Apr 2024 01:00:01 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fdd090c0db7881c3fd71359ac85fad26d43fe49f00cda0db36a7f686862774`  
		Last Modified: Wed, 10 Apr 2024 01:00:01 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a90fda6e59486b3e82428b9b4d8cf5a0c65fafae19b5cfaa4bbf6c6afa4c33`  
		Last Modified: Wed, 10 Apr 2024 00:59:59 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f453fdeaa33949f1dcf97095e30de2e3f0392b664ad8db13e40ced433dc174da`  
		Last Modified: Wed, 10 Apr 2024 00:59:59 GMT  
		Size: 82.3 KB (82309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc74f2c03cd05ca283b9db155909c55bd367e6cdb3c93546180455a1f077a1a2`  
		Last Modified: Wed, 10 Apr 2024 00:59:59 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f247cf0f729be399cdb4fe289896cd46a646141b7faf6a0f89587412b96debb3`  
		Last Modified: Wed, 10 Apr 2024 01:00:11 GMT  
		Size: 101.7 MB (101692842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fcbddbddc9f5db3cfa396637876e577d0034851b49fdceccbb4ce7f8067c10`  
		Last Modified: Wed, 10 Apr 2024 00:59:59 GMT  
		Size: 60.7 KB (60669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
