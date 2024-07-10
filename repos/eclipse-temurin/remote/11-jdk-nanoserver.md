## `eclipse-temurin:11-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:ff85132c47a7f2d00e6e3438034d945ebe673309ee81d3ffc1495ebffe1b3552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.20348.2582; amd64

```console
$ docker pull eclipse-temurin@sha256:97e5f5186324d872e654a8da8f1a39ac4750bda0afb753a24838bad30dd571fa
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.7 MB (314725650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1967ee4b9b66fdb79f3ccd2f0d9494639e2e9d81718e04dee2447fb07ad26d2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 09:30:07 GMT
RUN Apply image 10.0.20348.2582
# Wed, 10 Jul 2024 17:17:20 GMT
SHELL [cmd /s /c]
# Wed, 10 Jul 2024 17:18:26 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Wed, 10 Jul 2024 17:18:26 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 10 Jul 2024 17:18:27 GMT
USER ContainerAdministrator
# Wed, 10 Jul 2024 17:18:35 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jul 2024 17:18:36 GMT
USER ContainerUser
# Wed, 10 Jul 2024 17:18:47 GMT
COPY dir:8aa740e08efd9dadfa2fb1fd54d653720c8e2097106a2d2f0f8f1f0b127bcc3e in C:\openjdk-11 
# Wed, 10 Jul 2024 17:18:58 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Jul 2024 17:18:59 GMT
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
	-	`sha256:f49db8259042be4df6cd427a4f8d442f29492106caea180a69ab6e573bfede29`  
		Last Modified: Wed, 10 Jul 2024 17:39:35 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcae028b75a0ab4790b64c099f969203447b12bb79e308919e09b019a7d169b`  
		Last Modified: Wed, 10 Jul 2024 17:39:35 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de042bb20d46965d4aa43c5cea3a8d1aebfee8eb9a0bd7a00cc801f72bd12ce`  
		Last Modified: Wed, 10 Jul 2024 17:39:35 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614effc4c5e5f8461be75269c0ff2273b6958fe3364c1b0885c0c581ccbaf708`  
		Last Modified: Wed, 10 Jul 2024 17:39:33 GMT  
		Size: 81.2 KB (81195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dadaa039ffed31184e70603ab50918341815d96581fbeec22d8c5bbecbf0b89`  
		Last Modified: Wed, 10 Jul 2024 17:39:33 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ccc052f24aff545459ba8baec1f629ce324fa42839bae402a739f2e24ba07f`  
		Last Modified: Wed, 10 Jul 2024 17:39:47 GMT  
		Size: 194.1 MB (194084605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68440002cc3f0c9aa04a8978f52ba7ccc28b6273be750ebe774307a535b2e354`  
		Last Modified: Wed, 10 Jul 2024 17:39:33 GMT  
		Size: 62.6 KB (62618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898014a35142af6c0ade555223a4105fde1fd20c69b37be2fd40e78804dac0e9`  
		Last Modified: Wed, 10 Jul 2024 17:39:33 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.17763.6054; amd64

```console
$ docker pull eclipse-temurin@sha256:849c7986346f4b0cb745fb7f12846e57042a886cf48690466459c8e7dae84023
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.3 MB (349323808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bd170a0f91afd377e1e4fa28a762d14a4f08bcf5b01d70b9185f6303d7a6c3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 16:38:43 GMT
SHELL [cmd /s /c]
# Wed, 10 Jul 2024 16:46:39 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Wed, 10 Jul 2024 16:46:39 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 10 Jul 2024 16:46:40 GMT
USER ContainerAdministrator
# Wed, 10 Jul 2024 16:46:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jul 2024 16:46:48 GMT
USER ContainerUser
# Wed, 10 Jul 2024 16:46:58 GMT
COPY dir:8aa740e08efd9dadfa2fb1fd54d653720c8e2097106a2d2f0f8f1f0b127bcc3e in C:\openjdk-11 
# Wed, 10 Jul 2024 16:47:09 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Jul 2024 16:47:09 GMT
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
	-	`sha256:31c254e529e474f59a4578fb2028d068f7b14b05ac32bb741b48bddd3c305f91`  
		Last Modified: Wed, 10 Jul 2024 17:30:24 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03428648c72b9188308e33592b4f418c573a42c0dd50dfceccedf848fb9cb597`  
		Last Modified: Wed, 10 Jul 2024 17:30:24 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49fe0deee1dde51a87e53a2556f4de0d0653e1e3fb5dabfbe93f5a9e68729dec`  
		Last Modified: Wed, 10 Jul 2024 17:30:24 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc49ab9383cb6875d5fd12ff6e4009a9b34a7ad2037963f0aed12ac4a2127dc`  
		Last Modified: Wed, 10 Jul 2024 17:30:22 GMT  
		Size: 68.9 KB (68922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccd083b75e153d6a232a41157a52842d30b52f61057ee5fe680248fc19eef26`  
		Last Modified: Wed, 10 Jul 2024 17:30:22 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33092558debbe9ecad1287cccee39f1331af4635f769a0abe27f2ccae4715f15`  
		Last Modified: Wed, 10 Jul 2024 17:30:37 GMT  
		Size: 194.1 MB (194084975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba4e2b13b6b68fb3a6b73f8bfd56f69bb65ae7028ba11373b0f3cfb187265465`  
		Last Modified: Wed, 10 Jul 2024 17:30:22 GMT  
		Size: 81.6 KB (81608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fd05ad72f5379975d4e44085a3f345f07895048d03b1f9fb2947ea86d2d0b6`  
		Last Modified: Wed, 10 Jul 2024 17:30:22 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
