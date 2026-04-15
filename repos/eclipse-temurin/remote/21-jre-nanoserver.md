## `eclipse-temurin:21-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:1fa6a7552bff4512395187e0226468fd293f9c7fe58ff25e75f1cb775e014f96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.26100.32690; amd64

```console
$ docker pull eclipse-temurin@sha256:ee1ec4c8970d571f32ad2f440ec09debd6c37d75a5468f2af6cbaa78207f6539
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248946245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c6369af5af7cf59c4cbea3989abe0fbf989091c8c8386ef9f2e07918d6ff5a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 06:39:57 GMT
RUN Apply image 10.0.26100.32690
# Tue, 14 Apr 2026 22:10:47 GMT
SHELL [cmd /s /c]
# Tue, 14 Apr 2026 22:12:57 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 14 Apr 2026 22:12:57 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 14 Apr 2026 22:12:58 GMT
USER ContainerAdministrator
# Tue, 14 Apr 2026 22:13:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Apr 2026 22:13:00 GMT
USER ContainerUser
# Tue, 14 Apr 2026 22:13:13 GMT
COPY dir:60f2977da675e9d6a11be1282de5c19d751a1b21ff04571f86a073fb3e930423 in C:\openjdk-21 
# Tue, 14 Apr 2026 22:13:16 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:8af320c3b6d19296bcc7947e3beb8bc0c69cb12143db52efe988dc998ac088dc`  
		Last Modified: Tue, 14 Apr 2026 21:00:37 GMT  
		Size: 199.7 MB (199717094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9283504e7a4dc0b9369ebeee673efd11bfea17126a3b7e1ef073687a6f63449`  
		Last Modified: Tue, 14 Apr 2026 22:11:40 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a84c04a7a7fd351003487b53348bec3bb21717f745c84abf08d5a4eadbd2092`  
		Last Modified: Tue, 14 Apr 2026 22:13:21 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0bd90af5c1282bff42a07605439d017a4c2a952c26dac19c0cdd7a284f04fa`  
		Last Modified: Tue, 14 Apr 2026 22:13:21 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85eab2d91acfb104568ce6d0b722b5445977120fedbb8f2718294e19c404608`  
		Last Modified: Tue, 14 Apr 2026 22:13:20 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7bd50d66ecd9b25eeef58540fb1ddfa68a80fca4d86e89db4514ee1de9d2fd`  
		Last Modified: Tue, 14 Apr 2026 22:13:20 GMT  
		Size: 72.0 KB (72048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbab15da4f17a604ce01fb20d275fafabd987e80d33cb3c9ec40cb48fca9f26d`  
		Last Modified: Tue, 14 Apr 2026 22:13:20 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61665e2923deb8ff50d36d9b43677d9743e5293c0a67b6dc0a3c7bcedde9223`  
		Last Modified: Tue, 14 Apr 2026 22:13:26 GMT  
		Size: 49.0 MB (49039598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e95ac13808bb0f753f3f81471bea0d4124875dc1f4470c35c8674cf4047fad`  
		Last Modified: Tue, 14 Apr 2026 22:13:20 GMT  
		Size: 112.1 KB (112132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.20348.5020; amd64

```console
$ docker pull eclipse-temurin@sha256:bb8efc712a5c32390a6c761a34b082718d6424f0bd7a0568a76d40978ee31ab6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176178128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a16aa81ed4720b7061ba6566d14d96d91e6205bc40b9df0c218a77f5d33807e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 22:10:49 GMT
SHELL [cmd /s /c]
# Tue, 14 Apr 2026 22:11:31 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 14 Apr 2026 22:11:32 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 14 Apr 2026 22:11:32 GMT
USER ContainerAdministrator
# Tue, 14 Apr 2026 22:11:34 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Apr 2026 22:11:34 GMT
USER ContainerUser
# Tue, 14 Apr 2026 22:11:38 GMT
COPY dir:60f2977da675e9d6a11be1282de5c19d751a1b21ff04571f86a073fb3e930423 in C:\openjdk-21 
# Tue, 14 Apr 2026 22:11:41 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f577f04bf25fbe8b679de7ed1a1bb3aec05c54b5f22de311414b5b7e7dbe8fb5`  
		Last Modified: Tue, 14 Apr 2026 22:11:03 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f444cfaf66d2af85ad6c92d04d5d6294b282dfdca36b3f3d82c279039afbc7e`  
		Last Modified: Tue, 14 Apr 2026 22:11:46 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995b7bf9fe66ba46bb9f9afd85246167ea95c6afc06faeac49117fcf0e4eaf1a`  
		Last Modified: Tue, 14 Apr 2026 22:11:46 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b53bc8ff0a7ea651a55f4507aac5405943c2142f42599cec84a1005e004e204a`  
		Last Modified: Tue, 14 Apr 2026 22:11:45 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67aee23622aca747022f74995e0f00db4ab78d0ba370fc77c98084dff75fa518`  
		Last Modified: Tue, 14 Apr 2026 22:11:45 GMT  
		Size: 77.2 KB (77185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746620e945807c6fb1baa15a2230bd82b6c228e2e427526d1c674bb7dca462a9`  
		Last Modified: Tue, 14 Apr 2026 22:11:45 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a12a0aa810e10289d117eba50ee116f25aa3adc7ecb36a5e3782141fd19e035`  
		Last Modified: Tue, 14 Apr 2026 22:11:51 GMT  
		Size: 49.0 MB (49039685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebbe38fc3f73a660bcbc999f7669099e711dc22c9190a897bc9c0c808a1f5a3`  
		Last Modified: Tue, 14 Apr 2026 22:11:45 GMT  
		Size: 100.0 KB (100009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
