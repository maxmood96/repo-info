## `openjdk:26-ea-29-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:59a4191291601f601fbb7d03e4bf5b13ad9cd29b34ed02221832c3ac34bc449f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7462; amd64

### `openjdk:26-ea-29-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.7462; amd64

```console
$ docker pull openjdk@sha256:07a909657dc8bd4daf1e9de6467983a7b811df6cdb88c391a38782f442c456dc
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.9 MB (422897893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9d553ea9384ab4d1598fea728aad3f2c5749e06976f4271d2c8a1ef4f73b9d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Dec 2025 21:31:34 GMT
RUN Apply image 10.0.26100.7462
# Wed, 24 Dec 2025 06:11:55 GMT
SHELL [cmd /s /c]
# Wed, 24 Dec 2025 06:11:56 GMT
ENV JAVA_HOME=C:\openjdk-26
# Wed, 24 Dec 2025 06:11:57 GMT
USER ContainerAdministrator
# Wed, 24 Dec 2025 06:12:05 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 24 Dec 2025 06:12:06 GMT
USER ContainerUser
# Wed, 24 Dec 2025 06:12:07 GMT
ENV JAVA_VERSION=26-ea+29
# Wed, 24 Dec 2025 06:12:37 GMT
COPY dir:aceac1af5e514f13bd2af14bc760ceecc8137160caf73722d11683e6eac7c871 in C:\openjdk-26 
# Wed, 24 Dec 2025 06:12:44 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 24 Dec 2025 06:12:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a092205b76ca656d8483e99445def9f0619cb3acb2688bf9a33244c43ad44ce`  
		Last Modified: Tue, 09 Dec 2025 22:15:12 GMT  
		Size: 198.9 MB (198873947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8dca99ad75e6a24ba30d6443869285c9072c65d8b7e0398fbfd33f4ce243b75`  
		Last Modified: Wed, 24 Dec 2025 06:13:13 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7af4f47f2e55df72750f305e158f5b6bdf23bcb997f00b3802ccd0f81251cc`  
		Last Modified: Wed, 24 Dec 2025 06:13:14 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afeeef5a7c451b3fc3bee46c8cf7652d06a929666a6e24a80a9d6a667591a4ea`  
		Last Modified: Wed, 24 Dec 2025 06:13:14 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8dfe144ac60ca3dc762f49443485d3d6e1eabacd56098ad241e884a8b2c7af`  
		Last Modified: Wed, 24 Dec 2025 06:13:14 GMT  
		Size: 69.8 KB (69757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:371ba62c56b00df4f00989f37709b06105a884f1230ad922facf4e35acc921a0`  
		Last Modified: Wed, 24 Dec 2025 06:13:14 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf2e0d1b06a93656919b156f1753750a98a6cb3e603c4ebb8a3d3866c18d883`  
		Last Modified: Wed, 24 Dec 2025 06:13:14 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63989811d814315a0bde97fdc3df67c6c3173227ae323d2092bc8a354a61dc9`  
		Last Modified: Wed, 24 Dec 2025 06:13:26 GMT  
		Size: 223.8 MB (223835776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e08e6f0f38a3fa83fd4573c89898464d1e230820e5726cec669ee88bb120766`  
		Last Modified: Wed, 24 Dec 2025 06:13:14 GMT  
		Size: 112.0 KB (112017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78c525e8f7c04170254f064c7f191e51d51db0be5aad39f43bc05524297facf`  
		Last Modified: Wed, 24 Dec 2025 06:13:14 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
