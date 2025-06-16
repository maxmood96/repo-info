## `openjdk:25-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:1c36fad11c59fd0bf421310dff80b5e3f7ea59134a70e7542679600917c45c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `openjdk:25-ea-jdk-nanoserver` - windows version 10.0.26100.4349; amd64

```console
$ docker pull openjdk@sha256:6a25e810db907315810b952aa91e09f1b1d04f688aaab1be457cb88cfc76c414
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.7 MB (410722648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b14da3d6c4d11758522df4cdb2a34fb152b705d9f2f69c00a3594cab3987e83`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 07 Jun 2025 15:19:59 GMT
RUN Apply image 10.0.26100.4349
# Mon, 16 Jun 2025 18:14:30 GMT
SHELL [cmd /s /c]
# Mon, 16 Jun 2025 18:14:33 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 16 Jun 2025 18:14:35 GMT
USER ContainerAdministrator
# Mon, 16 Jun 2025 18:14:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 16 Jun 2025 18:14:39 GMT
USER ContainerUser
# Mon, 16 Jun 2025 18:14:40 GMT
ENV JAVA_VERSION=25-ea+27
# Mon, 16 Jun 2025 18:14:49 GMT
COPY dir:2bcf93e730bc13f11042dc43c69be34d610e16cef805ea8798b7cf4c0b507db0 in C:\openjdk-25 
# Mon, 16 Jun 2025 18:14:58 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 16 Jun 2025 18:14:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:709fa8bff22087ae5c45c65a3b0777eb6ee12afd1b773aece2a322e84b66b1d1`  
		Last Modified: Tue, 10 Jun 2025 22:41:49 GMT  
		Size: 192.1 MB (192082516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f762f7b55d82a4bb624336a360c0a6b1794066069ef9b12bd15621a9a207e3f`  
		Last Modified: Mon, 16 Jun 2025 21:23:33 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95da88da9dc37bb1be221eb3df9693efa2bf5da94fef6d7bdf55141a1f36ff16`  
		Last Modified: Mon, 16 Jun 2025 21:23:33 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00686c399df493273f7e000877fdae1cfcff01a3f2c397d6accb88c7333fba53`  
		Last Modified: Mon, 16 Jun 2025 21:23:33 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b2fbe8b0c396f7c7c250066ac189923c2bcea5e747548ea8fef03dd9f37398`  
		Last Modified: Mon, 16 Jun 2025 21:23:33 GMT  
		Size: 76.1 KB (76103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b9d1533ab6185fe231a5d40bac51bd8d3cc532e17178036d283faf234a91b7`  
		Last Modified: Mon, 16 Jun 2025 21:23:33 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0522b97d38794c6ee524a176b7155be0fc7bb518368b6f9f11fe2c7972f5d2ae`  
		Last Modified: Mon, 16 Jun 2025 21:23:34 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beba36cdde7503294a0410db42818659cf60a203123121650851afe8aa5f80fa`  
		Last Modified: Mon, 16 Jun 2025 21:23:40 GMT  
		Size: 218.4 MB (218443273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325d76a4164eacd99b22be9886bda67429fbbcb4957734f4dbbc2d8d3432a725`  
		Last Modified: Mon, 16 Jun 2025 21:23:34 GMT  
		Size: 114.3 KB (114311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:708f1355ab17ef46b2f57e4d6ad92f1476edeafc735aca6c556bb59880b457c5`  
		Last Modified: Mon, 16 Jun 2025 21:23:34 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-jdk-nanoserver` - windows version 10.0.20348.3807; amd64

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
