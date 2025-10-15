## `openjdk:26-ea-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:21fc0f66fd1903e1052a8f1e12bd5b50cebc1968e7f94d48eca108ddc427e084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6899; amd64

### `openjdk:26-ea-nanoserver-ltsc2025` - windows version 10.0.26100.6899; amd64

```console
$ docker pull openjdk@sha256:b8357191323892b2d5c8dabd939f16fce37b7253aa13d99ae2f2658ba0c28a40
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.4 MB (415423164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c7b36caf2be29333f4eb56729ec345c4daca350826aa31437a96b113bebec2b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 11 Oct 2025 15:58:41 GMT
RUN Apply image 10.0.26100.6899
# Tue, 14 Oct 2025 21:13:11 GMT
SHELL [cmd /s /c]
# Tue, 14 Oct 2025 21:14:45 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 14 Oct 2025 21:14:45 GMT
USER ContainerAdministrator
# Tue, 14 Oct 2025 21:14:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 14 Oct 2025 21:14:47 GMT
USER ContainerUser
# Tue, 14 Oct 2025 21:14:48 GMT
ENV JAVA_VERSION=26-ea+19
# Tue, 14 Oct 2025 21:14:57 GMT
COPY dir:83313e74e1bdca6c4da8521f7958b3cb9f989c8b9d5087396f320ade6e966d10 in C:\openjdk-26 
# Tue, 14 Oct 2025 21:15:02 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 14 Oct 2025 21:15:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:463edd10ad50b00cf92c69fc3eaa85e1fa40aad1b7938fa232899405bd80f001`  
		Last Modified: Tue, 14 Oct 2025 22:41:48 GMT  
		Size: 194.0 MB (194026741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f719d194ebc9e8b3b0637194afed2f42674cc3cd5b8a6ea2a1646a122f9fd22`  
		Last Modified: Tue, 14 Oct 2025 21:14:15 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7a2554bef5aef7b217fafc55e32cebbfef635abdb564393c8e6c88b4ff14a7`  
		Last Modified: Tue, 14 Oct 2025 21:15:28 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef6345790f3f0e35ae3ebbceb18c91bae7c77ccae0290cf2bdc0ce116daebbd`  
		Last Modified: Tue, 14 Oct 2025 21:15:28 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb8fc2276cbf80acbaadde3a30d70827fb9c38b4f167da37f43046e472f25ec`  
		Last Modified: Tue, 14 Oct 2025 21:15:27 GMT  
		Size: 72.8 KB (72776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bd5ae75af4c15ff59a521c667b6b9201749b5e5b8b1487810cd7b07f4e9d9d`  
		Last Modified: Tue, 14 Oct 2025 21:15:28 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70e5f7454e8f4aab1bea2e0e8f9c43758b246a42cebcd12ffc51dd9e26849878`  
		Last Modified: Tue, 14 Oct 2025 21:15:27 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f751e437b62cdc3c3958f9f7c4985bbeea3649144b0caaa4675fa899dc4e9556`  
		Last Modified: Wed, 15 Oct 2025 00:24:10 GMT  
		Size: 221.2 MB (221200542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6265efa5eae3b1c3406d85ff387003b7673d63abed571db6c1b02c541c52d3e`  
		Last Modified: Tue, 14 Oct 2025 21:15:27 GMT  
		Size: 116.7 KB (116724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4dd01d33eec031fc9b787f257f6c59a119c1b1e00cb1eeabd48dcb728dc1e3c`  
		Last Modified: Tue, 14 Oct 2025 21:15:27 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
