## `openjdk:24-ea-32-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:7a5ee3ae7094e702cafe9d34cfaeae4364b0b1939d9cfd0b27b2f3c24a54b6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `openjdk:24-ea-32-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:9535bc132d436271893c0543a35fc4d96b68bb5074e29cfd75ef750bf6df74fb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.3 MB (329339495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd61edc757b9cbf4ed1e4133b0e5978649e0e1e35eb25c178dd88e62af1c09b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Thu, 23 Jan 2025 23:08:16 GMT
SHELL [cmd /s /c]
# Thu, 23 Jan 2025 23:08:17 GMT
ENV JAVA_HOME=C:\openjdk-24
# Thu, 23 Jan 2025 23:08:18 GMT
USER ContainerAdministrator
# Thu, 23 Jan 2025 23:08:37 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 23 Jan 2025 23:08:38 GMT
USER ContainerUser
# Thu, 23 Jan 2025 23:08:38 GMT
ENV JAVA_VERSION=24-ea+32
# Thu, 23 Jan 2025 23:08:45 GMT
COPY dir:86d923ef445b254beb0a3a098fc78a6b4825f40d8c18f13f837cc4a7df771680 in C:\openjdk-24 
# Thu, 23 Jan 2025 23:08:52 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 23 Jan 2025 23:08:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524c5ff1c502b3ce4bf67b204d5a5b77cbab15aebaedd40bad446fcaaa0f7216`  
		Last Modified: Thu, 23 Jan 2025 23:08:59 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f6905910df7d14e3b583e3ffaa0f35a97451975c7ff48b55edef0a659d6f25`  
		Last Modified: Thu, 23 Jan 2025 23:08:58 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:954e0ab24a5e5cf838032468004a11aa5fe78bcaf9891961b0e49de3e8ddc8af`  
		Last Modified: Thu, 23 Jan 2025 23:08:58 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b975cceb428afa88e15406457de104c5f407f32440ec45751fe5f9ef3d82d3`  
		Last Modified: Thu, 23 Jan 2025 23:08:58 GMT  
		Size: 85.4 KB (85410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8016125919e6a3858b84b207d85c9056c2c15e5d697a81e6bf57929b56a5d95e`  
		Last Modified: Thu, 23 Jan 2025 23:08:57 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cc597579009d5fa55ccb3716d54f49ad5bbb2e1e9d22fecb6fd884ed145a7b`  
		Last Modified: Thu, 23 Jan 2025 23:08:56 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fedd76506ce74b04ef35498b93e2fce7c760db363e886d6598bf6a2cf4ef4f1b`  
		Last Modified: Thu, 23 Jan 2025 23:09:07 GMT  
		Size: 208.5 MB (208488746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367cb8ce6304f1b213c489fc6a5b05c27a481a1117a6810af61510536e49fdec`  
		Last Modified: Thu, 23 Jan 2025 23:08:57 GMT  
		Size: 97.6 KB (97562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134cfd3e2d5bd801fee21e9654bacebf7193d8a18e7a02995e9f9a092f2450ef`  
		Last Modified: Thu, 23 Jan 2025 23:08:57 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
