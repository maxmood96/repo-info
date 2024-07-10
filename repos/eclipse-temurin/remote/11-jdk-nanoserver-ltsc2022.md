## `eclipse-temurin:11-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:ab3adaf73f06ab453b2f48f0cedf46c60068fbaf2b7ed30ce0b6bad0c9c7752b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `eclipse-temurin:11-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.2582; amd64

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
