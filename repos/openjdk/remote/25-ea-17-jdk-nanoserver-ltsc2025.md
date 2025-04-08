## `openjdk:25-ea-17-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:a7532891361d352928466a1f548c2225e642060865f2915b9d8db884442cbe6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `openjdk:25-ea-17-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull openjdk@sha256:503c63806ab9c0452c2fbab9a34bf81a15e7d448b8b8a0bcd2fb0342a3acd029
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.5 MB (414455841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44a73d81243956c533feb16e6a82fe649cb1a727b82e646b86201a89b87531f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Mon, 07 Apr 2025 23:48:12 GMT
SHELL [cmd /s /c]
# Mon, 07 Apr 2025 23:48:12 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 07 Apr 2025 23:48:13 GMT
USER ContainerAdministrator
# Mon, 07 Apr 2025 23:48:16 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 07 Apr 2025 23:48:16 GMT
USER ContainerUser
# Mon, 07 Apr 2025 23:48:17 GMT
ENV JAVA_VERSION=25-ea+17
# Mon, 07 Apr 2025 23:48:25 GMT
COPY dir:31d4a08dd20e935927d81b33c56eb56ceaeead96529382a0c30c5f89fc836ee7 in C:\openjdk-25 
# Mon, 07 Apr 2025 23:48:32 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 07 Apr 2025 23:48:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b9ab54e1e778652e40f22bf7a2b51c00e90344a8188b86995b570cc32e8cb1`  
		Last Modified: Mon, 07 Apr 2025 23:48:38 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6241a00f7e4291236b5f35f5b95757f175ce0f7647733a36123d7a96c5e2f1`  
		Last Modified: Mon, 07 Apr 2025 23:48:38 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50e1bee598d64563fad7b0944759d98cfa68f121b82568f022809ba81f2f27b`  
		Last Modified: Mon, 07 Apr 2025 23:48:38 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2e103c7b6496251d6614ed5457c3c08e00a9e7574ea6de96cf8deef47da69a`  
		Last Modified: Mon, 07 Apr 2025 23:48:38 GMT  
		Size: 76.4 KB (76370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc0bd25cf59f5f41f37bc1132f8703b58d3fc498e2a6181691255f1314da968`  
		Last Modified: Mon, 07 Apr 2025 23:48:36 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabd5e3565a3c3387ee3e6812e3331f1fe1eff6b9e1f7335d52e4e7daae1443f`  
		Last Modified: Mon, 07 Apr 2025 23:48:36 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76275c5753cb3bb64649bc05f1bc242645a2b1ca36ea6ff0388aaf5f5d07b3d8`  
		Last Modified: Mon, 07 Apr 2025 23:48:49 GMT  
		Size: 208.0 MB (207956286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7df0f25bafe0c3c1973b597b568ac08a4db9366017044d23a10fe2e4537c812`  
		Last Modified: Mon, 07 Apr 2025 23:48:36 GMT  
		Size: 114.6 KB (114626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47260128b74b04275aea21e96390a1a9ba06361b68069c5b2c7621e91b7031e`  
		Last Modified: Mon, 07 Apr 2025 23:48:36 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
