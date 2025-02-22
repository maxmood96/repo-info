## `openjdk:25-ea-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:914e5f2034c73077dd60b1a6b8e5bc59cf21420b434a3ab30ce152fe75ac775b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `openjdk:25-ea-nanoserver-ltsc2022` - windows version 10.0.20348.3207; amd64

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
