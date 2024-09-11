## `eclipse-temurin:21-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:612889989844747f9540f084ebda851cbd9151d0775a6a4d1d6bc2886786371e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `eclipse-temurin:21-jdk-nanoserver` - windows version 10.0.20348.2700; amd64

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

### `eclipse-temurin:21-jdk-nanoserver` - windows version 10.0.17763.6293; amd64

```console
$ docker pull eclipse-temurin@sha256:ef6397bbdc5ad7b44248ea9ab1927bdf6765c5476c36ee617a5031f1345949da
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.8 MB (359758593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e9db3ee97732e144d265659ee941eb997a816e20ee43b57f314ea1926063f3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:38:01 GMT
SHELL [cmd /s /c]
# Wed, 11 Sep 2024 00:56:26 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Wed, 11 Sep 2024 00:56:27 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 11 Sep 2024 00:56:28 GMT
USER ContainerAdministrator
# Wed, 11 Sep 2024 00:56:35 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Sep 2024 00:56:36 GMT
USER ContainerUser
# Wed, 11 Sep 2024 00:56:51 GMT
COPY dir:a4ffd7e89e4f3b2e7536e802b1dd43338b71e63559dd6ffcb51f99d655bc67fd in C:\openjdk-21 
# Wed, 11 Sep 2024 00:57:28 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 11 Sep 2024 00:57:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340318059288cbbdb326eea5b7079e789361251409038a37867d4e395c9404a5`  
		Last Modified: Wed, 11 Sep 2024 01:21:36 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b92e12c8f6ec07a21a2271d3953b9e4199d822f6336369d764ad7fdc1bf812`  
		Last Modified: Wed, 11 Sep 2024 01:28:58 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab47d59758ea3159f4898e3cd3a8372bd6483dd1d570fb9bfe683d653a042c6`  
		Last Modified: Wed, 11 Sep 2024 01:28:58 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d00b86dc2ec21fdab4595f7240c2ff0ff21ff173e345376c512154bea1054b9`  
		Last Modified: Wed, 11 Sep 2024 01:28:58 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08c629607bc5b9c1be71f291aed5469a2a49e901959d71212f8677ed9de5382`  
		Last Modified: Wed, 11 Sep 2024 01:28:56 GMT  
		Size: 68.4 KB (68440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcfa7f4fb49e97d65a836414e690c0ab71ac0f6e67d8f65a912dc39cc2932f7`  
		Last Modified: Wed, 11 Sep 2024 01:28:56 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f232700620fc4e06a104ec6f35e9770dae1efae8f4b6801b9e7d30d9a22ee31`  
		Last Modified: Wed, 11 Sep 2024 01:29:14 GMT  
		Size: 200.8 MB (200777394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff28b07ca7a36e32f266309369f8ea30aa5caa821a4ade9a3ba106aea1528cd`  
		Last Modified: Wed, 11 Sep 2024 01:28:57 GMT  
		Size: 3.8 MB (3824995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9966a30486c75029f215f3cecc8633fc576bfad79e08102f461079dc2b786f2`  
		Last Modified: Wed, 11 Sep 2024 01:28:56 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
