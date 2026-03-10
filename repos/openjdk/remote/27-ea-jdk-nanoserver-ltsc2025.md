## `openjdk:27-ea-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:08b051b54b469c15a5398af3a3480dadc9800b04daff53ab6c5bbc83deb229be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `openjdk:27-ea-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull openjdk@sha256:d5bbdd2e48fcb6f43e7bb02376c34e6197fe033ed72b2f5856ae94de861d9b23
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.9 MB (423934804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f46636ac1e72a7d0dcec822c7bb93ddf3cb02b9ffd2f13b390305a07fec3aa25`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Mar 2026 01:45:55 GMT
RUN Apply image 10.0.26100.32522
# Tue, 10 Mar 2026 22:40:46 GMT
SHELL [cmd /s /c]
# Tue, 10 Mar 2026 22:44:40 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 10 Mar 2026 22:44:41 GMT
USER ContainerAdministrator
# Tue, 10 Mar 2026 22:44:42 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 10 Mar 2026 22:44:42 GMT
USER ContainerUser
# Tue, 10 Mar 2026 22:44:43 GMT
ENV JAVA_VERSION=27-ea+12
# Tue, 10 Mar 2026 22:44:53 GMT
COPY dir:39bc387d6f4a82116c9105a5f2b625fb020bc268f5298b0afe5a9520fad3060e in C:\openjdk-27 
# Tue, 10 Mar 2026 22:44:59 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 10 Mar 2026 22:44:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:06fab7822816d5f43d6835d07ac8db280fdf81384187f36d8dc43bbb7064a76d`  
		Last Modified: Tue, 10 Mar 2026 20:41:46 GMT  
		Size: 199.4 MB (199409325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf6224cd21bf161844346f3025994c2e26638f08f91e12dcda3c0bb82cc0a5b`  
		Last Modified: Tue, 10 Mar 2026 22:41:17 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf9d55f2b6ef2a49671ba812c4ca974f590efd74e0db91f30ccd66a318d4c77`  
		Last Modified: Tue, 10 Mar 2026 22:45:05 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e848739e35cb673ea6b96dcb4512fb0326efb20f7e74251bccb1554528890a`  
		Last Modified: Tue, 10 Mar 2026 22:45:05 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcc1123675108a542e973db7b299d81117c753f2caaf895c8120dcff341fb62`  
		Last Modified: Tue, 10 Mar 2026 22:45:05 GMT  
		Size: 72.1 KB (72098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ba676ee3f452a53259812ca97e7399e2b477d114632a3e64788166c6a023d1`  
		Last Modified: Tue, 10 Mar 2026 22:45:03 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a12c74c091c3fca2a44bca85949149ab7de2c76a2903cad2823bd9321a167f4`  
		Last Modified: Tue, 10 Mar 2026 22:45:03 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a05deb367f1f75dc3f115d527a3509865bc22ff7a5cd53502e54e8765f346e0`  
		Last Modified: Tue, 10 Mar 2026 22:45:18 GMT  
		Size: 224.3 MB (224333863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2207beb2e418b56ddbcf0bf65155a74472cac79b0670823c5a2d8740109d697d`  
		Last Modified: Tue, 10 Mar 2026 22:45:03 GMT  
		Size: 113.1 KB (113056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a07aa6d1a1170521b2bc58469e5ce256008370bab981f0bae0b28ae4b2eda8`  
		Last Modified: Tue, 10 Mar 2026 22:45:03 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
