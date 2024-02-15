## `eclipse-temurin:11-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:6bd6a6105a4529960c496017188a5f9b7d6d9e0280eebb79a72df41090f146e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `eclipse-temurin:11-jdk-nanoserver-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull eclipse-temurin@sha256:0c7af681683910f9c597c8112d5233745f6ddd97976f1019b1807d6defe71b97
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298775679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41bd27876dc917ba123e6b46381322e0aeb5e02d2c7435dd7bb0527dff1b919f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 19:41:52 GMT
SHELL [cmd /s /c]
# Wed, 14 Feb 2024 19:52:31 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 14 Feb 2024 19:52:31 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 14 Feb 2024 19:52:32 GMT
USER ContainerAdministrator
# Wed, 14 Feb 2024 19:52:41 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 Feb 2024 19:52:42 GMT
USER ContainerUser
# Wed, 14 Feb 2024 19:52:56 GMT
COPY dir:06bb700052ae5de12c7654c6d453b954bdaac52e59d87856592b85cdd3ce67e9 in C:\openjdk-11 
# Wed, 14 Feb 2024 19:53:09 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 14 Feb 2024 19:53:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cddfc54d18bb5861232283d3ff2ca5e214ade28a46dfcf6c1e7c7243809e5e85`  
		Last Modified: Thu, 15 Feb 2024 00:06:58 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3319aab0e85c73865f54cb2011da9cc0beb9ac20f12bbdffd5e3ac1b892d8142`  
		Last Modified: Thu, 15 Feb 2024 00:09:34 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3398b3bdd700f3b8b49044299f48076e670172694acfa7bf6140095c2f05a3a0`  
		Last Modified: Thu, 15 Feb 2024 00:09:34 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d23aff9121982bcd4082fc8bbdcd54c014d60c98f573b7e5494b46846f22ce`  
		Last Modified: Thu, 15 Feb 2024 00:09:34 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f843bf4ae9ad0643e317beb4a369fe03b6ddd1b04bac045b06125626624558b`  
		Last Modified: Thu, 15 Feb 2024 00:09:32 GMT  
		Size: 67.8 KB (67849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777c40462214ee9ade29f95b6280ed8186b0d4aadfa9818fe1729313f42a9f77`  
		Last Modified: Thu, 15 Feb 2024 00:09:32 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2902d3c467a94b41f20f1b77e77e753b32e4bdabb08483d78efa9ef5abcfb94c`  
		Last Modified: Thu, 15 Feb 2024 00:09:50 GMT  
		Size: 194.0 MB (193982285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201ab3df809345d3c60d21ba9d508bc266a4efc25d9f047095affffee5555207`  
		Last Modified: Thu, 15 Feb 2024 00:09:32 GMT  
		Size: 97.0 KB (96968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01303a10ccc803a6ed51cbd553020c47f8ecb3bccbead19fead8325033fd6af2`  
		Last Modified: Thu, 15 Feb 2024 00:09:32 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
