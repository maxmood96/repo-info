## `eclipse-temurin:21-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:6c7183eab432cd5fa3c74f0b37492ecd4aa1d7f412f6a66f2b2b5f7a2ea01da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `eclipse-temurin:21-jdk-nanoserver` - windows version 10.0.26100.4349; amd64

```console
$ docker pull eclipse-temurin@sha256:0155af1a845870bd8604778af153ef3b8735e396f82bd81c79b9fddc224455c2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393830328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f871ccf748d1ca2b4861acc11f4f146f311954d745c1b2809016eb8711aade60`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 07 Jun 2025 15:19:59 GMT
RUN Apply image 10.0.26100.4349
# Tue, 10 Jun 2025 22:14:41 GMT
SHELL [cmd /s /c]
# Tue, 10 Jun 2025 22:14:42 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Tue, 10 Jun 2025 22:14:42 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 10 Jun 2025 22:14:43 GMT
USER ContainerAdministrator
# Tue, 10 Jun 2025 22:14:46 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Jun 2025 22:14:47 GMT
USER ContainerUser
# Tue, 10 Jun 2025 22:14:53 GMT
COPY dir:db067bfbcc086396d5dfa4ac3979b5c2114a2c9ec3e102fbc339048e5a829713 in C:\openjdk-21 
# Tue, 10 Jun 2025 22:14:59 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 10 Jun 2025 22:15:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:709fa8bff22087ae5c45c65a3b0777eb6ee12afd1b773aece2a322e84b66b1d1`  
		Last Modified: Tue, 10 Jun 2025 22:41:49 GMT  
		Size: 192.1 MB (192082516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f01f8ccaeedfa276bc823ea222d03ea47f5961b7770173549e841265ac76f7`  
		Last Modified: Tue, 10 Jun 2025 22:15:44 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbba9f599eec03ff023de92f8b9dc849a4b7827287de063f7769b77570631ceb`  
		Last Modified: Tue, 10 Jun 2025 22:15:44 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bba5404bb6fe533d4a67dd40d5c48faf49229c52b4b4c9d1f571b0165031008`  
		Last Modified: Tue, 10 Jun 2025 22:15:44 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8365f2f8b588bc3c3723cbdc81217eb4558ef90ab33be52d7d136b4c2e528ec6`  
		Last Modified: Tue, 10 Jun 2025 22:15:44 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f41e941b6eacb5b89809cd0d41c515316f020e62cf83431c8e9574d5ef9dd2`  
		Last Modified: Tue, 10 Jun 2025 22:15:45 GMT  
		Size: 75.8 KB (75778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d7ee6fb193e39902d69f5637048fc6d906b01765f5bdb74c4b5177e3d755ab`  
		Last Modified: Tue, 10 Jun 2025 22:15:45 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001f0812ee97126c43d1e5bbf24ff00fb28797a0667274130c3e1946076839bb`  
		Last Modified: Wed, 11 Jun 2025 00:15:34 GMT  
		Size: 201.6 MB (201552111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42bb241dfccc9210f3dc187b54dad6752b18a357d1d173395e56f02026034251`  
		Last Modified: Tue, 10 Jun 2025 22:15:45 GMT  
		Size: 113.6 KB (113601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86a174b7a8f1816b739a447b4776b1234c03bd508fd8b582118d60eccb7cc8e`  
		Last Modified: Tue, 10 Jun 2025 22:15:45 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jdk-nanoserver` - windows version 10.0.20348.3807; amd64

```console
$ docker pull eclipse-temurin@sha256:fce0288388e0a9b005baedb7eee20962f020594f5d11bc54975c8145714c584a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.3 MB (324283630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119c5a9a23c47dce7108f37a9efd76ed2f92f2e5a81e27838446296b082ad75b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Tue, 10 Jun 2025 22:19:18 GMT
SHELL [cmd /s /c]
# Tue, 10 Jun 2025 22:19:18 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Tue, 10 Jun 2025 22:19:19 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 10 Jun 2025 22:19:20 GMT
USER ContainerAdministrator
# Tue, 10 Jun 2025 22:19:22 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Jun 2025 22:19:23 GMT
USER ContainerUser
# Tue, 10 Jun 2025 22:19:31 GMT
COPY dir:db067bfbcc086396d5dfa4ac3979b5c2114a2c9ec3e102fbc339048e5a829713 in C:\openjdk-21 
# Tue, 10 Jun 2025 22:19:36 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 10 Jun 2025 22:19:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce63afa885889bac2568373fd88d38c0f6998b42d81d00fcace7a89afc00767`  
		Last Modified: Tue, 10 Jun 2025 22:20:18 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ec560c2c240bf52206113eb6543f214ff71ae82120d34689c5b769e98c49c4`  
		Last Modified: Tue, 10 Jun 2025 22:20:18 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3804dc686e9025e3f5bc184378040d9b342cc0eedff1cb7787b7542c31ed0d`  
		Last Modified: Tue, 10 Jun 2025 22:20:18 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a771f473b778d8c583f6b04b85899c6d1407628e00dabf60213edb81a146014c`  
		Last Modified: Tue, 10 Jun 2025 22:20:18 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db105f24c3a55937cc64e0d117c77f3f5b3c4b32d82bb93bfb71d80efd8d6df6`  
		Last Modified: Wed, 11 Jun 2025 00:15:17 GMT  
		Size: 79.1 KB (79108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785d1b016e826b62fde226379c7b4f73b959d27c9f75d1c7349d479a8bb5b27e`  
		Last Modified: Wed, 11 Jun 2025 00:15:18 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b7a5e7e9a601acde0a556c077c828645a7d6fbdd81bfdf92a2a659cc418d5c`  
		Last Modified: Wed, 11 Jun 2025 00:15:35 GMT  
		Size: 201.6 MB (201551312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40bc5d7db5fc9b26e694fe7add9c1d1e53e33ae343edd65b3afe294f61323deb`  
		Last Modified: Wed, 11 Jun 2025 00:15:18 GMT  
		Size: 106.5 KB (106502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c00a3a0af329fcb566709f20b300e895645aa3d2516ae885ccd8a13d9256e6`  
		Last Modified: Wed, 11 Jun 2025 00:15:18 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
