## `openjdk:24-ea-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:4bce41f991ff947aa920be20120ce023619bf187d7645252bcb91773947edb14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `openjdk:24-ea-nanoserver-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:5c744e67951631ffc63b264579947e23513e6b8d5fcafd03a98f36f6c728aa68
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.8 MB (407774989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f081db26796f39b8b6d16c7a7ba9baaaea7395bf2d94473788bbbb8996535f1d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Wed, 05 Feb 2025 00:14:16 GMT
SHELL [cmd /s /c]
# Wed, 05 Feb 2025 00:14:17 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 05 Feb 2025 00:14:18 GMT
USER ContainerAdministrator
# Wed, 05 Feb 2025 00:14:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 05 Feb 2025 00:14:22 GMT
USER ContainerUser
# Wed, 05 Feb 2025 00:14:23 GMT
ENV JAVA_VERSION=24-ea+35
# Wed, 05 Feb 2025 00:14:31 GMT
COPY dir:8f8aac6961c71e892e6587cdd6058441c6f263293987c0242380c839d9a86912 in C:\openjdk-24 
# Wed, 05 Feb 2025 00:14:39 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 05 Feb 2025 00:14:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3785065b8aefe375f35a653421ce594381c387f22decbefb76bc070f9d5651ca`  
		Last Modified: Wed, 05 Feb 2025 00:14:48 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65f9a8f92a2b846e6566cc48ff72a0874c5abf3a9a5e8f9e630c15eac6edd2a`  
		Last Modified: Wed, 05 Feb 2025 00:14:48 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab57c1382df5388a6759ef6f51be49eaf016f80572daffed37c3d0d929b93e8`  
		Last Modified: Wed, 05 Feb 2025 00:14:48 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5ee7f6e299d1039fa0c5296c2ae317b0325d6e4918102631da3f1b50b4123a`  
		Last Modified: Wed, 05 Feb 2025 00:14:48 GMT  
		Size: 76.4 KB (76393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39040b7cb015ac6868d25900120d01b31f82ff8b2076d4a56c637ba9271d1da`  
		Last Modified: Wed, 05 Feb 2025 00:14:46 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a2fd83e1d741103614546cf6e1a5367c0eca07b4861b80ad9f29b59d613114`  
		Last Modified: Wed, 05 Feb 2025 00:14:46 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df307f49b6529e01caff3f062db9dc9dff7a0028d42f3a8f77bc231b33b30a6e`  
		Last Modified: Wed, 05 Feb 2025 00:14:57 GMT  
		Size: 208.5 MB (208533782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c71558448a4307e5df5c4906e88a77756a580b9be24e7156ae231a8ac99871a`  
		Last Modified: Wed, 05 Feb 2025 00:14:46 GMT  
		Size: 104.3 KB (104306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d01de5a4c01828b161d0943b856dc3d3545258b041e3ad1cde7fa1725febe7`  
		Last Modified: Wed, 05 Feb 2025 00:14:46 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
