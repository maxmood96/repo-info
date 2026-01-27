## `openjdk:27-ea-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:6ea16c1ab144443440cac3e18e2016413e7c388107a0bc10fed437538a73a9fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `openjdk:27-ea-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull openjdk@sha256:afb34e253c491cb97db8187407794f74e5fa43904909aa5ebe1e26daf6689e2b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.1 MB (351137317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17962292fbf752abd1c7bc4ee8fae944eb08c00a3db12c213bfc7fc9686ef1dc`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Mon, 26 Jan 2026 23:12:36 GMT
SHELL [cmd /s /c]
# Mon, 26 Jan 2026 23:15:03 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 26 Jan 2026 23:15:04 GMT
USER ContainerAdministrator
# Mon, 26 Jan 2026 23:15:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 26 Jan 2026 23:15:07 GMT
USER ContainerUser
# Mon, 26 Jan 2026 23:15:08 GMT
ENV JAVA_VERSION=27-ea+6
# Mon, 26 Jan 2026 23:16:15 GMT
COPY dir:70f85d11e72fbae24cc84d660c242da927e72cca58a6ae86631f6d18b6f9801a in C:\openjdk-27 
# Mon, 26 Jan 2026 23:16:22 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 26 Jan 2026 23:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e51f20a630010d929dc6108e426f6d138555f634eb15711b6e888053888c8f`  
		Last Modified: Mon, 26 Jan 2026 23:14:23 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f814946152b30164b4b7b95da9bc5f4508a25062e41ac0959d4285ff71d7a95`  
		Last Modified: Mon, 26 Jan 2026 23:16:35 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4854d0385a1c94cd9703cd42bbe5f337ea64d05f4d0b7b3b4a93753596683c7`  
		Last Modified: Mon, 26 Jan 2026 23:16:35 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d8fb1b64665e37ec66e98637cc0b062e7351d42fd84dd4d7137da03a01b503`  
		Last Modified: Mon, 26 Jan 2026 23:16:35 GMT  
		Size: 87.5 KB (87490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888dd32642ea1c391e89593ddf7d0e978e7d2ceed5b1cd8006b8ceda750db4b5`  
		Last Modified: Mon, 26 Jan 2026 23:16:33 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8a6caa58dc854278600d1e7866dd2ab3cb1044a6c37864f6346c8dbddde263`  
		Last Modified: Mon, 26 Jan 2026 23:16:33 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e81113f50efb92a48afc3c13d9aba08de0b87696baeaace510ace357dcdaab`  
		Last Modified: Mon, 26 Jan 2026 23:16:49 GMT  
		Size: 224.2 MB (224199533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd39330ba671926aee67f9c00527dc9c3568bed114fe9647416bf3ddcabdf610`  
		Last Modified: Mon, 26 Jan 2026 23:16:34 GMT  
		Size: 147.1 KB (147068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff2f59f80c166cf17b986cd12c882eb7741f3498878bdbdaf9933636de7c8f0`  
		Last Modified: Mon, 26 Jan 2026 23:16:34 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
