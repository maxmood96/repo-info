## `openjdk:24-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:a82f0bc188a20492f7b0046b5bdd6c30ddd32bb38b8b2be9a02b177f6c2fd804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `openjdk:24-jdk-nanoserver-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull openjdk@sha256:8c7cfb108bad820bc3eeaa0982b4f5b9d7a5fa685d967fb32534056564faacbb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.1 MB (368147303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec283a183b843412020f35af8862dcfe7ddfe46596041f5c2c61c8367d549bb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Mon, 06 Jan 2025 21:09:00 GMT
SHELL [cmd /s /c]
# Mon, 06 Jan 2025 21:09:02 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 06 Jan 2025 21:09:03 GMT
USER ContainerAdministrator
# Mon, 06 Jan 2025 21:09:22 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 06 Jan 2025 21:09:22 GMT
USER ContainerUser
# Mon, 06 Jan 2025 21:09:22 GMT
ENV JAVA_VERSION=24-ea+30
# Mon, 06 Jan 2025 21:09:36 GMT
COPY dir:3cc680a30d66a7f79a7fa9825c9ce6e74b7087816ba7c786a4e1567e9493764b in C:\openjdk-24 
# Mon, 06 Jan 2025 21:09:41 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 06 Jan 2025 21:09:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Tue, 10 Dec 2024 21:03:34 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a173da748e667691bd921790ef6189767a166714f278e2e9e88a87e46a64b784`  
		Last Modified: Mon, 06 Jan 2025 21:09:46 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e51b504f08dd7f1d246f992172ba6e15d309ba4d596f1f89eaca7e9f365fd9`  
		Last Modified: Mon, 06 Jan 2025 21:09:46 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64740dec185693bc31ad2f2660e2ee1d9e1878f86921a80aa4da86d32d006c58`  
		Last Modified: Mon, 06 Jan 2025 21:09:45 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5cd1cbdcecc395c2988670a18e86f8b3724bab545c3ca3e10b13452d9e69f8`  
		Last Modified: Mon, 06 Jan 2025 21:09:45 GMT  
		Size: 66.3 KB (66267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6888a8bb8e5492f9d180e7f7be26eef08d70ea85ba8fcb708c9b310751dd3b`  
		Last Modified: Mon, 06 Jan 2025 21:09:44 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af22714632e4f0a8f8b0b9951c43b0e9c512f23b73f783964eaa45c54d7ba13f`  
		Last Modified: Mon, 06 Jan 2025 21:09:45 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18bcff28d564bec53c68bf249bf76637b3ef28a3deb5a88eef94dd0e56e71c9`  
		Last Modified: Mon, 06 Jan 2025 21:09:55 GMT  
		Size: 208.5 MB (208473156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8e444b67fbae9093d629dce7b075e7f5f1741898ee75db80fb92b86b30cda7`  
		Last Modified: Mon, 06 Jan 2025 21:09:45 GMT  
		Size: 4.4 MB (4369956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83567ee0251b07b79e90eb37fb4b8f682189f0a9444f0fce1571fe74d360c1be`  
		Last Modified: Mon, 06 Jan 2025 21:09:44 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
