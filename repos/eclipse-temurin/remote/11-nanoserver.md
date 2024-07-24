## `eclipse-temurin:11-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:ac38c4e3215829a56d2ad80b9d59767a6aa0b722006d610442172c77734be859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:11-nanoserver` - windows version 10.0.20348.2582; amd64

```console
$ docker pull eclipse-temurin@sha256:3ebca537dab503a77dbe84762822c93dfa8c65c1f725266b1892c3e57f78f681
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314301113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57224e99b70f7507c33550104ab7797904f6faddb5467080a776cd0d64ecb6cc`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 09:30:07 GMT
RUN Apply image 10.0.20348.2582
# Wed, 10 Jul 2024 17:17:20 GMT
SHELL [cmd /s /c]
# Wed, 24 Jul 2024 01:36:41 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 01:36:41 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 24 Jul 2024 01:36:42 GMT
USER ContainerAdministrator
# Wed, 24 Jul 2024 01:36:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Jul 2024 01:36:55 GMT
USER ContainerUser
# Wed, 24 Jul 2024 01:37:07 GMT
COPY dir:b5e9d6d7234e205f01359f52140171f1743cc309a4dc5e4224755ced7d18fbfc in C:\openjdk-11 
# Wed, 24 Jul 2024 01:37:21 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 24 Jul 2024 01:37:22 GMT
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
	-	`sha256:c20dc591046184b55b0bb6005ffa2c6ef4f32fdf58514800e3e0bc01fdbe48c9`  
		Last Modified: Wed, 24 Jul 2024 02:27:18 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d55d752b62ae4f8e3cc86f24b85f7f3c75792bec7144c7c3bd32c796c88a43`  
		Last Modified: Wed, 24 Jul 2024 02:27:18 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed09a5a9d8d3c25ca564bdf5827f5efd85c147ea99a43246d5d90841f6094a7`  
		Last Modified: Wed, 24 Jul 2024 02:27:18 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243eb0ff119b70e32df3b69594bba59fbce402502c9109db759382659fd46a56`  
		Last Modified: Wed, 24 Jul 2024 02:27:16 GMT  
		Size: 83.9 KB (83892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbedae14638e846472f0126e17350c5d21eafd7078728d1458881d9b1e487a05`  
		Last Modified: Wed, 24 Jul 2024 02:27:16 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9773b7363100f48088ee0d76f508eafef6ea9c99454080b330da2eaf5c1635f3`  
		Last Modified: Wed, 24 Jul 2024 02:27:33 GMT  
		Size: 193.7 MB (193657898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1ae8e59230b339e0adc1529053945f0b804d441f742a5cae820fce36ac8eac`  
		Last Modified: Wed, 24 Jul 2024 02:27:16 GMT  
		Size: 62.0 KB (62026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ea0e5857ba93eda9acb502bf44148b2d3209f817de815829e3d31bd5523d10`  
		Last Modified: Wed, 24 Jul 2024 02:27:16 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-nanoserver` - windows version 10.0.17763.6054; amd64

```console
$ docker pull eclipse-temurin@sha256:06730eed2e12944e136386d5a3d5e1007c155669108d488bdbaa20d53547701f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.9 MB (348908205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:805a5e95c8e461517e7c73e4c768d4903f9b9c8c00855a6a4bf7ca907b9747a6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 16:38:43 GMT
SHELL [cmd /s /c]
# Wed, 24 Jul 2024 01:21:01 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 01:21:01 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 24 Jul 2024 01:21:02 GMT
USER ContainerAdministrator
# Wed, 24 Jul 2024 01:21:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Jul 2024 01:21:14 GMT
USER ContainerUser
# Wed, 24 Jul 2024 01:21:26 GMT
COPY dir:b5e9d6d7234e205f01359f52140171f1743cc309a4dc5e4224755ced7d18fbfc in C:\openjdk-11 
# Wed, 24 Jul 2024 01:21:38 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 24 Jul 2024 01:21:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00a79547db1bc3ab4a5550f2ec9ba165e302f4a4984af3c1bfbbbe1726a3bf6`  
		Last Modified: Wed, 10 Jul 2024 17:28:00 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa488de0e4d919f5a414618d07d781e2cdcad9a0d533c1c519faa4505ccffe7`  
		Last Modified: Wed, 24 Jul 2024 02:23:10 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe226e31ec8082ba27b93d6437d91e61a55584eeea4841839c8062ad4c90090`  
		Last Modified: Wed, 24 Jul 2024 02:23:10 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70a48df53bfc58e073ca92be0cb9907843eda0cf4920229e005922f36eda3b5`  
		Last Modified: Wed, 24 Jul 2024 02:23:09 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2935327bfad2d8994fee4429feedc3b9f95fbfb085cb02d8b5da6bc10228ed15`  
		Last Modified: Wed, 24 Jul 2024 02:23:08 GMT  
		Size: 75.4 KB (75390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cc6b4cc5f9bb1deac3a6fd56c4d9aad5fd461f05f5456e2df4688b846932a6`  
		Last Modified: Wed, 24 Jul 2024 02:23:07 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8e1dedce55711f0f1db868224f65fc78a81c41a7be849fd0473b74bc08bd83`  
		Last Modified: Wed, 24 Jul 2024 02:23:24 GMT  
		Size: 193.7 MB (193657293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea38bf2262435bf030767f11849e0b8fa5233ed2bfbb0a9ae9ef8a16ee5d1f1a`  
		Last Modified: Wed, 24 Jul 2024 02:23:08 GMT  
		Size: 87.3 KB (87276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769370eb11be97e149b893a575a786728f8e9028197fea35e1daa5f4dd65a350`  
		Last Modified: Wed, 24 Jul 2024 02:23:08 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
