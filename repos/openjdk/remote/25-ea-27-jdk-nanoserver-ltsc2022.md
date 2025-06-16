## `openjdk:25-ea-27-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:c6502b6598eb676ad2ed481eb66193054ac32c2dc27dc78683dc936faf4de679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `openjdk:25-ea-27-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull openjdk@sha256:83bf59cbcc014fd699b79d29aba76df0183cdd3c7623ef98f7fa61acf41f8d6a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.2 MB (341181731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f892050c9b99256f12f9962c1555d57c31397bec45f7c7a7d07612fa2b67957`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Mon, 16 Jun 2025 18:20:10 GMT
SHELL [cmd /s /c]
# Mon, 16 Jun 2025 18:20:11 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 16 Jun 2025 18:20:11 GMT
USER ContainerAdministrator
# Mon, 16 Jun 2025 18:20:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 16 Jun 2025 18:20:15 GMT
USER ContainerUser
# Mon, 16 Jun 2025 18:20:16 GMT
ENV JAVA_VERSION=25-ea+27
# Mon, 16 Jun 2025 18:20:25 GMT
COPY dir:2bcf93e730bc13f11042dc43c69be34d610e16cef805ea8798b7cf4c0b507db0 in C:\openjdk-25 
# Mon, 16 Jun 2025 18:20:30 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 16 Jun 2025 18:20:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:358ba3c853eece10dc251af10623ceb791c181e2d221dc59dbf8737c082ad2de`  
		Last Modified: Mon, 16 Jun 2025 18:21:18 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da86dee001351879b6ac2619d4ed8c6d5d8a219d020e41f615dd1e5beadef35`  
		Last Modified: Mon, 16 Jun 2025 18:21:17 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41097fbc743818074cf0202253b1d826aacba6fa5d5425250ca868477def8881`  
		Last Modified: Mon, 16 Jun 2025 18:21:18 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e3931d7c62a0ea5f05b0f89d8d9bac8460cba80a50bf713cc7f5287c3bc0610`  
		Last Modified: Mon, 16 Jun 2025 18:21:18 GMT  
		Size: 77.0 KB (77047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9dee5c5ae6fc07ab3c38bf1903c3730d46999bb9265dd027ad271a262c10f42`  
		Last Modified: Mon, 16 Jun 2025 18:21:18 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652b01611fb44a5c4b7b83c75fbacbfd21606f9f8917ebdee1f14057f3fc04b0`  
		Last Modified: Mon, 16 Jun 2025 18:21:20 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907f537284389513d110feda96cc0148afa80305257aef534a133df53941c693`  
		Last Modified: Mon, 16 Jun 2025 21:23:43 GMT  
		Size: 218.4 MB (218442321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62eb5d40db4374cd30e8b43d650faec9d2c3a6b1ea18f273a259db927116ed81`  
		Last Modified: Mon, 16 Jun 2025 18:21:20 GMT  
		Size: 115.6 KB (115573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb8175b243efa48f6214989d63e7d36b4e6ad2fce7ec6972190d1c959fe9f35`  
		Last Modified: Mon, 16 Jun 2025 18:21:20 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
