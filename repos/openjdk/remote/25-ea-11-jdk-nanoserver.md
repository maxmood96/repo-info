## `openjdk:25-ea-11-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:bc28c162599acafb61a641a6ab595ceaeee2db19a08cc4141d8d2739e4f78e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `openjdk:25-ea-11-jdk-nanoserver` - windows version 10.0.20348.3207; amd64

```console
$ docker pull openjdk@sha256:26932cd9ef6153a99def2ffde02f878661288a73deb93f4033c840329aaa2a83
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328428441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e9df74b107cedbe7eb008366c3e422aea5a3cde8673d7df66bfaeda8d10153`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 20:45:43 GMT
RUN Apply image 10.0.20348.3207
# Sat, 22 Feb 2025 01:15:08 GMT
SHELL [cmd /s /c]
# Sat, 22 Feb 2025 01:15:09 GMT
ENV JAVA_HOME=C:\openjdk-25
# Sat, 22 Feb 2025 01:15:10 GMT
USER ContainerAdministrator
# Sat, 22 Feb 2025 01:15:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 22 Feb 2025 01:15:13 GMT
USER ContainerUser
# Sat, 22 Feb 2025 01:15:14 GMT
ENV JAVA_VERSION=25-ea+11
# Sat, 22 Feb 2025 01:15:22 GMT
COPY dir:d106a0277e031719ecf57df75fb675ae173cc670fca8c773deb70f0105f67fe7 in C:\openjdk-25 
# Sat, 22 Feb 2025 01:15:27 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 22 Feb 2025 01:15:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:938e4585b186fc3df3c1959d47ba7a634fea121cec7545db7923ceb191d99a33`  
		Last Modified: Tue, 11 Feb 2025 22:43:09 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6699709989224f7ec2e5a9fefa2bd0fd19fac15067e127050988e3b7b60a6d26`  
		Last Modified: Sat, 22 Feb 2025 01:15:34 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc037a2c179867fa581e5a5850b5ccff0e528d720fdfcedf96b2657986dfb9c`  
		Last Modified: Sat, 22 Feb 2025 01:15:34 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640bcb6704545af075e966929ee835928b4644aa9adb113e97a1f08f87a5b48b`  
		Last Modified: Sat, 22 Feb 2025 01:15:34 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd1a1cf28522e12711123b0213448f2bee08f8a54407cd914fe98a975085606`  
		Last Modified: Sat, 22 Feb 2025 01:15:34 GMT  
		Size: 77.3 KB (77260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7f793b57b61a86b137f4f8fb71472f64329d44a34034bf6954902ca04ec22f`  
		Last Modified: Sat, 22 Feb 2025 01:15:32 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a57d07204c455133670edad2f24b88ff800a9cee8b46c20138182d5e2801b8`  
		Last Modified: Sat, 22 Feb 2025 01:15:32 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9d0ef1d7ab176c6569dac26e4f5d16661c720bbfdae3aad857e60645ed4cc8`  
		Last Modified: Sat, 22 Feb 2025 01:15:44 GMT  
		Size: 207.6 MB (207571334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9540b3f1751d9f64e247c3fa6db8c969e0e9d9be65a611376274a0dda27f346b`  
		Last Modified: Sat, 22 Feb 2025 01:15:32 GMT  
		Size: 106.9 KB (106860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d9903d41eba90beb533e2f7241dc112fdc148b4e92600b249dace9d16a0a799`  
		Last Modified: Sat, 22 Feb 2025 01:15:32 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-11-jdk-nanoserver` - windows version 10.0.17763.6893; amd64

```console
$ docker pull openjdk@sha256:51bd53be7a02fdc14ba7d5d338af34de19bb3741111ecb6f66523622287cead4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.0 MB (318965149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f762bfa8c1f86113d92700f719b72662ce9018d5795c3c339120c386cb88dda7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Sat, 22 Feb 2025 01:16:40 GMT
SHELL [cmd /s /c]
# Sat, 22 Feb 2025 01:16:42 GMT
ENV JAVA_HOME=C:\openjdk-25
# Sat, 22 Feb 2025 01:16:45 GMT
USER ContainerAdministrator
# Sat, 22 Feb 2025 01:16:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 22 Feb 2025 01:16:48 GMT
USER ContainerUser
# Sat, 22 Feb 2025 01:16:48 GMT
ENV JAVA_VERSION=25-ea+11
# Sat, 22 Feb 2025 01:16:55 GMT
COPY dir:d106a0277e031719ecf57df75fb675ae173cc670fca8c773deb70f0105f67fe7 in C:\openjdk-25 
# Sat, 22 Feb 2025 01:17:00 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 22 Feb 2025 01:17:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c499230b96efd8db69e05a0a40dad2e3f90e8571ef2ba9d726eb287f80ee35fb`  
		Last Modified: Sat, 22 Feb 2025 01:17:05 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b37eb3d6800d45798886865b50457e14d3de07c186d8f9f5e67c779ca17c150`  
		Last Modified: Sat, 22 Feb 2025 01:17:04 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964265a910379dfabbbf80c003022cc17be3e21bf371fcd54e6587b492f402cb`  
		Last Modified: Sat, 22 Feb 2025 01:17:04 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55dd2cbd2f2954a6149cae6e94e99ea3db187497f90f00579393ea54372bb7ea`  
		Last Modified: Sat, 22 Feb 2025 01:17:04 GMT  
		Size: 69.5 KB (69454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9675fa6067bd4e7c92b181b7db1e3afb6e7b4716133a01a4b62abfb90f5a0b5`  
		Last Modified: Sat, 22 Feb 2025 01:17:03 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7405f70900b0fcc5e2adfd958ef6196972e6fd4a1df6b5fcf1702007a9a9c01`  
		Last Modified: Sat, 22 Feb 2025 01:17:03 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9637732ed93c24d714b657af9cb9f1c5af6346fc72adeb1c7431b7f4a98747f3`  
		Last Modified: Sat, 22 Feb 2025 01:17:15 GMT  
		Size: 207.6 MB (207569055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e92469c8b65d80c8b3a048b0ae8983d7dcce49f57e4edd3d32a3a1286b9a2a0e`  
		Last Modified: Sat, 22 Feb 2025 01:17:04 GMT  
		Size: 4.4 MB (4404944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cbeebd70d8d5c02b895bf0980d21e14e227e230fbdf44f31ebc0e6d0122e32`  
		Last Modified: Sat, 22 Feb 2025 01:17:03 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
