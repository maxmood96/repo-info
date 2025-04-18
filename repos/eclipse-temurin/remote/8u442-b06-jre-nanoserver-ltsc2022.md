## `eclipse-temurin:8u442-b06-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:38d7bcfb5ba70f129d3d6a4f6aeb0c3de17839738a2db0419a5a77cd48b9eb51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `eclipse-temurin:8u442-b06-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull eclipse-temurin@sha256:a02b4f4cb22f170b6bbd65ab31fa9b50ad8686e5728d88ce3d099e89182e4dd5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163280912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2f67d5d875959397dc09602de018c6926612febe7244abf7101831773e081d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Fri, 18 Apr 2025 04:16:03 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:16:04 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Fri, 18 Apr 2025 04:16:05 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 18 Apr 2025 04:16:05 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:16:08 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:16:08 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:16:12 GMT
COPY dir:5687adced9ba5f2555526fe07fa3e848c7771941703db13fa4b29a0f81d58070 in C:\openjdk-8 
# Fri, 18 Apr 2025 04:16:17 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Wed, 16 Apr 2025 23:30:29 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5c77a4652f8ffaa8ad7f446a5ca0ef750b1a4d72271faaa417c8dea5acc870`  
		Last Modified: Fri, 18 Apr 2025 04:16:22 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f451e9dc45652475f076cc82c54f0c465367cd538d60084bbb5c217a2fa7f3e`  
		Last Modified: Fri, 18 Apr 2025 04:16:22 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce243a9083e9f2e73524538bba29f12545b030c662442982cb0d944444016385`  
		Last Modified: Fri, 18 Apr 2025 04:16:22 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2990e256e47f1dc5315dcc9b4fe3e074af6eed669a8d73c422bc04398914f1`  
		Last Modified: Fri, 18 Apr 2025 04:16:21 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86de86d2ea71ee40123a525d17b21c0beede395e4657a069e6633c8f069f3eac`  
		Last Modified: Fri, 18 Apr 2025 04:16:21 GMT  
		Size: 77.3 KB (77332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906aec2f9cdd615d84b281003539ea16b5097d9a65546a7e77a037343fdc27e4`  
		Last Modified: Fri, 18 Apr 2025 04:16:21 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efc4cc63b438109ec0ff0c40296dcbcc43939f4e0e694bb0f9423b0b85e3800`  
		Last Modified: Fri, 18 Apr 2025 04:16:24 GMT  
		Size: 40.6 MB (40552511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd331e0be33c88c7ce9b6088752065c5a9a6cf6e122c015609960e8c92f8bac`  
		Last Modified: Fri, 18 Apr 2025 04:16:21 GMT  
		Size: 106.8 KB (106830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
