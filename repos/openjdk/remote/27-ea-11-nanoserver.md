## `openjdk:27-ea-11-nanoserver`

```console
$ docker pull openjdk@sha256:47f55851ca2fe1f137e49e891073c27e02e645d444fa9524aa6f1e2568b2497c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32370; amd64
	-	windows version 10.0.20348.4773; amd64

### `openjdk:27-ea-11-nanoserver` - windows version 10.0.26100.32370; amd64

```console
$ docker pull openjdk@sha256:e32a099b8075e42922b97d0442135b4dae527e5fbf5bd876a46bd05d4531334a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.8 MB (423766796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16860878e758173fdc21eda54ebcab3b861d5b457eec1958b04dcd6e023f641`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 22:06:41 GMT
RUN Apply image 10.0.26100.32370
# Mon, 02 Mar 2026 22:00:04 GMT
SHELL [cmd /s /c]
# Mon, 02 Mar 2026 22:00:04 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 02 Mar 2026 22:00:04 GMT
USER ContainerAdministrator
# Mon, 02 Mar 2026 22:00:17 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 02 Mar 2026 22:00:18 GMT
USER ContainerUser
# Mon, 02 Mar 2026 22:00:18 GMT
ENV JAVA_VERSION=27-ea+11
# Mon, 02 Mar 2026 22:00:59 GMT
COPY dir:af46595f79fcb8d73761dba193931692f3b5202188dd94a1eb0f61760b71de69 in C:\openjdk-27 
# Mon, 02 Mar 2026 22:01:10 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 02 Mar 2026 22:01:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:77321bd03612cfa46920e790ae0c3b142758a5803ad759fdb406c98b6f2e4ed0`  
		Last Modified: Tue, 10 Feb 2026 22:50:26 GMT  
		Size: 199.3 MB (199251619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c91a5abbe2c5ece973e2df7d80d153e945a9f2f29edd2f4298cd66b2c268d8`  
		Last Modified: Mon, 02 Mar 2026 22:01:16 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f400fa50538139284766cee3e1772b3f9e7c03f4c5933bedb717257bc834333`  
		Last Modified: Mon, 02 Mar 2026 22:01:18 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9517002476751d5d215e4514a770d0484f339ce39814f8bc7d3cf126a0818ae2`  
		Last Modified: Mon, 02 Mar 2026 22:01:15 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e382e6a7ba65630d684cd097fc2fa4b6630aae8f6fd9f8d921b127385de176`  
		Last Modified: Mon, 02 Mar 2026 22:01:18 GMT  
		Size: 70.7 KB (70671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b0c578f2479c6db8aa7b1b6814dc1c69e4115eb8e683502d31d538af363f247`  
		Last Modified: Mon, 02 Mar 2026 22:01:14 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f5a8150be2721c4fca8bc9663a6c115dd43d139a1740ed2674a3d4dd12006f`  
		Last Modified: Mon, 02 Mar 2026 22:01:14 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeed86b1864d14a01d251696c8171b61b5ac73115b9a58440b63e9520aa69563`  
		Last Modified: Mon, 02 Mar 2026 22:01:30 GMT  
		Size: 224.3 MB (224335440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4743c18ef3deb29442beff05932dec4dc99bf0cddc54a1700c8ea5ce6a24afeb`  
		Last Modified: Mon, 02 Mar 2026 22:01:14 GMT  
		Size: 102.7 KB (102650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c4f56c937864a402101b30ac6588f670f4fdc41a96ca5aff349d68ccfd39f73`  
		Last Modified: Mon, 02 Mar 2026 22:01:14 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-11-nanoserver` - windows version 10.0.20348.4773; amd64

```console
$ docker pull openjdk@sha256:e1d47d96007443d95c97a33f88b4cd5a71a66d25af0284b6dac46e1b7a5879c6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.2 MB (351167950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5f68c4bedfbd567a65a54bdebfb426baba665978e13946820e15316c61e5072`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Mon, 02 Mar 2026 22:00:09 GMT
SHELL [cmd /s /c]
# Mon, 02 Mar 2026 22:00:09 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 02 Mar 2026 22:00:10 GMT
USER ContainerAdministrator
# Mon, 02 Mar 2026 22:00:24 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 02 Mar 2026 22:00:25 GMT
USER ContainerUser
# Mon, 02 Mar 2026 22:00:25 GMT
ENV JAVA_VERSION=27-ea+11
# Mon, 02 Mar 2026 22:01:53 GMT
COPY dir:af46595f79fcb8d73761dba193931692f3b5202188dd94a1eb0f61760b71de69 in C:\openjdk-27 
# Mon, 02 Mar 2026 22:01:59 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 02 Mar 2026 22:02:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1f17fd754b01a3e56863198c092e585c3db6f636998e48fabfe7126f50a822`  
		Last Modified: Mon, 02 Mar 2026 22:02:07 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b9b6af0f4c3b3bb5eb752a1eeee8475c3c4eb6c966affc965b7ed107aea233`  
		Last Modified: Mon, 02 Mar 2026 22:02:07 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecf7acaf079edd9bfdcd6108048ed6405f9ea061e393f77afa15ae01ce9cd4e`  
		Last Modified: Mon, 02 Mar 2026 22:02:07 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38fdf1895944eca84e7eca451c1ec93c1f904a2e6b5b6d0d9afd4a9faa2bbf51`  
		Last Modified: Mon, 02 Mar 2026 22:02:07 GMT  
		Size: 87.5 KB (87546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b9347366f079e9d1fe0020851698ab3c7d96012b34a73b020d9f83ada3eb31`  
		Last Modified: Mon, 02 Mar 2026 22:02:05 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6456980d83d46cbe2900a7e5e09ae617f3de104b3402473ffc8e9462ecd67850`  
		Last Modified: Mon, 02 Mar 2026 22:02:05 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d833eef747510fed15abccd90aad1b4c21a88217c43230670d565d64f9f5bf`  
		Last Modified: Mon, 02 Mar 2026 22:02:21 GMT  
		Size: 224.3 MB (224335557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af47a90493ab7642da9af52ba95d3c8dacd8d8164cdff20f5f931c0d97fbd00`  
		Last Modified: Mon, 02 Mar 2026 22:02:05 GMT  
		Size: 92.6 KB (92619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70d7f905da43dc0d999bc984bf191c3674cff9e0a001cbf06468a7a09ac2e30`  
		Last Modified: Mon, 02 Mar 2026 22:02:05 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
