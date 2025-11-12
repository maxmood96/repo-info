## `eclipse-temurin:8-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:5d4570ba33256908ec0944dc532f3b6b2f3f69580e967640cfc1f3b48301526b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `eclipse-temurin:8-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull eclipse-temurin@sha256:b2bc977e97c7cc2e1ad41c1195a5458aefc4cc6d920aba832212ac73a8dec3fd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228970241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fee0af1e71ca58610cb321c5101790c8cc65d36c20282bfb76ef118c4a3eaa2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 11 Nov 2025 20:10:27 GMT
SHELL [cmd /s /c]
# Tue, 11 Nov 2025 20:10:28 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Tue, 11 Nov 2025 20:10:28 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 11 Nov 2025 20:10:29 GMT
USER ContainerAdministrator
# Tue, 11 Nov 2025 20:10:31 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 11 Nov 2025 20:10:31 GMT
USER ContainerUser
# Tue, 11 Nov 2025 20:10:49 GMT
COPY dir:2635c350952b93f594bde5c3dd80336e4c4ce35889642cd7d3de9ae358e6cda3 in C:\openjdk-8 
# Tue, 11 Nov 2025 20:10:51 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc704c4257ca5dc0c86f854eff2df55a480551d342ee212cc3a99fcdb9018db`  
		Last Modified: Tue, 11 Nov 2025 20:11:34 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62958a8e9a781fada3830fd51047c3f3cde0d6b85845631731445ae423d98252`  
		Last Modified: Tue, 11 Nov 2025 20:11:34 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63eecfeb009eb64a162e1a6b928330b1493e61a769288ad4a0f10643e110ac17`  
		Last Modified: Tue, 11 Nov 2025 20:11:35 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4314d30523423744981e50532b7b70a0118da23396f686835f17da2063c366`  
		Last Modified: Tue, 11 Nov 2025 20:11:34 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12738ff4099d1c13655e4beda2406016f9b24ee778e1d0db5269876932d87fa2`  
		Last Modified: Tue, 11 Nov 2025 20:11:35 GMT  
		Size: 77.7 KB (77735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4831dd377d18cb918f11a0500bd256e239952a6b1ade037c7bf95570766f86`  
		Last Modified: Tue, 11 Nov 2025 20:11:35 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce25070529d8878f76ca413d6b6a17840a850d61e76c0000a8ad3bb664ca00f`  
		Last Modified: Tue, 11 Nov 2025 20:11:46 GMT  
		Size: 102.4 MB (102437992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758b519d7b2664b7970d8ccfe74d093a96d783908843c327213da7f201e8cf49`  
		Last Modified: Tue, 11 Nov 2025 20:11:35 GMT  
		Size: 100.2 KB (100162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
