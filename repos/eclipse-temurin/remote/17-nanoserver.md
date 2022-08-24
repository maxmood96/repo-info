## `eclipse-temurin:17-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:bc3e6adc3b2669e83c2c2113cc87912dc15737e7fafb41c71e9e1c531e13cbad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.887; amd64
	-	windows version 10.0.17763.3287; amd64

### `eclipse-temurin:17-nanoserver` - windows version 10.0.20348.887; amd64

```console
$ docker pull eclipse-temurin@sha256:22dabdd9cae2a2894eb488fff02c7fe6f8491642f631d4effa36d7d7367d3f04
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.6 MB (303594740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d1f53d41e283327a65f9dc3f8d4c0a2401689abe6f6840b6c10122737428b51`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Aug 2022 18:05:23 GMT
RUN Apply image 10.0.20348.887
# Wed, 10 Aug 2022 16:28:17 GMT
SHELL [cmd /s /c]
# Wed, 24 Aug 2022 19:40:38 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1
# Wed, 24 Aug 2022 19:40:40 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 24 Aug 2022 19:40:43 GMT
USER ContainerAdministrator
# Wed, 24 Aug 2022 19:40:58 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Aug 2022 19:41:01 GMT
USER ContainerUser
# Wed, 24 Aug 2022 19:41:20 GMT
COPY dir:de893fa6f4d02b385cd95015ab74e60b0c0c67a3785d10d2649390aedc7b2648 in C:\openjdk-17 
# Wed, 24 Aug 2022 19:41:45 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 24 Aug 2022 19:41:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ebf439f800cd4c1fccaf4a0545e6bff60caa5141295c8ab81f6c525073c423d`  
		Size: 118.1 MB (118088450 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5f1e06146ab0490d235fe89786637467a4b71853ee428e8740ea6efbc536c47c`  
		Last Modified: Wed, 10 Aug 2022 16:48:40 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f8f09b6d2d70f1c2f68489803ced9d9d3b3b55136647c8256ec2908b9318c4`  
		Last Modified: Wed, 24 Aug 2022 19:52:45 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267a9d00737098f557ec6bfa5da82c62015f2d2769d1697a62a5e9624565fe2d`  
		Last Modified: Wed, 24 Aug 2022 19:52:45 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47fce4612be13074888afe738ec73aab4f35b644d51abb81df3ed940e7dd9b0d`  
		Last Modified: Wed, 24 Aug 2022 19:52:44 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90dd6ce5232a0205cc4e7bc70e61f53b9846903db14e2cf2f1b0e2186dee0ae`  
		Last Modified: Wed, 24 Aug 2022 19:52:41 GMT  
		Size: 87.0 KB (86966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146607d1bae7d8de89b02f5a4a9a6831e3b045507dc4e622727110a68fa2d761`  
		Last Modified: Wed, 24 Aug 2022 19:52:41 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7042e9c0d683c228c17bdbc0b5b718d2f2e3b68431213b47577e5ffba2b498c1`  
		Last Modified: Wed, 24 Aug 2022 19:53:05 GMT  
		Size: 185.3 MB (185341915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d51e4cae5f7eaa436ab3ffa7b83b2e64c5ec3056462b5d172ba5db1d843aa35`  
		Last Modified: Wed, 24 Aug 2022 19:52:41 GMT  
		Size: 70.5 KB (70507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c854e47311ffc62deac49b92d3be9816fc0f4a966fefc4c1a3e1b473c92c0493`  
		Last Modified: Wed, 24 Aug 2022 19:52:41 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-nanoserver` - windows version 10.0.17763.3287; amd64

```console
$ docker pull eclipse-temurin@sha256:bbdaf500b58cd6624ba0f01a8407fd62638a9c479bfb0d4dfeee334e5f802802
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.3 MB (292276458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae554a74d77a5060c257f65e318a6bff0dd9a36c92895cdd67499757346c1061`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Aug 2022 18:08:38 GMT
RUN Apply image 10.0.17763.3287
# Wed, 10 Aug 2022 15:57:07 GMT
SHELL [cmd /s /c]
# Wed, 24 Aug 2022 19:32:32 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1
# Wed, 24 Aug 2022 19:32:34 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 24 Aug 2022 19:32:36 GMT
USER ContainerAdministrator
# Wed, 24 Aug 2022 19:32:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Aug 2022 19:32:49 GMT
USER ContainerUser
# Wed, 24 Aug 2022 19:33:04 GMT
COPY dir:de893fa6f4d02b385cd95015ab74e60b0c0c67a3785d10d2649390aedc7b2648 in C:\openjdk-17 
# Wed, 24 Aug 2022 19:33:24 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 24 Aug 2022 19:33:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5c9d6483dab113d2d9b50fdf3156622aa2ec3d6faaed5664d15a5568032d1714`  
		Size: 103.2 MB (103204200 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0f4438539876006761cb687527bd8cb94cc7a273cf8bb47563981044f2e1771e`  
		Last Modified: Wed, 10 Aug 2022 16:38:40 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87fa2b53daf0a009f5a5680ea21a6824afb9c997d21d4af46e7ecbd040aedb25`  
		Last Modified: Wed, 24 Aug 2022 19:49:56 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c58823a6432e12c859def58c6ade94ad6f5e69a17f00a498addd51bb3e720e`  
		Last Modified: Wed, 24 Aug 2022 19:49:56 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63421ad3f49280b92c57458103894100ddd4da8e3ca2d79c12d8822a49b362f`  
		Last Modified: Wed, 24 Aug 2022 19:49:56 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af847c6b5654a4d258551cb35881903437f1fe149b67a38f3f2a3b39a392e451`  
		Last Modified: Wed, 24 Aug 2022 19:49:53 GMT  
		Size: 68.3 KB (68322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe245120e2dcfd02c932cd908b4499472c897b5f9aa5bb5f17ec726e9fe901d`  
		Last Modified: Wed, 24 Aug 2022 19:49:53 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aadc3d604f775aa42e71ca1fb7ff33b21c6e929b26e1d5f32ca5decba98995be`  
		Last Modified: Wed, 24 Aug 2022 19:50:16 GMT  
		Size: 185.3 MB (185342139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de563374b39ab6624d5458fe7227f3af622f8172094688fb80688b00bb8282a5`  
		Last Modified: Wed, 24 Aug 2022 19:49:54 GMT  
		Size: 3.7 MB (3654912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0c5f28d5045625eb3d645a662920ec13d615ba724b4a9058bfcdbeb4f064b6`  
		Last Modified: Wed, 24 Aug 2022 19:49:53 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
