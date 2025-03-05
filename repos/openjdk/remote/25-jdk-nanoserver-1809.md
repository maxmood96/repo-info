## `openjdk:25-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:f1d4bc718c2e09a2f6b647bfe372c8a52b116e6cda5664c7fab588ab23c12c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `openjdk:25-jdk-nanoserver-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull openjdk@sha256:a1f40899fe1e9c05347d364d6771066bc7ece4fb88efb60349b9954b49c2b9d1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.9 MB (318908882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1001f1f40cd52bb4596dc106a60ee18bfdd930195daf34f1c43ed3dc32627ecc`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Tue, 04 Mar 2025 22:43:40 GMT
SHELL [cmd /s /c]
# Tue, 04 Mar 2025 22:43:42 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 04 Mar 2025 22:43:43 GMT
USER ContainerAdministrator
# Tue, 04 Mar 2025 22:44:01 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 04 Mar 2025 22:44:01 GMT
USER ContainerUser
# Tue, 04 Mar 2025 22:44:01 GMT
ENV JAVA_VERSION=25-ea+12
# Tue, 04 Mar 2025 22:44:12 GMT
COPY dir:e3a80d16f60f733e38f65676798afaa74a4cc6b6b9e0edd1774eacf12556d4ac in C:\openjdk-25 
# Tue, 04 Mar 2025 22:44:17 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 04 Mar 2025 22:44:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061f782b9fd12caea0f483589b063feb21f942f137d798e5bb3d27b990df9723`  
		Last Modified: Tue, 04 Mar 2025 22:44:22 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724cd741e3cd0f7dd0f6a6ffab21d57c4101e4b1acc0e57f35f469f90015299b`  
		Last Modified: Tue, 04 Mar 2025 22:44:21 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7025f713263ca3e5013a9701ce60f4350f08da9b7791caf087eeefcbe93d76`  
		Last Modified: Tue, 04 Mar 2025 22:44:21 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a88d13e78e2d7a96ebf7242ea66cec5283fc3791960c83b8951f76a4ed41e6`  
		Last Modified: Tue, 04 Mar 2025 22:44:21 GMT  
		Size: 68.0 KB (68039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75464489d8b70232cd685e65d80fa11fd59be46d15f0f7b628458aa92c344f0c`  
		Last Modified: Tue, 04 Mar 2025 22:44:20 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39c0df8e4d1e5fe657d0f5c059dce25d242383979d6b706602edebfc3930b16`  
		Last Modified: Tue, 04 Mar 2025 22:44:20 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6378fee93d5717240e23b0a00bd12e2f6088c600d932534064bee9911e8c18e0`  
		Last Modified: Tue, 04 Mar 2025 22:44:31 GMT  
		Size: 207.5 MB (207541773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c6922e19d3083228c3f79ffde53bae177b36c6e9ab6f5e8df3dc356820d9cf`  
		Last Modified: Tue, 04 Mar 2025 22:44:21 GMT  
		Size: 4.4 MB (4377320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d1343abfc49ef5c40bf1ecb5cca0d3e4b42a481948b8753347c498ead5b27f`  
		Last Modified: Tue, 04 Mar 2025 22:44:20 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
