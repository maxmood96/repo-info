## `eclipse-temurin:8u432-b06-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:9615bde837619c47a443234ec00699d997d1fc08997af5176c6488e4cdd032fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `eclipse-temurin:8u432-b06-jre-nanoserver` - windows version 10.0.20348.2966; amd64

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

### `eclipse-temurin:8u432-b06-jre-nanoserver` - windows version 10.0.17763.6659; amd64

```console
$ docker pull eclipse-temurin@sha256:f6ee7b843f40b00d163543dddb0449165613de50b5da7330aa5ca724acc59135
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.5 MB (196482652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3688718dc6c2cdb6c268dbe88796077287e15c7251268b50f338cdf06ef8b5df`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Wed, 11 Dec 2024 21:45:53 GMT
SHELL [cmd /s /c]
# Wed, 11 Dec 2024 21:45:55 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 11 Dec 2024 21:45:56 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 11 Dec 2024 21:45:56 GMT
USER ContainerAdministrator
# Wed, 11 Dec 2024 21:45:58 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Dec 2024 21:45:59 GMT
USER ContainerUser
# Wed, 11 Dec 2024 21:46:03 GMT
COPY dir:47bf2d2ef237403b98ba2f50909368ef2c147e2a609dd71db23cc690a276ad54 in C:\openjdk-8 
# Wed, 11 Dec 2024 21:46:07 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Tue, 10 Dec 2024 21:03:34 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9626640ab423cd0a88acb52877e09b09fad63f8f6654e7d53b80b30493a06cb8`  
		Last Modified: Wed, 11 Dec 2024 21:46:13 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab68430d7008da3888cc7bf0e9401d7d0a4380ac9961daaac11bf6f40e957ead`  
		Last Modified: Wed, 11 Dec 2024 21:46:13 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45745804f32211f15451a0e9e492596a076472a4f8f2e6d34268abf61e0c48b8`  
		Last Modified: Wed, 11 Dec 2024 21:46:13 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13bed07e8b854a18420062f120de24c07ad119e6687264d45e4d1aa1adbfadbb`  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339f8db0ec15b7a736298c44dff64927e47ba08a54bcc7754e2e90301be636bc`  
		Last Modified: Wed, 11 Dec 2024 21:46:11 GMT  
		Size: 83.8 KB (83826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9b21e65a692fdbd230e54f8291c0fd8c6aa3113c7b29bf89fe55059016573f`  
		Last Modified: Wed, 11 Dec 2024 21:46:11 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca104cf90f00a095c582dd65bcce29def7a6260e59739a87b39e8ff537a4481`  
		Last Modified: Wed, 11 Dec 2024 21:46:14 GMT  
		Size: 41.1 MB (41061481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ad61c8730cbe4bb0501a870816236a052ad56e51664dde917a15377d1144cd`  
		Last Modified: Wed, 11 Dec 2024 21:46:11 GMT  
		Size: 100.3 KB (100316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
