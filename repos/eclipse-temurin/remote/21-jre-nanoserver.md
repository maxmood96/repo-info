## `eclipse-temurin:21-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:a06ec28a62e1b2c4f2f1b5593c86357acf21ed8254ac9b937c7f470992671dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.26100.4349; amd64

```console
$ docker pull eclipse-temurin@sha256:4a642a32ec686596dd10fd493ee64d0c87860369437ecc32bd600092316b84a0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241205881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6c2e9f542d53dafba6d93f1de3be3abbe8071d15116deaab0a0ab83a8f78c7f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 07 Jun 2025 15:19:59 GMT
RUN Apply image 10.0.26100.4349
# Tue, 10 Jun 2025 22:14:28 GMT
SHELL [cmd /s /c]
# Tue, 10 Jun 2025 22:14:29 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Tue, 10 Jun 2025 22:14:30 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 10 Jun 2025 22:14:31 GMT
USER ContainerAdministrator
# Tue, 10 Jun 2025 22:14:33 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Jun 2025 22:14:34 GMT
USER ContainerUser
# Tue, 10 Jun 2025 22:14:38 GMT
COPY dir:e77a568eefeac18db14cfb92f416dab13c56713fa78f747642b83f8e2eb5149f in C:\openjdk-21 
# Tue, 10 Jun 2025 22:14:43 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:709fa8bff22087ae5c45c65a3b0777eb6ee12afd1b773aece2a322e84b66b1d1`  
		Last Modified: Tue, 10 Jun 2025 22:41:49 GMT  
		Size: 192.1 MB (192082516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05047007e1707d07554a764224f98b8dd9b05d2df5ff78159108db7e191b8f8c`  
		Last Modified: Tue, 10 Jun 2025 22:15:26 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a38df05f482862ab94e4a7af4cdb1a709dec83335fb73d0bc1ba8d6a1fab76be`  
		Last Modified: Tue, 10 Jun 2025 22:15:26 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03eebb15af5ec6e7ef7b434d523b5e3a9bef3cdd3e33396fe8df4e2518667811`  
		Last Modified: Tue, 10 Jun 2025 22:15:26 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60a6420ed456f4c4789a6be1929918d9278c2ebc3638d6ff6727e1ff54dda49`  
		Last Modified: Tue, 10 Jun 2025 22:15:27 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0549dcff77c567e1d100231157f90c9c5de8ce036673a06ee2e2d5a49b7af5`  
		Last Modified: Tue, 10 Jun 2025 22:15:27 GMT  
		Size: 77.4 KB (77354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5490bd6fb856708d6289c87c526d8afe271b53f8e60a9882121478f1d5adcdea`  
		Last Modified: Tue, 10 Jun 2025 22:15:27 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc3213f27941b4697eeb88c0db08f0872cef2d517012b68a68df5018e967840`  
		Last Modified: Tue, 10 Jun 2025 22:15:30 GMT  
		Size: 48.9 MB (48946990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e32eaae8e331fbedcc52d42e5316e9e2cd70d582b6485e7b8c173abd473eab`  
		Last Modified: Tue, 10 Jun 2025 22:15:28 GMT  
		Size: 93.8 KB (93752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.20348.3807; amd64

```console
$ docker pull eclipse-temurin@sha256:77c0a46773f836e48c957970c107e0d40f2b20e6a372ee647b64ca300a1aef1b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171679932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeadc0d730838bc18de2ac9a1fe2e173007c5f4f94800ee0ef35999b1f9f0572`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Tue, 10 Jun 2025 22:18:46 GMT
SHELL [cmd /s /c]
# Tue, 10 Jun 2025 22:18:46 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Tue, 10 Jun 2025 22:18:47 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 10 Jun 2025 22:18:48 GMT
USER ContainerAdministrator
# Tue, 10 Jun 2025 22:18:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Jun 2025 22:18:51 GMT
USER ContainerUser
# Tue, 10 Jun 2025 22:18:56 GMT
COPY dir:e77a568eefeac18db14cfb92f416dab13c56713fa78f747642b83f8e2eb5149f in C:\openjdk-21 
# Tue, 10 Jun 2025 22:19:00 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcf3db784119b3711cd6c0871d32fcd214d0d62feeac41527b204370f37724a`  
		Last Modified: Tue, 10 Jun 2025 22:19:27 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86c982eb76fd458df8adc822909c72af2bec202488a1645a09f7a05834f52e7`  
		Last Modified: Tue, 10 Jun 2025 22:19:28 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91741916a12aa6fc0dbafd54343173350b8e9ffdcb51619679b2275f04e3e10`  
		Last Modified: Tue, 10 Jun 2025 22:19:28 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a10d108d2cf51bb854688e047959b8f428f6cc31fac671ae314c5b6a44b4b1`  
		Last Modified: Tue, 10 Jun 2025 22:19:28 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2b1e5ecdc8e10e173d1fe7d3c0061aa68f2c7969348241831d9d527a0b1e65`  
		Last Modified: Tue, 10 Jun 2025 22:19:28 GMT  
		Size: 80.5 KB (80470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7703cebb99b5e52cd6d7e341ed51daf6fe32979a2d9ef9da05de5d527be337`  
		Last Modified: Tue, 10 Jun 2025 22:19:28 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a2cc4597a73a8add5804cc54f372cc3b8c353213cdaa23933b41dc75207d793`  
		Last Modified: Tue, 10 Jun 2025 22:19:37 GMT  
		Size: 48.9 MB (48945922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f2c15bd0ecd8c6cb05617c8f0fc1ef46dee415e0acdb870660b1ae12f5daf4`  
		Last Modified: Tue, 10 Jun 2025 22:19:29 GMT  
		Size: 107.8 KB (107834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
