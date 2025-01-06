## `openjdk:24-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:8464eb5f39dc6cbb0e85ca61d8b16c57e575cb96ab51fe8a48c5f7e3d781928d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `openjdk:24-jdk-nanoserver-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull openjdk@sha256:b53375a10b82daca35a8b40469ccda647a47a31cee4017cb72660e13c7da3969
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.1 MB (368129580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc7fd31e5232bd397475cf54bfdff91a17ed7d7183d8f7d0c6baf6d394d3a34`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Sat, 14 Dec 2024 01:29:36 GMT
SHELL [cmd /s /c]
# Sat, 14 Dec 2024 01:29:37 GMT
ENV JAVA_HOME=C:\openjdk-24
# Sat, 14 Dec 2024 01:29:37 GMT
USER ContainerAdministrator
# Sat, 14 Dec 2024 01:29:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 14 Dec 2024 01:29:48 GMT
USER ContainerUser
# Sat, 14 Dec 2024 01:29:49 GMT
ENV JAVA_VERSION=24-ea+28
# Sat, 14 Dec 2024 01:30:00 GMT
COPY dir:3e04785cb1b92e22bfbfee7c4f92b5f2304c0392f1007bb025c071f815d65d06 in C:\openjdk-24 
# Sat, 14 Dec 2024 01:30:06 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 14 Dec 2024 01:30:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Tue, 10 Dec 2024 21:03:34 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c803ce37aca570a8bc916efe0466e2af18c0fdd57f5b0dbebc842603cab31dc`  
		Last Modified: Sat, 14 Dec 2024 01:30:11 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb262f662a064cec34a4215473d512dae567e2db23bf0d2dbaf05d70c683bcd3`  
		Last Modified: Sat, 14 Dec 2024 01:30:10 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922d4f9fe562c4eed6d0f91aa130239b3cd090bfda84732bdd33c5011d203379`  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ae6999faddfd2d310ce32c65d4ded64ae0d2e32d7cced97801125b65eea394`  
		Last Modified: Sat, 14 Dec 2024 01:30:10 GMT  
		Size: 66.7 KB (66655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38c561a92cf947680fc57edcace124a60fbafbb9ef1e5a7f9f3429c6f456b00`  
		Last Modified: Sat, 14 Dec 2024 01:30:09 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91066e48e9d900a18dfacf77ca887d9bb6e36852aac3533a6fe51b968f0d6964`  
		Last Modified: Sat, 14 Dec 2024 01:30:09 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d0abdee564b6a162a9b6fca9a2899e9715de35aebe8b2ad06876fc44d6328b`  
		Last Modified: Sat, 14 Dec 2024 01:30:21 GMT  
		Size: 208.5 MB (208453203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43dfe56547b9bcd635f42083372723d9aeb21a2e754900f83f82263d260718d`  
		Last Modified: Sat, 14 Dec 2024 01:30:10 GMT  
		Size: 4.4 MB (4371659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9b81ee194b4bac4954426c1305c75a5f91894c8250c68112ce83e6b4f75ba7`  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
