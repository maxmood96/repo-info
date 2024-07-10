## `eclipse-temurin:17-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:ad1f70be92c9ea00533194cb3593e0818d8fe47df0f56ece6855d1697db48b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `eclipse-temurin:17-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull eclipse-temurin@sha256:7648641a1f0bcc4ea3ad1ec4dfcda634ee92311eff592be95f8cf6fe9b996522
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.5 MB (307471844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b097f67de8a676ea9bffe71e8f45b84f85b5e486f761a351fcf70c5a54a503`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 09:30:07 GMT
RUN Apply image 10.0.20348.2582
# Wed, 10 Jul 2024 17:17:20 GMT
SHELL [cmd /s /c]
# Wed, 10 Jul 2024 17:19:32 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Wed, 10 Jul 2024 17:19:32 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 10 Jul 2024 17:19:33 GMT
USER ContainerAdministrator
# Wed, 10 Jul 2024 17:19:40 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jul 2024 17:19:41 GMT
USER ContainerUser
# Wed, 10 Jul 2024 17:19:55 GMT
COPY dir:58180deb8c422e61d331dbc12d9d7d83d7afe3e9097adb59bd0860aff4211c36 in C:\openjdk-17 
# Wed, 10 Jul 2024 17:20:06 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Jul 2024 17:20:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:652774a5d82a114642848f8b0b8d486ec1b4995f9dda56e36fe4ac7563429990`  
		Last Modified: Tue, 09 Jul 2024 20:33:26 GMT  
		Size: 120.5 MB (120490378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1dbb650483c31087741ccfe7cfef17abfd7465711d0851e35d39eabc775bdae`  
		Last Modified: Wed, 10 Jul 2024 17:38:52 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209b6d582ca07a8ad019f834e8f79481f49f89d1e585ca849741e74b2081ee6e`  
		Last Modified: Wed, 10 Jul 2024 17:40:13 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f5a420bd5f1f85b2efd86f74d8a9268e851fdb924eab9b194e5bf0d0af48fb`  
		Last Modified: Wed, 10 Jul 2024 17:40:13 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63a4a4f2b2bd08ea5614fd3874942750a7415ced6074db59d834c47d906dda8`  
		Last Modified: Wed, 10 Jul 2024 17:40:12 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1536f69bdc26f875560be5a91533c69bb2132df259963ee3fea4f6c48bf4768`  
		Last Modified: Wed, 10 Jul 2024 17:40:11 GMT  
		Size: 75.9 KB (75912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b37c683c3ca57ffe27ba0993dfc501d56f1cde178bd6e267a17ef8ee6317fd`  
		Last Modified: Wed, 10 Jul 2024 17:40:11 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a342439f0c87bc9a91570c3cc9a099e2805739235087269da2579e2fdaf1ac`  
		Last Modified: Wed, 10 Jul 2024 17:40:24 GMT  
		Size: 186.8 MB (186837644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29177a81664eb2200e8408c07a84a3bd9abd26c13f6ef4d85a5dd2f4d8b19d4`  
		Last Modified: Wed, 10 Jul 2024 17:40:11 GMT  
		Size: 61.0 KB (60976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6aced2e6e64f1db1ec2d84ab7009926fffddf7a98eb6e239b796b059c84353`  
		Last Modified: Wed, 10 Jul 2024 17:40:11 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
