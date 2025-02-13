## `openjdk:25-ea-9-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:456f061aee946abe56b9f3e07e9ee2f8ad02f335514e4646ce16b8b341e44d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `openjdk:25-ea-9-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:1c75c1e7228498a3bc6080b8e9973fa56ffa4db97d214d8f85836a4d3a138259
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.3 MB (328344781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf0c3a808089af6da4757775f8e4e4dd2134f818eb1565d229e6c6d0a5104524`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Tue, 11 Feb 2025 01:27:43 GMT
SHELL [cmd /s /c]
# Tue, 11 Feb 2025 01:27:44 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 11 Feb 2025 01:27:45 GMT
USER ContainerAdministrator
# Tue, 11 Feb 2025 01:27:58 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 11 Feb 2025 01:27:58 GMT
USER ContainerUser
# Tue, 11 Feb 2025 01:27:59 GMT
ENV JAVA_VERSION=25-ea+9
# Tue, 11 Feb 2025 01:28:07 GMT
COPY dir:d7acfa7ae78317b124adc15f4373b266207aef9ee64c7b37ba0d0b39bb9389f0 in C:\openjdk-25 
# Tue, 11 Feb 2025 01:28:12 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 11 Feb 2025 01:28:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Wed, 15 Jan 2025 01:24:28 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec4371e05de61188dabfd1db464cc871528a821b7d40045cfed1ca5c3a430f1`  
		Last Modified: Tue, 11 Feb 2025 08:57:24 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff43f898360944bcfdb11818b3618b14f46cc58622baa0fea9c3750f28e2dd90`  
		Last Modified: Tue, 11 Feb 2025 08:57:25 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e3a6052982087b5f719d9ae3883c9184c56671ab65e2ee785d73b1eba9dcac`  
		Last Modified: Wed, 12 Feb 2025 09:01:26 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e872eeb66e49bc35e189095ee3f3933a1347eff32ccac52e0e734cb7fe5c8d72`  
		Last Modified: Tue, 11 Feb 2025 08:57:25 GMT  
		Size: 87.5 KB (87482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7605987bd8df853473ecba10f8d87d47016f8680e6812b943e11ff68e9abaa6c`  
		Last Modified: Tue, 11 Feb 2025 15:03:22 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239fd1e1005860f8dec30d25e6f2bbca280f2d218324f450f30298d132b7b898`  
		Last Modified: Tue, 11 Feb 2025 15:03:22 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34be423673a6d1a81a4518a8baa173a896239f9056d1e8d10eb63dcbb19ec78`  
		Last Modified: Tue, 11 Feb 2025 08:57:41 GMT  
		Size: 207.5 MB (207491655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f363b8de8562e6f63f635374654bb2ae5a02c56796ed8f65f4264a5669db6224`  
		Last Modified: Tue, 11 Feb 2025 08:57:44 GMT  
		Size: 97.8 KB (97824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06019fcc1ca6ae7c43a9f301f61651e061efdb65c255b48f4381bbe7514e2c63`  
		Last Modified: Tue, 11 Feb 2025 15:03:23 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
