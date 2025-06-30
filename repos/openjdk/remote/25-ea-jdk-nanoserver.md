## `openjdk:25-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:09624d927db9ef555195bb7c60f81a471188f195dc150e586e6b41bc10ce335d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `openjdk:25-ea-jdk-nanoserver` - windows version 10.0.26100.4349; amd64

```console
$ docker pull openjdk@sha256:ee65e72bc4f9e80b3c7ae13e4aaab9763c0fa32f849c7fc172302f9dc522f2ec
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.8 MB (410787550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6241377a5ae8c00634d418c6d158d87f0f901be1beb94d93fddad0472f24e4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 07 Jun 2025 15:19:59 GMT
RUN Apply image 10.0.26100.4349
# Mon, 30 Jun 2025 18:14:42 GMT
SHELL [cmd /s /c]
# Mon, 30 Jun 2025 18:14:43 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 30 Jun 2025 18:14:44 GMT
USER ContainerAdministrator
# Mon, 30 Jun 2025 18:14:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 30 Jun 2025 18:14:48 GMT
USER ContainerUser
# Mon, 30 Jun 2025 18:14:49 GMT
ENV JAVA_VERSION=25-ea+29
# Mon, 30 Jun 2025 18:14:58 GMT
COPY dir:42ea662c144d042c5c993e4ad460b12969ac9552d3e3695a34b691e1b9c80eac in C:\openjdk-25 
# Mon, 30 Jun 2025 18:15:05 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 30 Jun 2025 18:15:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:709fa8bff22087ae5c45c65a3b0777eb6ee12afd1b773aece2a322e84b66b1d1`  
		Last Modified: Tue, 10 Jun 2025 22:41:49 GMT  
		Size: 192.1 MB (192082516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b936cb450ccc6032edd1a3cb44bebaa8c2fe0ee2bfe559522089f6acd549b0`  
		Last Modified: Mon, 30 Jun 2025 18:15:53 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7235d886459d0899149f553e67fd5e8d18b35a1bf8692cfd3f0e1e9714a545e`  
		Last Modified: Mon, 30 Jun 2025 18:15:53 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808ce20c38dee62b31cc080104de2f77db83a557c43a457b200e0b2df5e0a9d7`  
		Last Modified: Mon, 30 Jun 2025 18:15:53 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c90f05de2fa9bd84b7d77bd5991e95e35d4200c7605bf8c91990110c2d54030`  
		Last Modified: Mon, 30 Jun 2025 18:15:53 GMT  
		Size: 76.3 KB (76305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1feb3a5a2c169a31b5a7a186fa827267b8e87a67b8287962baf5fd74360955cb`  
		Last Modified: Mon, 30 Jun 2025 18:15:53 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9922fa774122a0d802916432f4cc260e226b408e87574f800090a452747dc1`  
		Last Modified: Mon, 30 Jun 2025 18:15:53 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3bb01ba9adb42180d3130bbf86da4bf5d67f9ee7a0daf7047d9fd0c8a998bc`  
		Last Modified: Mon, 30 Jun 2025 21:24:19 GMT  
		Size: 218.5 MB (218496851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f19e1cadeec5505e20e75c69a8ec510be900b2aaacaa4f61d8e6e179c8bc35`  
		Last Modified: Mon, 30 Jun 2025 18:15:53 GMT  
		Size: 125.6 KB (125565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef48cf7ec026adacb3d1700b30b3c0edb897d371ba274f78cf476479f313a28a`  
		Last Modified: Mon, 30 Jun 2025 18:15:53 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-jdk-nanoserver` - windows version 10.0.20348.3807; amd64

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
