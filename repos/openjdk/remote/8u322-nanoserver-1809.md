## `openjdk:8u322-nanoserver-1809`

```console
$ docker pull openjdk@sha256:d79c520f4af74a9092859e77660eb02c5d90a1ee52b597e4bedbae7fd2e80636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `openjdk:8u322-nanoserver-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull openjdk@sha256:6ff0a6147d06f1b545ac1476b5f98a4c87d9e7b89de6744c96e21bbb7481ef39
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.3 MB (204336962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a95e24a4ade4359df1d096ea3bac688d63ce13eb21fcecea2c2b37acf11139fc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 18 Jan 2022 01:20:34 GMT
RUN Apply image 1809-amd64
# Wed, 19 Jan 2022 22:25:45 GMT
SHELL [cmd /s /c]
# Wed, 19 Jan 2022 22:39:29 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 19 Jan 2022 22:39:30 GMT
USER ContainerAdministrator
# Wed, 19 Jan 2022 22:39:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 19 Jan 2022 22:39:39 GMT
USER ContainerUser
# Thu, 03 Feb 2022 20:27:17 GMT
ENV JAVA_VERSION=8u322
# Thu, 03 Feb 2022 20:27:37 GMT
COPY dir:70b73c62c79b1e3a83236c8add186d48955c92966a80012af2e52ff572318d7b in C:\openjdk-8 
# Thu, 03 Feb 2022 20:27:54 GMT
RUN echo Verifying install ... 	&& echo   javac -version && javac -version 	&& echo   java -version && java -version 	&& echo Complete.
```

-	Layers:
	-	`sha256:b5c97e1d373f591225559869af7f4f01399c201f89d21f903b1d23c830aa0a3f`  
		Size: 103.0 MB (103046552 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a1b3e13bb7b3d4b61b5f49a91d6eb9bfcf5539ab89c3687d608f17713c2409b5`  
		Last Modified: Thu, 20 Jan 2022 02:21:30 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:338bf0e38fb7f2b8a0fb5e7eb7fab0a55b72f807f8f29e8a8cca893d27d9a3a8`  
		Last Modified: Thu, 20 Jan 2022 02:42:25 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad2e28cd185f66eb0db90aedacf18508ccfd1a587b64c68b818e6a6ccf36580`  
		Last Modified: Thu, 20 Jan 2022 02:42:25 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8734a1268ea949016e9c473f5bdb78cb61ed8fe90ee65b5ba7b2ebd765496205`  
		Last Modified: Thu, 20 Jan 2022 02:42:23 GMT  
		Size: 70.7 KB (70719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d88295d21d31aa302a0382ecc8affcdb2d99175e66a11a9467f383a411d75e`  
		Last Modified: Thu, 20 Jan 2022 02:42:23 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0648c8a62783a7b11fca5e2be3809acab53076a9a7d0222b50c4b3b7d67a17a`  
		Last Modified: Thu, 03 Feb 2022 21:29:54 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ece9b4d96e24af3f4add048a65ce3d6ea768ab6792219c31a746f318539d82f`  
		Last Modified: Thu, 03 Feb 2022 21:30:08 GMT  
		Size: 101.1 MB (101094246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0cfb210cb6cd580f568bd7110c05b73b7e15cb574710003caf868684bbcb42`  
		Last Modified: Thu, 03 Feb 2022 21:29:55 GMT  
		Size: 119.8 KB (119773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
