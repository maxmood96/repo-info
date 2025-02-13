## `openjdk:25-ea-nanoserver`

```console
$ docker pull openjdk@sha256:f61b91660b0a788d9b2069d3d89aa939d8f7f81a27601b29eba05d79d3c63ffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `openjdk:25-ea-nanoserver` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:752e40e0e9df0eda0913ece08efe1b6e61061415e7e6168c1fbce6752c4a9cc6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406721025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48f25b3d30f91109a203c991569e60a7527e157b92472b9e04e1b9f2a41013d7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Tue, 11 Feb 2025 01:31:41 GMT
SHELL [cmd /s /c]
# Tue, 11 Feb 2025 01:31:41 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 11 Feb 2025 01:31:42 GMT
USER ContainerAdministrator
# Tue, 11 Feb 2025 01:31:44 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 11 Feb 2025 01:31:45 GMT
USER ContainerUser
# Tue, 11 Feb 2025 01:31:45 GMT
ENV JAVA_VERSION=25-ea+9
# Tue, 11 Feb 2025 01:31:52 GMT
COPY dir:d7acfa7ae78317b124adc15f4373b266207aef9ee64c7b37ba0d0b39bb9389f0 in C:\openjdk-25 
# Tue, 11 Feb 2025 01:31:58 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 11 Feb 2025 01:31:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Wed, 22 Jan 2025 08:02:27 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140e01ee1c13ca37b35e581776495593f51e7a6c29eb4e65c935b423854548e0`  
		Last Modified: Wed, 12 Feb 2025 21:50:50 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893b118f97c0dd29192d5157cd21eeb0e7425a1822414c62f52df9c772e33434`  
		Last Modified: Wed, 12 Feb 2025 21:50:51 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88b3541f10dd70bdb925a68c463698e497a4100094a19071b3fa735fef1f9ef`  
		Last Modified: Wed, 12 Feb 2025 21:50:52 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686d895ffc360568bd1ca652853ebfc0740f2c68411fa22aea870a758f93ab86`  
		Last Modified: Wed, 12 Feb 2025 21:50:52 GMT  
		Size: 75.7 KB (75706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da557ece925761d9dd9b9a55b0c0869ee07f55ab894886c678e7fbf594d2da1`  
		Last Modified: Wed, 12 Feb 2025 21:50:54 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb254d90661960d93bb4389fadd62504c23aa9b057499c72767795e53c56917`  
		Last Modified: Wed, 12 Feb 2025 21:50:55 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029cdb3cc24f6d6c4f82d78fa2d56a1e630550c26df478a5724bf27b1b150a9d`  
		Last Modified: Tue, 11 Feb 2025 01:32:14 GMT  
		Size: 207.5 MB (207492194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5460dd801f2e3569b985d6c87605a6c98c480f579f63d910e3463348a3edb37d`  
		Last Modified: Wed, 12 Feb 2025 21:51:43 GMT  
		Size: 92.5 KB (92461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2cb44344e4b0b8d7a6497fb04ffaf43476061e7b935924af9ff8a1131c1bd03`  
		Last Modified: Wed, 12 Feb 2025 21:51:44 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
