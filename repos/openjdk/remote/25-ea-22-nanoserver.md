## `openjdk:25-ea-22-nanoserver`

```console
$ docker pull openjdk@sha256:30aa6801da32df73f8eba93e6f5d649efd72650d53b660f0f0f7f636c4bc6adb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64
	-	windows version 10.0.17763.7314; amd64

### `openjdk:25-ea-22-nanoserver` - windows version 10.0.26100.4061; amd64

```console
$ docker pull openjdk@sha256:359658374fbdd9dff095d33634b17e68fa158b0be47f2a5d41d7916de2853cf5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.0 MB (399956726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a60e3e1f946e9b9e932cd67191337dc93cf1015985f60c44dc022c33edc0c59`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 10 May 2025 00:58:48 GMT
RUN Apply image 10.0.26100.4061
# Wed, 14 May 2025 21:14:08 GMT
SHELL [cmd /s /c]
# Wed, 14 May 2025 21:14:09 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 14 May 2025 21:14:10 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 21:14:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 14 May 2025 21:14:14 GMT
USER ContainerUser
# Wed, 14 May 2025 21:14:15 GMT
ENV JAVA_VERSION=25-ea+22
# Wed, 14 May 2025 21:14:25 GMT
COPY dir:d2aeeab016ce5cfb722c90fbb6527341de5d03dac18528814b93fc4084ba77f8 in C:\openjdk-25 
# Wed, 14 May 2025 21:14:32 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 14 May 2025 21:14:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9824510349be04d2eb26f9aaba1d016eddcbed10bdcd6681f4636c948766f3d1`  
		Last Modified: Tue, 13 May 2025 23:02:56 GMT  
		Size: 191.4 MB (191412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7be936c5bae6798509722388fef548775f98172c3002406e3f616451819ffb`  
		Last Modified: Wed, 14 May 2025 21:14:39 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d42a68adf4a5f6273fca0894b3d91aa66344ed1e320efb65a8c1b5934418e7e`  
		Last Modified: Wed, 14 May 2025 21:14:39 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e989cec3f93ca5db5e12f8da959e0532603b12334895fc26576b88b75ff11a`  
		Last Modified: Wed, 14 May 2025 21:14:39 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9032652dc193211ca8c52af5623b82241e86b3d502aacaf96f2715e490720ab5`  
		Last Modified: Wed, 14 May 2025 21:14:39 GMT  
		Size: 76.2 KB (76162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22bdd871400fdba24a02da3436188164a1fde98908334edc8184f56351c786d`  
		Last Modified: Wed, 14 May 2025 21:14:37 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4075a8e58c5bc386f4c10da47d63bfce27c2285ea5246545da02c370f11116d6`  
		Last Modified: Wed, 14 May 2025 21:14:37 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594e03a12128dc8b7b4c982a8932bab39bf29e25a7641c511c8f8124099d703e`  
		Last Modified: Wed, 14 May 2025 21:14:48 GMT  
		Size: 208.4 MB (208367631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827dde15c6082ca3083f4c1d23714a2a8d7392944dbb2c80da4503454ba8bcb7`  
		Last Modified: Wed, 14 May 2025 21:14:37 GMT  
		Size: 94.6 KB (94617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1ea0fc678634ee0a5d6bb4bb36e14518eed40f3e131519c01dc3be921c38f4`  
		Last Modified: Wed, 14 May 2025 21:14:37 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-22-nanoserver` - windows version 10.0.20348.3692; amd64

```console
$ docker pull openjdk@sha256:c4afbf1e2b4362b8ff37363840c395543109570d1942914ebe6f4bcdb4555e44
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.1 MB (331132219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a63403ebbe9b09622baa4cea8e89855d756bddd0f8f9d9a2f5b8a014a15f48c6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Wed, 14 May 2025 21:22:24 GMT
SHELL [cmd /s /c]
# Wed, 14 May 2025 21:22:25 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 14 May 2025 21:22:25 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 21:22:28 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 14 May 2025 21:22:28 GMT
USER ContainerUser
# Wed, 14 May 2025 21:22:29 GMT
ENV JAVA_VERSION=25-ea+22
# Wed, 14 May 2025 21:22:36 GMT
COPY dir:d2aeeab016ce5cfb722c90fbb6527341de5d03dac18528814b93fc4084ba77f8 in C:\openjdk-25 
# Wed, 14 May 2025 21:22:42 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 14 May 2025 21:22:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Tue, 13 May 2025 19:42:18 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c00bca83a11cc4fa60fed30864e3bd8e5fb69758dd2bc115394605fcc52daa6`  
		Last Modified: Wed, 14 May 2025 21:22:46 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a8e5b93aa2ae84cc35ff4e577e3de900fa198f4884a5f895f6afaed8a85660`  
		Last Modified: Wed, 14 May 2025 21:22:46 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed2148a31003cb6b6c9d5bb636caaddcf5f1d5b66180e1dd7cc394e5888a55e`  
		Last Modified: Wed, 14 May 2025 21:22:46 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e326816d6d7726d85bf1c8a00b56f26fccfd3cf6c448712a4f993493be3e7811`  
		Last Modified: Wed, 14 May 2025 21:22:46 GMT  
		Size: 76.9 KB (76867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd54da081518263083ddb39736f4cb12e829232c5738f35925507a3573e571f`  
		Last Modified: Wed, 14 May 2025 21:22:45 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f374a6b5fd8754590d22c9df7a9f55ecb9f2c1d393143c2433d3a4ec77ba521c`  
		Last Modified: Wed, 14 May 2025 21:22:45 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b12a7250f27ee5c3674aa7328b9381b36e6d37caeffcad3bb746386cc93f69`  
		Last Modified: Wed, 14 May 2025 21:22:56 GMT  
		Size: 208.4 MB (208365835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e3735577fbc70fc11c9315a371764af552afc9e8cf02bc6225ab2727e13c3a`  
		Last Modified: Wed, 14 May 2025 21:22:45 GMT  
		Size: 106.7 KB (106717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b269613484078069fccfdab448eba3b61cbd6798de13d6d6e6ba35a9459576`  
		Last Modified: Wed, 14 May 2025 21:22:45 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-22-nanoserver` - windows version 10.0.17763.7314; amd64

```console
$ docker pull openjdk@sha256:a3ba540e7eda561381f24b38ca17c3661b1f273e07e5bb5c7b8a5c064e206830
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.6 MB (321641319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c41127d941b6842aa268a8d29296355c1b14a5eeb8fc8485b8e101d9ce173a5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Wed, 14 May 2025 22:10:54 GMT
SHELL [cmd /s /c]
# Wed, 14 May 2025 22:10:55 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 14 May 2025 22:10:55 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 22:10:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 14 May 2025 22:10:57 GMT
USER ContainerUser
# Wed, 14 May 2025 22:10:58 GMT
ENV JAVA_VERSION=25-ea+22
# Wed, 14 May 2025 22:11:04 GMT
COPY dir:d2aeeab016ce5cfb722c90fbb6527341de5d03dac18528814b93fc4084ba77f8 in C:\openjdk-25 
# Wed, 14 May 2025 22:11:09 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 14 May 2025 22:11:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Tue, 13 May 2025 19:41:43 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a36e792622af88113228a82b02f51e00d1193caf98bf62d9dd5d430a2420f0`  
		Last Modified: Wed, 14 May 2025 22:11:16 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab254fd0082f3dfafcfcfcaff73d34bbd786362000eebd3321915f10df591c1a`  
		Last Modified: Wed, 14 May 2025 22:11:15 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077941f894a09876eef2dfa40fa6aa80daf89c17e174a5c1a454b9a1f51df750`  
		Last Modified: Wed, 14 May 2025 22:11:15 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ad71391053ff562107e55bceb0e9cca39f70769a61641f0484cbd58ba3e7ac`  
		Last Modified: Wed, 14 May 2025 22:11:15 GMT  
		Size: 68.7 KB (68702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3526665ebcf0433715f10ee965e479ecb4bcbd05cff56fb17c3f529376147d4`  
		Last Modified: Wed, 14 May 2025 22:11:13 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2238c8170e48ccc782309833db5f05d2f8ead94087296d26751d1a3a023ebdd3`  
		Last Modified: Wed, 14 May 2025 22:11:13 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02197cf11c8ce1129d0658836bcfc3a27e0f2ef150b823d3998df2cf642f5091`  
		Last Modified: Wed, 14 May 2025 22:11:25 GMT  
		Size: 208.4 MB (208366191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7124649093354b73c5da4eb232fccd4d05789e787e67333f123207cb85d5fc7d`  
		Last Modified: Wed, 14 May 2025 22:11:14 GMT  
		Size: 4.4 MB (4419658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7146fc7d0fc7cad5bf0c2b1311bae145c2a4ce70071634ba294ed4411936ab0`  
		Last Modified: Wed, 14 May 2025 22:11:14 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
