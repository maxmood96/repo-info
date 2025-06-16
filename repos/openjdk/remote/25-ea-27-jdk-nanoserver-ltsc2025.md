## `openjdk:25-ea-27-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:907e18f4c9f8d579e6bbf68a4f22cabb8d17a200124a55d14b628c39d3f6ba48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `openjdk:25-ea-27-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.4349; amd64

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
