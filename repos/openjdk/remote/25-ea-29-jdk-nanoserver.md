## `openjdk:25-ea-29-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:d159395bb28538c115d94ee34359ae2a509015d78b57071ec6b844995ae9541e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `openjdk:25-ea-29-jdk-nanoserver` - windows version 10.0.20348.3807; amd64

```console
$ docker pull openjdk@sha256:2bcf9b98da0c340c6f75ff8e08b17fc3e278abd299ce44020761067e4515f363
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.2 MB (341222028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2cd2cdf20f500e1033af93d7aa1641ad2a9878466d8016a50b7d356560e20e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Mon, 30 Jun 2025 17:37:06 GMT
SHELL [cmd /s /c]
# Mon, 30 Jun 2025 17:37:07 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 30 Jun 2025 17:37:08 GMT
USER ContainerAdministrator
# Mon, 30 Jun 2025 17:37:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 30 Jun 2025 17:37:14 GMT
USER ContainerUser
# Mon, 30 Jun 2025 17:37:15 GMT
ENV JAVA_VERSION=25-ea+29
# Mon, 30 Jun 2025 17:37:24 GMT
COPY dir:42ea662c144d042c5c993e4ad460b12969ac9552d3e3695a34b691e1b9c80eac in C:\openjdk-25 
# Mon, 30 Jun 2025 17:37:30 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 30 Jun 2025 17:37:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38837685b6350ed767662aa48b9641ce6956846b789596b14baa38c4d16d50c5`  
		Last Modified: Mon, 30 Jun 2025 17:37:59 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d157b296e669882d3111e7385ac2913c6821134d3ececd7eeeb823fa618303`  
		Last Modified: Mon, 30 Jun 2025 17:37:59 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da680f394c256e4740c2453b3e98941ef224897e1dcad475d52de788c669a9c1`  
		Last Modified: Mon, 30 Jun 2025 17:38:01 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4143629a030d8b5051cef32494efa98a01c939dd4cf76231649ca6224f3d82`  
		Last Modified: Mon, 30 Jun 2025 17:37:59 GMT  
		Size: 79.4 KB (79409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda592d7cdb670c45ef05c97cd9f8f0146ea7d51de5ff18b0842f5dcac219116`  
		Last Modified: Mon, 30 Jun 2025 17:37:59 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8390c430d7289622350923588d35b0342e43d1cc4d620d79b222b5ed4790b52`  
		Last Modified: Mon, 30 Jun 2025 17:37:59 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db4a56f0651a75746412f99acf94c3c1d17ef7a61e11a2b7e4a0f57b298a08a`  
		Last Modified: Mon, 30 Jun 2025 18:24:04 GMT  
		Size: 218.5 MB (218498314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef7db600e44e2d0c15497d49d6aa6fd6b51e94c26c97f558013ad171fc092dd8`  
		Last Modified: Mon, 30 Jun 2025 17:37:59 GMT  
		Size: 97.5 KB (97452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658b627df290be437d3606975f1e436d0e06c2e832919b0e6b40cc43d134e708`  
		Last Modified: Mon, 30 Jun 2025 17:37:59 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
