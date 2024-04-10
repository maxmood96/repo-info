## `eclipse-temurin:8-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:861318833d3c1df2f17cdbbfc8d4927c768e40a5b2233651325ea02c485e2a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull eclipse-temurin@sha256:5f31ed45d23b3ef558165a57ad9216f437d0e6f066f620de858839e72083e1f2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161254834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b41ec1f5d8e8d46c3a92f1db6f3896bd4374ae762a1a8f705260fbe79749e6`
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
# Wed, 10 Apr 2024 00:35:52 GMT
COPY dir:db8ed4bc6cf3fc1a9a530d737bd8bcda792821f4f1e3e610cedaee77629ebb36 in C:\openjdk-8 
# Wed, 10 Apr 2024 00:36:04 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:65cfeb19f401711b3d01ff54fb985dc56a68201eb0d31da3222c0b9fad55b9cb`  
		Last Modified: Wed, 10 Apr 2024 01:00:40 GMT  
		Size: 40.1 MB (40112878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3aa469ec10b927b1ddadb34953ee723646cf73cf867d1d8bbd1ae3e22355a13`  
		Last Modified: Wed, 10 Apr 2024 01:00:34 GMT  
		Size: 60.7 KB (60729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
