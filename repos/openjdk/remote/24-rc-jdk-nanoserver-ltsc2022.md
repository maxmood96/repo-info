## `openjdk:24-rc-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:ae82a5d480673fc074601b47c64da7e685eff4faf1026ff7bf3e69d9786f5d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `openjdk:24-rc-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:72a7c54ee9c084003b3ca5a192c13d03a4b8265737fe95ff11d81eafaabbafb4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.4 MB (329378275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f77d90ecb675039c97581a24bf6dd31cebb0a8e1ee464139a7c6dca367916b5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Tue, 11 Feb 2025 02:08:14 GMT
SHELL [cmd /s /c]
# Tue, 11 Feb 2025 02:08:14 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 11 Feb 2025 02:08:15 GMT
USER ContainerAdministrator
# Tue, 11 Feb 2025 02:08:33 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 11 Feb 2025 02:08:34 GMT
USER ContainerUser
# Tue, 11 Feb 2025 02:08:34 GMT
ENV JAVA_VERSION=24
# Tue, 11 Feb 2025 02:08:43 GMT
COPY dir:cf5ecdf170ed29d5224593d2b3a510464d2e7297517065c397a2229de8b2a139 in C:\openjdk-24 
# Tue, 11 Feb 2025 02:08:49 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 11 Feb 2025 02:08:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Wed, 15 Jan 2025 01:24:28 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c9b14e7c383b9d19a004e99387b95147ffca114fe022436f0f01f5c2450d0e`  
		Last Modified: Wed, 12 Feb 2025 21:51:30 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b879f70c688ca76849d42862ac84f6057b864d2f9751f121ce35f12557c0b0`  
		Last Modified: Wed, 12 Feb 2025 21:51:31 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d7a2a44f1c27541b8be59ceba6ce678f61b858880423e6659f55bda975b297`  
		Last Modified: Tue, 11 Feb 2025 02:10:10 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a0fb31da926939b82c71af07d4ef64bc190b6a7e9af56a1babc354a5bb4bb9`  
		Last Modified: Tue, 11 Feb 2025 02:10:10 GMT  
		Size: 86.0 KB (85972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd7bd8de31312bfb56146a89f6ce369091156ecc6a51f7ed458f535c1e3f9e7`  
		Last Modified: Tue, 11 Feb 2025 02:10:10 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20a8e44714436e92e3812641c66f1f6ce020bdce1d271426df520f23a4f648c`  
		Last Modified: Tue, 11 Feb 2025 02:10:10 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa417497cea233dc4190668c0fcbe4f3da0d3ac44dc047782daadbfea3042ba`  
		Last Modified: Tue, 11 Feb 2025 02:09:03 GMT  
		Size: 208.5 MB (208527408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4215867c0b68ce8e0ea2c9acba05aeb607adef319c6dc25553b182c5653648e`  
		Last Modified: Tue, 11 Feb 2025 02:10:11 GMT  
		Size: 97.1 KB (97142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63d8cc246cbdb21e17e49bbe132e3b94e62b52bd2968b436146b9974a38403c`  
		Last Modified: Wed, 12 Feb 2025 21:52:07 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
