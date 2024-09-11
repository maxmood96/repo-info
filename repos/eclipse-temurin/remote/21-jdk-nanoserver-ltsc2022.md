## `eclipse-temurin:21-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:1cc991af846148ac92b82abc2eeebdb016072e3fd608b364ccf283ee3400d625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `eclipse-temurin:21-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull eclipse-temurin@sha256:6461ad5aa1846661f7cdae1befa63cdec0fc2b40c4aa2d2100376700d9f4ac70
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.4 MB (321438517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433a8c7cf69a07e3bd2a0e2fb59db4b6b815c5eae37d6788f6fa229c98cca318`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Sep 2024 23:48:03 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 01:05:47 GMT
SHELL [cmd /s /c]
# Wed, 11 Sep 2024 01:09:06 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Wed, 11 Sep 2024 01:09:07 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 11 Sep 2024 01:09:08 GMT
USER ContainerAdministrator
# Wed, 11 Sep 2024 01:09:17 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Sep 2024 01:09:18 GMT
USER ContainerUser
# Wed, 11 Sep 2024 01:09:33 GMT
COPY dir:a4ffd7e89e4f3b2e7536e802b1dd43338b71e63559dd6ffcb51f99d655bc67fd in C:\openjdk-21 
# Wed, 11 Sep 2024 01:09:44 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 11 Sep 2024 01:09:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a447243899be39b01c34fc7e1bcecb47ce42b14668876fdd121f8b5e2d4d4a86`  
		Last Modified: Tue, 10 Sep 2024 22:28:02 GMT  
		Size: 120.5 MB (120509521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015f530aeae2fa9f5c34641a19099e9949880479ad7319678bd0506ba1927a95`  
		Last Modified: Wed, 11 Sep 2024 01:33:11 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d37494348c9f0c3dc4712fe54e54161f8e2b0bda7769a69c1c11e74cff80d9b`  
		Last Modified: Wed, 11 Sep 2024 01:35:18 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9e9f140007c0567936ebbeeef2fa1c892ca487870bc4cca712593eb076fb44`  
		Last Modified: Wed, 11 Sep 2024 01:35:18 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bde01b60b204ad3e323821d5b0951406a12e2e9ad293887fce102341720ec43`  
		Last Modified: Wed, 11 Sep 2024 01:35:18 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41387b66ef5cd39a47b9083edb50b1324df3f1f69d1f1d594e9e6b8de2b0753d`  
		Last Modified: Wed, 11 Sep 2024 01:35:16 GMT  
		Size: 82.2 KB (82243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c558ee7b13ccd2688c7f23ecc770e31683af1dcec2ad28ee81af7f40ecd9c943`  
		Last Modified: Wed, 11 Sep 2024 01:35:16 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b53645823d594957907ede6552f93181df463e06336e1d12d23009273a50ca`  
		Last Modified: Wed, 11 Sep 2024 01:35:34 GMT  
		Size: 200.8 MB (200777325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6b5689fd57b2d14bfd0a2e8ee6f07456ea618d6ffc1ded077faa100fc1d5b9`  
		Last Modified: Wed, 11 Sep 2024 01:35:16 GMT  
		Size: 62.5 KB (62498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f386dd3763b13361ce0e5b7a91d3aef10f5a2ae29065a3a2942c768af8cd3f8`  
		Last Modified: Wed, 11 Sep 2024 01:35:16 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
