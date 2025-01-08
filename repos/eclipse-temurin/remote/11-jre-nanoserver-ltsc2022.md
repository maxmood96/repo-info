## `eclipse-temurin:11-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:77a1d8c2011ab1268db6dc9ab6c0f1b85ad90c17fcbdee8ac2adb979d84afdd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2966; amd64

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
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a9e3f93bc2c77439ac3ba58c44e2d9f326206fabe6d6b00e55fe0f2f7cba8e`  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db23d9ed7ba2bd74c3cc84e6ddee0dd8c9aa8f43964938adf679b17a2b8f2ef`  
		Last Modified: Wed, 11 Dec 2024 21:48:12 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f50b7c8e2a401fd466f48a39fcbbbb012ddf7c13bb5897356dafdcd427e3d67`  
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
