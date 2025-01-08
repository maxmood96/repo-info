## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:ad41f2fe18ddadfee69e1b095ccd3419318c611f28ac74d41962874e1159b22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.20348.2966; amd64

```console
$ docker pull eclipse-temurin@sha256:9f4225f1012b990c975d409f51db4bc25f0746b549b87c0a167bbabfe04df347
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.1 MB (165090536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f007097646b9c85386962c72ca70f041c7f7c87d686d015083d010f00bcfcaa5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Dec 2024 01:18:54 GMT
RUN Apply image 10.0.20348.2966
# Wed, 11 Dec 2024 21:47:56 GMT
SHELL [cmd /s /c]
# Wed, 11 Dec 2024 21:47:57 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 11 Dec 2024 21:47:57 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 11 Dec 2024 21:47:58 GMT
USER ContainerAdministrator
# Wed, 11 Dec 2024 21:48:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Dec 2024 21:48:01 GMT
USER ContainerUser
# Wed, 11 Dec 2024 21:48:04 GMT
COPY dir:a15dacd11bbcaacf83a6b6e1490d6483ae4af68a125407fd4cb6bb7a70e4639c in C:\openjdk-11 
# Wed, 11 Dec 2024 21:48:08 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:f9d5d5ca3244fc2c429a892cbe6066394790f649f32d59acfdf012e490896378`  
		Last Modified: Tue, 10 Dec 2024 18:34:17 GMT  
		Size: 120.6 MB (120601318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef3a79478ad48f1e0e90ace8c4d93d59abfe31d2c50ee6b311c2e5ed5036e9f`  
		Last Modified: Wed, 11 Dec 2024 21:48:14 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b509500cba771d920fe5f87af5fa15c673f62545b0047bfce3c7448b867bfe20`  
		Last Modified: Wed, 11 Dec 2024 21:48:14 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a9e3f93bc2c77439ac3ba58c44e2d9f326206fabe6d6b00e55fe0f2f7cba8e`  
		Last Modified: Wed, 11 Dec 2024 21:48:13 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db23d9ed7ba2bd74c3cc84e6ddee0dd8c9aa8f43964938adf679b17a2b8f2ef`  
		Last Modified: Wed, 11 Dec 2024 21:48:12 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f50b7c8e2a401fd466f48a39fcbbbb012ddf7c13bb5897356dafdcd427e3d67`  
		Last Modified: Wed, 11 Dec 2024 21:48:12 GMT  
		Size: 75.9 KB (75860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:586e034520968665fa47687da18d75af79be3fa0a7a92a82b1239a729c8bc61a`  
		Last Modified: Wed, 11 Dec 2024 21:48:12 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956f88c9b37f2dac3068f2fa1b2c6955cdb02a490958b7f91dbb7afca75e55fd`  
		Last Modified: Wed, 11 Dec 2024 21:48:17 GMT  
		Size: 44.3 MB (44309479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da55e1698648b446cb4a3c004621f2cb0faa93b94d687a580fcd2e3de6d3cb64`  
		Last Modified: Wed, 11 Dec 2024 21:48:12 GMT  
		Size: 98.7 KB (98716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.17763.6659; amd64

```console
$ docker pull eclipse-temurin@sha256:5624b88b9d3deb4581c44730496b835d3862670b20b7eb045f7518cdc982dab6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.7 MB (199724370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f664a33547675bb7752d63ac2ff9854d23b884d2de51af9359b07fd5ed7fa1b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Wed, 11 Dec 2024 21:43:49 GMT
SHELL [cmd /s /c]
# Wed, 11 Dec 2024 21:43:50 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 11 Dec 2024 21:43:50 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 11 Dec 2024 21:43:51 GMT
USER ContainerAdministrator
# Wed, 11 Dec 2024 21:43:53 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Dec 2024 21:43:54 GMT
USER ContainerUser
# Wed, 11 Dec 2024 21:43:58 GMT
COPY dir:a15dacd11bbcaacf83a6b6e1490d6483ae4af68a125407fd4cb6bb7a70e4639c in C:\openjdk-11 
# Wed, 11 Dec 2024 21:44:02 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Tue, 10 Dec 2024 21:03:34 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c068b62d88b5b79cfbdf44568d1ff918b65241f593ce632ac92e7de65aa1722e`  
		Last Modified: Wed, 11 Dec 2024 21:44:08 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d76f417169f7b87472419551ed78472e421501f61f505c0c7116716e1db673`  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2778987866d642bccdc61db386dea813cb898755ce15a83409fe105248dae9b2`  
		Last Modified: Wed, 11 Dec 2024 21:44:08 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ef8b8866bf38c5789401afefdee73e7ac829e75d3b03838534639f72a4022c`  
		Last Modified: Wed, 11 Dec 2024 21:44:05 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:433db8527f0d66a532b299fdb92afb37b97592a45412e9af4a9c39e98a757582`  
		Last Modified: Wed, 11 Dec 2024 21:44:06 GMT  
		Size: 71.7 KB (71689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd7aba15e660513d47a6861cd5a21f07a24aa6a954b4bf78355b49982b3c2b6`  
		Last Modified: Wed, 11 Dec 2024 21:44:05 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffc5d13bb8c289c766d24390753ceae973639c21b0df7d0d49737c8342216f7`  
		Size: 44.3 MB (44308575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7719eaf8beec98af78ad883734d6090e9d74dcb3afabd691fd1e3c3b5bf00c49`  
		Last Modified: Wed, 11 Dec 2024 21:44:05 GMT  
		Size: 107.3 KB (107284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
