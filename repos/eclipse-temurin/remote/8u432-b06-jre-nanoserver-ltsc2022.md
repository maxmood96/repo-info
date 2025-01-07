## `eclipse-temurin:8u432-b06-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:9440d52d90dac7e724d1ee96b173252cda8ede86baca1b4c4df55150cc743341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `eclipse-temurin:8u432-b06-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull eclipse-temurin@sha256:4e292cd928c3b59ce99acca6b27ad98c2a7fa04b95af8dfc769cc8a5fc96103b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.8 MB (161844695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69c1ae9bb727269d381ced3a354129cac20b99d99ffe6903c93252ea0d1d899`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Dec 2024 01:18:54 GMT
RUN Apply image 10.0.20348.2966
# Wed, 11 Dec 2024 21:47:53 GMT
SHELL [cmd /s /c]
# Wed, 11 Dec 2024 21:47:53 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 11 Dec 2024 21:47:54 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 11 Dec 2024 21:47:54 GMT
USER ContainerAdministrator
# Wed, 11 Dec 2024 21:47:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Dec 2024 21:47:57 GMT
USER ContainerUser
# Wed, 11 Dec 2024 21:48:00 GMT
COPY dir:47bf2d2ef237403b98ba2f50909368ef2c147e2a609dd71db23cc690a276ad54 in C:\openjdk-8 
# Wed, 11 Dec 2024 21:48:03 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:f9d5d5ca3244fc2c429a892cbe6066394790f649f32d59acfdf012e490896378`  
		Last Modified: Tue, 10 Dec 2024 18:34:17 GMT  
		Size: 120.6 MB (120601318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db25314a3bd3e1657c211e02dac4ab06325714a369a8588f6fb72173219f2cb`  
		Last Modified: Wed, 11 Dec 2024 21:48:07 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21d1ecd1a36ee9c8bde40c097b3c7e08c1ca041a78770920d0d0e80c3ff1558`  
		Last Modified: Wed, 11 Dec 2024 21:48:07 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ad598a356a6f9103ea648e1045e394596ce4f272697aa15e5f60b7702b72ca`  
		Last Modified: Wed, 11 Dec 2024 21:48:07 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef89821502fc7a1e0c9a134ab370ade8bbc54367ebaf94d526bbe4136ba36ed1`  
		Last Modified: Wed, 11 Dec 2024 21:48:06 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d7befd8f911c2e48043b8c5a854be05153147aa0d5c6661e17d756ac5757cf`  
		Last Modified: Wed, 11 Dec 2024 21:48:06 GMT  
		Size: 75.9 KB (75916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4935d4f670d0ae79363928de6bc74820ecb06063e40a1395a8bad07dcfadab9d`  
		Last Modified: Wed, 11 Dec 2024 21:48:06 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de2e16120b48668d0bfa4a809e30d7ea4d9dd2edb3b9a7de8c07d20ffc33ced`  
		Size: 41.1 MB (41061297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706c2292077489bff2f9fefa73028981656f6536db977ccde0ea0f196c707ebe`  
		Last Modified: Wed, 11 Dec 2024 21:48:06 GMT  
		Size: 101.0 KB (100995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
