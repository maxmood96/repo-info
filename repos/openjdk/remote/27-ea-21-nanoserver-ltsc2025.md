## `openjdk:27-ea-21-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:53ec5eaf76bc34942b2b93c8f9ba4669ab21ef74a3fcf66c238772fa2e33266d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `openjdk:27-ea-21-nanoserver-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull openjdk@sha256:bc648a185808cecd53626b3020f7898d6b3de3a9511f86407b93d1cddde151fa
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.7 MB (424654781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9091f11bb80fc51e4271573c858e51efc565ce82654ea15dd5c9a5c69bec9b6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 06:39:57 GMT
RUN Apply image 10.0.26100.32690
# Tue, 12 May 2026 01:13:01 GMT
SHELL [cmd /s /c]
# Tue, 12 May 2026 01:13:03 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 12 May 2026 01:13:03 GMT
USER ContainerAdministrator
# Tue, 12 May 2026 01:13:18 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 12 May 2026 01:13:18 GMT
USER ContainerUser
# Tue, 12 May 2026 01:13:19 GMT
ENV JAVA_VERSION=27-ea+21
# Tue, 12 May 2026 01:13:59 GMT
COPY dir:21b86086b1737f2f7722d7588722f1390e0aa73709337ec2a22a64f142e83a09 in C:\openjdk-27 
# Tue, 12 May 2026 01:14:05 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 12 May 2026 01:14:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8af320c3b6d19296bcc7947e3beb8bc0c69cb12143db52efe988dc998ac088dc`  
		Last Modified: Tue, 14 Apr 2026 21:00:37 GMT  
		Size: 199.7 MB (199717094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2a6a8f14a64d8bc842f6c2d5f940105cc858a825f3e0db769c7c4b972d591c`  
		Last Modified: Tue, 12 May 2026 01:14:11 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b689c2a9f61f91e41e628eb5d6d8d3a24c549e98cc30d69fe673fea0d6d9f15`  
		Last Modified: Tue, 12 May 2026 01:14:11 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cfee114b95270b36f76536b7918324c081afe2369ad233f76e329cdc5213dc`  
		Last Modified: Tue, 12 May 2026 01:14:11 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9bd6d43edc237afbb1fecd7c53516b20944a219c3c63e3471c1c78c5c785e0`  
		Last Modified: Tue, 12 May 2026 01:14:11 GMT  
		Size: 70.0 KB (70011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ec1b5736c0ff22c00a0a78a43a1911c75163165444b8d37e5c471aa99cdd3b`  
		Last Modified: Tue, 12 May 2026 01:14:09 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1a823688bfa5341deaf8cc11e42c2740e4e8ce2c215f21d15a8b55fec075f6`  
		Last Modified: Tue, 12 May 2026 01:14:09 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c1f1a4320b15de8b348e648d04706d9e22427fb7d3f97cb0d1318bc888efec`  
		Last Modified: Tue, 12 May 2026 01:14:25 GMT  
		Size: 224.8 MB (224768749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7363923bca19919b99f0101de7bf7fde2ff9d0888b9790a847922cbaa571fe5c`  
		Last Modified: Tue, 12 May 2026 01:14:09 GMT  
		Size: 92.6 KB (92562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86c8e07d0d97537d57b7d72e7d64d3bb1b253357999bbb1c73e337c42f476da`  
		Last Modified: Tue, 12 May 2026 01:14:09 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
