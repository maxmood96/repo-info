## `openjdk:26-ea-20-nanoserver`

```console
$ docker pull openjdk@sha256:481523e8cdf28f9ad0a4c3c1deda1cda6d4d2fd5d14140730face873a42cc3ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6899; amd64
	-	windows version 10.0.20348.4294; amd64

### `openjdk:26-ea-20-nanoserver` - windows version 10.0.26100.6899; amd64

```console
$ docker pull openjdk@sha256:0542fc7e96d936e2064724d44b388e7dac029547d8a072ac3eccae9648f86925
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.4 MB (415361078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0cbb47fe4ca1a2db604f7ce102e8d057b9866d21cc3baacaef3ddcba2eec171`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 11 Oct 2025 15:58:41 GMT
RUN Apply image 10.0.26100.6899
# Tue, 21 Oct 2025 18:44:08 GMT
SHELL [cmd /s /c]
# Tue, 21 Oct 2025 18:44:08 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 21 Oct 2025 18:44:09 GMT
USER ContainerAdministrator
# Tue, 21 Oct 2025 18:44:18 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 21 Oct 2025 18:44:18 GMT
USER ContainerUser
# Tue, 21 Oct 2025 18:44:18 GMT
ENV JAVA_VERSION=26-ea+20
# Tue, 21 Oct 2025 18:44:57 GMT
COPY dir:6bffdfd50160c82e6869fd0a690d084eedfe2bd58671ef19a440f7d2cd9a5727 in C:\openjdk-26 
# Tue, 21 Oct 2025 18:45:05 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 21 Oct 2025 18:45:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:463edd10ad50b00cf92c69fc3eaa85e1fa40aad1b7938fa232899405bd80f001`  
		Last Modified: Tue, 14 Oct 2025 22:41:48 GMT  
		Size: 194.0 MB (194026741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a9379bed8c757acc59ccb9f5ce5bf296a2421772d0d238e785bc40dae32cbd8`  
		Last Modified: Tue, 21 Oct 2025 18:45:33 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de98efda076ad243d9ebc74f1874adf66dc303ea27dcaa46ebe8f9d85dc6e269`  
		Last Modified: Tue, 21 Oct 2025 18:45:34 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c049d866ce3271c0a25f7ac0f9d3ea569c946c91794b1f9f335b6ee33faae0ba`  
		Last Modified: Tue, 21 Oct 2025 18:45:33 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca7e84fcdc83464eca6873bb5358d0590cc2f89a055d6f3fd5b6d91f6018f72`  
		Last Modified: Tue, 21 Oct 2025 18:45:34 GMT  
		Size: 77.8 KB (77797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a870b9800bbec2f6a94e3819e5b49d1f83d99b9fe74e3e289d3f110bcf97d22`  
		Last Modified: Tue, 21 Oct 2025 18:45:33 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9b6b60097f034a71a12e1efed6d9cf85e5f9f1f14f0937d0bcb39691fbc8a8`  
		Last Modified: Tue, 21 Oct 2025 18:45:33 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54433fe344b363584388ea4920f6e6716dfddbfdd2ed96bdd211b65d214c7f02`  
		Last Modified: Tue, 21 Oct 2025 21:24:50 GMT  
		Size: 221.2 MB (221153064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ed1f25597a502edcba03bf22f698954b37a64874fb9dad3ba4520e8e4d7966`  
		Last Modified: Tue, 21 Oct 2025 18:45:33 GMT  
		Size: 97.1 KB (97058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0605eba44b0d8b11fb94bcb96c83ea8c8fe8da20f8f6158f1a261d52813f56`  
		Last Modified: Tue, 21 Oct 2025 18:45:34 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-ea-20-nanoserver` - windows version 10.0.20348.4294; amd64

```console
$ docker pull openjdk@sha256:4e593bd7f06a26d61ee01949c5cc44c5c66786f40ccf99649c1d962d99c5bd9f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.0 MB (344049944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164ec86f4473e6951b59e3b2fc5d3f33608c423ed27c9f85b3de24f78478f6d8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Oct 2025 07:34:08 GMT
RUN Apply image 10.0.20348.4294
# Tue, 21 Oct 2025 18:44:10 GMT
SHELL [cmd /s /c]
# Tue, 21 Oct 2025 18:44:10 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 21 Oct 2025 18:44:11 GMT
USER ContainerAdministrator
# Tue, 21 Oct 2025 18:44:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 21 Oct 2025 18:44:21 GMT
USER ContainerUser
# Tue, 21 Oct 2025 18:44:22 GMT
ENV JAVA_VERSION=26-ea+20
# Tue, 21 Oct 2025 18:45:35 GMT
COPY dir:6bffdfd50160c82e6869fd0a690d084eedfe2bd58671ef19a440f7d2cd9a5727 in C:\openjdk-26 
# Tue, 21 Oct 2025 18:45:40 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 21 Oct 2025 18:45:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f68a3bbf3ee20b515c5b8b801e5627a9dac3782ef264e37060c34ed80e5d8874`  
		Last Modified: Tue, 14 Oct 2025 20:41:53 GMT  
		Size: 122.7 MB (122688886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309da51cee11a15e2c84bab8b626f7e505c07445b3ba442104f7fd5e5a704761`  
		Last Modified: Tue, 21 Oct 2025 18:46:19 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41018dfc9ef3346063a85ee2f0f6fbda2dcaa229de0f8c74f7a91b602b9ec237`  
		Last Modified: Tue, 21 Oct 2025 18:46:19 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780268177bae32b37f61e35bcc511152e32e1bb5a53ad22d7332d3a0cdd33363`  
		Last Modified: Tue, 21 Oct 2025 18:46:19 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb35e0356b230b2f024a4d9c0d119b3f6c5f0d868953ccd0a0169a9f254063b`  
		Last Modified: Tue, 21 Oct 2025 18:46:19 GMT  
		Size: 87.5 KB (87480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f62c8d197bc9af7b2e0256074b23fed9908a3d3b6cbbf2b9ee0571636773dc`  
		Last Modified: Tue, 21 Oct 2025 18:46:19 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6394b9ea1ea4b1c881dc217a7f21c366281258a3eb052bee3a7fdd40897698`  
		Last Modified: Tue, 21 Oct 2025 18:46:19 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d2d1afc655c35faa696e2e4069275dbac77dae14825b38d128f4b97527c46b`  
		Last Modified: Tue, 21 Oct 2025 21:24:08 GMT  
		Size: 221.2 MB (221152653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e5be6aaa661097faf6b5e21ad0be7afbef343d23e4f04d9c5b2d8f48b16933`  
		Last Modified: Tue, 21 Oct 2025 18:46:20 GMT  
		Size: 114.5 KB (114526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a0c94b9c8272ff10e37ab05d4af7a76c3e7f4204e2f5dfb11e7db4bcc882e9`  
		Last Modified: Tue, 21 Oct 2025 18:46:19 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
