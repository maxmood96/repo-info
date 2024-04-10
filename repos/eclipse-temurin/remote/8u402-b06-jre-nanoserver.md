## `eclipse-temurin:8u402-b06-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:ce4ca9c2aa55b5141f345121c0b3ec4d36ee8a85a8f8d1de8266fecfef990e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `eclipse-temurin:8u402-b06-jre-nanoserver` - windows version 10.0.20348.2402; amd64

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

### `eclipse-temurin:8u402-b06-jre-nanoserver` - windows version 10.0.17763.5696; amd64

```console
$ docker pull eclipse-temurin@sha256:90b1dc7e2a32e687b807f7a312416a51326a67f2341a222ed52d86551981ddc3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145164937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:319ee8757f988129758e81d9fd6c613541a63a473f55b0cec7c888a6a66723fc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Tue, 09 Apr 2024 23:42:55 GMT
SHELL [cmd /s /c]
# Tue, 09 Apr 2024 23:42:55 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Tue, 09 Apr 2024 23:42:56 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 09 Apr 2024 23:42:57 GMT
USER ContainerAdministrator
# Tue, 09 Apr 2024 23:43:11 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Apr 2024 23:43:12 GMT
USER ContainerUser
# Tue, 09 Apr 2024 23:48:37 GMT
COPY dir:db8ed4bc6cf3fc1a9a530d737bd8bcda792821f4f1e3e610cedaee77629ebb36 in C:\openjdk-8 
# Tue, 09 Apr 2024 23:48:48 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b591b5f81c02344da39dc8a9084b5791cbf552c1eb85e79db1f38dfc715a681`  
		Last Modified: Wed, 10 Apr 2024 00:47:46 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f488ee65de2b011deb88b648a2fd4a8df01a6335e42405d991c1303f90ecc8`  
		Last Modified: Wed, 10 Apr 2024 00:47:46 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852d1dc582f1e8accc43aef8daeca6eb89735a124fb1f967b7f73ef3f9be2e91`  
		Last Modified: Wed, 10 Apr 2024 00:47:46 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576c3d12347d0a39213fcd0330b9f36d0b8dd7f058cb28dc6c5a90efab178eb6`  
		Last Modified: Wed, 10 Apr 2024 00:47:44 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1e9364eb12671c19584d282ec60e21d04e812386049c863e0a536a61ada0e3`  
		Last Modified: Wed, 10 Apr 2024 00:47:44 GMT  
		Size: 66.6 KB (66551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c2b0dd596df841ed6302a2df14e30ef0baac11bcf940216ef52ac8afbde390`  
		Last Modified: Wed, 10 Apr 2024 00:47:44 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05475690ba99de61f49f9bcb963ea2e28d247dae783aa516ab53eafc5310208`  
		Last Modified: Wed, 10 Apr 2024 00:48:59 GMT  
		Size: 40.1 MB (40117597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58cfd7c63fadcc806fa012d963fd773e9269931da21c0c92d85d290a1401eac`  
		Last Modified: Wed, 10 Apr 2024 00:48:53 GMT  
		Size: 85.9 KB (85885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
